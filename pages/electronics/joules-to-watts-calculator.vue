<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Joules to watts <hr>
    <h1 class="w3-text-teal"><b>Joules to watts Calculator</b></h1>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>
    <form id="desingform" autocomplete="off">
  <table>
  <tbody>
  <tr>
  <td>Enter joules:</td>
  <td><input type="number" min="0" step="any" class="intext" v-model="joules" autofocus></td>
  <td>  J</td>
  </tr>
  <tr>
  <td>Enter seconds:</td>
  <td><input type="number" min="0" step="any" class="intext" v-model="seconds"></td>
  <td>  S</td>
  </tr>
  <tr>
  <td>&nbsp;</td>
  <td>
  <button type="button" title="Calculate" class="btn btn-secondary" @click="convert()"><span>=></span> Answer</button></td>
  <td>&nbsp;</td>
  </tr>
  <tr>
  <td>watts:</td>
  <td><input type="text" v-model="answer" readonly></td>
  <td> W</td>
  </tr>
  </tbody>
  </table>
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
        <h1 class=""><b>Other Electronics tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kw"> Amps to KW</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-va"> Amps to VA</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-volts"> Amps to volts(V)</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-watts"> Amps to watts</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kva"> Amps to Kva</a></span><br>
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
      title: 'Joules to watts',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Joules to watts converter.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/joules-to-watts-calculator'}
    ]
    }
    },
  data(){
    return {
      joules: '',
      seconds: '',
      answer: ''
    }
  },
  methods: {
convert(){
this.answer = this.joules/this.seconds;
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
@media all and (max-width: 800px) {
   #desingform { padding:10px; }
}

</style>
