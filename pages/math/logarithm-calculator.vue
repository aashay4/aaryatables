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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Logarithm Calculator<hr>
      <h1 class="w3-text-teal"><b>Logarithm Calculator</b></h1>
        <p>Enter a base of a number and use this Logarithm Calculator.</p>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
      <form id="formnumber1" name="formnumber1" autocomplete="off">
<div class="form-row">
<div id="standoop444" class="col-2">
<input type="text" placeholder="1" class="form-control">
</div>
<div id="standoop44433" class="col-auto mt-2">&times;</div>
<div id="standoop1" class="col-auto">log</div>
<div id="abcdiv" class="col-3 mt-4 input-group">
<input type="text" v-model="baseinput" class="form-control" autofocus>
</div>
<div class="col">
<input type="text" v-model="input" class="form-control">
</div>
</div>
<div id="boat563" class="form-group">
<select id="standoop12" class="form-control">
<option>+</option>
<option>-</option>
<option>&times;</option>
<option>&divide;</option>
</select>
</div>
<div id="boat5634" class="form-row">
<div id="coefdiv2a" class="col-2">
<input type="text" placeholder="1" class="form-control">
</div>
<div id="coefdiv2b" class="col-auto mt-2">&times;</div>
<div id="intothelog" class="col-auto">log</div>
<div id="tabless1245" class="col-3 mt-4 input-group">
<input type="text" id="b2" name="b2" class="form-control">
<select id="standoop" class="form-control">
<option>&nbsp;</option>
<option>2</option>
<option>e</option>
<option>10</option>
</select>
</div>
<div class="col">
<input type="text" id="x2" name="x2" class="form-control">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<div class="input-group mb-3">
<input type="text" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>
</form>

</div><br>
    <div class="w3-padding">
      <h1>How log works?</h1>
      <p>
        Logarithm calculator is one of the most important calculations in the maths. It works on the following formula:
      </p>
      <p>Assume you need to solve this mathemetical equation:</p>
        <p><i>a<sup> b</sup> = c</i></p></p>
<p>This calculation can be simplified by the base b logarithm of a number x:</p>
<p>log<i><sub>a </sub>c</i> = <i>b</i></p>
<p>Base of a log play the biggest role in the logarithm calculation. You can take any number as a base. By default it is a base e and it's value is equal to 2.718281828459045.</p>
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
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
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
      title: 'Logarithm Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'log calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/logarithm-calculator'}
    ]
    }
    },
  data(){
    return {
      answer: '',
      baseinput: '',
      input: ''
    }
  },
  methods: {
    reset(){
      this.answer = '';
      this.baseinput = '';
      this.input = '';
    },
    calculate(){
      if(this.baseinput === 'e'){
        this.baseinput = Math.E;

      }
      var b = this.baseinput;
      var rr = this.input;
//      var x = str2num(rr);
      var y = Math.log(rr)/Math.log(b);
      y = y.toFixed(10);
      this.answer = y;
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
#abcdiv, #tabless1245 { max-width:100px; }
#standoop { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#standoop1, #intothelog { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#formnumber1 button i { vertical-align: bottom; }
#standoop444, #standoop44433 span { vertical-align: bottom; }
/*.btn b, .btn b2 { font-size:large; }*/
#standoop12 { font-weight:bold; margin-top:10px; }
#standoop444, #standoop44433, #boat563, #boat5634 { display:none; }
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
