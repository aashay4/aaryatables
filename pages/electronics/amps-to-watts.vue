<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; AMPs to Watts(W) <hr>
    <h1 class="w3-text-teal"><b>Amps to watts Calculator</b></h1><br>
    <p>AMPs to Watts converter and how to convert? Use the below tool to convert amts to watts.</p>
    <form id="calcform1" name="calcform" autocomplete="off">
<div class="form-group">
<label for="phase">Select current type</label>
<select id="phase" name="phase" v-model="currenttype" @change="currentchange()" class="form-control" autofocus>
<option>AC - Single phase</option>
<option>AC - Three phase</option>
<option>DC</option>
</select>
</div>
<div class="form-group">
<label for="x1">Enter current in amps</label>
<div class="input-group">
<input type="number" v-model="number1" name="x1" min="0" step="any" class="form-control" required>
<div class="input-group-append">
<select v-model="amperselect" class="form-control">
<option>mA</option>
<option selected>A</option>
<option>kA</option>
</select>
</div>
</div>
</div>
<div class="form-group" v-if="threephase === true">
<label for="volt">Select voltage type</label>
<select id="volt" name="volt" v-model="voltagetype" class="form-control">
<option>Line to line voltage</option>
<option>Line to neutral voltage</option>
</select>
</div>
<div class="form-group">
<label for="x2">Enter voltage in volts</label>
<div class="input-group">
<input type="number" min="0" step="any" v-model="number2" name="x2" class="form-control" required>
<div class="input-group-append">
<select v-model="voltagechange" class="form-control">
<option>mV</option>
<option selected>V</option>
<option>kV</option>
</select>
</div>
</div>
</div>
<div class="form-group" v-if="powerfactor === true">
<label for="pf">Enter power factor</label>
<input type="number" v-model="powerfactorinput" class="form-control">
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="currentchange()"><span>=></span> Answer</button>
<button type="reset" title="Reset" class="btn btn-secondary" onclick="setfocus()"><span>↺</span> Reset</button>
<button type="button" title="Swap conversion" class="btn btn-secondary" onclick="location.href='kW_to_Amp_Calculator.html';"><span></span> Swap</button>
</div>
<div class="form-group">
<label for="y">Power result in kilowatts</label>
<div class="input-group">
<input type="text" v-model="kw" name="y" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">kW</span>
</div>
</div>
</div>
<div class="form-group">
<label for="y">Power result in watts</label>
<div class="input-group">
<input type="text" v-model="w" name="y2" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">W</span>
</div>
</div>
</div>
<div class="form-group">
<label for="y">Power result in milliwatts</label>
<div class="input-group">
<input type="text" v-model="mw" name="y3" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">mW</span>
</div>
</div>
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
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-volts"> Amps to volts(V)</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/amps-to-kva"> Amps to Kva</a></span><br>
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
</template>

<script>
export default {
  head() {
    // sets document title
    return {
      title: 'Amps to watts',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Amps to watts.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/amps-to-watts'}
    ]
    }
    },
  data(){
    return {
      currenttype: 'AC - Single phase',
      powerfactor: false,
      threephase: false,
      amperselect: 'A',
      voltagechange: 'V',
      kw: '',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      voltagetype: 'Line to line voltage'
    }
  },
  methods: {
    currentchange(){
      if(this.currenttype === "AC - Single phase"){
        this.powerfactor = true;
        this.threephase = false;
          if(this.powerfactorinput === '1'){
            if(this.amperselect === "A" && this.voltagechange === "V"){
              var x = this.number1/1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "mA" && this.voltagechange === "V"){
              var x = this.number1/1000000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "kA" && this.voltagechange === "V"){
              var x = this.number1/1;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "mA" && this.voltagechange === "mV"){
              var x = this.number1/1000000000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "A" && this.voltagechange === "mV"){
              var x = this.number1/1000000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "kA" && this.voltagechange === "mV"){
              var x = this.number1/1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "mA" && this.voltagechange === "kV"){
              var x = this.number1/1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "A" && this.voltagechange === "kV"){
              var x = this.number1/1;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
            }
            else if(this.amperselect === "kA" && this.voltagechange === "kV"){
              var x = this.number1 * 1000;
              this.kw = x * this.number2;
              this.w = this.kw * 1000;
              this.mw = this.kw * 1000000;
          }
          else if(this.currenttype === "AC - Three phase"){
            this.threephase = true;
            this.powerfactor = true;
          }
          else{
            this.kw = 0;
            this.w = 0;
            this.mw = 0;
          }
          }

      }
      else if(this.currenttype === "DC"){
        this.powerfactor = false;
        if(this.amperselect === "A" && this.voltagechange === "V"){
          var x = this.number1/1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "mA" && this.voltagechange === "V"){
          var x = this.number1/1000000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "kA" && this.voltagechange === "V"){
          var x = this.number1/1;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "mA" && this.voltagechange === "mV"){
          var x = this.number1/1000000000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "A" && this.voltagechange === "mV"){
          var x = this.number1/1000000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "kA" && this.voltagechange === "mV"){
          var x = this.number1/1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "mA" && this.voltagechange === "kV"){
          var x = this.number1/1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "A" && this.voltagechange === "kV"){
          var x = this.number1/1;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
        }
        else if(this.amperselect === "kA" && this.voltagechange === "kV"){
          var x = this.number1 * 1000;
          this.kw = x * this.number2;
          this.w = this.kw * 1000;
          this.mw = this.kw * 1000000;
      }
      else{
        console.log("not right decision")
      }

}
      else if(this.currenttype === "AC - Three phase"){
        this.threephase = true;
        this.powerfactor = true;
        if( this.amperselect === "kA" ) this.number1/=1000;
        if( this.amperselect === "mA" ) this.number1/=1000;
        if( this.voltagechange === "mV" ) this.number2/=1000;
        if( this.voltagechange === "kV" ) this.number2/=1000;
        var kw = this.number1*this.number2/1000;

        if( this.voltagetype === "Line to line voltage" )
   kw*=(this.powerfactorinput*Math.sqrt(3));
else
   kw*=(this.powerfactorinput*3);
   this.kw = kw;
   this.w = 1000*kw;
   this.mw = 1000000*kw;
      }

  },
    reset(){
      this.number1 = null;
      this.number2 = null;
      this.answer = ''
    }
  },
  beforeMount(){
   this.currentchange();
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
