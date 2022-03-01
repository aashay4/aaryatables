<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Scientific Notation Calculator<hr>
          <h1 class="w3-text-teal"><b>Scientific Notation Calculator</b></h1>
          <p>Scientific notation calculator and conversion tool.</p>
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
    <table class="">
    <tbody>
    <tr>
      <label class="col-sm-4 col-form-label">First number:</label>
    <td rowspan="2">
      <input style="" type="number" v-model="n1" class="intext" autofocus></td><span class="math">&times;10&nbsp;</span>

    <td><input type="number" step="any" v-model="e1" style="width:70px; text-align:left" class="intext"></td>
    <td rowspan="2"></td>
    </tr>
    <tr>
    <td colspan="3">&nbsp;</td>
    </tr>
    <tr>
      <div class="form-group row mb-0">
      <div class="input-group col-sm-9">
<select class="form-control" v-model="option" name="op">
<option>+</option>
<option>-</option>
<option>&times;</option>
<option>&divide;</option>
</select>
</div>
      </div>
    </tr>
    <tr>
      <label class="col-sm-4 col-form-label">Second number:</label>
    <td rowspan="2">
      <input style="" type="number" step="any" name="x3" v-model="n2" class="intext" autofocus></td><span class="math">&times;10&nbsp;</span>

    <td><input type="number" step="any" name="x4" v-model="e2" style="width:70px; text-align:left" class="intext"></td>
    <td rowspan="2"></td>
    </tr>
    <tr>
    <td colspan="3">&nbsp;</td>
    </tr>
    </tbody>
    </table>
<div class="form-group row">
<label class="col-sm-4 col-form-label">&nbsp;</label>
<div class="col-sm-8">
<button type="button" @click="convertdiv()" class="btn btn-primary"><span>=></span> Answer</button>
<button type="reset" @click="reset()" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label for="y" class="col-sm-4 col-form-label">Scientific notation result</label>
<div class="col-sm-8">
<input type="text" v-model="science" :class="{ buttonclicked1 : fractclicked1 }" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="y2" class="col-sm-4 col-form-label">E notation</label>
<div class="col-sm-8">
<input type="text" v-model="enotation" :class="{ buttonclicked1 : fractclicked1 }" class="form-control" readonly>
</div>
</div>
<div class="form-group row mb-0">
<label for="y3" class="col-sm-4 col-form-label">Notation result</label>
<div class="col-sm-8">
<input type="text" v-model="notation" :class="{ buttonclicked1 : fractclicked1 }" class="form-control" readonly>
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
      title: 'Scientific Notation Calculator (calculator)',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Scientific Notation Calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/scientific-notation-calculator'}
    ]
    }
    },
  data(){
    return {
      option: '+',
      science: '',
      notation : '',
      enotation: '',
      fractclicked1: false,
      n1: '',
      e1: '',
      n2: '',
      e2: ''
    }
  },
  methods: {
    reset(){
      this.option = '+';
      this.science = '';
      this.notation = '';
      this.enotation = '';
      this.n1 = '';
      this.n2 = '';
      this.e1 = '';
      this.e2 = '';
    },
    convertdiv(){
      this.fractclicked1 = true;
      setTimeout(() => this.fractclicked1 = false, 500);
      var n1 = this.str2num(this.n1);
var e1 = this.str2num(this.e1);
var n2 = this.str2num(this.n2);
var e2 = this.str2num(this.e2);
var i = this.option;
//if( e1=="" ) e1="0";
//if( e2=="" ) e2="0";
e1 = parseInt(e1);
e2 = parseInt(e2);

var dec1 = n1*Math.pow(10,e1);
var dec2 = n2*Math.pow(10,e2);
if(i=='+')
{
   var dec = dec1+dec2;
   var en = dec.toExponential();
   var n=en;
   var e=0;
   var i=en.indexOf('e');
   if( i!=-1 )
   {
      n = en.substring(0,i);
      e = en.substring(i+1,en.length);
   }
   e = parseInt(e);
}
else if(i=='-')
{
   var dec = dec1-dec2;
   var en = dec.toExponential();
   n=en; e=0;
   i=en.indexOf('e');
   if( i!=-1 )
   {
      n = en.substring(0,i);
      e = en.substring(i+1,en.length);
   }
   e = parseInt(e);
}
else if(i=='×')
{
   n = n1*n2;
   e = e1+e2;
   dec = n*Math.pow(10,e);
}
else
{
   n = n1/n2;
   e = e1-e2;
   dec = n*Math.pow(10,e);
}
if( n==0 )
   f=0;
else
   var f = Math.floor( Math.log(Math.abs(n))*Math.LOG10E );
var norm = n/Math.pow(10,f);
norm = this.roundnum(norm,10);
var norm2= parseInt(e)+f;
var sign=""; if(norm2>=0) sign="+";
en = norm+"e"+sign+norm2;

this.notation = dec;
this.enotation = en;
this.science = norm + ' × 10^' + norm2;
this.sci = norm;
this.sci2 = norm2;

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
.calc, table.calc td { background:#a7c9b8; }
#designform { background:#a7c9b8; padding:20px; }
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
 #op { font-weight:bold; }
 #td11, #td14 { display:none; }
#td12, #tabetd, #tabetd14 { padding-bottom:0px; }
#td21, #td22, #tabetd1455, #td42 { border-top:#666 3px solid; padding-top:1px; }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
 }
</style>
