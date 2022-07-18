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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; Base calculator<hr>
      <h1 class="w3-text-teal"><b>Number base calculator for binary, decimal, hexadecimal and octal numbers</b></h1>
      <p>Add, subtract, devide, and multiply binary, hex, decimal and octal numbers easily.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <form id="designstyle" autocomplete="off">
<div class="form-group">
<label for="base">Select base</label>
<select v-model="base" class="form-control" autofocus>
<option value="2">2 (binary)</option>
<option value="3">3</option>
<option value="4">4</option>
<option value="5">5</option>
<option value="6">6</option>
<option value="7">7</option>
<option value="8">8 (octal)</option>
<option value="9">9</option>
<option value="10">10 (decimal)</option>
<option value="11">11</option>
<option value="12">12</option>
<option value="13">13</option>
<option value="14">14</option>
<option value="15">15</option>
<option value="16">16 (hex)</option>
<option value="17">17</option>
<option value="18">18</option>
<option value="19">19</option>
<option value="20">20</option>
<option value="21">21</option>
<option value="22">22</option>
<option value="23">23</option>
<option value="24">24</option>
<option value="25">25</option>
<option value="26">26</option>
<option value="27">27</option>
<option value="28">28</option>
<option value="29">29</option>
<option value="30">30</option>
<option value="31">31</option>
<option value="32">32</option>
<option value="33">33</option>
<option value="34">34</option>
<option value="35">35</option>
<option value="36">36</option>
</select>
</div>
<div class="form-group">
<label for="x">First number</label>
<input type="text" v-model="x" class="form-control">
</div>
<div class="form-group">
<label for="op">Operation</label>
<select v-model="op" class="form-control">
<option value="0">+</option>
<option value="1">-</option>
<option value="2">&times;</option>
<option value="3">&div;</option>
</select>
</div>
<div class="form-group">
<label>Second number</label>
<input type="text" v-model="x2" class="form-control">
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-success" @click="calculate()"><span>=</span> Calculate</button>
<button type="reset" title="Reset" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<label for="y">Result number</label>
<textarea rows="2" v-model="y" class="form-control" readonly></textarea>
</div>
</form>

</div><br>
<div class="w3-padding w3-raw w3-align">
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
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary code translator</a></span><br>
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
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hexadecimal calculator</a></span><br>
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
//import { BigNumber } from 'bignumber.js'
export default {
  head() {
    // sets document title
    return {
      title: 'Base Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Base Calculator for students and professionals.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/base-calculator'}
  ],
  script: [
    {src: 'https://www.rapidtables.com/lib/bignumber/bignumber9.0.0.min.js'},
    {src: 'https://cdnjs.cloudflare.com/ajax/libs/mathjs/10.1.1/math.min.js', integrity: 'sha512-o7l/Uxf+iFLa5H6VpPjFdrY+bF+JtYI47FXfYJp6zlCRhs8K8sO1EVyEiS/1FeEvw1b6HeK6oXT3Plza8L/NIQ=='}
  ]
    }
    },
  data(){
    return {
      base: '10',
      x: '',
      op: '0',
      x2: '',
      y: ''
    }
  },
  methods: {
    calculate(){
      const base=this.base;
      const opelem=this.op;
      const x1elem=this.x;
      const x2elem=this.x2;
      const yelem=this.y;
		var b = parseFloat(base);
		var op = parseInt(opelem);
		var x1 = x1elem;
		var x2 = x2elem;
      var y;
		try {
			x1 = new BigNumber(x1, b);
			//x1elem.style.background="white";
		}
		catch(err) {
//			x1elem.style.background="#fff0f0";
			this.y="";
			return;
		}
		try {
			x2 = new BigNumber(x2, b);
	//		x2elem.style.background="white";
		}
		catch(err) {
		//	x2elem.style.background="#fff0f0";
			this.y="";
			return;
		}
      switch(op) {
         case 0:
               y = x1.plus(x2); //.toString(b).toUpperCase();
               break;
         case 1:
               y = x1.minus(x2); //.toString(b).toUpperCase();
               break;
         case 2:
               y = x1.times(x2); //.toString(b).toUpperCase();
               break;
         case 3:
               y = x1.div(x2); //.toString(b).toUpperCase();
               break;
      }
      BigNumber.set({ DECIMAL_PLACES: 16 });
      y = y.toString(b).toUpperCase();
		this.y=y;

},
reset(){
  this.number1 = "";
  this.answer = "";
  this.base8 = "";
  this.base10 = "";
  this.base16 = "";
  this.fa = "";
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
#designstyle { background:#a7c9b8; padding:20px; }
#designstyle button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designstyle { padding:10px; }
}

</style>
