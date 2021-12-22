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
          <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; kva to amps<hr>
      <h1 class="w3-text-teal"><b>kVa to amps</b></h1><br>
      <p>kilovolt-amp(kVA) to amps converter.</p>
      <form id="calcform1" name="calcform" autocomplete="off">
        <div class="form-group">
<table class="calc2">
<tbody>
<tr>
<td>Select phase:</td>
<td class="w3-padding"><select v-model="voltagechange" @change="changedthings()" autofocus>
<option>Single phase</option>
<option>Three phase</option>
</select></td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Enter kilovolt-amps:</td>
<td class="math w3-padding"><input type="number" v-model="number1" min="0" step="any" class="intext"></td>
<td class="mathsymbol w3-padding" style="text-align:left">Kva</td>
</tr>
<tr id="row1" v-if="showthis === true">
<td>Enter volts:</td>
<td class="w3-padding"><select v-model="volt" @change="changedthings()">
<option>Line to line voltage</option>
<option>Line to neutral voltage</option>
</select></td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Enter volts:</td>
<td class="w3-padding math"><input type="number" v-model="number2" min="0" step="any" class="intext"></td>
<td class="mathsymbol" style="text-align:left">V</td>
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
              <span class="w3-large"><a class="removelink" href="/electronics/kva-to-kw"> Kva to kw</a></span><br>
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
      title: 'kVA to Amps',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'kilovolt-amps to ampere (kVA to A) Calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/kva-to-amps'}
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
        var kva = x1*57.735/1000;
        if(this.volt === "Line to line voltage")
        {
this.answer = x1*577.35/x2;
        }
        else if(this.volt === "Line to neutral voltage"){
          kva*=3;
          this.answer = x1*333.333/x2;
        }
      }
      else if(this.voltagechange === "Single phase"){

          this.showthis = false;
          var x = this.number1/this.number2;
          this.answer = x*1000;

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
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }

</style>
