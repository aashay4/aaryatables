<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Fractions Calculator<hr>
          <h1 class="w3-text-teal"><b>Fractions Calculator</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
          </Adsense>
<div class="">
  <form id="calcform" name="calcform" autocomplete="off">
  <div class="btn-group" data-toggle="buttons">
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simpleclicked()" checked> Simple Fractions
  </label>
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simple()"> Mixed Fractions
  </label>
  </div>
  <div class="form-group mt-3">
  <table>
  <tr>
  <td id="td11" rowspan="2" v-if="showleft === true"><input type="number" step="1" v-model="x1" class="form-control form-control-lg"></td>
  <td id="td12"><input type="number" step="1" v-model="n1" class="form-control" autofocus></td>
  <td id="td13" rowspan="2" class="pl-2 pr-2">
  <select id="op" v-model="selected" class="form-control form-control-lg">
  <option selected>+</option>
  <option>-</option>
  <option>&times;</option>
  <option>&divide;</option>
  </select>
  </td>
  <td id="td14" rowspan="2" v-if="showright === true"><input type="number" step="1" v-model="x2" class="form-control form-control-lg"></td>
  <td id="td15"><input type="number" step="1" v-model="n2" class="form-control"></td>
  </tr>
  <tr>
  <td id="td21"><input type="number" step="1" v-model="d1" class="form-control"></td>
  <td id="td22"><input type="number" step="1" v-model="d2" class="form-control"></td>
  </tr>
  </table>
  </div>
  <div class="form-group">
  <button type="button" title="Calculate" class="btn btn-secondary" @click="fract()"><span>= ></span> Calculate</button>
  <button type="reset" title="Reset" class="btn btn-secondary" onclick="freset()"><span>&times;</span> Reset</button>
  </div>
  <div class="form-group">
  <label>Result</label>
  <table>
  <tr>
  <td id="td31"><input type="text" v-model="n3" class="form-control" readonly></td>
  <td id="td32" v-if="equalshow === true" rowspan="2" class="pl-2 pr-2">=</td>
  <td id="td33" rowspan="2" v-if="x3if === true"><input type="text" v-model="x3" class="form-control" readonly></td>
  <td id="td34" v-if="n4if === true"><input type="text" v-model="n4" class="form-control" readonly></td>
  </tr>
  <tr>
  <td id="td41"><input type="text" v-model="d3" class="form-control" readonly></td>
  <td id="td42" v-if="d4if === true"><input type="text" v-model="d4" class="form-control" readonly></td>
  </tr>
  </table>
  </div>
  </form>


