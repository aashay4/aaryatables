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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Hexadecimal to Decimal<hr>
      <h1 class="w3-text-teal"><b>Convert Hexadecimal to Decimal (Hex converter)</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <p>Hexadecimal to decimal conversion tool.</p>
      <form id="designbase" name="designbase" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" v-model="number1" class="form-control" placeholder="Enter the Hex here .... ">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <h1>Hex to Decimal Conversion</h1>
<div class="input-group mb-3">
<input type="text" id="y" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

</form><br>
    </div>
    <div class="w3-padding">
    <h1 class="w3-center">How to convert hex to decimal?</h1>
    <p>A decimal number is a base-10 number that includes 0 to 9. A hexadecimal number is a base-16 number that includes 0 to 9 along with A to F. Since hexadecimal is a base-16 number, to perform hexadecimal conversion multiply each number with the power of 16. Consider the following example for the hex to numbers:</p>
    <p>16<sub><span style="font-size: 0.8em">(16)</span></sub> = 1&times;16<sup>1</sup>+6&times;16<sup>0</sup></p>
    <p>=> 16+6</p>
    <p>=> 22</p>
    <p>Consider this example to understand hex to decimal conversion for a number with the alphabet letters A to F.</p>
    <p>6A<sub><span style="font-size: 0.8em">(16)</span></sub> = 6&times;16<sup>1</sup>+10&times;16<sup>0</sup></p>
    <p> => 96+10</p>
    <p> => 106</p>
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
        <h1 class=""><b>Other Numbers tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-hexadecimal"> Binary to Hex</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary converter</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-binary"> Decimal to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-hexadecimal"> Numbers to Hex</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-binary"> Hex to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-decimal"> Binary to Decimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/text-to-binary"> Text to Binary</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div></div>

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
import { BigNumber } from 'bignumber.js'
export default {
  head() {
  return {
    title: 'Hexadecimal to decimal conversion tool (Hex to numbers)',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: 'Free online hexadecimal to decimal (number) translator and learn how to perform the hexadecimal conversion.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/hexadecimal-to-decimal'}
  ]
  }
  },
  data(){
    return {
      number1: '',
      answer: '',
      base8: '',
      base10: '',
      base16: '',
      fa: ''
    }
  },
  methods: {
    calculate() {
      var x = new BigNumber(this.number1, 16)
    var dectobin = x.toString(10);
    this.answer = dectobin;
},
reset(){
  this.number1 = "";
  this.answer = "";
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
#designbase { background:#a7c9b8; padding:20px; }
.btn span { font-weight: bold; font-size:large; }
#designbase button i { vertical-align: bottom; }
#diventry { display:none; }
@media all and (max-width: 800px) {
   #designbase { padding:10px; }
}

</style>
