<template>
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

<div class="w3-row">

<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; Weight Converter<hr>
    <h1 class="w3-text-teal"><b>Weight Converter</b></h1>
      </div>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <div class="w3-padding">
        <div class="input-group">
        <input type="number" v-model="number1" min="0" step="any" class="form-control" placeholder="Enter a value for weight converter" @change="convert()" required>
        <div class="input-group-append">
        <select v-model="convertweight" @change="convert()" class="form-control">
        <option>tonne</option>
        <option>Gram</option>
        <option>Kilogram</option>
        <option>Milligram</option>
        <option>Microgram</option>
        <option>Ounce</option>
        <option>Imperial ton</option>
        <option>Stone</option>
        <option>Pound</option>

        </select>
        </div>
        </div>
      </div>
      <form name="calcform" autocomplete="off">
        <div class="w3-padding">
<table class="calc2">
<tr>
<td><label for="ton">Tonne:</label></td>
<td class="math"><input type="number" v-model="tonne" min="0" step="any" id="ton" name="ton" autofocus> :</td>
<td class="mathsymbol"> t</td>
</tr>
<tr>
<td><label for="kg">Kilograms:</label></td>
<td class="math"><input v-model="kilogram" type="number" min="0" step="any" id="kg" name="kg"></td>
<td class="mathsymbol"> kg</td>
</tr>
<tr>
<td><label for="gr">Grams:</label></td>
<td class="math"><input type="number" v-model="gram" min="0" step="any" id="gr" name="gr"></td>
<td class="mathsymbol"> g</td>
</tr>
<tr>
<td><label for="mg">Milligrams:</label></td>
<td class="math"><input type="number" v-model="milligram" min="0" step="any" id="mg" name="mg"></td>
<td class="mathsymbol"> mg</td>
</tr>
<tr>
<td><label for="mcg">Micrograms:</label></td>
<td class="math"><input type="number" v-model="microgram" min="0" step="any" id="mcg" name="mcg"></td>
<td class="mathsymbol"> mcg</td>
</tr>
<tr>
<td><label for="st">Stones:</label></td>
<td class="math"><input type="number" v-model="stones" min="0" step="any" id="st" name="st"></td>
<td class="mathsymbol"> st</td>
</tr>
<tr>
<td><label for="lb">Pounds:</label></td>
<td class="math"><input type="number" v-model="pounds" min="0" step="any" id="lb" name="lb"></td>
<td class="mathsymbol"> lb</td>
</tr>
<tr>
<td><label for="oz">Ounces:</label></td>
<td class="math"><input type="number" v-model="ounches" min="0" step="any" id="oz" name="oz"></td>
<td class="mathsymbol"> oz</td>
</tr>
<tr>
<td><label for="oz">Imperial ton:</label></td>
<td class="math"><input type="number" min="0" v-model="imperialton" step="any" id="oz" name="oz"></td>
<td class="mathsymbol"> Im</td>
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
          <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-kilograms"> Grams to Kilograms</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/kilograms-to-grams"> Kilograms to Grams</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-milligrams"> Grams to Milligrams</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-ounces"> Grams to Ounces</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/grams-to-pounds"> Grams to Pounds</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/kilograms-to-milligrams"> Kilograms to Milligrams</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/kilograms-to-pounds"> Kilograms to Pounds</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/kilograms-to-tons"> Kilograms to Tons</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/weight-converter/milligrams-to-grams"> Milligrams to Grams</a></span><br>
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
      <h4><b>Weight Online Tools</b></h4>
      <p>Use these weight tools to convert Kilogram, Milligram, Ounces, Pounds and Grams.</p>
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
    title: 'Weight Converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: ''}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/weight-converter'}
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
      gram: '',
      kilogram: '',
      milligram: '',
      microgram: '',
      stones: '',
      tonne: '',
      ounches: '',
      imperialton: '',
      pounds: ''
    }
  },
  methods: {
    reset(){
      this.number1 = '';
      this.convertweight = '';
      this.tonne = '';
      this.gram = '';
      this.kilogram = '';
      this.milligram = '';
      this.microgram = '';
      this.stones = '';
      this.tonne = '';
      this.ounches = '';
      this.imperialton = '';
      this.pounds = '';
    },
    convert(){
      if(this.convertweight === "tonne"){
        var d = this.number1;
        d = parseFloat(d);
        var x = d*1000000;
        this.gram = x;
        this.kilogram = d*1000;
        this.milligram = d*1e9;
        this.microgram = d*1e12;
        this.stones = d*157.473;
        this.pounds = d*2204.623;
        this.ounches = d*35273.96;
        this.imperialton = d*0.984207;
        this.tonne = d*1;
      }
      else if(this.convertweight === "Gram"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d;
        this.kilogram = d*0.001;
        this.milligram = d*1000;
        this.microgram = d*1000000;
        this.stones = d*0.000157473;
        this.pounds = d*0.002204623;
        this.ounches = d*0.03527396;
        this.imperialton = d*9.8421e-7;
        this.tonne = d*0.000001;
      }
      else if(this.convertweight === "Kilogram"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*1000;
        this.kilogram = d*1;
        this.milligram = d*1000000;
        this.microgram = d*1e+9;
        this.stones = d*0.157473;
        this.pounds = d*2.204623;
        this.ounches = d*35.27396;
        this.imperialton = d*0.000984207;
        this.tonne = d*0.001;
      }
      else if(this.convertweight === "Milligram"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*0.001;
        this.kilogram = d*0.000001;
        this.milligram = d*1;
        this.microgram = d*1000;
        this.stones = d*1.57473e-7;
        this.pounds = d*0.000002204623;
        this.ounches = d*0.00003527396;
        this.imperialton = d*0.000984207;
        this.tonne = d*1e-9;
      }
      else if(this.convertweight === "Microgram"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*0.000001;
        this.kilogram = d*1e-9;
        this.milligram = d*0.001;
        this.microgram = d*1;
        this.stones = d*1.57473e-10;
        this.pounds = d*2.204623e-9;
        this.ounches = d*3.527396e-8;
        this.imperialton = d*9.8420699999997899e-13;
        this.tonne = d*1e-12;
      }
      else if(this.convertweight === "Ounches"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*28.34952;
        this.kilogram = d*0.02834952;
        this.milligram = d*28349.52;
        this.microgram = d*2.834952e+7;
        this.stones = d*0.004464286;
        this.pounds = d*0.0625;
        this.ounches = d*1;
        this.imperialton = d*2.7902e-5;
        this.tonne = d*0.00002834952;
      }
      else if(this.convertweight === "Imperial ton"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*1.016e+6;
        this.kilogram = d*1016.05;
        this.milligram = d*1.016e+9;
        this.microgram = d*1.016e+12;
        this.stones = d*160;
        this.pounds = d*2240;
        this.ounches = d*35840;
        this.imperialton = d*1;
        this.tonne = d*1.016;
      }
      else if(this.convertweight === "Stone"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*6350.293;
        this.kilogram = d*6.350293;
        this.milligram = d*6350293;
        this.microgram = d*6.350293e+9;
        this.stones = d*1;
        this.pounds = d*14;
        this.ounches = d*224;
        this.imperialton = d*0.00625;
        this.tonne = d*0.006350293;
      }
      else if(this.convertweight === "Pound"){
        var d = this.number1;
        d = parseFloat(d);
        this.gram = d*453.5924;
        this.kilogram = d*0.4535924;
        this.milligram = d*453592.4;
        this.microgram = d*4.535924e+8;
        this.stones = d*0.07142857;
        this.pounds = d*1;
        this.ounches = d*16;
        this.imperialton = d*0.000446429;
        this.tonne = d*0.0004535924;
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
