<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Root calculator<hr>
          <h1 class="w3-text-teal"><b>Square root calculator</b></h1>
          <p>Simple and nth Square root calculator.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">
  <form id="designform" name="designform" autocomplete="off">
    <label class="btn btn-secondary">
    <input type="radio" name="fractype" @click="simple()" checked> Simple square root
    </label>
    <label class="btn btn-secondary">
    <input type="radio" name="fractype" @click="simpleclicked()"> Nth root
    </label>
    <div class="form-group">
      <p>Enter fractions: </p>
    </div>
    <div v-if="showleft === true" class="form-group input-group">
<span>&#8730;</span>
<span>
<input type="text" v-model="x" class="form-control" autofocus>
</span>
<div class="form-group">
<button type="button" @click="simpleroot()" class="btn btn-secondary"><span>=</span> Calculate</button>
<button @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group input-group">
<input :class="{ buttonclicked1 : fractclicked1 }" type="text" v-model="y" class="form-control" readonly>
<div class="input-group-append">
<button type="button" title="Ans" class="btn btn-outline-secondary input-group-text">Ans</button>
</div>
</div>

</div>

<form id="designform2" v-if="showright === true" name="designform2" autocomplete="off">
<div class="form-group input-group">
<input type="number" min="2" step="1" v-model="n" class="form-control w-25">
<div class="input-group-append">
<span>&#8730;</span>
<span>
<input type="text" v-model="x2" class="form-control">
</span>
</div>
</div>
<div class="form-group">
<button type="button" @click="nthroot()" class="btn btn-secondary"><span>=</span> Calculate</button>
<button type="reset" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group input-group">
<input :class="{ buttonclicked1 : fractclicked1 }" type="text" v-model="y2" class="form-control" readonly>
<div class="input-group-append">
<button type="button" title="Ans" class="btn btn-outline-secondary input-group-text">Ans</button>
</div>
</div>
</form>

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
      title: 'Square root calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Square root calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/root-calculator'}
    ]
    }
    },
  data(){
    return {
      showleft: true,
      showright: false,
      fractclicked1: false,
      x: '',
      y: '',
      y2: '',
      n: '',
      x2: ''
    }
  },
  methods: {
    simple(){
this.showleft = true;
this.showright = false;
    },
    simpleclicked(){
      this.showleft = false;
      this.showright = true;
    },
    reset(){
      this.showleft = true;
      this.showright = false;
      this.fractclicked1 = false;
      this.x = "";
      this.y = "";
      this.y2 = "";
      this.n = "";
      this.x2 = "";
    },
    simpleroot(){
      this.fractclicked1 = true;
      setTimeout(() => this.fractclicked1 = false, 500);
      this.y = '';
var x=this.str2num(this.x);
if( x<0 ) return;
var y = Math.pow(x,0.5);
y = this.roundresult(y);
if( x>0 ) y='\u00B1'+y;
this.y = y;
},
nthroot(){
  this.fractclicked1 = true;
  setTimeout(() => this.fractclicked1 = false, 500);

  this.y2 = '';
var n=this.n;
var x=this.str2num(this.x2);
if( n!=Math.round(n) ) return;
if( x<0 && (n%2)==0 ) return;
var minus=false;
if( x<0 ) { x=Math.abs(x); minus=true; }
var y = Math.pow(x,1/n);
y = this.roundresult(y);
if( minus==false && (n%2)==0 ) y='\u00B1'+y;
if( minus ) y='-'+y;
this.y2 = y;

},
roundresult(x) {
  var y = parseFloat(x);
  y = this.roundnum(y,10);
  return y;
},
removeAt(s,i) {
  s = s.substring(0,i)+s.substring(i+1,s.length);
  return s;
},
roundnum(x,p) {
  var i;
  var j;
  var n=parseFloat(x);
  var m=n.toFixed(p);
  var y=String(m);
  i=y.length;
  j=y.indexOf('.');
  if( i>j && j!=-1 )
  {
    while(i>0)
    {
      if(y.charAt(--i)=='0')
        y = this.removeAt(y,i);
      else
        break;
    }
    if(y.charAt(i)=='.')
      y = this.removeAt(y,i);
  }
  return y;
},
str2num(s)
{
   s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
   if( s=='' ) return 0;
   return Function('"use strict";return ('+s+')')();
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
