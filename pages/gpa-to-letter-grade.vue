<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; GPA to letter grade<hr>
          <h1 class="w3-text-teal"><b>GPA to letter grade</b></h1>
          <p>Calculate GPA to letter easily.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">

  <form id="pendesign" autocomplete="off">
  <div class="form-group row">
  <label for="avg0" class="col-sm-4 col-form-label">GPA</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="gpa" class="form-control" autofocus>
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
  <label for="final0" class="col-sm-4 col-form-label">Letter grade</label>
  <div class="input-group col-sm-8">
  <input type="text" min="0" step="any" v-model="letter" class="form-control" readonly>
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
              <span class="w3-large"><a class="removelink" href="/final-grade-calculator"> Final grade calculator</a></span><br>
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
      title: 'GPA to letter grade calculator.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'An easy to use GPA to letter grade calculator online.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/gpa-to-letter-grade'}
    ]
    }
    },
  data(){
    return {
gpa: '',
letter: ''
      }
  },
  methods: {
    calculate(){
      var gpa = this.gpa;
			gpa = parseFloat(gpa);
			var llook=["A+","A","A-","B+","B","B-","C+","C","C-","D+","D","D-","F"];
			var tlook=[4.165,3.835,3.5,3.165,2.835,2.5,2.165,1.835,1.5,1.165,0.835,0.335];
			var i;
			for(i=0; i<12; i++)
				if( gpa>=tlook[i] ) break;
			this.letter = llook[i];
    },
reset(){
  this.gpa = "";
  this.letter = "";
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
 #pendesign { padding:15px; background:#a7c9b8; border:1px solid #e0e0e0; border-radius:7px; }
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
