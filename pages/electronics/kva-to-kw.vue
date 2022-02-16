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
          <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; kva to kilo-watts<hr>
      <h1 class="w3-text-teal"><b>kva to kw</b></h1><br>
      <p>kilovolt-amp(kVA) to kw converter.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <form id="calcform1" name="calcform" autocomplete="off">
        <div class="form-group">
<table class="calc2">
<tbody>
<tr>
<td>Enter kilovolt-amps:</td>
<td class="math w3-padding"><input type="number" v-model="number1" min="0" step="any" class="intext"></td>
<td class="mathsymbol w3-padding" style="text-align:left">Kva</td>
</tr>
<tr>
<td>Enter Power factor:</td>
<td class="w3-padding math"><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td class="mathsymbol" style="text-align:left"></td>
</tr>
<tr>
<td>&nbsp;</td>
<td class="w3-padding"><button @click="changedthings()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button onclick="setfocus()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Amps result:</td>
<td class="math w3-padding"><input type="text" v-model="answer" class="outtext" readonly></td>
<td class="mathsymbol" style="text-align:left">A</td>
</tr>
</tbody>
</table>
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
        <h1 class=""><b>Other Electronics tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/kva-to-amps"> Kva to amps</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/kva-to-va"> Kva to va</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/kva-to-watts"> Kva to watts</a></span><br>
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
      title: 'kva to kw',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'kilovolt-amps to kw (kVA to kw) converter.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/kva-to-kw'}
    ]
    }
    },
  data(){
    return {
      number1: null,
      number2: null,
      answer: '',
      powerfactor: '',
      showthis: false,
      volt: 'Line to line voltage'
    }
  },
  methods: {
    changedthings(){
      if(this.number2 === "1")
    {    this.answer = this.number1*this.number2;}
    else if(this.number2 === "0"){
      this.answer = 0;
    }
    else{
      alert("Please enter power-factor in zero or one")
    }

}}
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
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }

</style>
