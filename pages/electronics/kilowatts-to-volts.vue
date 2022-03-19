<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Kw to volts <hr>
    <h1 class="w3-text-teal"><b>Kilowatts to volts</b></h1>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>
    <form autocomplete="off">
  <div class="form-group">
  <label for="phase">Select current type</label>
  <select v-model="currenttype" name="phase" @change="currentchange()" class="form-control" autofocus>
  <option>DC</option>
  <option>AC - Single phase</option>
  <option>AC - Three phase</option>
  </select>
  </div>
  <div class="form-group">
  <label for="x1">Enter power in kilowatts</label>
  <div class="input-group">
  <input type="number" v-model="number1" min="0" step="any" class="form-control" required>
  </div>
  </div>
  <div class="form-group" v-if="threephase === true">
  <label>Enter current amps</label>
  </div>
  <div class="form-group">
  <label for="x2">Enter current in amps</label>
  <div class="input-group">
  <input type="number" min="0" step="any" v-model="number2" class="form-control" required>
  <div class="input-group-append">
    <div class="input-group-append">
    <span class="input-group-text">A</span>
    </div>
  </div>
  </div>
  </div>
  <div class="form-group" v-if="powerfactor === true">
  <label for="pf">Enter power factor</label>
  <input type="number" v-model="powerfactorinput" class="form-control">
  </div>
  <div class="form-group">
  <button type="button" title="Calculate" class="btn btn-secondary" @click="currentchange()"><span>=></span> Answer</button>
  </div>
  <div class="form-group">
  <label>Voltage in volts</label>
  <div class="input-group">
  <input type="text" v-model="ansam" class="form-control" readonly>
  <div class="input-group-append">
  <span class="input-group-text">V</span>
  </div>
  </div>
  </div>
  </form>
      </div>
        </div>
  <hr>

  </div>


  <!-- Introduction menu -->
  <div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-margin">
    <div class="w3-container w3-white">
      <div class="w3-margin w3-white">
          <div class="w3-container w3-padding">
        <h1 class=""><b>Other Electronics tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/kw-to-amps"> kw to amps</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>


  </div>

  <!-- END GRID -->
  </div><br>

  <!-- END w3-content -->
  </div>

  <!-- Footer -->
  <footer class="w3-container w3-dark-grey w3-padding-32 w3-margin-top">
  <p>© AaryaTables</p>
  </footer>

  </div>
</template>

