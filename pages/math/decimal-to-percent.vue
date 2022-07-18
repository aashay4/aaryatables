<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">
        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Decimal to percent converter<hr>
          <h1 class="w3-text-teal"><b>Learn how to convert number to percentage.</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
          <p>Number to fraction converter.</p>
<div class="">
  <form id="desingiput" name="desingiput" autocomplete="off">
<div class="form-group">
<label >Enter number here:</label>
<div class="input-group">
<input type="number" v-model="x" min="0" step="any" class="form-control" required>
</div>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="calculate()"><span>=></span> Answer</button>
<button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<label for="y">Result in percentage:</label>
<div class="input-group">
<input type="text" v-model="y" class="form-control" readonly>
</div>
</div>
<div class="form-group">
<label for="y">Calculation</label>
<div class="input-group">
<textarea type="text" v-model="area" class="form-control outtext" readonly></textarea>
</div>
</div>
</form><br>


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
      title: 'Convert decimal to percentage with this conversion tool',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Decimal to percentage calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/decimal-to-percent'}
    ]
    }
    },
  data(){
    return {
      area: '',
      showy: false,
      x: '',
      thrrepiece: '',
      minusvalue: false,
      d1: '',
      n2: '',
      d2: '',
      n3: '',
      d3: '',
      d4: '',
      n4: '',
      sign: '',
      x2: '',
      x3: '',
      n31: '',
      selected: '',
      n: '',
      y: '',
      d: ''
    }
  },
  methods: {
    reset(){
      this.area = "";
      this.showy = false;
      this.x1 = "";
      this.thrrepiece = "";
      this.minusvalue = false;
      this.d1 = "";
      this.n2 = "";
      this.d2 = "";
      this.n3 = "";
      this.d3 = "";
      this.d4 = "";
      this.n4 = "";
      this.sign = "";
      this.x2 = "";
      this.x3 = "";
      this.n31 = "";
      this.selected = "";
      this.n = "";
      this.y = "";
      this.d = "";
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
  calculate(){
    var x = this.x;
  var y = parseFloat(x);
  var n = y*100;
  n = this.roundresult(n);
  y = x+"\u00D7100% \n= "+n+"%";
  this.y = n+"%";
  this.area = y;
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
 }
</style>
