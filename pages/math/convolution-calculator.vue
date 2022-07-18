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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Convolution calculator<hr>
      <h1 class="w3-text-teal"><b>An easy to use convolution calculator</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
    <form id="designpq" autocomplete="off">
<table class="calc">
<tr>
<td>First array of data sequence:</td>
</tr>
<tr>
<td><textarea v-model="ta1" autofocus>1 1 1 0 0 0</textarea></td>
</tr>
<tr>
<td>Second array of data sequence:</td>
</tr>
<tr>
<td><textarea v-model="ta2" tabindex="2">0.5 0.2 0.3</textarea></td>
</tr>
<tr>
<td>
<button type="button" title="Calculate" class="btn btn-secondary" @click="calculate()" tabindex="3"><img src="/lib/icons/glyphicons_all/glyphicons_halflings/glyphicons_halflings_018_cog.png" alt=""> Calculate</button>
<button type="reset" @click="reset()" title="Reset" class="btn btn-secondary" tabindex="4"> Reset</button>
</td>
</tr>
<tr>
<td>Result data sequence:</td>
</tr>
<tr>
<td><textarea v-model="ta3" name="TA3" class="outtext" readonly tabindex="5"></textarea></td>
</tr>
</table>
</form>


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
              <span class="w3-large"><a class="removelink" href="/math/addition-table"> Addition Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/logarithm-calculator"> Logarithm Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/division-calculator"> Division Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/fractions-calculator"> Fractions Calculator</a></span><br>
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
      title: 'Convolution calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Online convolution calculator for students and professionals.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/convolution-calculator'}
    ]
    }
    },
  data(){
    return {
      ta1: '1 1 1 0 0 0',
      ta2: '0.5 0.2 0.3',
      ta3: '',
      number1: null,
      number2: null,
      answer: ''
    }
  },
  methods: {
    calcfunc(n) {
  if( n == 0 )
    return 1.0;
  if( n < 0 )
    return "Enter non negative number";
  if( n != Math.floor(n) )
    return "Enter an integer number";
  for(var i=1,f=1; i<n; i+=1,f*=i);
  return f;
},
    calculate(){
      var x = new Array();
			var h = new Array();
			var y = new Array();
			var x1 = this.ta1;
			var x2 = this.ta2;
			x1 = x1.replace(/[ ]*,[ ]*|[ ]+/g,' ');
			x2 = x2.replace(/[ ]*,[ ]*|[ ]+/g,' ');
			x1 = x1.split(' ');
			x2 = x2.split(' ');
			var Nx = x1.length;
			var Nh = x2.length;
			var Ny = Nx+Nh-1;

			for(var i=0; i<Nh-1; i++)
				x[i] = 0;
			for(i=0; i<Nx; i++)
				x[i+Nh-1] = parseFloat(x1[i]);
			for(i=Nx+Nh-1; i<Nx+2*(Nh-1); i++)
				x[i] = 0;
			for(i=0; i<Nh; i++)
				h[i] = parseFloat(x2[i]);

			for(i=0; i<Ny; i++)
			{
				y[i] = 0;
				for(var j=0; j<Nh; j++)
					y[i] += x[i+j]*h[Nh-1-j];
			}

			//xx = '';
			var yy = '';
			for(i=0; i<Ny; i++) {
				yy+=String(y[i])+' ';
				//xx+=String(x[i])+' ';
			}
			this.ta3 = yy;

    },
    reset(){
      this.ta1 = "1 1 1 0 0 0";
      this.ta2 = "0.5 0.2 0.3";
      this.ta3 = "";
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
#designpq { background:#a7c9b8; padding:20px; }
#designpq button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designpq { padding:10px; }
}

</style>
