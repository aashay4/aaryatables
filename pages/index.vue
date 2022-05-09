<template>
  <div class="w3-light-grey">
    <div class="w3-content" style="max-width:1400px">

<!-- Header -->
<header class="w3-container w3-center w3-padding-32">
  <h1><b class="w3-text-teal">Aarya Tables</b></h1>
  <p><b>Free Online Tools and Converters</b></p>
</header>

<!-- Grid -->
<div class="w3-row">

<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-card-4 w3-margin w3-white">
      <div class="w3-container w3-padding">
        <h4 class="w3-text-teal"><b>Tools & Converters</b></h4>
      </div>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <ul class="w3-ul w3-hoverable w3-white">
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math"> Math Tools</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/electronics"> Electronics Tools</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/numbers"> Number Converter</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy"> Energy</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter"> Temperature</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter"> Weight</a></span><br>
        </li>

      </ul>
  </div>
  <hr>
<div class="w3-card-4 w3-margin w3-white">
  <div class="w3-container w3-padding">
    <h4 class="w3-text-teal"><b>Other Converters</b></h4>
  </div>
      <ul class="w3-ul w3-hoverable w3-white">
        <li>
          <span class="w3-large"><a class="removelink" href="/unit-conversion"> Unit Conversion</a></span><br>
        </li>
        <li>
          <span class="w3-large"><a class="removelink" href="/random-letter-generator"> Random letter generator</a></span><br>
        </li>
        <li>
          <span class="w3-large"><a class="removelink" href="/word-counter"> Word counter</a></span><br>
        </li>
        <li>
          <span class="w3-large"><a class="removelink" href="/case-converter"> Case Converter</a></span><br>
        </li>
      </ul>
</div>
  <!-- Blog entry -->

</div>


<!-- Introduction menu -->
<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-card w3-margin w3-margin-top">
    <div class="w3-container w3-white w3-padding">
      <h4><b>About AaryaTables</b></h4>
      <p>AaryaTables is a website with 1000+ online tools. These tools are about electronics, energy, maths, numbers, temperature, weight, and many other.</p>
    </div>
  </div><hr>

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
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  head() {
  return {
    title: 'Online tools and Calculators',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: ''}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/'}
  ]
  }
  },
  components: {
    Logo
  },
  data(){
    return{
      converteropen: 'close'
    }
  },
  methods: {
    converteropen1(){
      if(this.converteropen === 'close'){
        this.converteropen = "open";
      }
      else{
        this.converteropen = "close"
      }
    }
  }
}
</script>

<style>
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
body,h1,h2,h3,h4,h5 {font-family: "Raleway", sans-serif}
.removelink{
    text-decoration: none;
}
</style>
