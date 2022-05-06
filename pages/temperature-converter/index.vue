<template>
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

<div class="w3-row">

<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; Temperature Converter<hr>
    <h1 class="w3-text-teal"><b>Temperature Converter</b></h1>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>
      </div>
      <div class="w3-padding">
        <div class="input-group">
        <input type="number" v-model="number1" min="0" step="any" class="form-control" placeholder="Enter a value for weight converter" @input="convert()" required>
        <div class="input-group-append">
        <select v-model="convertweight" @change="convert()" class="form-control">
        <option>Fahrenheit:	</option>
        <option>Rankine:	</option>
        <option>Celsius:	</option>
        <option>Centigrade:	</option>
        <option>Kelvin:	</option>

        </select>
        </div>
        </div>
      </div>
      <form autocomplete="off">
        <div class="w3-padding">
<table>
<tr>
<td><label>Fahrenheit:</label></td>
<td><input type="number" v-model="Fahrenheit" min="0" step="any" autofocus></td>
<td> °F</td>
</tr>
<tr>
<td><label>Rankine:</label></td>
<td><input v-model="Rankine" type="number" min="0" step="any"></td>
<td> °R</td>
</tr>
<tr>
<td><label>Celsius:</label></td>
<td><input type="number" v-model="Celsius" min="0" step="any"></td>
<td> °C</td>
</tr>
<tr>
<td><label>Centigrade:</label></td>
<td><input type="number" v-model="Centigrade" min="0" step="any"></td>
<td> °C</td>
</tr>
<tr>
<td><label>Kelvin:</label></td>
<td><input type="number" v-model="Kelvin" min="0" step="any"></td>
<td> K</td>
</tr>
<tr>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td><input type="reset" value="Reset" @click="reset()"></td>
</tr>
</table>
</div>
</form>

      <ul class="w3-ul w3-hoverable w3-white">
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/rankine-to-fahrenheit"> Rankine to Fahrenheit</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/rankine-to-celsius"> Rankine to Celsius</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/rankine-to-kelvin"> Rankine to Kelvin</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/kelvin-to-fahrenheit"> Kelvin to Fahrenheit</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/kelvin-to-celsius"> Kelvin to Celsius</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/kelvin-to-rankine"> Kelvin to Rankine conversion</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/fahrenheit-to-celsius"> Fahrenheit to Celsius</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/fahrenheit-to-kelvin"> Fahrenheit to Kelvin Converter</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/fahrenheit-to-rankine"> Fahrenheit to Rankine Conversion</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/celsius-to-fahrenheit"> Celsius to Fahrenheit Conversion</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/celsius-to-kelvin"> Celsius to Kelvin Conversion</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/temperature-converter/celsius-to-rankine"> Celsius to Rankine Conversion</a></span><br>
        </li>
      </ul>
  </div>
  <hr>

</div>


<!-- Introduction menu -->
<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-card w3-margin w3-margin-top">
    <div class="w3-container w3-white w3-padding">
      <h4><b>Temperature Converter</b></h4>
      <p>Use these temperature conversion tools to convert various temperature units easily.</p>
    </div>
  </div><hr>

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
import Logo from '~/components/Logo.vue'

export default {
  head() {
  return {
    title: 'Temperature Converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: ''}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/temperature-converter'}
  ]
  }
  },
  components: {
    Logo
  },
  data(){
    return{
      convertweight: '',
      number1: '',
      Fahrenheit: '',
      Rankine: '',
      Celsius: '',
      Centigrade: '',
      Kelvin: ''
    }
  },
  methods: {
    reset(){
      this.number1 = '';
      this.convertweight = '';
      this.Fahrenheit = '';
      this.Rankine = '';
      this.Celsius = '';
      this.Centigrade = '';
      this.Kelvin = '';
    },
    convert(){
      if(this.convertweight === "Fahrenheit:"){
        var d = this.number1;
        d = parseFloat(d);
//        var x = d*1000000;
        this.Fahrenheit = d;
        this.Rankine = d+459.67;
        this.Celsius = ((d-32)*5/9).toFixed(3);
        this.Centigrade = ((d-32)*5/9).toFixed(3);
        this.Kelvin = ((d+459.67)*5/9).toFixed(2);
      }
      else if(this.convertweight === "Rankine:"){
        var d = this.number1;
        d = parseFloat(d);
//        var x = d*1000000;
        this.Fahrenheit = d-459.67;
        this.Rankine = d;
        this.Celsius = ((d-491.67)*5/9).toFixed(3);
        this.Centigrade = ((d-491.67)*5/9).toFixed(3);
        this.Kelvin = (d*5/9).toFixed(6);
      }
      else if(this.convertweight === "Celsius:"){
        var d = this.number1;
        d = parseFloat(d);
        this.Fahrenheit = ((d*9/5)+32).toFixed(1);
        this.Rankine = ((d+273.15)*9/5).toFixed(2);
        this.Celsius = d;
        this.Centigrade = d;
        this.Kelvin = (d+273.15).toFixed(2);
      }
      else if(this.convertweight === "Centigrade:"){
        var d = this.number1;
        d = parseFloat(d);
        this.Fahrenheit = ((d*9/5)+32).toFixed(1);
        this.Rankine = ((d+273.15)*9/5).toFixed(2);
        this.Celsius = d;
        this.Centigrade = d;
        this.Kelvin = (d+273.15).toFixed(2);
      }
      else if(this.convertweight === "Kelvin:"){
        var d = this.number1;
        d = parseFloat(d);
        this.Fahrenheit = ((d*9/5)-459.67).toFixed(2);
        this.Rankine = (d*9/5).toFixed(2);
        this.Celsius = (d-273.15).toFixed(2);
        this.Centigrade = (d-273.15).toFixed(2);
        this.Kelvin = d;
      }
      else{
        if(this.number1 === ''){
          alert("please enter a value")
        }else
        {alert("please slect an option")}
      }
    }
  }
}
</script>

<style>
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
body,h1,h2,h3,h4,h5 {font-family: "Raleway", sans-serif}
h1 { font-size:1.6rem; }
.removelink{
    text-decoration: none;
}
</style>
