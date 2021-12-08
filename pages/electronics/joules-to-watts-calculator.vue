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

    <form name="calcform" autocomplete="off">
  <table class="calc2">
  <tbody>
  <tr>
  <td>Enter joules:</td>
  <td class="math"><input type="number" min="0" step="any" name="x1" class="intext" v-model="joules" autofocus></td>
  <td class="mathsymbol">  J</td>
  </tr>
  <tr>
  <td>Enter seconds:</td>
  <td class="math"><input type="number" min="0" step="any" name="x2" class="intext" v-model="seconds"></td>
  <td class="mathsymbol">  S</td>
  </tr>
  <tr>
  <td>&nbsp;</td>
  <td>
  <button type="button" title="Calculate" class="btn btn-secondary" @click="convert()"><span>=></span> Answer</button></td>
  <td>&nbsp;</td>
  </tr>
  <tr>
  <td>watts:</td>
  <td class="math"><input type="text" v-model="answer" class="outtext" readonly></td>
  <td class="mathsymbol"> W</td>
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
//document.getElementById("y2").value = roundresult(1000*a);
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
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
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
