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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Binary to Hexadecimal<hr>
      <h1 class="w3-text-teal"><b>Binary to Hexadecimal</b></h1>
      <p>Binary to hexadecimal convert and learn how to convert.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <form id="designstyle" name="designstyle" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" v-model="number1" class="form-control" placeholder="Enter the Binary here .... ">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <h1>Binary to Hex Conversion</h1>
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
<h1 class="w3-center">How to convert binary to hexadecimal?</h1>
<p>To convert binary to hexadecimal, consider the first four numbers of a binary. Once determined first four digits, convert the four digits into equivalent hex numbers with the help of binary to hexadecimal table.</p>
<p>Consider 00011111 binary number as an example.</p>
<ul>
  <li>
    The first four numbers are 0001
  </li>
  <li>Convert 0001 into hex number. 0001 into hex is 1.</li>
  <li>Determine another four numbers - 1111, and convert them into the hex</li>
  <li>So, the final answer for 00011111 is 1F.</li>
</ul>
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-decimal"> Binary to Decimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary Converter</a></span><br>
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
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hexadecimal Converter</a></span><br>
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
      title: 'Binary to Hexadecimal',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Binary to hexadecimal converter and know how to convert binary to hex.' }
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
    calculate() {
      var bin = this.number1;
            var m = new  BigNumber(bin, 2)
            var binn = m.toString(16).toUpperCase();
            this.answer = binn;
},
reset(){
  this.number1 = "";
  this.answer = "";
  this.base8 = "";
  this.base10 = "";
  this.base16 = "";
  this.fa = "";
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
#designstyle { background:#a7c9b8; padding:20px; }
#designstyle button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designstyle { padding:10px; }
}

</style>
