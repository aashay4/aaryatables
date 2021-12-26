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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Binary to text<hr>
      <h1 class="w3-text-teal"><b>Binary to text</b></h1>
      <p>Binary to text conversion tool to translate binary code to text with one click. Enter the binary number you wish to convert to text and you will get the conversion answer in the text box below.</p>
      <form id="calcform1" name="calcform1" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col">
<input type="text" id="x" name="x" v-model="number1" class="form-control" placeholder="Enter the binary number .... ">
</div>
</div>
<div id="logdiv2" class="form-row">
<div id="coefdiv2a" class="col-2">
<input type="text" placeholder="1" class="form-control">
</div>
<div id="coefdiv2b" class="col-auto mt-2">&times;</div>
</div>
<div class="form-group mt-4">
<button @click="calculate(); bintodecimal(); bintohexadecimal(); bintooctal();" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button onclick="onReset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
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

</form>
</div><br>
<div class="w3-padding w3-raw w3-align">
<h2 class="w3-center"><b>Binary to text</b></h2>
<p>This is an easy-to-use <b>binary to text</b> tool to convert binary code to text in just an easy step. All you need to do is enter a binary number in the form of zeros and ones and you will get an answer in the form ASCII text value.</p>
<h2>Importance of binary to text translation</h2>
<p>A binary to text converter becomes important because all the electronic systems understand just the binary numbers while it becomes next to impossible for humans to send an instruction in the binary number. As binary numbers include just zeros and ones, the instruction becomes big and complicated. For that reason, it becomes really important for the software engineers to convert binary to text and then send the instruction to the machine. If you are also working on such a product then you can consider using our tool for such conversion.</p>
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary translator</a></span><br>
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
      title: 'Binary to text translator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'A really simple binary to text converter' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/binary-to-text'}
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
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
#bdiv, #bdiv2, #bdiv3 { max-width:100px; }
#b, #b2, #b3 { max-width:70px; }
#bsel,#b2sel,#b3sel { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#log, #log2, #log3 { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#txtarea, #txt3 { font-family:math; }
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
