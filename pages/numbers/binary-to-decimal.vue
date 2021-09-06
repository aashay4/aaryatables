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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Binary to Decimal<hr>
      <h1 class="w3-text-teal"><b>Binary to Decimal Converter</b></h1><br>
      <p>Binary to decimal converter tool.</p>
      <form id="calcform1" name="calcform1" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" id="x" name="x" v-model="number1" class="form-control" placeholder="Enter the Binary here .... ">
</div>
</div>
<div id="logdiv2" class="form-row">
<div id="coefdiv2a" class="col-2">
<input type="text" id="c2" name="c2" placeholder="1" class="form-control">
</div>
<div id="coefdiv2b" class="col-auto mt-2">&times;</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <h1>Binary to Decimal Conversion</h1>
<div class="input-group mb-3">
<input type="text" id="y" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

</form>

    </div>
    <div class="w3-padding">
      <h1 class="w3-center">How to Convert Binary to Decimal?</h1>
      <p>The calculation of binary to decimal is equal to the sum of the total binary digits times their power of 2:</p>
      <p>For example, 00110100<sub>2</sub> = 0*2<sup>7</sup> + 0*2<sup>6</sup> + 1*2<sup>5</sup> + 1*2<sup>4</sup> + 0*2<sup>3</sup> + 1*2<sup>2</sup> + 0*2<sup>1</sup> + 0*2<sup>0</sup></p>
      <p> => 0 + 0 + 32 + 16 + 0 + 4 + 0 + 0</p>
      <p> => 52</p>
      <h2>Decimal Numbers</h2>
      <p>Decimal numbers are the most common type of numbering system. Decimal numbers are used in our daily life for trading and calculation. Decimal numbers are the easiest for humans to understand. For that reason, it is popular.</p>
    </div>
    <div class="w3-padding">
      <h2>Code to Convert Decimal to Binary:</h2>
        <pre>
  <code>
    function binarytodecimal() {
          var input = document.getElementById("input_value").value;
          var answer = new BigNumber(input, 2);
          document.getElementById("answer").innerHTML = answer;
          }
  </code>
</pre>
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-hexadecimal"> Binary to Hexadecimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary Translator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-binary"> Decimal to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-hexadecimal"> Decimal to Hexadecimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-binary"> Hexadecimal to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hexadecimal to Decimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/text-to-binary"> Text to Binary</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

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
import { BigNumber } from 'bignumber.js'
export default {
  head() {
    // sets document title
    return {
      title: 'Binary to Decimal Converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Convert binary to decimal easily with this tool.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/binary-to-decimal'}
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
    reset(){
      this.number1 = '';
      this.answer = '';
      this.base8 = '';
      this.base10 = '';
      this.base16 = '';
      this.fa = '';
    },
    calculate() {
      this.fa = parseInt(this.number1)
      var cc = new BigNumber(parseInt(this.number1, 2))
      if (isNaN(cc)) {
        this.answer = 'This number cannot be converted into Decimal'
      } else {
        this.answer = cc
      }
}
}
}
</script>

<style lang="css">
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
pre code {
  background-color: #eee;
  border: 1px solid #999;
  display: block;
  padding: 20px;
  font-size: 20px;
}
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
#bdiv, #bdiv2, #bdiv3 { max-width:100px; }
#b, #b2, #b3 { max-width:70px; }
#bsel,#b2sel,#b3sel { max-width:20px; padding:0; }
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
