<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Volts to Amps<hr>
    <h1 class="w3-text-teal"><b>Volts to Amperes</b></h1><br>
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
      <label for="volt">Enter units:</label>
      <select name="volt" @change="showme()" v-model="voltagetype" class="form-control">
      <option>With Watts</option>
      <option>With Ohm</option>
      </select>
      </div>
<div class="form-group">
<label for="x1">Enter volts:</label>
<div class="input-group">
<input type="number" v-model="number1" min="0" step="any" class="form-control" required>
</div>
</div>
<div v-if="showwatts === true" class="form-group">
<label for="x2">Enter Watts</label>
<div class="input-group">
<input type="number" min="0" step="any" v-model="number2" name="x2" class="form-control" required>
</div>
</div>
<div v-if="showohms === true" class="form-group">
<label for="x2">Enter Ohms</label>
<div class="input-group">
<input type="number" min="0" step="any" v-model="number3" name="x3" class="form-control" required>
</div>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="currentchange()"><span>=></span> Answer</button>
<button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<label >Amps:</label>
<div class="input-group">
<input type="text" v-model="kw" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">A</span>
</div>
</div>
</div>
</form>

      </div>
      <div class="w3-padding w3-raw w3-align">
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
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-ev"> volts to ev</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-joules"> volts to joules</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-kilowatts"> volt sto kilowatts</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-watts"> Volts to watts</a></span><br>
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
      title: 'Volts to Amperes',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Volts to amps.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/volts-to-amps'}
    ]
    }
    },
  data(){
    return {
      currenttype: 'AC - Single phase',
      powerfactor: true,
      threephase: false,
      amperselect: 'W',
      voltagechange: 'V',
      kw: '',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      voltagetype: 'With Watts',
      showwatts: true,
      showohms: false
    }
  },
  methods: {
    showme(){
      if(this.voltagetype === "With Watts"){
        this.showwatts = true;
        this.showohms = false;
      }
      else{
        this.showwatts = false;
        this.showohms = true;
      }
    },
    currentchange(){
      if(this.showwatts === true){
                this.kw = this.number2/this.number1;
      }
      else{
        this.kw = this.number1/this.number3;
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
    },

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
