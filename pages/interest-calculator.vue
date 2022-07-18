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
          <a href="/">Home</a> &rsaquo; Simple interest calculator<hr>
      <h1 class="w3-text-teal"><b>Simple interest calculator</b></h1>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>
      <form id="formnumber1" autocomplete="off">
      <div class="form-group row">
      <label for="Text1" class="col-sm-3 col-form-label">Principle amount:</label>
      <div class="input-group col-sm-9">
      <span class="input-group-text" id="cur1"></span>
      <input v-model="Text1" type="text" class="form-control">
      </div>
      </div>
      <div class="form-group row">
      <label for="Text2" class="col-sm-3 col-form-label">Yearly interest:</label>
      <div class="input-group col-sm-9">
      <input v-model="Text2" name="Text2" type="text" class="form-control" value="10">
      <span class="input-group-text">%</span>
      </div>
      </div>
      <div class="form-group row">
      <label for="ltin" class="col-sm-3 col-form-label">Loan term</label>
      <div class="input-group col-sm-9">
      <input type="number" min="1" step="1" v-model="Text3" class="form-control" placeholder="20">

      <select v-model="Select2" class="form-select" style="max-width:160px;">
      <option value="0">Days</option>
      <option value="1">Weeks</option>
      <option value="2">Months</option>
      <option value="3">Quarters</option>
      <option value="4">Years</option>
      </select>
      </div>
      </div>
      <div class="form-group row">
      <label for="" class="col-sm-3 col-form-label">&nbsp;</label>
      <div class="input-group col-sm-9">
      <button type="button" title="Calculate" class="btn btn-success mr-2" @click="calculate()"><span>=></span> Calculate</button>
      <button type="button" title="Reset" class="btn btn-secondary" @click="reset()"><span>X</span> Reset</button>
      </div>
      </div>
      <div class="form-group row">
      <label for="Text5" class="col-sm-3 col-form-label">GST amount</label>
      <div class="input-group col-sm-9">
      <input v-model="Text6" name="Text6" type="text" class="form-control" readonly>
      </div>
      </div>
      <div class="form-group row">
      <label for="Text5" class="col-sm-3 col-form-label">Gross amount</label>
      <div class="input-group col-sm-9">
      <input v-model="Text7" name="Text7" type="text" class="form-control" readonly>
      </div>
      </div>
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
              <span class="w3-large"><a class="removelink" href="/mortgage-calculator"> Mortgage calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/effective-interest-rate-calculator"> Effective interest rate calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/vat-calculator"> VAT calculator</a></span><br>
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
      title: 'Simple interest counter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Simple interest calculator online.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/interest-calculator'}
    ]
    }
    },
  data(){
    return {
      Select2: '2',
      Text1: '',
      Text2: '',
      verdict: 0,
      Text5: '',
      Text6: '',
      Text7: '',
      Text3: 20
    }
  },
  methods: {
    reset(){
      this.Select2 = "2";
      this.Text1 = "";
      this.Text2 = "";
      this.verdict = 0;
      this.Text5 = "";
      this.Text6 = "";
      this.Text7 = "";
      this.Text3 = 20;
    },
    numberWithCommas(x)
   {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
   },
    calculate(){
      var x0 = this.Text1;
var rate = this.Text2;
var period = this.Text3;
var i = this.Select2;
i = parseFloat(i);
var ilook = [365,52,12,4,1];
rate /= ilook[i];
if( x0=='' ) x0='0';
x0 = parseFloat(x0);
var Is = x0*rate*period/100;
var y = x0+Is;
Is = Is.toFixed(2);
y  = y.toFixed(2);
Is = this.numberWithCommas(Is);
y = this.numberWithCommas(y);
this.Text6 = Is;
this.Text7 = y;
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
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#formnumber1 button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
