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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Factorial calculator<hr>
      <h1 class="w3-text-teal"><b>Factorial Calculator</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <form id="designpq" autocomplete="off" class="rounded">
      <table>
      <tbody>
      <tr class="">
      <td><input type="number" step="any" v-model="number1" class="intext" autofocus><span>!</span> <input type="button" value="  " class="btn"></td>
      </tr>
      <tr>
      <td><input @click="calculate()" type="button" value="Calculate" class="btn btn-secondary"> <input type="reset" class="btn btn-secondary"></td>
      </tr>
      <tr>
      <td>Result:</td>
      </tr>
      <tr>
      <td><input type="text" v-model="answer" class="outtext" readonly></td>
    </tr><br>
      </tbody>
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
      title: 'Free factorial calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Factorial Calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/factorial-calculator'}
    ]
    }
    },
  data(){
    return {
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
    var  x = this.number1;
      		 var	n = parseFloat(x);
           var y = this.calcfunc(n);

      		 	var txt='';
            if( !isNaN(n) )
      		 	{
      			 	if( n<=200 )
      			 	{
      			 		txt=n+"! = ";
      			 		if( n>1 )
      			 		{
      				 		for(var i=1; i<=n; i++)
      				 		{
      				 			if( i<n )
      						 		txt+=i+'\u00D7';
      						 	else
      						 		txt+=i;
      						}
      					}
      			 		txt+="\n= "+y;
      			 	}
      			}
            this.answer = y;
    },
    reset(){
      this.number1 = null;
      this.number2 = null;
      this.answer = ''
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
