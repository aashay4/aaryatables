<template lang="html">
<div>
  <div class="">

    <div class="w3-content" style="max-width:1400px">
<div class="w3-row">
<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
    <div class="w3-container w3-padding">
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Division Calculator<hr>
      <h1 class="w3-text-teal"><b>Division Calculator</b></h1>
      <form id="calcform" autocomplete="off">
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
<button type="reset" onclick="setfocus()" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label for="y" class="col-sm-4 col-form-label">Quotient (decimal)</label>
<div class="col-sm-8">
<input type="text" id="y" v-model="quotientdec" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="y2" class="col-sm-4 col-form-label">Quotient (integer)</label>
<div class="col-sm-8">
<input type="text" id="y2" v-model="quotientint" class="form-control" readonly>
</div>
</div>
<div class="form-group row mb-0">
<label for="y3" class="col-sm-4 col-form-label">Remainder</label>
<div class="col-sm-8">
<input type="text" id="y3" v-model="remainder" class="form-control" readonly>
</div>
</div>
<div class="form-group row mb-0">
<label for="y3" class="col-sm-4 col-form-label">&nbsp;</label>
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
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/fractions-calculator"> Fractions Calculator</a></span><br>
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
</div>
</template>

<script>
import { BigNumber } from 'bignumber.js';

export default {
  head() {
    // sets document title
    return {
      title: 'Division Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Division Calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/division-calculator'}
    ]
    }
    },
  data(){
    return {
      dividend: '',
      divisor: '',
      quotientdec: '',
      quotientint: '',
      remainder: ''
        }
  },
  methods: {
    convertdiv(){
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
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.2rem; }
h4 { font-size:1.2rem; }
.btn span { font-size:large; font-weight:bold; }
.calcform { background:#f0eedc; padding:15px; border-radius:7px; margin-bottom:20px; }
.calcform div { display:inline-block; }
.calcform div:nth-child(2) { margin-top:10px; }
.calcform div:nth-child(1) input[type=text] { width:100px; display:inline-block; }
.calcform div:nth-child(2) input[type=text] { width:100px; display:inline-block; margin-left:5px; }
.calcform div:nth-child(3) { display:none; margin-top:10px; }
#calcform4 input[type=text] { margin-top:10px; }
#tbl5 tr:nth-child(2) td:nth-child(4) { border-bottom:2px #666 solid }
@media all and (max-width: 672px) {
   .calcform { padding:10px; }
   .calcform div:nth-child(2) { display:block; }
   .calcform input[type=text] { margin:5px 0; }
   .calcform div:nth-child(1) input[type=text] { width:90px; }
   #calcform5 { padding:10px; }
   #calcform5 button[type=reset] { float:left; }
   #resetbtn1 { display:none; }
}
@media all and (min-width: 673px) {
   .calcform div:nth-child(2) { margin-left:20px; }
   #resetbtn2 { display:none; }
}

</style>
