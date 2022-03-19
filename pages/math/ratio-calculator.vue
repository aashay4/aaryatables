<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Ratio Calculator<hr>
          <h1 class="w3-text-teal"><b>Ratio Calculator</b></h1>
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
<table class="calc" style="padding:15px; width:100%">
<tr>
<td>Enter ratio:</td>
</tr>
<tr>
<td class="">
<input type="text" v-model="firstvalue" style="width:50px; text-align:center" autofocus>
<span style="font-weight:bold;">:</span>
<input type="text" v-model="secondvalue" name="b" style="width:50px; text-align:center">
</td>
</tr>
<tr>
<td>&nbsp;</td>
</tr>
<tr>
<td>
<button type="button" title="Calculate" class="btn btn-secondary" @click="fract1()"> Calculate</button>
<button type="reset" @click="reset()" title="Reset" class="btn btn-secondary"> Reset</button>
</td>
</tr>
<tr>
<td>&nbsp;</td>
</tr>
<tr>
<td><textarea v-model="ans2" rows="3" style="width:100%; font-size:x-large"></textarea></td>
</tr>
</table>
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
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percent-error-calculator"> Percent error calculator</a></span><br>
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
      title: 'Ratio Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Ratio Calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/ratio-calculator'}
    ]
    }
    },
  data(){
    return {
      ans2: '',
      fractclicked1: false,
      decdiv: false,
      firstvalue: '',
      secondvalue: '',
      change: '',
      pchange: '',
      difference: '',
      explanation: '',
      decrease: ''
    }
  },
  methods: {
    reset(){
      this.firstvalue = '';
      this.secondvalue = '';
      this.ans2 = '';
      this.difference = '';
      this.explanation = '';
      this.decdiv = false;
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
  fract1(){
    var a = this.firstvalue;
    var b = this.secondvalue;
    var out=a+":"+b;
    a==Math.round(a);
    var int_a=(a==Math.round(a));
    var int_b=(b==Math.round(b));
    var g=1;
    if( int_a && int_b )
      g=this.gcd(a,b);
    if( (g!=1)&&((a/g)!=1)&&((b/g)!=1) )
    //  out+=" = "+(a/g)+":"+(b/g);
      if( a!=1 )
      out+=" = 1:"+(b/a);
    if( b!=1 )
      out+=" = "+(a/b)+":1";
    this.ans2 = out;
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
 #boxx { padding:20px; max-width:500px; background:#a7c9b8; }
 #boxx td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #boxx td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #boxx .btn span { font-weight: bold; font-size:large; }
 #boxx .btn img { filter:invert(1); }
 #boxx { padding:10px; }
 #boxx td input[type=number] { width:60px; }
 #boxx td input[type=text] { width:60px; }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
 }
</style>
