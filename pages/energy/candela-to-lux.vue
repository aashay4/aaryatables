<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/energy">Energy</a> &rsaquo; Candela to lux <hr>
    <h1 class="w3-text-teal"><b>Candela to lux</b></h1><br>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>
    <form id="designmodel" autocomplete="off">
<div class="form-group">
<label for="x1">Enter Candela</label>
<div class="input-group">
<input type="number" v-model="number1" min="0" step="any" class="form-control" required>
</div>
</div>
<div class="form-group">
<label for="x2">Enter degrees:</label>
<div class="input-group">
<input type="number" min="0" step="any" v-model="number2" name="x2" class="form-control" required>
</div>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="currentchange()"><span>=></span> Answer</button>
<button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<label >Lux:</label>
<div class="input-group">
<input type="text" v-model="kw" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">Feet</span>
</div>
</div>
<div class="form-group">
<label >Lux:</label>
<div class="input-group">
<input type="text" v-model="kc" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">Meter</span>
</div>
</div>
</div>
</div>
</form>

      </div>
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
        <h1 class=""><b>Other Electronics tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/candela-to-lumens"> Candela to lumens</a></span><br>
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
</template>

<script>
export default {
  head() {
    // sets document title
    return {
      title: 'Candela to lux',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: '' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/energy/candela-to-lux'}
    ]
    }
    },
  data(){
    return {
      currenttype: 'AC - Single phase',
      powerfactor: true,
      threephase: false,
      kc: '',
      amperselect: 'W',
      voltagechange: 'V',
      kw: '',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      voltagetype: 'Line to line voltage'
    }
  },
  methods: {
    currentchange(){
      var i = 0;
      var cd = parseFloat(this.number1);
      var d  = parseFloat(this.number2);
      var lx = cd/(d*d);
      this.kc = lx;
      if( i==0 ) lx*=10.76391;
this.kw = lx;
  },
    reset(){
      this.currenttype = "AC - Single phase";
      this.powerfactor = true;
      this.threephase = false;
      this.amperselect = "A";
      this.voltagechange = "V";
      this.kw = "";
      this.w = "";
      this.mw = "";
      this.number1 = "";
      this.number2 = "";
      this.powerfactorinput = "";
      this.voltagetype = "Line to line voltage";
      this.kc = "";
    },

  },
  beforeMount(){
   this.currentchange();
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
#designmodel { background:#a7c9b8; padding:20px; }
#designmodel button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designmodel { padding:10px; }
}

</style>
