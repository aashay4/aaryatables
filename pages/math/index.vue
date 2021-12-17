<template>
  <div class="">
    <div class="w3-content" style="max-width:1400px">

<div class="w3-row">

<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; Math <hr>
    <h1 class="w3-text-teal"><b>Math Tools</b></h1>
      </div>
      <ul class="w3-ul w3-hoverable w3-white">
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/logarithm-calculator"> Logarithm Calculator</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/fractions-calculator"> Fractions Calculator</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/addition-table"> Addition Table</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/math/division-calculator"> Division Calculator</a></span><br>
        </li>
      </ul>
  </div>
  <hr>

</div>


<!-- Introduction menu -->
<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-card w3-margin w3-margin-top">
    <div class="w3-container w3-white w3-padding">
      <h4><b>Math Tools</b></h4>
      <p>Use these math tools to perform addition, subtraction, division, fractions and percentage.</p>
    </div>
  </div><hr>

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
    // sets document title
    return {
      title: 'Math Tools',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'fractions calculator online' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math'}
    ]
    }
    },
  components: {
    Logo
  },
  data(){
    return{
    }
  },
  methods: {

  }
}
</script>

<style>
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
body,h1,h2,h3,h4,h5 {font-family: "Raleway", sans-serif}
.removelink{
    text-decoration: none;
}
</style>
