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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Convert Text to Binary<hr>
      <h1 class="w3-text-teal"><b>Ascii to Binary</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <p>English to binary conversion tool. Enter the text in the box and click on the button to get the Ascii to binary answer. For example, enter the letter English letter 'D' in the box and you will get the "01000100" binary number in the answer box.</p>
      <form id="designstyle" name="designstyle" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" v-model="number1" class="form-control" placeholder="Enter the Text here .... ">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <h1>Text to Binary Conversion</h1>
<div class="input-group mb-3">
<input type="text" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

</form>
    </div>
    <div class="w3-padding">
    <h1 class="w3-center">How to convert ASCII text to binary?</h1>
    <p>To convert ASCII to binary, convert each letter in the text string separately. Consider the following steps for conversion:</p>
    <ul>
      <li>
        Get the character
      </li>
      <li>Get the binary number of that character from the Ascii table</li>
      <li>Continue the same process for every number in a string.</li>
    </ul>
    <p>For example, consider this English string "ACJ" for the text to binary conversion.</p>
    <p><b>Steps:</b></p>
    <ul>
      <li>Get the first character from the String. In this case, it is an A</li>
      <li>Get the binary code for A. For A, it is 01000001.</li>
      <li>Perform the same operation for another two characters. So, the final answer after conversion would be " 01000001 01000011 01001010"</li>
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-hexadecimal"> Binary to Hexadecimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary to English</a></span><br>
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
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hexadecimal tool</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-decimal"> Binary to Decimal</a></span><br>
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
  return {
    title: 'Text ASCII to binary code converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: 'A text to binary tool and also a converts english to binary.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/text-to-binary'}
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
      this.answer = '';
            for (var i=0; i < this.number1.length; i++)
            {
              var e = this.number1[i].charCodeAt(0);
              var s = "";
              do {
                var a = e % 2;
                e = (e - a) / 2;
        s = a + s;
      }while(e!=0);
        while(s.length<8) {
          if(s.length === 7) {
            s = " 0" + s;
            this.answer += s;
          }
          if(s.length === 6) {
          s = " 00" + s;
          this.answer += s;
          }
          if(s.length === 5) {
          s = " 000" + s;
          this.answer += s;
          }
          if(s.length === 4) {
          s = " 0000" + s;
          this.answer += s;
          }
          if(s.length === 3) {
          s = " 00000" + s;
          this.answer += s;
          }
        }
              }
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
