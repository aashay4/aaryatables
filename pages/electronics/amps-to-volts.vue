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
      <form id="calcform" name="calcform" autocomplete="off">
        <div class="form-group">
<table class="calc2">
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
<td class="math"><input type="number" v-model="number1" min="0" step="any" class="intext"></td>
<td class="mathsymbol" style="text-align:left">A</td>
</tr><br>
<tr v-if="watts === true">
<td>Enter watts:</td>
<td class="math"><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td class="mathsymbol" style="text-align:left">V</td>
</tr><br>
<tr v-if="ohms === true">
<td>Enter ohms:</td>
<td class="math"><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td class="mathsymbol" style="text-align:left">&#937;</td>
</tr>
<tr>
<td><input @click="changedthings()" type="button" value="Calculate" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray"> <input onclick="setfocus()" type="reset" value="Reset" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray"></td>
<td>&nbsp;</td>
</tr><br>
<tr>
<td>Result in kilovolt-amps:</td>
<td class="math"><input type="text" v-model="answer" class="outtext" readonly></td>
<td class="mathsymbol" style="text-align:left">kVA</td>
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
        <h1 class=""><b>Other Number tools</b></h1>
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
      this.answer = ''
    }
  }

}
</script>

<style lang="css">
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
#calcform,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
#bdiv, #bdiv2, #bdiv3 { max-width:100px; }
#b, #b2, #b3 { max-width:70px; }
#bsel,#b2sel,#b3sel { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#log, #log2, #log3 { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#txt, #txt3 { font-family:math; }
#drop, #drop2, #drop3 { background:#fff; color:#212529; }
#calcform1 button i { vertical-align: bottom; }
#coefdiv1a, #coefdiv1b span { vertical-align: bottom; }
#graph { display:none; }
/*.btn b, .btn b2 { font-size:large; }*/
#opsel { font-weight:bold; margin-top:10px; }
#coefdiv1a, #coefdiv1b, #opdiv, #logdiv2 { display:none; }
@media all and (max-width: 800px) {
   #ln { padding-right:35px; }
   #calcform1, #calcform3 { padding:10px; }
}
</style>
