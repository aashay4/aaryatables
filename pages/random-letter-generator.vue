<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Random letters generator<hr>
          <h1 class="w3-text-teal"><b>Random letters generator</b></h1>
          <p>Generate any alphabetic random letters.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense>
<div class="">
  <div id="designform" name="designform">
<div class="form-group row">
<label for="min" class="col-sm-3 col-form-label">Enter number of letters:</label>
<div class="col-sm-9">
<input type="number" v-model="min" name="min" min="step" class="form-control">
</div>
</div>
<div class="form-group row">
<label class="col-sm-3 col-form-label">&nbsp;</label>
<div class="col-sm-9">

<button @click="fract()" class="btn btn-primary">=> Generate</button>
<button title="Reset" class="btn btn-secondary" @click="reset()"><span>&times;</span> Reset</button>
</div>
</div>
<div class="form-group">
<label for="area">Generate random Alphabet</label>
<textarea :class="{ buttonclicked1 : fractclicked1 }" v-model="area" rows="3" readonly class="form-control form-control-lg"></textarea>
</div>
</div><br>
</div><br>
  </div>
</div></div>

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
              <span class="w3-large"><a class="removelink" href="/math/logarithm-calculator"> Logarithm Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/decimal-to-fraction"> Decimal to fraction</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/division-calculator"> Division Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

  <!-- Labels / tags -->

<!-- END Introduction Menu -->
</div>

</div>
<footer class="w3-container w3-dark-grey w3-padding-32 w3-margin-top">
  <p>© AaryaTables</p>
</footer>

</div>
</template>

<script>
export default {
  head() {
    // sets document title
    return {
      title: 'Random letter generator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Generate random letters from A to Z.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/random-letter-generator'}
    ]
    }
    },
  data(){
    return {
      fractclicked: false,
      fractclicked1: false,
      area: '',
      min: 1,
      max: 10,
      max1: 10,
      min1: 1,
      area1: [],
      length: 3,
      showleft: false,
      showright: false,
      x1: '',
      thrrepiece: '',
      minusvalue: false,
      d1: '',
      n2: '',
      d2: '',
      n3: '',
      d3: '',
      d4: '',
      n4: '',
      sign: '',
      x2: '',
      x3: '',
      n31: '',
      selected: '',
      n: '',
      y: '',
      d: ''
    }
  },
  methods: {
reset1(){
  this.min1 = '';
  this.max1 = '';
  this.area1 = [];
  this.length = '';
  this.fractclicked = false;
},
    reset(){
      this.min = '';
      this.max = '';
      this.area = '';
      this.fractclicked1 = false;
    },
  fract(){
    this.fractclicked1 = true;
    setTimeout(() => this.fractclicked1 = false, 250);
    var length = this.min;
    var max = this.max;
    length = parseFloat(length);
    max = parseFloat(max);
    var num = this.getrandom(length)
  },
  getrandom(length){
    //var num = Math.floor(Math.random() * (max - min + 1)) + min;
    //this.area = num;
    var result           = '';
var characters       = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
var charactersLength = characters.length;
for ( var i = 0; i < length; i++ ) {
  result += characters.charAt(Math.floor(Math.random() * charactersLength)) + ' ';
  this.area = result;
}

  },
  fract1(){
    this.area1 = [];
    this.fractclicked = true;
    setTimeout(() => this.fractclicked = false, 500);
    var min = this.min1;
    var max = this.max1;
    var length = this.length;
    min = parseFloat(min);
    max = parseFloat(max);
    if( max<min ) {
          this.min=max;
          this.max=min;
          min = max;
          max = parseFloat(this.max.value);
    }
    var num = this.getrandom1(min,max,length)
  },
  getrandom1(min,max,length){
    var num = [];
    if(this.length === "1"){
      this.area = '';
      var num = Math.floor(Math.random() * (max - min + 1)) + min;
      this.area1.push(num);
    }
    else if(this.lengh === "2"){
      alert("length 2")
      this.area1 = [];

    }
    else
    {
    for(var i=0; i<this.length; i++) {
   var xx = Math.floor(Math.random() * (max - min + 1)) + min;
   //num[i] = Math.floor(Math.random()*n)*step + min;
   //num[i] = roundresult(num[i]);
   this.area1.push(xx);
}
}
}
}
}
</script>

<style lang="css" scoped>
.buttonclicked{
  background-color: Violet;
}
.buttonclicked1{
  background-color: Violet;
}
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
.adslot_1 { display:none; }
 h1 { font-size:1.6rem; }
 h2 { font-size:1.4rem; }
 h3 { font-size:1.4rem; }
 h4 { font-size:1.2rem; }
 #designform { padding:20px; max-width:500px; background:#a7c9b8; }
 #designform td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #designform td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #designform .btn span { font-weight: bold; font-size:large; }
 #designform .btn img { filter:invert(1); }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
 }
</style>
