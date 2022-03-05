<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Decimal to Fraction<hr>
          <h1 class="w3-text-teal"><b>Decimal to fraction converter</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
          <p>Simple decimal to fraction calculator.</p>
<div class="">
  <form id="calcform" name="calcform" autocomplete="off">
<div class="form-group mt-3">
<table>
  <tr>
  <td><label for="x">Enter decimal number:</label></td>
  </tr>
  <tr>
  <td class="math"><input type="text" style="width: 100%" v-model="x1" class="form-control" autofocus></td>
  </tr>

</table>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="fract()"><span>=></span> Answer</button>
<button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <p>Fractions answer: </p><hr>
<table>
<tr>
<td rowspan="2" v-if="showy === false"><input type="text" v-model="y" class="form-control" readonly></td>
<td id="tabetd14"><input type="text" v-model="n" class="form-control" readonly></td>
</tr>
<tr>
<td id="tabetd1455"><input type="text" v-model="d" class="form-control" readonly></td>
</tr>
</table>
<table>
<tr>
<td>Calculation:</td>
</tr>
<tr>
<td><textarea rows="7" v-model="area" class="outtext" readonly></textarea>
<input type="submit" style="display: none" /></td>
</tr>
</table>
</div>
</form>

</div><br>
<div class="">
  <h2>Decimal to fraction conversion:</h2>
  <h3>Steps of decimal to fraction:</h3>
  <p>First of all, note down the digits that are on the right side of the decimal point and the power of 10</p>
  <p>Once done, find the greatest common divisor of the same number</p>
  <p>Reduce the fraction by dividing with the greatest common divisor(gcd). You can consider the following example for detailed information.</p>
  <h3>Example for the decimal to fraction conversion:</h3>
  <p>Convert the 0.44 decimal number to fraction:</p>
  <h2>0.44</h2>
  <h1> => 0.44 = 44/100</h1>
    <p>Find out the GCD of the above numbers. Here, in the above number, we have 4.</p>
    <p>Now, divide both numbers with 4.</p>
    <h2> => 0.44 = (44/4)/(100/4)</h2>
    <p>After the division, the answer would be,</p>
    <h2> => 11/25</h2>
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
      title: 'Decimal to fraction converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Free decimal to fraction converter.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/decimal-to-fraction'}
    ]
    }
    },
  data(){
    return {
      area: '',
      showy: false,
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
  fract(){
    var xelem = this.x1;
    var gcd2 = function(a, b, f) {
   if( f )
   {
         if ( b<=1 )
            return a;
      }
      else
   {
         if ( !b )
            return a;
      }
      return gcd2(b, a % b, f);
};

    var sign = '';
  var sign2 = '+';
  var x = this.str2num(xelem);
  var x2 = this.roundresult(x);
  var absx=Math.abs(x2);
  var y=Math.floor(absx);
  var frac=this.roundresult(absx-y);
  if( x2<0 ) sign = sign2 = '-';
  var d = this.digits_after_period(absx);
  var den = Math.round(Math.pow(10,d));
  var num = Math.round(frac*den);
  var len=num.toString().length;
  var f=false;
  if( len>8 ) f=true;
  var g = gcd2(num,den,f);
  var num2 = Math.round(num/g);
  var den2 = Math.round(den/g);
  //var txt=x+"\n";
  var txt=x2+" ";
  if( absx>=1 ) {
  //   document.getElementById('td11').style.display="table-cell";
     //txt+="= "+sign+y+sign2+frac+"\n";
     txt+="= "+sign+y+sign2+frac+" ";
     txt+="= "+sign+y+sign2;
  }
  else {
  //   document.getElementById('td11').style.display="none";
     txt+="= "+sign;
  }
  txt+=num+"/"+den+"\n";
  if( g>1 ) {
     txt+="gcd("+num+","+den+") = "+g+"\n";
     txt+=x2+" ";

     txt+="= "+sign;
     if( absx>=1 )
        txt+=y+sign2;
     txt+="("+num+"/"+g+")/("+den+"/"+g+") ";

     txt+="= "+sign;
     if( absx>=1 )
        txt+=y+sign2;
     txt+=num2+"/"+den2+" ";
  }

  if( y>0 )
     txt+="= "+sign+(num2+den2*y)+"/"+den2;
  this.y=sign+y;
  if(this.y === '0'){
    this.showy === true;
  }
  if(this.y != '0'){
    this.showy === false;
  }
  if( absx>=1 )
     this.n=num2;
  else
     this.n=sign+num2;
  this.d=den2;
  if( frac==0 ) {
    // document.getElementById('td12').style.display="none";
     //document.getElementById('td21').style.display="none";
     txt="";
  }
  else {
  //   document.getElementById('td12').style.display="table-cell";
  //   document.getElementById('td21').style.display="table-cell";
  }
  this.area=txt;

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
 #calcform { padding:20px; max-width:500px; background:#a7c9b8; }
 #calcform td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #calcform td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #calcform .btn span { font-weight: bold; font-size:large; }
 #calcform .btn img { filter:invert(1); }
 #op { font-weight:bold; }
 #td11, #td14 { display:none; }
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
