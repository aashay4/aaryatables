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
          <a href="/">Home</a> &rsaquo; gst calculator<hr>
      <h1 class="w3-text-teal"><b>gst calculator</b></h1>
      <p>Calculating GST for various payments might be a headache. To resolve the issue, we bring this GST calculator for professionals.</p>
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
      <label for="Text1" class="col-sm-3 col-form-label">Initial amount</label>
      <div class="input-group col-sm-9">
      <span class="input-group-text" id="cur1"></span>
      <input v-model="Text1" type="text" class="form-control">
      </div>
      </div>
      <div class="form-group row">
      <label for="Text2" class="col-sm-3 col-form-label">GST Rate</label>
      <div class="input-group col-sm-9">
      <input v-model="Text2" name="Text2" type="text" class="form-control" value="10">
      <span class="input-group-text">%</span>
      </div>
      </div>
      <div class="form-group row">
      <label for="" class="col-sm-3 col-form-label">&nbsp;</label>
      <div class="input-group col-sm-9">
      <button type="button" title="Add GST" class="btn btn-success mr-2" @click="addgst()"><span>+</span> Add GST</button>
      <button type="button" title="Subtract GST" class="btn btn-secondary" @click="removegst()"><span>-</span> Remove GST</button>
      </div>
      </div>
      <div class="form-group row">
      <label for="Text5" class="col-sm-3 col-form-label">Net amount</label>
      <div class="input-group col-sm-9">
      <input v-model="Text5" type="text" class="form-control" readonly>
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
              <span class="w3-large"><a class="removelink" href="/vat-calculator"> Vat calculator</a></span><br>
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
      title: 'gst tax calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'GST calculator online.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/gst-calculator'}
    ]
    }
    },
  data(){
    return {
      Text1: '',
      Text2: '',
      verdict: 0,
      Text5: '',
      Text6: '',
      Text7: ''
    }
  },
  methods: {
    reset(){
    },
    plus(){
      this.verdict = "0";
    },
    minus(){
      this.verdict = "1";
    },
    addgst(){
var amount = this.Text1;
if( amount=='' ) amount='0';
amount = parseFloat(amount);
var gst = this.Text2;
if( gst=='' ) gst='0';
gst = parseFloat(gst);
   var net_amount = amount;
   var gst_amount = amount*gst/100;
   var gross_amount = parseFloat(net_amount)+parseFloat(gst_amount);
net_amount 	= net_amount.toFixed(2);
gst_amount 	= gst_amount.toFixed(2);
gross_amount = gross_amount.toFixed(2);
this.Text5 = net_amount;
this.Text6 = gst_amount;
this.Text7 = gross_amount;

    },
    removegst(){
      var amount = this.Text1;
      if( amount=='' ) amount='0';
      amount = parseFloat(amount);
      var gst = this.Text2;
      if( gst=='' ) gst='0';
      gst = parseFloat(gst);

         var gross_amount = amount;
         var net_amount = 100*amount/(100.0+parseFloat(gst));
         var gst_amount = parseFloat(gross_amount)-parseFloat(net_amount);
         net_amount 	= net_amount.toFixed(2);
         gst_amount 	= gst_amount.toFixed(2);
         gross_amount = gross_amount.toFixed(2);
         this.Text5 = net_amount;
         this.Text6 = gst_amount;
         this.Text7 = gross_amount;
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
/*.btn b, .btn b2 { font-size:large; }*/
#standoop12 { font-weight:bold; margin-top:10px; }
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
