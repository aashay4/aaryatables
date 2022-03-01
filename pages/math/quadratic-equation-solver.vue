<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Quadratic equation solver<hr>
          <h1 class="w3-text-teal"><b>quadratic equation solver</b></h1>
          <p>An online tool to solve quadratic equations.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">

<form id="designform">
  <table>
    <tbody>
      <tr>
      <td><input type="number" step="any" v-model="x" class="intext"></td>
      <td style="font-size: 2.1em;" class="math"><i>x</i><span style="font-size: 0.8em"><sup>2 </sup>+</span></td>
      <td><input type="number" step="any" v-model="x2" class="intext"></td>
      <td style="font-size: 2.1em" class="math"><i>x </i><span style="font-size: 0.8em">+</span></td>
      <td><input type="number" step="any" v-model="x3" class="intext"></td>
      <td style="font-size: 2.1em" class="math">= 0</td>
      </tr>
      <tr>
      <td>&nbsp;</td>
      </tr>
      <tr>
        <td colspan="6">
        <input @click="fract()" type="button" value="Calculate" class="btn btn-secondary" tabindex="4">
        <input @click="reset()" type="reset" value="Reset" class="btn btn-secondary"></td>
      </tr><br>
      <tr>
      <td>Discriminat:</td>
      <td>&#916;&nbsp; = </td>
      <td colspan="5"><input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="y0" class="outtext" readonly></td>
      </tr>
      <tr>
      <td>Quadratic formula:</td>
      <td class="math"><i>x</i><sub><span style="font-size: 0.8em">1,2</span></sub>=</td>
      <td colspan="5"><input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="y3" class="outtext" readonly></td>
      </tr>
      <tr>
      <td>First root:</td>
      <td class="math"><i>x</i><sub><span style="font-size: 0.8em">1&nbsp;&nbsp; </span></sub>=</td>
      <td colspan="5"><input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="y1" class="outtext" readonly></td>
      </tr>
      <tr>
      <td>Second root:</td>
      <td class="math"><i>x</i><sub><span style="font-size: 0.8em">2</span></sub> =</td>
      <td colspan="5"><input type="text" :class="{ buttonclicked1 : fractclicked1 }" v-model="y2" class="outtext" readonly></td>
      </tr>
    </tbody>
  </table>
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
      title: 'quadratic equation solver tool',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Quadratic equation solver.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/quadratic-equation-solver'}
    ]
    }
    },
  data(){
    return {
      fractclicked1: false,
      x: '',
      x2: '',
      x3: '',
      y0: '',
      y1: '',
      y2: '',
      y3: ''
        }
  },
  methods: {
    reset(){
      this.firstvalue = '';
      this.change = '';
      this.pchange = '';
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
  fract(){
    this.fractclicked1 = true;
    setTimeout(() => this.fractclicked1 = false, 500);
    var a = this.x;
    var b = this.x2;
    var c = this.x3;
    var d = b*b-4*a*c;
    this.y0 = this.roundresult(d);
    if( d>=0 )
    {
      this.y1 = this.roundresult((-b+Math.sqrt(d))/(2*a));
      this.y2 = this.roundresult((-b-Math.sqrt(d))/(2*a));
    }
    else
    {
      var re = this.roundresult(-b/(2*a));
      var im = this.roundresult(Math.sqrt(-d)/(2*a));
      this.y1 = re+' + i'+im;
      this.y2 = re+' - i'+im;
    }
    b=-b;
    this.y3 = '('+b.toString()+' \xb1 \u221A('+d.toString()+')) / (2\xd7'+a.toString()+')';
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
.intext{background:#fff;padding-left:3px;border:1px inset #eee}
 #inputstyle td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #inputstyle td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #inputstyle .btn span { font-weight: bold; font-size:large; }
 #inputstyle .btn img { filter:invert(1); }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #inputstyle { padding:10px; }
    #inputstyle td input[type=number] { width:60px; }
    #inputstyle td input[type=text] { width:60px; }
 }
 #designform { background:#a7c9b8; padding:20px; }
 .btn span { font-weight: bold; font-size:large; }
 #designform button i { vertical-align: bottom; }
 /*.btn b, .btn b2 { font-size:large; }*/
 @media all and (max-width: 800px) {
    #designform, #calcform3 { padding:10px; }
 }
</style>
