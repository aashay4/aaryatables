<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Fraction to decimal<hr>
          <h1 class="w3-text-teal"><b>Fraction to decimal</b></h1>
          <p>Simple fraction to decimal calculator. For the simple fraction to decimal conversion, leave the left box blank, our tool will still work. For the mixed conversion, enter all three numbers.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">
  <form id="inputdesign" name="inputdesign" autocomplete="off">
    <label class="btn btn-secondary">
    <input type="radio" name="fractype" @click="simpleclicked()" checked> Simple Fractions
    </label>
    <label class="btn btn-secondary">
    <input type="radio" name="fractype" @click="simple()"> Mixed Fractions
    </label>
    <div class="form-group">
      <p>Enter fractions: </p>
    </div>
    <table>
    <tr>
    <td rowspan="2"><input v-if="showleft === true" type="text" v-model="y" class="form-control"></td>
    <td id="tabetd14"><input type="text" v-model="n" class="form-control"></td>
    </tr>
    <tr>
    <td  id="tabetd1455"><input type="text" v-model="d" class="form-control"></td>
    </tr>
  </table><br>
    <div class="form-group">
    <button type="button" title="Calculate" class="btn btn-secondary" @click="fract()"><span>=></span> Answer</button>
    <button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>↺</span> Reset</button>
    </div><hr>
<div class="form-group mt-3">
<table>
  <tr>
  <td><label for="x">Answer in decimal number:</label></td>
  </tr>
  <tr>
  <td class="math"><input type="text" style="width: 100%" v-model="x1" id="x" name="x" class="intext" readonly></td>
</tr><hr>
  <tr>
  <td>Calculation:</td>
  </tr>
  <tr>
  <td><textarea rows="3" v-model="area" class="outtext" readonly></textarea></td>
  </tr>

</table>
</div>

</form>

</div><br>
<div class="">
  <h2>How to convert fraction to decimal?</h2>
  <p>Expand the denominator to the power of 10 and the best way to do this is just to make it multiply by 10.</p>
  <p>For example, consider we want to convert the number 3/4 into a decimal number. To convert this fraction into an equivalent decimal number, you need to multiply the with 25.</p>
  <p> => After multiplying it by 25, you will get 3×25/4×25</p>
  <p> => 75/100</p>
  <p> => 0.75</p>
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
export default {
  head() {
    // sets document title
    return {
      title: 'Fraction to decimal calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Fraction to decimal converter' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/fraction-to-decimal'}
    ]
    }
    },
  data(){
    return {
      area: '',
      showleft: false,
      showright: false,
      x1: '',
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
      this.area = '';
      this.x1 = '';
      this.y = '';
      this.n = '';
      this.d = '';
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
    var aa = this.y;
    var ab = this.n;
    var ad = this.d;
    var s = 1;
          var x = this.str2num(aa);
          var n = this.str2num(ab);
          var d = this.str2num(ad);
          if( n=='' || d=='' )
          {
             alert("Please enter fraction");
             return;
          }
          if( x=='-' ) { s=-1; x='0'; }
          if( x=='' ) x='0';
          x = this.str2num(x);
          n = parseInt(n);
          d = parseInt(d);
          if( x<0 ) { s=-1; x=-x; }
          if( x==0 && (n/d)<0 ) { s=-1; }
          n = Math.abs(n);
          d = Math.abs(d);
          if( x!=0 )
          {
             this.n=n;
             this.d=d;
          }
          var y = s*(x+n/d);
          var y = this.roundresult(y);
          this.x1=y;
          var out='';
          if( s==-1 ) out+='-';
          if( x!=0 ) {
             out+=x;
             if( s==-1 )
                out+='-';
             else
                out+='+';
          }
          out+=n+'/'+d;
          out+='\n= '+y;
          out+='\n= '+this.roundresult(y*100)+'%';
          this.area=out;
          //var nl=(d>15?true:false);
          //var obj = document.getElementById("frac");

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
 #inputdesign { padding:20px; max-width:500px; background:#a7c9b8; }
 #inputdesign td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #inputdesign td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #inputdesign .btn span { font-weight: bold; font-size:large; }
 #inputdesign .btn img { filter:invert(1); }
 #tabetd, #tabetd14 { padding-bottom:0px; }
 #tabetd1455 { border-top:#666 3px solid; padding-top:1px; }
 #oooppp { margin-right:0; padding:10px; border:1px #ccc solid; background:#e9ecef; }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #inputdesign { padding:10px; }
    #inputdesign td input[type=number] { width:60px; }
    #inputdesign td input[type=text] { width:60px; }
 }
</style>
