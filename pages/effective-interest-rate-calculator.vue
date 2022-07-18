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
          <a href="/">Home</a> &rsaquo; Calculate effective interest rate<hr>
      <h1 class="w3-text-teal"><b>Effective interest rate calculator</b></h1>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>

      <form id="formnumber1" autocomplete="off">
<table>
<tr>
<td>Interest rate per year:</td>
<td class="math"><input v-model="Text1" type="number" min="0" max="100" step="0.25" class="intext" style="width:120px" value="4"> %</td>
<td colspan="2">per year</td>
</tr>
<tr>
<td>Compounding Interest period:</td>
<td><select v-model="Select1" @change="changed()">
<option>Days</option>
<option>Weeks</option>
<option>Months</option>
<option>Quarters</option>
</select></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>Compounding periods Duration:</td>
<td class="math"><input v-model="Text2" type="number" min="1" max="365" class="intext" style="width:120px" value="12" onchange="OnPeriodNumChange()"></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td>&nbsp;</td>
<td colspan="3">
<input type="button" value="Calculate" style="font-size:medium; width:120px; padding:5px" @click="calculate()">
<input type="button" value="reset" @click="reset()" style="font-size:medium; width:120px; padding:5px">
</td>
</tr>
<tr>
<td>Effective period interest rate:</td>
<td class="math"><input v-model="Text6" name="Text6" type="text" class="outtext" style="width:120px" readonly="readonly">%</td>
<td colspan="2" id="td1" style="width:70px">per month</td>
</tr>
<tr>
<td>Effective annual interest rate:</td>
<td class="math"><input v-model="Text7" type="text" class="outtext" style="width:120px" readonly="readonly">%</td>
<td colspan="2">per year</td>
</tr>
</table>
</form>

</div><br>
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
              <span class="w3-large"><a class="removelink" href="/simple-interest-calculator"> Simple interest calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/compound-interest-calculator"> Compound interest calculator</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

  <!-- Labels / tags -->


<!-- END Introduction Menu -->
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
      title: 'Effective Interest Rate Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculator effective interest rate with this online tool.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/effective-interest-rate-calculator'}
    ]
    }
    },
  data(){
    return {
      Text1: '',
      Select1: 'Months',
      Text2: 12,
      verdict: 0,
      Text5: '',
      Text6: '',
      Text7: ''
    }
  },
  methods: {
    reset(){
      this.Text1 = "";
      this.Select1 = "Months";
      this.Text2 = 12;
      this.verdict = 0;
      this.Text5 = "";
      this.Text6 = "";
      this.Text7 = "";
    },
    changed(){
      if(this.Select1 === "Days"){
        this.Text2 = 365;
      }
      if(this.Select1 === "Weeks"){
        this.Text2 = 52;
      }
      if(this.Select1 === "Months"){
        this.Text2 = 12;
      }
      if(this.Select1 === "Quarters"){
        this.Text2 = 4;
      }
    },
calculate(){
  var i = this.Text1;
var n = this.Text2;
i = parseFloat(i)/100;
var imonth = i/n*100;
var iyear  = (Math.pow((1+i/n),n)-1)*100;
this.Text6 = imonth.toFixed(3);
this.Text7 = iyear.toFixed(3);
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
#formnumber1 { background:#a7c9b8; padding:20px; }
#abcdiv, #tabless1245 { max-width:100px; }
#standoop { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#standoop1, #intothelog { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#formnumber1 button i { vertical-align: bottom; }
#standoop444, #standoop44433 span { vertical-align: bottom; }
/*.btn b, .btn b2 { font-size:large; }*/
#standoop12 { font-weight:bold; margin-top:10px; }
#standoop444, #standoop44433, #boat563, #boat5634 { display:none; }
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