<script>
export default {
  head() {
    // sets document title
    return {
      title: 'kilowatts to volts',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'KW to volts converter' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/kilowatts-to-volts'}
    ]
    }
    },
  data(){
    return {
      currenttype: 'DC',
      powerfactor: false,
      threephase: false,
      wattchange: 'kW',
      voltagechange: 'V',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      kilowatinput: '',
      voltagetype: 'Line to line voltage',
      ansam: ''
    }
  },
  methods: {
    currentchange(){
      if(this.currenttype === "AC - Single phase"){
        this.powerfactor = true;
        this.threephase = false;
        var x1 = this.number1;
        var x2 = this.number2;
        if(this.powerfactorinput === '1'){
        this.ansam = (x1/x2)*1000;
    }
      else if(this.powerfactorinput === '0'){
        this.ansam = Infinity;
      }
      else{
        alert("enter power in 0 or 1")
      }
      }
      else if(this.currenttype === "AC - Three phase"){
        this.powerfactor = true;
        this.threephase = false;
        var x1 = this.number1;
        var x2 = this.number2;
        if(this.powerfactorinput === '1'){
        this.ansam = (x1/x2)*577.35026919;
      }
      else if(this.powerfactorinput === '0'){
        this.ansam = Infinity;
      }
      else{
        alert("enter power in 0 or 1")
      }
      }
      else if(this.currenttype === "DC"){
        var x1=this.number1;
        var x2=this.number2;
            this.ansam = (x1/x2)*1000;
}
      else if(this.currenttype === "AC - Three phase"){
        this.threephase = true;
        this.powerfactor = true;
        var x1 = this.number1;
        var x2 = this.number2;
        if( this.wattchange === "kW" ) x1/=1000000;
        if( this.wattchange === "mW" ) x1/=1000;
        if( this.voltagechange === "mV" ) x2/=1000;
        if( this.voltagechange === "kV" ) x2/=1000;
                var a = 1000*this.number1/this.number2;
        if(this.wattchange === "kW" && this.voltagechange === "V"){


            if( this.voltagetype === "Line to line voltage")
        {      a/=(this.powerfactorinput*Math.sqrt(3));
          this.ansam = a;
        }
           else
  {            a/=(this.powerfactorinput*3);
      this.ansam = a;
  }
        }
        else if(this.wattchange === "kW" && this.voltagechange === "mV"){
          if( this.voltagetype === "Line to line voltage")
      {      a/=(this.powerfactorinput*Math.sqrt(3));
        this.ansam = a*1000;
      }
         else
{            a/=(this.powerfactorinput*3);
    this.ansam = a*1000;
}
}
else if(this.wattchange === "kW" && this.voltagechange === "kV"){
  if( this.voltagetype === "Line to line voltage")
{      a/=(this.powerfactorinput*Math.sqrt(3));
this.ansam = a;
this.ansam = a/1000;
}
 else
{            a/=(this.powerfactorinput*3);
this.ansam = a/1000;
}
}
else if(this.wattchange === "W" && this.voltagechange === "mV"){
  if( this.voltagetype === "Line to line voltage")
{      a/=(this.powerfactorinput*Math.sqrt(3));
this.ansam = a;
this.ansam = a;
}
 else
{            a/=(this.powerfactorinput*3);
this.ansam = a;
}
}
else if(this.wattchange === "W" && this.voltagechange === "V"){
  if( this.voltagetype === "Line to line voltage")
{      a/=(this.powerfactorinput*Math.sqrt(3));
this.ansam = a/1000;
}
 else
{            a/=(this.powerfactorinput*3);
this.ansam = a/1000;
}
}
else if(this.wattchange === "mW" && this.voltagechange === "mV"){
  if( this.voltagetype === "Line to line voltage")
{      a/=(this.powerfactorinput*Math.sqrt(3));
this.ansam = a/1000;
}
 else
{            a/=(this.powerfactorinput*3);
this.ansam = a/1000;
}
}
else if(this.wattchange === "mW" && this.voltagechange === "V"){
  if( this.voltagetype === "Line to line voltage")
{      a/=(this.powerfactorinput*Math.sqrt(3));
this.ansam = a/1000000;
}
 else
{            a/=(this.powerfactorinput*3);
this.ansam = a/1000000;
}
}
else if(this.wattchange === "mW" && this.voltagechange === "kV"){
  if( this.voltagetype === "Line to line voltage")
{      a/=(this.powerfactorinput*Math.sqrt(3));
this.ansam = a/1000000000;
}
 else
{            a/=(this.powerfactorinput*3);
this.ansam = a/1000000000;
}
}
else{
  alert("not number")
}
}
      }

  },
    reset(){
      this.currenttype = "DC";
      this.powerfactor = false;
      this.threephase = false;
      this.wattchange = "kW";
      this.voltagechange = "V";
      this.w = "";
      this.mw = "";
      this.number1 = "";
      this.number2 = "";
      this.powerfactorinput = "";
      this.kilowatinput = "";
      this.voltagetype = "Line to line voltage";
      this.ansam = "";
    }
  }
</script>

<style lang="css">
@keyframes cssAnimation {
  to   { visibility: visible; }
}
@media (min-width: 350px) {
    .infeed {
      height: 290px;
    }
  }
 @media (min-width: 500px) {
    .infeed {
      height: 290px;
    }
  }
 @media (min-width: 800px) {
    .infeed {
      height: 290px;
    }
  }
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
@media all and (max-width: 800px) {
}

</style>
