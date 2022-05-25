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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Binary Converter<hr>
      <h1 class="w3-text-teal"><b>Binary Translator</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <p>With the help of this binary translator, you can convert binary to text and text to binary in just less than a second. This binary translation tool works offline as well. Once the website is loaded, you do not need an internet connection to converter a number.</p>
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
</form><br><hr>
<h1 style="color: teal;">Text to Binary</h1>
<form id="theraldesign" name="theraldesign" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" v-model="number11" class="form-control" placeholder="Enter the Text here .... ">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate1()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset1()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<h1>Text to Binary Conversion</h1>
<div class="input-group mb-3">
<input type="text" v-model="answer1" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

</form>
</div><br>
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
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hex to Decimal</a></span><br>
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
      title: 'Binary converrter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Binary converter.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/binary-converter'}
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
      fa: '',

      number11: '',
      answer1: ''
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
    reset1(){
      this.number11 = "";
      this.answer1 = "";
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
    calculate1() {
      this.answer1 = '';
            for (var i=0; i < this.number11.length; i++)
            {
              var e = this.number11[i].charCodeAt(0);
              var s = "";
              do {
                var a = e % 2;
                e = (e - a) / 2;
        s = a + s;
      }while(e!=0);
        while(s.length<8) {
          if(s.length === 7) {
            s = " 0" + s;
            this.answer1 += s;
          }
          if(s.length === 6) {
          s = " 00" + s;
          this.answer1 += s;
          }
          if(s.length === 5) {
          s = " 000" + s;
          this.answer1 += s;
          }
          if(s.length === 4) {
          s = " 0000" + s;
          this.answer1 += s;
          }
          if(s.length === 3) {
          s = " 00000" + s;
          this.answer1 += s;
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
#theraldesign { background:#a7c9b8; padding:20px; }
#theraldesign button i { vertical-align: bottom; }
/*.btn b, .btn b2 { font-size:large; }*/
#ultimatedes { display:none; }
@media all and (max-width: 800px) {
   #theraldesign { padding:10px; }
}

</style>
