<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Energy Consumption Calculator <hr>
    <h1 class="w3-text-teal"><b>Energy Consumption Calculator</b></h1>
<p>A tool to calculate energy consumption of a house of an office.</p>
<Adsense
class="adsbygoogle infeed"
style="display:block"
data-ad-client="ca-pub-6829148792481216"
data-ad-slot="4199493091"
data-ad-format="auto"
data-full-width-responsive="true">
</Adsense>
    <form id="desingiput" name="desingiput" autocomplete="off">
<div class="form-group">
<label>Typical appliance:</label>
<div class="input-group-append">
  <select class="form-control" v-model="cosvalue" @change="cosvaluechange()">
  <option>-- select --</option>
  <option value="600">Air conditioner</option>
  <option value="3000">Clothes dryer</option>
  <option value="2400">Clothes iron</option>
  <option value="1600">Dishwasher</option>
  <option value="2000">Electric kettle</option>
  <option value="70">Fan</option>
  <option value="2000">Heater</option>
  <option value="800">Microwave oven</option>
  <option value="100">Computer</option>
  <option value="50">Laptop</option>
  <option value="600">Refrigerator</option>
  <option value="600">Stereo receiver</option>
  <option value="600">Television</option>
  <option value="600">Toaster oven</option>
  <option value="600">Vacuum cleaner</option>
  <option value="600">Washing machine</option>
  <option value="600">Water heater</option>
  </select>
</div>
</div>
<div class="form-group" v-if="threephase === true">
<label for="volt">Select voltage type</label>
<select v-model="voltagetype" class="form-control">
<option>Line to line voltage</option>
<option>Line to neutral voltage</option>
</select>
</div>
<div class="form-group">
<label>Power Consumption:</label>
<div class="input-group">
<input type="number" v-model="cosvalue" class="form-control" required>
<div class="input-group-append">
<select v-model="voltagechange" class="form-control">
<option selected>Watts</option>
<option>Kilowatts</option>
</select>
</div>
</div>
</div>
<div class="form-group">
<label>Enter usage(Total hours per day):</label>
<input type="number" v-model="powerfactorinput" class="form-control">
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="cosvaluechange()"><span>=></span> Answer</button>
</div>
<div class="form-group">
<label>Electricity cost per day:</label>
<div class="input-group">
<input type="text" v-model="kw" class="form-control" readonly>
</div>
</div>
<div class="form-group">
<label for="y">Electricity cost per month:</label>
<div class="input-group">
<input type="text" v-model="w" class="form-control" readonly>
</div>
</div>
<div class="form-group">
<label for="y">Electricity cost per Year:</label>
<div class="input-group">
<input type="text" v-model="mw" class="form-control" readonly>
</div>
</div>
</form><br>
      </div>
        </div>
  <hr>

  </div>


  <!-- Introduction menu -->

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
      title: 'Energy Consumption Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculate your house or office energy consumption.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/energy-consumption-calculator'}
    ]
    }
    },
  data(){
    return {
      countryprice: '',
      currenttype: 'DC',
      powerfactor: false,
      threephase: false,
      amperselect: 'A',
      voltagechange: 'Watts',
      kw: '',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      voltagetype: 'Line to line voltage',
      cosvalue: ''
    }
  },
  methods: {
    cosvaluechange(){
      if(this.voltagechange === "Watts"){
      var kw = this.cosvalue * this.powerfactorinput;
      this.kw = kw/1000;
      this.w = this.kw*30;
      var ggg = this.kw*365;
      this.mw = this.roundnum(ggg, 5);
    }else{
      var kw = this.cosvalue * this.powerfactorinput;
      this.kw = kw;
      this.w = this.kw*30;
      var gg = this.kw*365;
      this.mw = this.roundnum(gg, 5);
    }
    },
    roundnum(x,p) {
      var i;
      var j;
      var n=parseFloat(x);
      var m=n.toFixed(p);
      var y=String(m);
      i=y.length;
      j=y.indexOf('.');
      if( i>j && j!=-1 )
      {
        while(i>0)
        {
          if(y.charAt(--i)=='0')
            y = this.removeAt(y,i);
          else
            break;
        }
        if(y.charAt(i)=='.')
          y = this.removeAt(y,i);
      }
      return y;
    },
    removeAt(s,i) {
      s = s.substring(0,i)+s.substring(i+1,s.length);
      return s;
    },
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
      this.currenttype = "Watt",
      this.powerfactor = false,
      this.threephase = false,
      this.amperselect = "A",
      this.voltagechange = "V",
      this.kw = "",
      this.w = "",
      this.mw = "",
      this.number1 = "",
      this.number2 = "",
      this.powerfactorinput = "",
      this.voltagetype = "Line to line voltage"
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

#desingiput { background:#a7c9b8; padding:20px; }
.btn span { font-weight: bold; font-size:large; }
/*.btn b, .btn b2 { font-size:large; }*/
@media all and (max-width: 800px) {
}
</style>
