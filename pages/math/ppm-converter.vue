<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">
        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; ppm converter Calculator<hr>
          <h1 class="w3-text-teal"><b>Convert ppm</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
          <p>A simple to use ppm calculator.</p>
<div class="">
  <form id="desingiput" autocomplete="off">
<table class="calc2">
<tbody>
<tr>
<td><label for="ratio">Enter decimal:</label></td>
<td class="math"><input @input="Convert_Ratio()" type="number" step="any" v-model="ratio" name="ratio"></td>
<td class="mathsymbol">&nbsp;</td>
</tr>
<tr>
<td><label for="percent">Enter percent:</label></td>
<td class="math"><input @input="Convert_Percent()" type="number" min="0" step="any" v-model="percent" name="percent"></td>
<td class="mathsymbol"></td>
</tr>
<tr>
<td><label for="permil">Enter permille:</label></td>
<td class="math"><input @input="Convert_Permil()" type="number" min="0" step="any" v-model="permil" name="permil"></td>
<td class="mathsymbol">&permil;</td>
</tr>
<tr>
<td><label for="ppm">Enter ppm:</label></td>
<td class="math"><input @input="Convert_PPM()" type="number" min="0" step="any" v-model="ppm" name="ppm"></td>
<td class="mathsymbol">ppm</td>
</tr>
<tr>
<td><label for="ppb">Enter ppb:</label></td>
<td class="math"><input @input="Convert_PPB()" type="number" min="0" step="any" v-model="ppb" name="ppb"></td>
<td class="mathsymbol">ppb</td>
</tr>
<tr>
<td><label for="ppt">Enter ppt:</label></td>
<td class="math"><input @input="Convert_PPT()" type="number" min="0" step="any" v-model="ppt" name="ppt"></td>
<td class="mathsymbol">ppt</td>
</tr>
<tr>
<td class="mathsymbol"><input type="button" @click="reset()" value="Reset"></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</tbody>
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
              <span class="w3-large"><a class="removelink" href="/math/fraction-to-decimal"> Fraction to decimal</a></span><br>
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
      title: 'ppm converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'ppm conversion tool.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/ppm-converter'}
    ]
    }
    },
  data(){
    return {
      ratio: '',
      percent: '',
      permil: '',
      ppm: '',
      ppb: '',
      ppt: ''
    }
  },
  methods: {
    reset(){
      this.ratio = "";
      this.percent = "";
      this.permil = "";
      this.ppm = "";
      this.ppb = "";
      this.ppt = "";
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
Convert_Ratio()
{
  var ratio = this.ratio;
  if( ratio=="" )
    return;
  ratio = parseFloat(ratio);
  this.percent = this.roundnum(ratio*100, 12);
  this.permil  = this.roundnum(ratio*1e3, 12);
  this.ppm 	= this.roundnum(ratio*1e6, 12);
  this.ppb 	= this.roundnum(ratio*1e9, 12);
  this.ppt 	= this.roundnum(ratio*1e12, 12);
},
Convert_Percent()
{
  var percent = this.percent;
  if( percent=="" )
    return;
  percent = parseFloat(percent);
  this.ratio   = this.roundnum(percent/100, 12);
  this.permil  = this.roundnum(percent*1e1, 12);
  this.ppm 	= this.roundnum(percent*1e4, 12);
  this.ppb 	= this.roundnum(percent*1e7, 12);
  this.ppt 	= this.roundnum(percent*1e10, 12);
},
 Convert_Permil()
{
  var permil = this.permil;
  if( permil=="" )
    return;
  permil = parseFloat(permil);
  this.ratio   = this.roundnum(permil/1e3, 12);
  this.percent = this.roundnum(permil/1e1, 12);
  this.ppm 	= this.roundnum(permil*1e3, 12);
  this.ppb 	= this.roundnum(permil*1e6, 12);
  this.ppt 	= this.roundnum(permil*1e9, 12);
},
Convert_PPM()
{
  var ppm = this.ppm;
  if( ppm=="" )
    return;
  ppm = parseFloat(ppm);
  this.ratio   = this.roundnum(ppm/1e6, 12);
  this.percent = this.roundnum(ppm/1e4, 12);
  this.permil 	= this.roundnum(ppm/1e3, 12);
  this.ppb 	= this.roundnum(ppm*1e3, 12);
  this.ppt 	= this.roundnum(ppm*1e6, 12);
},
Convert_PPB()
{
  var ppb = this.ppb;
  if( ppb=="" )
    return;
  ppb = parseFloat(ppb);
  this.ratio   = this.roundnum(ppb/1e9, 12);
  this.percent = this.roundnum(ppb/1e7, 12);
  this.permil 	= this.roundnum(ppb/1e6, 12);
  this.ppm 	= this.roundnum(ppb/1e3, 12);
  this.ppt 	= this.roundnum(ppb*1e3, 12);
},
Convert_PPT()
{
  var ppt = this.ppt;
  if( ppt=="" )
    return;
  ppt = parseFloat(ppt);
  this.ratio   = this.roundnum(ppt/1e12, 12);
  this.percent = this.roundnum(ppt/1e10, 12);
  this.permil 	= this.roundnum(ppt/1e9, 12);
  this.ppm 	= this.roundnum(ppt/1e6, 12);
  this.ppb 	= this.roundnum(ppt/1e3, 12);
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
 #desingiput { background:#a7c9b8; padding:20px; }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    .ntable td { width:120px; }
.calc2 button { margin:20px auto; padding:7px; }
 }
</style>
