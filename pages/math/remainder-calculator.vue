<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Remainder calculator<hr>
          <h1 class="w3-text-teal"><b>Remainder calculator</b></h1>
          <p>Simple remainder calculation tool.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">
  <form id="designform" autocomplete="off">
<div class="form-group row mb-0">
<label for="x" class="col-sm-4 col-form-label">Dividend</label>
<div class="col-sm-8">
<input type="number" v-model="dividend" class="form-control" autofocus>
</div>
</div>
<div class="form-group row mb-0">
<label class="col-sm-4 col-form-label">&nbsp;</label>
<div class="col-sm-8 h2">&divide;</div>
</div>
<div class="form-group row">
<label for="x2" class="col-sm-4 col-form-label">Divisor</label>
<div class="col-sm-8">
<input type="number" step="any" id="x2" v-model="divisor" class="form-control">
</div>
</div>
<div class="form-group row">
<label class="col-sm-4 col-form-label">&nbsp;</label>
<div class="col-sm-8">
<button type="button" @click="convertdiv()" class="btn btn-primary"><span>=></span> Answer</button>
<button type="reset" @click="reset()" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label for="y" class="col-sm-4 col-form-label">Quotient (decimal)</label>
<div class="col-sm-8">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="quotientdec" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="y2" class="col-sm-4 col-form-label">Quotient (integer)</label>
<div class="col-sm-8">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="quotientint" class="form-control" readonly>
</div>
</div>
<div class="form-group row mb-0">
<label for="y3" class="col-sm-4 col-form-label">Remainder</label>
<div class="col-sm-8">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="remainder" class="form-control" readonly>
</div>
</div>
<div class="form-group row mb-0">
<label for="y3" class="col-sm-4 col-form-label">&nbsp;</label>
</div>
</form>
</div><br>
<div class="">

</div>
  </div>
</div></div>

<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-margin">
    <div class="w3-container w3-white">
      <div class="w3-margin w3-white">
          <div class="w3-container w3-padding">
        <h1 class=""><b>Other Number tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/addition-table"> Addition Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/logarithm-calculator"> Logarithm Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/decimal-to-fraction"> Decimal to fraction</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/division-calculator"> Division Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
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
import { BigNumber } from 'bignumber.js';
export default {
  head() {
    // sets document title
    return {
      title: 'Remainder calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Online remainder calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/remainder-calculator'}
    ]
    }
    },
  data(){
    return {
      dividend: '',
      divisor: '',
      quotientdec: '',
      quotientint: '',
      remainder: '',
      fractclicked1: false
    }
  },
  methods: {
    simple(){
this.showleft = true;
this.showright = true;
    },
    simpleclicked(){
      this.showleft = false;
      this.showright = false;
    },
    reset(){
      this.dividend = '';
      this.divisor = '';
      this.quotientdec = '';
      this.quotientint = '';
      this.remainder = '';
    },
    convertdiv(){
      this.fractclicked1 = true;
      setTimeout(() => this.fractclicked1 = false, 500);
      var x1val=this.dividend;
    var x2val=this.divisor;
    var x1 = new BigNumber(x1val);
    var x2 = new BigNumber(x2val);
    var y = x1.div(x2);
    var y2 = x1.idiv(x2).toString();
    var y3 = x1.mod(x2);
    if( x2.eq(0) )
    y = y2 = y3 = undefined;

    this.quotientdec = y;
    this.quotientint = y2;
    this.remainder = y3;
  }
}
}
</script>

<style lang="css" scoped>
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
 #designform { padding:20px; max-width:500px; background:#a7c9b8; }
 #designform td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #designform td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #designform .btn span { font-weight: bold; font-size:large; }
 #designform .btn img { filter:invert(1); }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
 }
</style>
