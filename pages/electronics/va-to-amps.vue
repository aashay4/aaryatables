<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; VA to Amps <hr>
    <h1 class="w3-text-teal"><b>VA to Amps calculator</b></h1>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>

    <form id="designmodel" autocomplete="off">
    <table><br>
    <tbody>
    <tr>
    <td>Enter phase #:</td>
    <td><select v-model="currenttype" autofocus>
    <option>Single phase</option>
    <option>Three phase</option>
    </select></td>
    <td>&nbsp;</td>
    </tr><br>
    <tr>
    <td>Enter volt-amps:</td>
    <td class=""><input type="number" v-model="number1" class="intext"></td>
    <td class="">VA</td>
    </tr><br>
    <tr>
    <td>Enter line to line volts:</td>
    <td class=""><input type="number" v-model="number2" step="any" name="x2" class="intext"></td>
    <td class="">V</td>
    </tr><br>
    <tr>
    <td>&nbsp;</td>
    <td><input @click="currentchange()" type="button" value="Calculate" class="btn btn-secondary"> <input @click="reset()" type="reset" value="Reset" class="btn btn-secondary"></td>
    <td>&nbsp;</td>
    </tr><br>
    <tr>
    <td>Result in amps:</td>
    <td class=""><input type="text" v-model="answer" class="outtext" readonly="readonly"></td>
    <td class="">A</td>
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
              <span class="w3-large"><a class="removelink" href="/electronics/va-to-kva"> va to kva</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/va-to-kw"> va to kw</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/va-to-watts"> va to watts</a></span><br>
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
      title: 'Volt-amps (VA) to amps (A) converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'VA to AMPs' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/va-to-amps'}
    ]
    }
    },
  data(){
    return {
      currenttype: 'Single phase',
      powerfactor: false,
      threephase: false,
      wattchange: 'kW',
      voltagechange: 'V',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      phase: '',
      powerfactorinput: '',
      kilowatinput: '',
      voltagetype: 'Line to line voltage',
      answer: ''
    }
  },
  methods: {
    currentchange(){
      if(this.currenttype === 'Single phase')
      {
  var x1= this.number1;
  var x2 = this.number2;
  this.answer = (x1/x2);
}
else{
  var x1= this.number1;
  var x2 = this.number2;
  this.answer = (x1/x2)*0.57735026919;
}
  },
    reset(){
      this.currenttype = "Single phase";
      this.powerfactor = false;
      this.threephase = false;
      this.wattchange = "kW";
      this.voltagechange = "V";
      this.w = "";
      this.mw = "";
      this.number1 = "";
      this.number2 = "";
      this.phase = "";
      this.powerfactorinput = "";
      this.kilowatinput = "";
      this.voltagetype = "Line to line voltage";
      this.answer = "";
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
#designmodel button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designmodel { padding:10px; }
}

</style>
