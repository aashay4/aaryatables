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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Ln Calculator<hr>
      <h1 class="w3-text-teal"><b>Ln calculator converter</b></h1>
      <p>Enter the number that you want to convert and click on the calculate button.</p>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>
        <form id="inputdesign" name="inputdesign">
  <div class="form-group">
  <div class="form-row">
  <div id="ln" class="col-1">ln</div>
  <div class="col">
  <input type="number" min="0" step="any" v-model="x" name="x" class="form-control form-control-lg" autocomplete="off">
  </div>
  </div>
  </div>
  <div class="form-group">
  <button type="button" @click="calculate()" class="btn btn-secondary"><span>= ></span> Calculate</button>
  <button type="reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
  </div>
  <div class="form-group">
  <label for="y">Result</label>
  <div class="input-group mb-3">
  <input type="text" v-model="y" class="form-control form-control-lg" readonly>
  <div class="input-group-append">
  <button type="button" title="Copy" onclick="OnCopy()" class="btn btn-lg btn-outline-secondary">Ans</button>
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
        <h1 class=""><b>Other Number tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/addition-table"> Addition Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/division-calculator"> Division Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/fractions-calculator"> Fractions Calculator</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

  <!-- Labels / tags -->


<!-- END Introduction Menu -->
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
export default {
  head() {
    // sets document title
    return {
      title: 'Ln converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Ln calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/ln-calculator'}
    ]
    }
    },
  data(){
    return {
      x: '',
      y: ''
    }
  },
  methods: {
    reset(){
      this.answer = '';
      this.baseinput = '';
      this.input = '';
    },
    calculate(){
      var x=this.x;
      if( x=="" ) return;
      if( x=="e" ) x=Math.E;
      var y=Math.log(x);
      var px=parseFloat(x);
      var py=parseFloat(y);
      this.y = y;
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
#formnumber1,#inputdesign2,#inputdesign3,#inputdesign { background:#a7c9b8; padding:20px; }
#bdiv, #bdiv2, #bdiv3 { max-width:100px; }
#ln { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#inputdesign button i { vertical-align: bottom; }
#b, #b2, #b3 { max-width:70px; }
#bsel,#b2sel,#b3sel { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#log, #log2, #log3 { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#asdf, #asdf3 { font-family:math; }
#drop, #drop2, #drop3 { background:#fff; color:#212529; }
#formnumber1 button i { vertical-align: bottom; }
#characterfidi, #charryberry span { vertical-align: bottom; }
#lkjh { display:none; }
/*.btn b, .btn b2 { font-size:large; }*/
#opsel { font-weight:bold; margin-top:10px; }
#characterfidi, #charryberry, #opdiv, #logdiv2 { display:none; }
@media all and (max-width: 800px) {
   #ln { padding-right:35px; }
   #formnumber1, #inputdesign3 { padding:10px; }
}

</style>
