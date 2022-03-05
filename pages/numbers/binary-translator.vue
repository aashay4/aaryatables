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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Binary Translator<hr>
      <h1 class="w3-text-teal"><b>Binary Translator (Binary to text)</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <p>Binary translator to convert binary to text and other numbering systems. Enter a binary number and click on the answer button for binary translation. For example, enter a binary number <b>01000001</b> in the box and click on the answer button. You will get an A as the binary to text conversion.</p>
      <form id="theraldesign" name="theraldesign" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" v-model="number1" class="form-control" placeholder="Enter the number here .... ">
</div>
</div>
<div id="ultimatedes" class="form-row">
<div id="coefdiv2a" class="col-2">
<input type="text" placeholder="1" class="form-control">
</div>
<div id="coefdiv2b" class="col-auto mt-2">&times;</div>
</div>
<div class="form-group mt-4">
<button @click="calculate(); bintodecimal(); bintohexadecimal(); bintooctal();" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <h1>Binary to text</h1>
<div class="input-group mb-3">
<input type="text" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

<div class="form-group">
  <h2>({{ number1 }}) to dec-base-10</h2>
<div class="input-group mb-3">
<input type="text" v-model="base10" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

<div class="form-group">
  <h2>({{ number1 }}) to hex-base-16</h2>
<div class="input-group mb-3">
<input type="text" v-model="base16" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>


<div class="form-group">
  <h2>({{ number1 }}) to oct-base-8</h2>
<div class="input-group mb-3">
<input type="text" v-model="base8" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>
</form>
</div><br>
<div class="w3-padding w3-raw w3-align">
<h2 class="w3-center"><b>Binary Translator</b></h2>
<p><b>Binary translator</b> is a tool that helps users to convert binary to all other major numbering systems. Along with all other numbering systems, users can convert binary to English (text) as well.</p>
<h2>About Binary Numbering System</h2>
<p>Binary numbering system contains just zeros and ones. Many electronics systems use binary in the processors to perform computer organization operations. For that reason, it is a base-2 number. It has become an integral part of modern electronics. Earlier, many developers used to complain about the size of a binary number. To store data in just zeros and ones was difficult. Binary occupies more space on a machine. But today, with the help of supercomputers and decent storage facilities, it has become easy to store binary.</p>
<p>Earlier, many developers used to complain about the size of a binary number. To store data in just zeros and ones was difficult and it used to occupy more space on a machine. But today with the help of supercomputers and decent storage facilities, it has become very easy to store binary.</p>
<h1><b>Binary to Text</b></h1>
<p>The binary to text conversion is one of the most common conversions for computer programmers. It is necessary for the machines that take input from the humans and instruct the machine's processor in the language it understands - Binary. To develop such apps, developers often need to use a binary translator to convert binary to text. With the help of a binary translator, a developer converts the user input to binary then the server sends binary to the microprocessor. The microprocessor processes the binary and converts response binary to text, sends it back to the users.</p>
<p>It is the most basic working of a binary translator. Many NoSQL databases implement the concepts of binary numbers to store images and then process and representing data faster.</p>
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-decimal"> Binary to Decimal</a></span><br>
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-text"> Binary to Text</a></span><br>
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
      title: 'Binary Translator (Binary to text converter)',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Easy to use binary translator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/binary-translator'}
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
      this.number1 = "";
      this.answer = "";
      this.base8 = "";
      this.base10 = "";
      this.base16 = "";
      this.fa = "";
    },
    calculate(){
      var bintext, textresult = '', binlength
var aaa = this.number1;
bintext = aaa.replace(/[^01]/g, '')
binlength = bintext.length - (bintext.length % 8)
for (var z = 0; z < binlength; z = z + 8) {
  textresult += String.fromCharCode(parseInt(bintext.substr(z, 8), 2))
  this.answer = textresult
}
},
    bintodecimal(){
      this.fa = parseInt(this.number1)
      var cc = new BigNumber(parseInt(this.number1, 2))
      if (isNaN(cc)) {
        this.base10 = 'This number cannot be converted into Decimal'
      } else {
        this.base10 = cc
      }
    },
     bintohexadecimal(){
       var bin = this.number1;
             var m = new  BigNumber(bin, 2)
             var binn = m.toString(16).toUpperCase();
             this.base16 = binn;
    },
     bintooctal(){
       this.xxx = parseInt(this.number1)
         var bintooct = parseInt(this.xxx, 2).toString(8)
         if (isNaN(bintooct)) {
           this.base8 = 'This number cannot be converted into Octal'
         } else {
           this.base8 = bintooct
         }
    },
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
#theraldesign { background:#a7c9b8; padding:20px; }
table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#txtarea, #txt3 { font-family:math; }
#drop, #drop2, #drop3 { background:#fff; color:#212529; }
#theraldesign button i { vertical-align: bottom; }
/*.btn b, .btn b2 { font-size:large; }*/
#ultimatedes { display:none; }
@media all and (max-width: 800px) {
   #theraldesign { padding:10px; }
}

</style>
