<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Calculate body fat<hr>
          <h1 class="w3-text-teal"><b>Body fat calculator</b></h1>
          <p>Body fat, body mass, lean body mass calculator.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">
  <form id="designform" autocomplete="off">
  <div class="form-group grid">
  <label class="row ml-0">Units Type</label>
  <div class="btn-group btn-group-toggle row ml-0" data-toggle="buttons">
  <button type="button" @click="metricclicked()" class="btn btn-secondary">Metric Units</button><hr>
  </div>
  </div>
  <div class="form-group">
    <h5 class="w3-opacity"><b>Select gender!</b></h5>
    <input type="radio" id="male" value="male" v-model="gender">
  <label for="male">Male</label><br>
  <input type="radio" id="female" value="female" v-model="gender">
  <label for="female">Female</label><br>
  </div>
  <div class="form-group">
  <label>Height</label>
  <div class="input-group" v-if="showunits === true">
  <input type="number" min="0" class="form-control" v-model="ft" placeholder="feet">
  <div class="input-group-append mr-2">
  <span class="input-group-text">ft</span>
  </div>
  <input type="number" min="0" class="form-control" v-model="inches" placeholder="inches">
  <div class="input-group-append">
  <span class="input-group-text">in</span>
  </div>
  </div>
  <div class="input-group" v-if="showmetric === true" id="designhjl">
  <input type="number" min="0" class="form-control" v-model="cm" placeholder="centimeters">
  <div class="input-group-append">
  <span class="input-group-text">cm</span>
  </div>
  </div>
  </div>

  <div class="form-group">
  <label>Age</label>
  <div class="input-group" id="designhjl">
  <input type="number" min="0" class="form-control" v-model="age" placeholder="years">
  <div class="input-group-append">
  <span class="input-group-text">age</span>
  </div>
  </div>
  </div>



  <div class="form-group">
  <label>Neck</label>
  <div class="input-group" v-if="showunits === true">
  <input type="number" min="0" class="form-control" v-model="nft" placeholder="feet">
  <div class="input-group-append mr-2">
  <span class="input-group-text">ft</span>
  </div>
  <input type="number" min="0" class="form-control" v-model="ninches" placeholder="inches">
  <div class="input-group-append">
  <span class="input-group-text">in</span>
  </div>
  </div>
  <div class="input-group" v-if="showmetric === true" id="designhjl">
  <input type="number" min="0" class="form-control" v-model="ncm" placeholder="centimeters">
  <div class="input-group-append">
  <span class="input-group-text">cm</span>
  </div>
  </div>
  </div>


  <div class="form-group">
  <label>Waist</label>
  <div class="input-group" v-if="showunits === true">
  <input type="number" min="0" class="form-control" v-model="wft" placeholder="feet">
  <div class="input-group-append mr-2">
  <span class="input-group-text">ft</span>
  </div>
  <input type="number" min="0" class="form-control" v-model="winches" placeholder="inches">
  <div class="input-group-append">
  <span class="input-group-text">in</span>
  </div>
  </div>
  <div class="input-group" v-if="showmetric === true" id="designhjl">
  <input type="number" min="0" class="form-control" v-model="wcm" placeholder="centimeters">
  <div class="input-group-append">
  <span class="input-group-text">cm</span>
  </div>
  </div>
  </div>


  <div class="form-group" v-if="gender === 'female'">
  <label>Hip</label>
  <div class="input-group" v-if="showunits === true">
  <input type="number" min="0" class="form-control" v-model="hft" placeholder="feet">
  <div class="input-group-append mr-2">
  <span class="input-group-text">ft</span>
  </div>
  <input type="number" min="0" class="form-control" v-model="hinches" placeholder="inches">
  <div class="input-group-append">
  <span class="input-group-text">in</span>
  </div>
  </div>
  <div class="input-group" v-if="showmetric === true" id="designhjl">
  <input type="number" min="0" class="form-control" v-model="hcm" placeholder="centimeters">
  <div class="input-group-append">
  <span class="input-group-text">cm</span>
  </div>
  </div>
  </div>




  <div class="form-group">
  <label>Weight</label>
  <div v-if="showunits === true" class="input-group" id="lbdiv">
  <input type="number" min="0" class="form-control" v-model="lb" placeholder="pounds">
  <div class="input-group-append">
  <span class="input-group-text">lb</span>
  </div>
  </div>
  <div class="input-group" v-if="showmetric === true" id="koshijlk">
  <input type="number" min="0" class="form-control" v-model="kg" placeholder="kilograms">
  <div class="input-group-append">
  <span class="input-group-text">kg</span>
  </div>
  </div>
  </div>
  <div class="form-group">
  <button type="button" title="Calculate" @click="fract()" class="btn btn-success"><span>= ></span> Calculate</button>
  <button type="reset" title="Reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
  </div>
  <div class="form-group">
  <label for="bmi">Body Fat</label>
  <div class="input-group">
  <input type="number" min="0" class="form-control" v-model="bmi" readonly>
  <div class="input-group-append">
  <span class="input-group-text">%</span>
  </div>
  </div>
  </div>
  </form>

