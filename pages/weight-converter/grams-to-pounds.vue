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
          <a href="/">Home</a> &rsaquo; <a href="/weight-converter">Weight</a> &rsaquo; Grams to Pounds<hr>
      <h1 class="w3-text-teal"><b>Grams to Pounds (g to lbs)</b></h1>
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
<div class="col-auto">Enter Grams:</div>
<div class="col">
<input type="number" v-model="number1" class="form-control">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</div>
<div class="form-group">
<div class="input-group mb-3">
<input type="text" v-model="answer" readonly class="form-control form-control-lg">
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
        <h1 class=""><b>Other Weight tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-milligrams"> Grams to Milligrams</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-ounces"> Grams to Ounces</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-kilograms"> Grams to Kilograms</a></span><br>
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
  return {
    title: 'Grams to Pounds',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: ''}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/weight-converter/grams-to-pounds'}
  ]
  }
  },
  data(){
    return {
      number1: null,
      number2: null,
      answer: ''
    }
  },
  methods: {
    calculate(){
        this.answer = parseFloat(this.number1)*0.00220462 + ' Pounds';
    },
    reset(){
      this.number1 = null;
      this.number2 = null;
      this.answer = ''
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
#designstyle { background:#a7c9b8; padding:20px; }
#designstyle button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designstyle { padding:10px; }
}

</style>
