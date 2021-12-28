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
      <form name="calcform" autocomplete="off" class="rounded">
      <table class="calc">
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
.calc td { font-family:Arial, Helvetica, sans-serif; }
.calc span { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
.calc select { font-size:x-large; font-family:"Times New Roman", Times, serif; }
.calc input { font-size:x-large; font-family:Arial, Helvetica, sans-serif; }
.calc input[type=text] { width:100%; }
.calc textarea { font-size:large; }
@media all and (max-width: 576px) {
	.calc { width:100%; padding:8px; }
	.calc input[type=number] { width:180px; }
	.calc textarea { width:100%; }
}
@media all and (min-width: 577px) {
	.calc { padding:20px; }
	.calc input[type=number], .calc input[type=text], .calc textarea { width:240px; }
	.calc input[type=button], .calc input[type=reset] { font-size:large; }
}

h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
#bdiv, #bdiv2, #bdiv3 { max-width:100px; }
#b, #b2, #b3 { max-width:70px; }
#bsel,#btnhh,#b3sel { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#log, #log2, #log3 { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#txt, #txt3 { font-family:math; }
#drop, #drop2, #drop3 { background:#fff; color:#212529; }
#calcform1 button i { vertical-align: bottom; }
#coefdiv1a, #coefdiv1b span { vertical-align: bottom; }
#graph { display:none; }
/*.btn b, .btn b2 { font-size:large; }*/
#opsel { font-weight:bold; margin-top:10px; }
#coefdiv1a, #coefdiv1b, #opdiv, #logdiv2 { display:none; }
@media all and (max-width: 800px) {
   #ln { padding-right:35px; }
   #calcform1, #calcform3 { padding:10px; }
}

</style>
