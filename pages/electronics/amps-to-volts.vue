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
          <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; AMPs to volts<hr>
      <h1 class="w3-text-teal"><b>Amps to volts Converter</b></h1>
      <p>Amps to Volts converter. Select one between Ohm and Watts and enter the numbers that you want to convert and click on the answer box.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <form id="designmodel" name="designmodel" autocomplete="off">
        <div class="form-group">
<table>
<tbody>
<tr>
<td>Select Conversion:</td>
<td><select v-model="voltagechange" @change="changedthings()" autofocus>
<option>In watts</option>
<option>In ohms</option>
</select></td>
<td>&nbsp;</td>
</tr><br>
<tr>
<td>Enter amps:</td>
<td><input type="number" v-model="number1" min="0" step="any" class="intext"></td>
<td style="text-align:left">A</td>
</tr><br>
<tr v-if="watts === true">
<td>Enter watts:</td>
<td><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td style="text-align:left">V</td>
</tr><br>
<tr v-if="ohms === true">
<td>Enter ohms:</td>
<td><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td style="text-align:left">&#937;</td>
</tr>
<tr>
<td><input @click="changedthings()" type="button" value="Answer" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray"> <input @click="reset()" type="reset" value="Reset" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray"></td>
<td>&nbsp;</td>
</tr><br>
<tr>
<td>Result in kilovolt-amps:</td>
<td><input type="text" v-model="answer" class="outtext" readonly></td>
<td style="text-align:left">kVA</td>
</tr><br>
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
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kw"> Amps to KW</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-va"> Amps to VA</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kva"> Amps to Kva</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-watts"> Amps to watts</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/kw-to-amps"> Kw to Amps</a></span><br>
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
      title: 'Amps to volts',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Amps to volts.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/amps-to-volts'}
    ]
    }
    },
  data(){
    return {
      number1: null,
      number2: null,
      answer: '',
      voltagechange: 'In watts',
      watts: true,
      ohms: false,
      volt: 'Line to line voltage'
    }
  },
  methods: {
    changedthings(){
      if(this.voltagechange === "In watts"){
        this.ohms = false;
        this.watts = true;
        var x1 = this.number1;
        var x2 = this.number2;
        var kva = x2/x1;
        this.answer = kva;
      }
      else if(this.voltagechange === "In ohms"){

          this.ohms = true;
          this.watts = false;
          var x = this.number1 * this.number2;
          this.answer = x;

        }
    },
    reset(){
      this.number1 = null;
      this.number2 = null;
      this.answer = "";
      this.voltagechange = "In watts";
      this.watts = true;
      this.ohms = false;
      this.volt = "Line to line voltage";
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
#designmodel { background:#a7c9b8; padding:20px; }
@media all and (max-width: 800px) {
   #ln { padding-right:35px; }
   #designmodel1, #designmodel3 { padding:10px; }
}
</style>
