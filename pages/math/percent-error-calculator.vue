<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Percent error calculator<hr>
          <h1 class="w3-text-teal"><b>Percent error calculator</b></h1>
          <p>Find out the accurate error in the number with this percent error calculator.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">
  <form id="inputstyle" name="inputstyle" autocomplete="off">
<div class="form-group row">
<label class="col-sm-5 col-form-label">Enter changed value:</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="firstvalue" name="e" class="form-control" autofocus>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Actual value:</label>
<div class="col-sm-7">
<input type="number" step="any" v-model="change" class="form-control">
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
<label class="col-sm-5 col-form-label">Error in percentage:</label>
<div class="col-sm-7 input-group">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="pchange" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">%</span>
</div>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">+/-</label>
<div class="col-sm-7 input-group">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="difference" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label class="col-sm-5 col-form-label">Difference:</label>
<div class="col-sm-7 input-group">
<input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="explanation" class="form-control" readonly>
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
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-change-calculator"> Percent change calculator</a></span><br>
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
      title: 'Percent error calculator | Calculate error in percent',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Percent error calculator online.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/percent-error-calculator'}
    ]
    }
    },
  data(){
    return {
      fractclicked1: false,
      firstvalue: '',
      change: '',
      pchange: '',
      difference: '',
      explanation: ''
    }
  },
  methods: {
    reset(){
      this.firstvalue = '';
      this.change = '';
      this.pchange = '';
      this.difference = '';
      this.explanation = '';
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
    var v1 = this.firstvalue;
var v2 = this.change;
var aerr = Math.abs(v1-v2);
var naperr = this.roundresult((v1-v2)/v2*100);
var perr = Math.abs(naperr);
this.pchange = perr+"%";
this.difference = naperr+"%";
this.explanation = aerr;

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
 #inputstyle { padding:20px; max-width:500px; background:#a7c9b8; }
 #inputstyle td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #inputstyle td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #inputstyle .btn span { font-weight: bold; font-size:large; }
 #inputstyle .btn img { filter:invert(1); }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #inputstyle { padding:10px; }
    #inputstyle td input[type=number] { width:60px; }
    #inputstyle td input[type=text] { width:60px; }
 }
</style>
