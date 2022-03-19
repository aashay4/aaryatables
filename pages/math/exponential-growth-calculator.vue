<template lang="html">
<div>
  <div class="">

    <div class="w3-content" style="max-width:1400px">
<div class="w3-row">
<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
    <div class="w3-container w3-padding">
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Exponential growth calculator<hr>
      <h1 class="w3-text-teal"><b>Exponential growth calculator</b></h1>
        <p>An easy to use Exponential growth/decay calculator for free.</p>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
        <form name="formnumber1" autocomplete="off">
  <table>
  <tbody>
  <tr>
  <td>Number:<i> </i>(<i>x</i><sub style="font-size: 0.8em">0</sub>):</td>
  <td><input type="number" step="any" v-model="number1" class="intext" autofocus></td>
  <td>&nbsp;</td>
  </tr>
  <tr>
  <td>Growth/Decay Rate : </td>
  <td><input type="number" step="any" v-model="number2" class="intext"></td>
  <td>%</td>
  </tr>
  <tr>
  <td>Amount of time (<i>t</i>):</td>
  <td><input type="number" step="any" v-model="number3" class="intext"></td>
  <td>&nbsp;</td>
  </tr>
  <tr>
  <td>&nbsp;</td>
  <td><button @click="calculate()" type="button" title="Calculate" class="btn btn-secondary" > Ans =></button>
<button @click="reset()" type="button" title="Calculate" class="btn btn-secondary" > Reset</button>
  </td>
  <td>&nbsp;</td>
  </tr>
  <tr>
  <td>Value at time t (<i>x</i>(t)):</td>
  <td><input type="text" v-model="answer" class="outtext" readonly></td>
  <td>&nbsp;</td>
  </tr>
  </tbody>
  </table>
  </form>
</div><br>
    <div class="w3-padding">
      </div>
  </div>
  <hr>

</div>


<!-- Introduction menu -->
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
              <span class="w3-large"><a class="removelink" href="/math/complex-numbers-calculator"> Complex numbers calculator</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

  <!-- Labels / tags -->


<!-- END Introduction Menu -->
</div>

<!-- END GRID -->
</div><br>

<!-- END w3-content -->
</div>

<!-- Footer -->
<footer class="w3-container w3-dark-grey w3-padding-32 w3-margin-top">
  <p>© AaryaTables</p>
</footer>

  </div>
</div>
</template>

<script>
export default {
  head() {
    // sets document title
    return {
      title: 'Exponential growth & decay calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Exponential growth calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/exponential-growth-calculator'}
    ]
    }
    },
  data(){
    return {
      answer: '',
      number1: '',
      number2: '',
      number3: ''
    }
  },
  methods: {
    reset(){
      this.answer = '';
      this.number1 = '';
      this.number2 = '';
      this.number3 = '';
    },
    calculate(){
      var x0=this.number1;
			var r=this.number2;
			var t=this.number3;
			var x=(1+r/100);
			var y = x0*Math.pow(x,t);
			y = this.roundresult(y);
			this.answer = y;
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
    }
  }

}
</script>

<style lang="css">
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
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
#formnumber1 { background:#a7c9b8; padding:20px; }
#formnumber1 button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
