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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Decimal to Binary<hr>
      <h1 class="w3-text-teal"><b>Decimal to Binary</b></h1>
      <p>Decimal to binary converter.</p>
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
<input type="text" v-model="number1" class="form-control" placeholder="Enter the Decimal Number here .... ">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate(); dectohexa(); dectooctal();" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button onclick="onReset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
  <h1>Decimal to Binary Conversion Answer</h1>
<div class="input-group mb-3">
<input type="text" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

<div class="form-group">
  <h1>({{number1}}) to base-16</h1>
<div class="input-group mb-3">
<input type="text" id="y" v-model="base16" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

<div class="form-group">
  <h1>({{number1}}) to base-8</h1>
<div class="input-group mb-3">
<input type="text" id="y" v-model="base8" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button" class="btn btn-lg btn-outline-secondary">ANS</button>
</div>
</div>
</div>

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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-decimal"> Binary to Decimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-hexadecimal"> Decimal to Hexadecimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-binary"> Hexadecimal to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hexadecimal to Decimal Online</a></span><br>
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
      title: 'Decimal to Binary',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'A decimal to binary converter and read how to convert' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/decimal-to-binary'}
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
      var x = new BigNumber(this.number1, 10)
          var dectobin = x.toString(2);
          this.answer = dectobin;
},
dectohexa()
{
  var xzc = new BigNumber(this.number1, 10)
  var dectohexo = xzc.toString(16).toUpperCase ();
  this.base16 = dectohexo;
},
dectooctal() {
var xmm = new BigNumber(this.number1, 10)
var dectoocto = xmm.toString(8);
this.base8 = dectoocto;
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
#designstyle { background:#a7c9b8; padding:20px; }
#designstyle button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designstyle { padding:10px; }
}

</style>
