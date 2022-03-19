<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; AMPs to Watts(W) <hr>
    <h1 class="w3-text-teal"><b>Amps to watts Calculator</b></h1><br>
    <p>AMPs to Watts converter and how to convert? Use the below tool to convert amts to watts.</p>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>
    <form id="designmodel" autocomplete="off">
<div class="form-group">
<label for="phase">Select current type</label>
<select id="phase" name="phase" v-model="currenttype" @change="currentchange()" class="form-control" autofocus>
<option>AC - Single phase</option>
<option>AC - Three phase</option>
<option>DC</option>
</select>
</div>
<div class="form-group">
<label for="x1">Enter current in amps</label>
<div class="input-group">
<input type="number" v-model="number1" name="x1" min="0" step="any" class="form-control" required>
<div class="input-group-append">
<select v-model="amperselect" class="form-control">
<option>mA</option>
<option selected>A</option>
<option>kA</option>
</select>
</div>
</div>
</div>
<div class="form-group" v-if="threephase === true">
<label for="volt">Select voltage type</label>
<select id="volt" name="volt" v-model="voltagetype" class="form-control">
<option>Line to line voltage</option>
<option>Line to neutral voltage</option>
</select>
</div>
<div class="form-group">
<label for="x2">Enter voltage in volts</label>
<div class="input-group">
<input type="number" min="0" step="any" v-model="number2" name="x2" class="form-control" required>
<div class="input-group-append">
<select v-model="voltagechange" class="form-control">
<option>mV</option>
<option selected>V</option>
<option>kV</option>
</select>
</div>
</div>
</div>
<div class="form-group" v-if="powerfactor === true">
<label for="pf">Enter power factor</label>
<input type="number" v-model="powerfactorinput" class="form-control">
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="currentchange()"><span>=></span> Answer</button>
<button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<label for="y">Power result in kilowatts</label>
<div class="input-group">
<input type="text" v-model="kw" name="y" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">kW</span>
</div>
</div>
</div>
<div class="form-group">
<label for="y">Power result in watts</label>
<div class="input-group">
<input type="text" v-model="w" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">W</span>
</div>
</div>
</div>
<div class="form-group">
<label for="y">Power result in milliwatts</label>
<div class="input-group">
<input type="text" v-model="mw" name="y3" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">mW</span>
</div>
</div>
</div>
</form>

      </div>
      <div class="w3-padding w3-raw w3-align">
      <h2 class="w3-center"><b>Amps to watts</b></h2>
      <p>Amps to watts conversion is one of the most important electronic conversions in recent times. There are two types of current, AC & DC and you can perform the Amps to watts conversion on both of these currents.</p>
      <h2>How to convert Amps to Watts?</h2>
      <p>To convert Amps to Watts, you need a power factor that should be less than 1. Once you have that, you need to decide the type of current you want to convert. Select from AC and DC currents. Once selected, you need to enter the current in A, mA, or kA and then select voltage in V, mV, or kV.</p>
      <p>Once you enter all the values, just enter the values you want to convert and click on the conversion button.</p>
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
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kw"> Amps to KW</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-va"> Amps to VA</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-volts"> Amps to volts(V)</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kva"> Amps to Kva</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/kw-to-amps"> Kw to Amps</a></span><br>
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
      title: 'Amps to watts',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Amps to watts.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/amps-to-watts'}
    ]
    }
    },
  data(){
    return {
      currenttype: 'AC - Single phase',
      powerfactor: true,
      threephase: false,
      amperselect: 'A',
      voltagechange: 'V',
      kw: '',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      voltagetype: 'Line to line voltage'
    }
  },
  methods: {
    currentchange(){
      if(this.currenttype === "AC - Single phase"){
        this.powerfactor = true;
        this.threephase = false;
          if(this.powerfactorinput === '1'){
            if(this.amperselect === "A" && this.voltagechange === "V"){
              var x = this.number1/1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "mA" && this.voltagechange === "V"){
              var x = this.number1/1000000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "kA" && this.voltagechange === "V"){
              var x = this.number1/1;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "mA" && this.voltagechange === "mV"){
              var x = this.number1/1000000000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "A" && this.voltagechange === "mV"){
              var x = this.number1/1000000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "kA" && this.voltagechange === "mV"){
              var x = this.number1/1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "mA" && this.voltagechange === "kV"){
              var x = this.number1/1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "A" && this.voltagechange === "kV"){
              var x = this.number1/1;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "kA" && this.voltagechange === "kV"){
              var x = this.number1 * 1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
          }
          else if(this.currenttype === "AC - Three phase"){
            this.threephase = true;
            this.powerfactor = true;
          }
          else{
            this.kw = 0;
            this.w = 0;
            this.mw = 0;
          }
          }

      }
      else if(this.currenttype === "DC"){
        this.powerfactor = false;
        if(this.amperselect === "A" && this.voltagechange === "V"){
          var x = this.number1/1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "mA" && this.voltagechange === "V"){
          var x = this.number1/1000000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "kA" && this.voltagechange === "V"){
          var x = this.number1/1;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "mA" && this.voltagechange === "mV"){
          var x = this.number1/1000000000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "A" && this.voltagechange === "mV"){
          var x = this.number1/1000000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "kA" && this.voltagechange === "mV"){
          var x = this.number1/1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "mA" && this.voltagechange === "kV"){
          var x = this.number1/1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "A" && this.voltagechange === "kV"){
          var x = this.number1/1;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "kA" && this.voltagechange === "kV"){
          var x = this.number1 * 1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
      }
      else{
        console.log("not right decision")
      }

}
      else if(this.currenttype === "AC - Three phase"){
        this.threephase = true;
        this.powerfactor = true;
        if( this.amperselect === "kA" ) this.number1/=1000;
        if( this.amperselect === "mA" ) this.number1/=1000;
        if( this.voltagechange === "mV" ) this.number2/=1000;
        if( this.voltagechange === "kV" ) this.number2/=1000;
        var kw = this.number1*this.number2/1000;

        if( this.voltagetype === "Line to line voltage" )
   kw*=(this.powerfactorinput*Math.sqrt(3));
else
   kw*=(this.powerfactorinput*3);
   this.kw = kw;
   this.w = 1000*kw;
   this.mw = 1000000*kw;
      }

  },
    reset(){
      this.currenttype = "AC - Single phase";
      this.powerfactor = true;
      this.threephase = false;
      this.amperselect = "A";
      this.voltagechange = "V";
      this.kw = "";
      this.w = "";
      this.mw = "";
      this.number1 = "";
      this.number2 = "";
      this.powerfactorinput = "";
      this.voltagetype = "Line to line voltage";
    }
  },
  beforeMount(){
   this.currentchange();
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
#designmodel { background:#a7c9b8; padding:20px; }
#designmodel button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designmodel { padding:10px; }
}

</style>
