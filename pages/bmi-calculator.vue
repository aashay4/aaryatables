<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; BMI Calculator<hr>
          <h1 class="w3-text-teal"><b>BMI Calculator</b></h1>
          <p>BMI calculator in feet/inches/pounds for women, men and kids.</p>
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
  <button type="button" @click="unitclicked()" class="btn btn-secondary active">FT/IN Units</button>
  <button type="button" @click="metricclicked()" class="btn btn-secondary">Other Units</button>
  </div>
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
  <label for="bmi">BMI</label>
  <div class="input-group">
  <input type="number" min="0" class="form-control" v-model="bmi" readonly>
  <div class="input-group-append">
  <span class="input-group-text">kg/m<sup>2</sup></span>
  </div>
  </div>
  </div>
  <div class="form-group">
  <label for="risk">BMI category</label>
  <input type="text" class="form-control" v-model="category" readonly>
  </div>
  <div class="form-group">
  <label for="risk">Health risk</label>
  <input type="text" class="form-control" v-model="risk" readonly>
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
      title: 'BMI calculator.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'BMI calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/bmi-calculator'}
    ]
    }
    },
  data(){
    return {
ft: '',
inches: '',
lb: '',
bmi: '',
category: '',
risk: '',
cm: '',
showunits: true,
showmetric: false,
isMetric: false,
kg: ''
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
         var cm=this.cm;
         var kg=this.kg;
         if( cm=="" ) cm="0";
         if( kg=="" ) kg="0";
         cm=parseFloat(cm);
         kg=parseFloat(kg);
         var m=cm/100.0;
         var bmi=kg/(m*m);
         this.bmi=bmi.toFixed(1);
      }
      else{
    var ft=this.ft;
    var inch=this.inches;
    var lbs=this.lb;
    if( ft=="" ) ft="0";
    if( inch=="" ) inch="0";
    if( lbs=="" ) lbs="0";
    ft=parseFloat(ft);
    inch=parseFloat(inch);
    lbs=parseFloat(lbs);
    inch+=12.0*ft;
    //var bmi=703.069*lbs/(inch*inch);
    var bmi=703*lbs/(inch*inch);
    this.bmi=bmi.toFixed(1);
  }
    var risk="",cat="";
    if( bmi<18.5 ) { cat="Underweight"; risk="Malnutrition risk"; }
    else if( bmi<25 ) { cat="Normal weight"; risk="Low risk"; }
    else if( bmi<30 ) { cat="Overweight"; risk="Enchanced risk"; }
    else if( bmi<35 ) { cat="Moderately obese"; risk="Medium risk"; }
    else if( bmi<40 ) { cat="Severely obese"; risk="High risk"; }
    else if( bmi>=40 ) { cat="Very severely obese"; risk="Very high risk"; }
    this.category= cat;
    this.risk = risk;
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
