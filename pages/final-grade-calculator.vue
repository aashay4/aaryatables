<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Final grade calculator<hr>
          <h1 class="w3-text-teal"><b>Final grade calculator</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">

  <form id="lolakhuj" autocomplete="off">
  <div class="form-group row">
  <label for="avg0" class="col-sm-4 col-form-label">Recent grade</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="avg0" class="form-control" autofocus>
  <div class="input-group-append">
  <span class="input-group-text">%</span>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label for="total0" class="col-sm-4 col-form-label">Enter Target class grade</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="total0" class="form-control">
  <div class="input-group-append">
  <span class="input-group-text">%</span>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label for="weight0" class="col-sm-4 col-form-label">Weight for final exam:</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="weight0" class="form-control">
  <div class="input-group-append">
  <span class="input-group-text">%</span>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label class="col-sm-4 col-form-label">&nbsp;</label>
  <div class="input-group col-sm-8">
  <button type="button" @click="calculate()" title="Calculate" class="btn btn-success"><span>=</span> Calculate</button>
  <button type="button" @click="reset()" title="Reset" class="btn btn-secondary ml-1"><span>&times;</span> Reset</button>
  </div>
  </div>
  <div class="form-group row">
  <label for="final0" class="col-sm-4 col-form-label">Grade required in the final exam to get target class grade</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="final0" class="form-control" readonly>
  <div class="input-group-append" style="height:38px">
  <span class="input-group-text">%</span>
  </div>
  </div>
  </div>
  </form>
<br>

</div><br>
  </div>
</div></div>

<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-margin">
    <div class="w3-container w3-white">
      <div class="w3-margin w3-white">
          <div class="w3-container w3-padding">
        <h1 class=""><b>Other tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/gpa-calculator"> GPA calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/gpa-to-letter-grade"> GPA to letter grade</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/grade-calculator"> Grade calculator</a></span><br>
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
      title: 'Final grade calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'An easy to use final grade calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/final-grade-calculator'}
    ]
    }
    },
  data(){
    return {
avg0: '',
total0: '',
weight0: '',
final0: ''
      }
  },
  methods: {
    calculate(){
      var avg=this.avg0;
var total=this.total0;
var weight=this.weight0;
var final=(total-avg*(100.0-weight)/100.0)/(weight/100.0);
final = final.toFixed(2);
this.final0=final;
var p=final;
if( p>100 ) p=100;
//$("#finalcircle0").percircle({percent: p,text: final+"%"});
//$("#finalcircle0").show();

    },
reset(){
  this.avg0 = "";
  this.total0 = "";
  this.weight0 = "";
  this.final0 = "";
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
 #wrapper td { padding-left:3px; padding-right:3px; }
 #lolakhuj { padding:15px; background:#a7c9b8; border:1px solid #e0e0e0; border-radius:7px; }
 .btn span { font-weight:bold; font-size:large; }
@media all and (max-width: 600px) {
 .nav-tabs { display:none; }
}
.btn span { font-weight:bold; font-size:large; }

@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
 }
</style>
