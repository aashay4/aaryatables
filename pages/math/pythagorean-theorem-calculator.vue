<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; pythagorean theorem calculator<hr>
          <h1 class="w3-text-teal"><b>pythagorean theorem calculator</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">
  <form id="boxx" name="boxx" autocomplete="off">
<div class="form-group row">
<label class="col-sm-5 col-form-label">Enter leg (b):</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="firstvalue" class="form-control" autofocus>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Hypotenuse (c):</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="secondvalue" class="form-control">
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">&nbsp;</label>
<div class="col-sm-7">
<button type="button" title="Calculate" class="btn btn-secondary" @click="fract()"><span>= ></span> Answer</button>
<button type="reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Leg (a) :</label>
<div class="col-sm-7 input-group">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="ans1" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">%</span>
</div>
</div>
</div>
</form><hr>
<div class="">
  <p>Leg (a) conversion:
</p>
</div>
<form id="boxx" name="boxx" autocomplete="off">
<div class="form-group row">
<label class="col-sm-5 col-form-label">Enter leg (a):</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="firstvalue1" class="form-control" autofocus>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Enter leg(b):</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="secondvalue1" class="form-control">
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">&nbsp;</label>
<div class="col-sm-7">
<button type="button" title="Calculate" class="btn btn-secondary" @click="fract1()"><span>= ></span> Answer</button>
<button type="reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Hypotenuse (c) result :</label>
<div class="col-sm-7 input-group">
<input type="text" :class="{ buttonclicked2 : fractclicked2 }" v-model="ans2" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">%</span>
</div>
</div>
</div>
</form><hr>
<div class="">
  <p>Leg (b) conversion:
</p>
</div>
<form id="boxx" name="boxx" autocomplete="off">
<div class="form-group row">
<label class="col-sm-5 col-form-label">Enter leg (a):</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="firstvalue2" class="form-control" autofocus>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Enter hypotenuse:</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="secondvalue2" class="form-control">
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">&nbsp;</label>
<div class="col-sm-7">
<button type="button" title="Calculate" class="btn btn-secondary" @click="fract2()"><span>= ></span> Answer</button>
<button type="reset" @click="reset2()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Leb (b) :</label>
<div class="col-sm-7 input-group">
<input type="text" :class="{ buttonclicked3 : fractclicked3 }" v-model="ans3" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">%</span>
</div>
</div>
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
        <h1 class=""><b>Other tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/arcsin-calculator"> Arcsin calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/arctan-calculator"> Arcstan calculator</a></span><br>
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
      title: 'Pythagorean theorem calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Pythagorean theorem calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/pythagorean-theorem-calculator'}
    ]
    }
    },
  data(){
    return {
      fractclicked1: false,
      fractclicked2: false,
      fractclicked3: false,
      decdiv: false,
      firstvalue: '',
      secondvalue: '',
      firstvalue1: '',
      secondvalue1: '',
      firstvalue2: '',
      secondvalue2: '',
      change: '',
      ans1: '',
      ans2: '',
      ans3:''
    }
  },
  methods: {
    reset(){
      this.firstvalue = '';
      this.secondvalue = '';
      this.ans1 = '';
    },
    reset1(){
      this.firstvalue1 = '';
      this.secondvalue1 = '';
      this.ans2 = '';
    },
    reset2(){
      this.firstvalue2 = '';
      this.secondvalue2 = '';
      this.ans3 = '';
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
    digits_after_period(x)
{
	var f = x.toString();
	var i = f.indexOf('.');
	var len = f.length-i-1;
	return len;
},
  fract(){
    this.fractclicked1 = true;
    setTimeout(() => this.fractclicked1 = false, 500);
    var a = this.firstvalue;
    var b = this.secondvalue;
    var c = Math.sqrt(a*a+b*b);
    this.ans1 = this.roundresult(c);
  },
  fract2(){
    this.fractclicked3 = true;
    setTimeout(() => this.fractclicked3 = false, 500);
    var a = this.firstvalue2;
    var c = this.secondvalue2;
    b = parseFloat(b);
    c = parseFloat(c);
if( a=="" || c=="" ) return;
if( c<a ) {
  alert("infinite")
    this.ans3 = '';
  return;
}
var b = Math.sqrt(c*c-a*a);
this.ans3 = this.roundresult(b);
  },
  fract1(){
    this.fractclicked2 = true;
    setTimeout(() => this.fractclicked2 = false, 500);
    var b = this.firstvalue1;
    var c = this.secondvalue1;
    b = parseFloat(b);
    c = parseFloat(c);
if( b=="" || c=="" ) return;
if( c<b ) {
  alert("infinite")
    this.ans2 = '';
  return;
}
var a = Math.sqrt(c*c-b*b);
this.ans2 = this.roundresult(a);
  },
  str2num(s)
  {
     s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
     if( s=='' ) return 0;
     return Function('"use strict";return ('+s+')')();
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
.buttonclicked1{
  background-color: Violet;
}
.buttonclicked2{
  background-color: Violet;
}
.buttonclicked3{
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
 #boxx { padding:20px; max-width:500px; background:#a7c9b8; }
 #boxx td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #boxx td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #boxx .btn span { font-weight: bold; font-size:large; }
 #boxx .btn img { filter:invert(1); }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #boxx { padding:10px; }
    #boxx td input[type=number] { width:60px; }
    #boxx td input[type=text] { width:60px; }
 }
</style>