</div><br>
  </div>
</div></div>

<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-margin">
    <div class="w3-container w3-white">
      <div class="w3-margin w3-white">
          <div class="w3-container w3-padding">
        <h1 class=""><b>Other tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/unit-conversion"> Unit Conversion</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/random-letter-generator"> Random letter generator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/word-counter"> Word counter</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

  <!-- Labels / tags -->

<!-- END Introduction Menu -->
</div>

</div>
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
      title: 'Body fat calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculate body fat.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/body-fat-calculator'}
    ]
    }
    },
  data(){
    return {
      age: '',
ft: 5,
gender: 'male',
inches: 10.5,
lb: 152,
bmi: '',
category: '',
risk: '',
cm: '',
showunits: false,
showmetric: true,
isMetric: false,
kg: '',
nft: 1,
ninches: 7.5,
ncm: '',
wft: 3,
winches: 1.5,
wcm: '',
hft: '',
hcm: '',
hinches: ''
      }
  },
  methods: {
    reset(){
      this.ft = "";
      this.inches = "";
      this.lb = "";
      this.bmi = "";
      this.category = "";
      this.risk = "";
      this.cm = "";
      this.showunits = true;
      this.showmetric = false;
      this.isMetric = false;
      this.kg = "";
    },
    unitclicked(){
        this.showunits = true;
        this.showmetric = false;
        this.isMetric = false;
    },
    metricclicked(){
        this.showmetric = true;
      this.showunits = false;
this.isMetric = true;
    },
  fract(){
    if( this.isMetric ) {
      if(this.gender === "female"){
        var waist = this.wcm;
        var hip = this.hcm;
        var neck = this.ncm;
        var height = this.cm;
        var x = parseFloat(waist)+ parseFloat(hip);
        x = x-neck;
        var y = Math.log(x)/Math.log(10);
        y = y.toFixed(10);
        var xx = Math.log(height)/Math.log(10);
        xx = xx.toFixed(10);
        var first = 0.35004 * y;
        var second = 0.22100 * xx;
        var koko = 1.29579 - first;
        koko = parseFloat(koko) + parseFloat(second);
        var koko1 = 495/koko;
        koko1 = koko1.toFixed(1);
        this.bmi = koko1 - 450;
        this.bmi = this.bmi.toFixed(1);
      }
      else {
        var logp = this.wcm-this.ncm;
              var y = Math.log(logp)/Math.log(10);
              y = y.toFixed(10);
              var x = Math.log(this.cm)/Math.log(10);
              x = x.toFixed(10);
var step1 = 1.0324 - 0.19077 * y + 0.15456 * x;
var step2 = 495/step1;
this.bmi = step2 - 450;
this.bmi = this.bmi.toFixed(1);
      }
        }
      else{
if(this.gender === "female"){
  alert("female")
}
else{
  var nft=this.nft;
  var ninch=this.ninches;
  var ft=this.ft;
  var inch=this.inches;
  var lbs=this.lb;
  var wft = this.wft;
  var win = this.winches;
  ft=parseFloat(ft);
  inch=parseFloat(inch);
  nft=parseFloat(nft);
  ninch=parseFloat(ninch);
  lbs=parseFloat(lbs);
  wft=parseFloat(wft);
  win=parseFloat(win);
  ninch+=12.0*nft;
  win+=12.0*wft;
  var tyty = win - ninch;
  alert(tyty);
  var y = Math.log(11.5)/Math.log(10);
  y = y.toFixed(10);
  inch+=12.0*ft;
  var x = Math.log(inch);
  x = x.toFixed(10);
var bbp = 86.010 * y;
var bbp2 = 70.041 * x;
var lp = parseFloat(bbp) - parseFloat(bbp2);
var gb = parseFloat(lp) + parseFloat(36.76);
this.bmi = gb.toFixed(1);
}

  }

    }
}
}
</script>

<style lang="css" scoped>
.buttonclicked{
  background-color: Violet;
}
.buttonclicked1{
  background-color: Violet;
}
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
.adslot_1 { display:none; }
 h1 { font-size:1.6rem; }
 h2 { font-size:1.4rem; }
 h3 { font-size:1.4rem; }
 h4 { font-size:1.2rem; }
 #wrapper td { padding:.75rem; }
#designform {
   padding:15px;
   background:#a7c9b8;
   border:1px solid #eee;
   border-radius:7px;
   max-width:500px;
}
.btn span { font-weight:bold; font-size:large; }

@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
 }
</style>