</div><br>
<div class="">
  <h2>Fractions calculator Examples:</h2>
  <p><b>Addition:</b></p>
  <p>3/7 + 4/9 = (3&times;9) + (7&times;4) / (9&times;7) = 27+28/63 = 55/63</p>
  <p><b>Subtraction</b></p>
  <p>1/3 - 1/4 = (1&times;4) - (1&times;3) / (4&times;3) = (4-3) / 12 = 1/12</p>
  <p><b>Multiplication</b></p>
  <p>1/3 &times; 1/4 = (1&times;1) / (4&times;3) = 1/12</p>
  <p><b>Division</b></p>
  <p>1/3 &divide; 1/4 = (1&times;1) / (4&times;3) = 1/12</p>
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
export default {
  head() {
    // sets document title
    return {
      title: 'Fractions Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'fractions calculator online' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/fractions-calculator'}
    ]
    }
    },
  data(){
    return {
      equalshow: false,
      x3if: false,
      n4if: false,
      d4if: false,
      showleft: false,
      showright: false,
      n1: '',
      thrrepiece: '',
      minusvalue: false,
      d1: '',
      n2: '',
      d2: '',
      x1: '',
      x2: '',
      n3: '',
      d3: '',
      d4: '',
      n4: '',
      sign: '',
      x2: '',
      x3: '',
      n31: '',
      selected: '+'
    }
  },
  methods: {
    freset(){
      this.x3if = false;
      this.n4if = false;
      this.d4if = false;
      this.showleft = false;
      this.showright = false;
      this.n1 = '';
      this.thrrepiece = '';
      this.minusvalue = false;
      this.d1 = '';
      this.equalshow = '';
      this.n2 = '';
      this.d2 = '';
      this.x1 = '';
      this.x2 = '';
      this.n3 = '';
      this.d3 = '';
      this.d4 = '';
      this.n4 = '';
      this.sign = '';
      this.x2 = '';
      this.x3 = '';
      this.n31 = '';
      this.selected = '+';
    },
    simple(){
this.showleft = true;
this.showright = true;
    },
    simpleclicked(){
      this.showleft = false;
      this.showright = false;
    },
    reset(){
      this.n1 = '',
      this.thrrepiece = '';
      this.minusvalue = false;
      this.d1 = '';
      this.n2 = '';
      this.d2 = '';
      this.n3 = '';
      this.d3 = '';
      this.d4 = '';
      this.n4 = '';
      this.sign = '-';
      this.n31 = '';
      this.x2 = '';
      this.x3 = '';
      this.selected = '';
    },
    roundresult(x) {
      var y = parseFloat(x);
      y = this.roundnum(y,10);
      return y;
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
    removeAt(s,i) {
    	s = s.substring(0,i)+s.substring(i+1,s.length);
    	return s;
    },
  fract(){
    var out1 = '';
    var out2 = '';
var s1=1;
var s2=1;
var s3=1;
var a;
var b;
var g;
var n3;
var d3;
var w1 = this.x1;
var n1 = this.n1;
var d1 = this.d1;
var w2 = this.x2;
var n2 = this.n2;
var d2 = this.d2;
var op = this.selected;
if( n1=='' || d1=='' || n2=='' || d2=='' )
{
  alert("Please enter fractions");
  return;
}
if( w1=='-' ) { s1=-1; w1='0'; }
if( w2=='-' ) { s2=-1; w2='0'; }
if( w1=='' ) w1='0';
if( w2=='' ) w2='0';
w1 = parseInt(w1);
n1 = parseInt(n1);
d1 = parseInt(d1);
w2 = parseInt(w2);
n2 = parseInt(n2);
d2 = parseInt(d2);
//op = parseInt(op);
if( w1==0 && (n1/d1)<0 ) s1=-1;
if( w2==0 && (n2/d2)<0 ) s2=-1;
n1 = Math.abs(n1);
d1 = Math.abs(d1);
n2 = Math.abs(n2);
d2 = Math.abs(d2);
if( w1!=0 || w2!=0 )
{
  this.n1 = n1;
  this.d1 = d1;
  this.n2 = n2;
  this.d2 = d2;
}
if( w1<0 ) { s1=-1; w1=-w1; }
if( w2<0 ) { s2=-1; w2=-w2; }

n1 = s1*(n1+w1*d1);
n2 = s2*(n2+w2*d2);
if( op== '+' ) // +
{
  n3 = n1*d2+n2*d1;
  d3 = d1*d2;
}
else if( op== '-' ) // -
{
  n3 = n1*d2-n2*d1;
  d3 = d1*d2;
}
else if( op== '×' ) // x
{
  n3 = n1*n2;
  d3 = d1*d2;
}
else
{
  n3 = n1*d2;
  d3 = d1*n2;
}
if( (n3/d3)<0 ) s3=-1;
n3 = Math.abs(n3);
d3 = Math.abs(d3);
g = this.gcd(n3,d3);
n3/=g;
d3/=g;
var sn3 = s3*n3;
var sd3 = d3;
//out1 = sn3+'/'+sd3;
var sign='';
if( n3>d3 ) {
  var i = Math.floor(n3/d3);
  var j = n3-i*d3;
  if( j>0 ) {
    if( s3==-1 ) sign = '-';
  }
}
this.n3 = sn3;
this.d3 = sd3;
if( n3>d3 ) {
      this.x3 = sign+i;
      this.n4 = j;
      this.d4 = d3;
//      $('#td32').show();
//      $('#td33').show();
  //    $('#td34').show();
    //  $('#td42').show();
    this.x3if = true;
    this.n4if = true;
    this.d4if = true;
    this.equalshow = true;
   }
   else {
//      $('#td32').hide();
  //    $('#td33').hide();
  //    $('#td34').hide();
  //    $('#td42').hide();
  this.x3if = false;
  this.n4if = false;
  this.d4if = false;
  this.equalshow = false;
   }

var ops = [' + ',' - ',' \u00D7 ',' / '][op];
var out = '';
if( w1!='' ) out+=w1+' ';
out += (s1*n1)+'/'+d1;
out += ops;
if( w2!='' ) out+=w2+' ';
out += (s2*n2)+'/'+d2;
if( w1!=0 || w2!=0 ) {
  out += '\n= ';
  out += (n1+d1*w1)+'/'+d1;
  out += ops;
  out += (n2+d2*w2)+'/'+d2;
}
var d4 = d1*d2/this.gcd(d1,d2);
out += '\n= ';
if( op==0 || op==1 ) {
  out += (n1*d4/d1)+'/'+d4+ops+(n2*d4/d2)+'/'+d4;
  if( op==0 ) {
    a = (n1*d4/d1+n2*d4/d2);
    b = d4;
  }
  else {
    a = (n1*d4/d1-n2*d4/d2);
    b = d4;
  }
}
else if( op==2 ) {
  out += '('+n1+'\u00D7'+n2+') / ('+d1+'\u00D7'+d2+')';
  a = (n1*n2);
  b = (d1*d2);
}
else {
  out += '('+n1+'\u00D7'+d2+') / ('+d1+'\u00D7'+n2+')';
  a = (n1*d2);
  b = (d1*n2);
}
out += '\n= ';
out += a+'/'+b;
g = this.gcd(a,b);
if( g>1 )
{
  a/=g;
  b/=g;
  out += '\n= ';
  out += a+'/'+b;
}
out += '\n= ';
out += this.roundresult(a/b);


var w3=0;
if( n3>d3 ) {
  w3 = Math.floor(n3/d3);
  n3 -= w3*d3;
}

  },
  gcd(x, y){
  if ((typeof x !== 'number') || (typeof y !== 'number'))
    return false;
  x = Math.abs(x);
  y = Math.abs(y);
  while(y) {
    var t = y;
    y = x % y;
    x = t;
  }
  return x;
  }
}
}
</script>

<style lang="css" scoped>
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
 #calcform { padding:20px; max-width:500px; background:#a7c9b8; }
 #calcform td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #calcform td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #calcform .btn span { font-weight: bold; font-size:large; }
 #calcform .btn img { filter:invert(1); }
 #op { font-weight:bold; }
#td12, #tabetd, #tabetd14 { padding-bottom:0px; }
#td21, #td22, #tabetd1455, #td42 { border-top:#666 3px solid; padding-top:1px; }
 #oooppp { margin-right:0; padding:10px; border:1px #ccc solid; background:#e9ecef; }
 #craf { height:42px; }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #calcform { padding:10px; }
    #calcform td input[type=number] { width:60px; }
    #calcform td input[type=text] { width:60px; }
 }
</style>
