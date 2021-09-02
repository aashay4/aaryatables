<template>
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

<div class="w3-row">

<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; Energy<hr>
    <h1 class="w3-text-teal"><b>Energy Conversion Tools</b></h1>
      </div>
      <ul class="w3-ul w3-hoverable w3-white">
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/kj-to-joules"> kj to joules</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/kj-to-btu"> kj to BTU</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/kj-to-calories"> kJ to calories</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/kj-to-kcal"> kJ to kcal</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/joules-to-kj"> joules to Kilojoules</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/joules-to-calories"> joules to Calories</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/energy/joules-to-kcal"> joules to kilocalories</a></span><br>
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
      <h4><b>Energy Online Tools</b></h4>
      <p>Use these energy tools to convert various units easily.</p>
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
      title: 'Energy Tools',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Electronics tools and converters.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/energy'}
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
body,h1,h2,h3,h4,h5 {font-family: "Raleway", sans-serif}
.removelink{
    text-decoration: none;
}
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
</style>
