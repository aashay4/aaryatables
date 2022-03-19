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
          <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; AMPs to kVA<hr>
      <h1 class="w3-text-teal"><b>Amps to kVA</b></h1><br>
      <p>AMPs to kilovolt-amp(kVA) converter.</p>
      <p>Select the phase between single-phase and three-phase, enter Amperes and Volts in the text box, click on the answer button to convert Amps to kVA.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <form id="linewise" autocomplete="off">
        <div class="form-group">
<table>
<tbody>
<tr>
<td>Select phase #:</td>
<td class="w3-padding"><select v-model="voltagechange" @change="changedthings()" autofocus>
<option>Single phase</option>
<option>Three phase</option>
</select></td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Enter amps:</td>
<td class="w3-padding"><input type="number" v-model="number1" min="0" step="any" class="intext"></td>
<td class="w3-padding" style="text-align:left">A</td>
</tr>
<tr v-if="showthis === true">
<td>Select voltage type:</td>
<td class="w3-padding"><select v-model="volt" @change="changedthings()">
<option>Line to line voltage</option>
<option>Line to neutral voltage</option>
</select></td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Enter volts:</td>
<td class="w3-padding"><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td style="text-align:left">V</td>
</tr>
<tr>
<td>&nbsp;</td>
<td class="w3-padding"><button @click="changedthings()" type="button" class="btn btn-secondary"><span>=></span> Answer</button>
<button onclick="setfocus()" type="reset" class="btn btn-secondary"><span>↺</span> Reset</button>
</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Result in kilovolt-amps:</td>
<td class="w3-padding"><input type="text" v-model="answer" class="outtext" readonly></td>
<td style="text-align:left">kVA</td>
</tr>
</tbody>
</table>
</div>
</form>


    </div>
    <div class="w3-padding">
    <h2>AMPS to KVA Calculation <i>steps</i></h2>
    <h3>Single Phase:</h3>
    <p>To convert AMPs to KVA for a single-phase, multiply Amperes and volts. Once multiplied, divide the answer by 1000.</p>
    <i> S = I &times; V </i><br>
    <h3>
      Calculation with line to line voltage:
    </h3><br>
    <p><i>S</i><sub>(kVA)</sub> = <i>&#8730;</i><span style="text-decoration: overline">3</span>
    &times; <i> I</i><sub>(A)</sub><i> </i>&times;<i> V</i><sub>L-L(V)</sub><i> </i>/ 1000&nbsp;</p>
    <h3>
      Calculation with line to neutral voltage
    </h3>
    <p><p><i>S</i><sub>(kVA)</sub> = 3 &times; <i> I</i><sub>(A)</sub><i> </i>&times;<i> V</i><sub>L-N(V)</sub><i> </i>/ 1000</p>
<p>&nbsp;</p>
</p>
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
      title: 'Amps to kVA Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Amps to kilovolt-amps (A to kVA) Calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/amps-to-kva'}
    ]
    }
    },
  data(){
    return {
      number1: null,
      number2: null,
      answer: '',
      voltagechange: 'Single phase',
      showthis: false,
      volt: 'Line to line voltage'
    }
  },
  methods: {
    changedthings(){
      if(this.voltagechange === "Three phase"){
        this.showthis = true;
        var x1 = this.number1;
        var x2 = this.number2;
        var kva = x1*x2/1000;
        if(this.volt === "Line to line voltage")
        {
          kva*=Math.sqrt(3);
          this.answer = kva;
        }
        else if(this.volt === "Line to neutral voltage"){
          kva*=3;
          this.answer = kva;
        }
      }
      else if(this.voltagechange === "Single phase"){

          this.showthis = false;
          var x = this.number1/this.number2;
          this.answer = x*10;

        }
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
#linewise { background:#a7c9b8; padding:20px; }
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }

</style>
