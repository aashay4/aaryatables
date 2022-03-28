<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Electricity bill calculator <hr>
    <h1 class="w3-text-teal"><b>Calculator electricity bill</b></h1>
<p>A tool to calculate electricity of a house of an office.</p>
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
<label>Select Your country</label>
<div class="input-group-append">
<select v-model="countryprice" class="form-control" @change="cosvaluechange()">
<option>-- select --</option>
<option value="0.002">Sudan</option>
<option value="0.004">Libya</option>
<option value="0.004">Iran</option>
<option value="0.005">Lebanon</option>
<option value="0.007">Ethiopia</option>
<option value="0.008">Kyrgyzstan</option>
<option value="0.024">Iraq</option>
<option value="0.016">Suriname</option>
<option value="0.017">Bhutan</option>
<option value="0.026">Angola</option>
<option value="0.026">Oman</option>
<option value="0.030">Cuba</option>
<option value="0.030">Kuwait</option>
<option value="0.032">Zambia</option>
<option value="0.032">Qatar</option>
<option value="0.034">Burma</option>
<option value="0.034">Zimbabwe</option>
<option value="0.036">Kazakhstan</option>
<option value="0.037">Algeria</option>
<option value="0.041">Egypt</option>
<option value="0.041">Azerbaijan</option>
<option value="0.043">Russia</option>
<option value="0.043">Afghanistan</option>
<option value="0.045">Laos</option>
<option value="0.048">Saudi Arabia</option>
<option value="0.048">Bahrain</option>
<option value="0.050">Sri Lanka</option>
<option value="0.051">Ghana</option>
<option value="0.052">Trinidad & Tobago</option>
<option value="0.053">Pakistan</option>
<option value="0.053">Malaysia</option>
<option value="0.053">Argentina</option>
<option value="0.054">Turkey</option>
<option value="0.057">Nigeria</option>
<option value="0.057">Ukraine</option>
<option value="0.058">Paraguay</option>
<option value="0.062">Georgia</option>
<option value="0.064">Belarus</option>
<option value="0.065">Bangladesh</option>
<option value="0.068">Nepal</option>
<option value="0.071">Tunisia</option>
<option value="0.075">India</option>
<option value="0.081">United Arab Emirates</option>
<option value="0.082">Vietnam</option>
<option value="0.082">Armenia</option>
<option value="0.082">Moldova</option>
<option value="0.083">DR Congo</option>
<option value="0.084">Cameroon</option>
<option value="0.084">Mexico</option>
<option value="0.085">Northern Macedonia</option>
<option value="0.090">China</option>
<option value="0.093">Dominican Republic</option>
<option value="0.096">Ecuador</option>
<option value="0.096">Serbia</option>
<option value="0.099">Taiwan</option>
<option value="0.099">Tanzania</option>
<option value="0.100">Jordan</option>
<option value="0.100">Bosnia & Herz</option>
<option value="0.101">Indonesia</option>
<option value="0.103">Albania</option>
<option value="0.103">South Korea</option>
<option value="0.104">Lesotho</option>
<option value="0.105">Botswana</option>
<option value="0.110">Hungary</option>
<option value="0.111">Costa Rica</option>
<option value="0.112">Madagascar</option>
<option value="0.113">Thailand</option>
<option value="0.115">Canada</option>
<option value="0.116">Malawi</option>
<option value="0.117">Swaziland</option>
<option value="0.118">Bolivia</option>
<option value="0.120">Morocco</option>
<option value="0.122">Ivory Coast</option>
<option value="0.129">Bulgaria</option>
<option value="0.130">Namibia</option>
<option value="0.137">Mauritius</option>
<option value="0.137">Sierra Leone</option>
<option value="0.141">Mozambique</option>
<option value="0.143">Iceland</option>
<option value="0.144">Macao</option>
<option value="0.145">Norway</option>
<option value="0.148">Malta</option>
<option value="0.149">Hong Kong</option>
<option value="0.150">Colombia</option>
<option value="0.151">Brazil</option>
<option value="0.151">Croatia</option>
<option value="0.151">Cambodia</option>
<option value="0.153">USA</option>
<option value="0.155">Panama</option>
<option value="0.160">Philippines</option>
<option value="0.166">Romania</option>
<option value="0.167">Estonia</option>
<option value="0.171">Latvia</option>
<option value="0.171">Israel</option>
<option value="0.171">South Africa</option>
<option value="0.173">Chile</option>
<option value="0.173">Finland</option>
<option value="0.173">Nicaragua</option>
<option value="0.174">Senegal</option>
<option value="0.178">Singapore</option>
<option value="0.178">Poland</option>
<option value="0.180">Honduras</option>
<option value="0.181">Lithuania</option>
<option value="0.181">Sweden</option>
<option value="0.182">Netherlands</option>
<option value="0.185">Aruba</option>
<option value="0.186">Slovakia</option>
<option value="0.189">Uganda</option>
<option value="0.194">El Salvador</option>
<option value="0.195">Togo</option>
<option value="0.197">Slovenia</option>
<option value="0.203">Peru</option>
<option value="0.204">France</option>
<option value="0.206">Greece</option>
<option value="0.207">Gabon</option>
<option value="0.208">Burkina Faso</option>
<option value="0.209">New Zealand</option>
<option value="0.211">Kenya</option>
<option value="0.215">Uruguay</option>
<option value="0.221">Belize</option>
<option value="0.221">Mali</option>
<option value="0.223">Switzerland</option>
<option value="0.228">Spain</option>
<option value="0.233">Luxembourg</option>
<option value="0.236">Austria</option>
<option value="0.238">Australia</option>
<option value="0.245">Japan</option>
<option value="0.246">Czech Republic</option>
<option value="0.248">Barbados</option>
<option value="0.252">Italy</option>
<option value="0.255">Rwanda</option>
<option value="0.256">Portugal</option>
<option value="0.257">Guatemala</option>
<option value="0.260">Liechtenstein</option>
<option value="0.262">Cyprus</option>
<option value="0.267">Bahamas</option>
<option value="0.273">Ireland</option>
<option value="0.273">Venezuela</option>
<option value="0.274">Cape Verde</option>
<option value="0.283">United Kingdom</option>
<option value="0.293">Jamaica</option>
<option value="0.309">Belgium</option>
<option value="0.324">Cayman Islands</option>
<option value="0.350">Denmark</option>
<option value="0.350">Germany</option>
<option value="0.370">Bermuda</option>
</select>
</div>
</div>
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
<label>1 kilowatt-hour (kWh) cost in your country ($ - US Dollars):</label>
<input type="number" v-model="countryprice" class="form-control">
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
<h2>About AMPS to KW tool:</h2>
<p>To use this AMPs to KW tool, select the current type phase from DC, AC-single phase and AC-three phase. Once selected, enter the current unit in Ampere and voltage in volts. Once inserted, click on the "Answer" button. After clicking on the button, check the answers in Kilowatts, Watts and Milliwatts.</p>
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
      title: 'Electricity bill calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculate your house or office electricity bill.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/electricity-bill-calculator'}
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
      var kw = this.cosvalue * this.powerfactorinput * this.countryprice;
      this.kw = kw/1000;
      this.w = this.kw*30.4375;
      var ggg = this.kw*365.25
      this.mw = this.roundnum(ggg, 5);
    }else{
      var kw = this.cosvalue * this.powerfactorinput * this.countryprice;
      this.kw = kw;
      this.w = this.kw*30.4375;
      var gg = this.kw*365.25;
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
      this.currenttype = "DC",
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
