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
          <a href="/">Home</a> &rsaquo; <a href="/energy">Energy</a> &rsaquo; joules to kcal<hr>
      <h1 class="w3-text-teal"><b>joules to kcal Converter</b></h1>
      <form id="calcform1" name="calcform1" autocomplete="off" class="rounded">
<div class="form-row">
<div id="log" class="col-auto">Enter Joules:</div>
<div class="col">
<input type="number" id="x" name="x" v-model="number1" class="form-control">
</div>
</div>
<div id="logdiv2" class="form-row">
<div id="coefdiv2a" class="col-2">
<input type="text" id="c2" name="c2" placeholder="1" class="form-control">
</div>
<div id="coefdiv2b" class="col-auto mt-2">&times;</div>
<div id="bdiv2" class="col-3 mt-4 input-group">
<input type="text" id="b2" name="b2" class="form-control">
<select id="b2sel" class="form-control">
<option>&nbsp;</option>
<option>2</option>
<option>e</option>
<option>10</option>
</select>
</div>
<div class="col">
<input type="text" id="x2" name="x2" class="form-control">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<div class="input-group mb-3">
<input type="text" id="y" v-model="answer" readonly class="form-control form-control-lg">
<div class="input-group-append">
<button type="button"  class="btn btn-lg btn-outline-secondary">kcal</button>
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
        <h1 class=""><b>Other Energy tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/joules-to-calories"> joules to calories</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/joules-to-kj"> joules to kj</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/kj-to-btu"> kj to btu</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/kj-to-calories"> kj to calories</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/kj-to-joules"> kj to joules</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/energy/kj-to-kcal"> kj to kcal</a></span><br>
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
export default {
  head() {
    // sets document title
    return {
      title: 'Joules to kCal',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Joules to kCal converter.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/energy/joules-to-kcal'}
    ]
    }
    },
  data(){
    return {
      number1: null,
      answer: ''
    }
  },
  methods: {
    calculate(){
      var d = this.number1;
      d = parseFloat(d);
        this.answer = (d/4184).toFixed(13);
    },
    reset(){
      this.number1 = null;
      this.answer = ''
    }
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
#txt, #txt3 { font-family:math; }
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
