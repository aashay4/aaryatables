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
          <a href="/">Home</a> &rsaquo; Mortgage calculator<hr>
      <h1 class="w3-text-teal"><b>Mortgage calculator</b></h1>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
        <form id="formnumber1">
<div class="mb-3">
<label for="calcsel1" class="form-label">Select one option:</label>
<div>
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simpleclicked()" checked> Monthly payment
  </label>
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simple()"> Loan Amount
  </label>
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simple1()"> Loan Term
  </label>
</div>
</div>
<div class="mb-3 divs" v-if="homeprice1">
<label for="hpin" class="form-label">Home price</label>
<div class="input-group">
<span class="input-group-text cur">$</span>
<input type="number" min="0" step="1" v-model="hpin" name="hpin" value="400000" placeholder="400000" class="form-control" oninput="OnHomePrice()">

</div>
</div>
<div class="mb-3 divs" v-if="downpayment1">
<label for="dpin" class="form-label">Down payment</label>
<div class="row g-2">
<div class="col-sm-8">
<div class="input-group">
<span class="input-group-text cur">$</span>
<input type="number" min="0" step="1" v-model="dpin" name="dpin" value="100000" placeholder="100000" class="form-control" oninput="OnDP()">
</div>
</div>
<div class="col-sm-4">
<div class="input-group">
<input type="number" min="0" step="1" v-model="dpperin" name="dpperin" value="25" placeholder="25" class="form-control" oninput="OnDPPercent()">
<span class="input-group-text">%</span>
</div>
</div>
</div>
</div>
<div class="mb-3 divs" v-if="secondfclicked">
<label for="lain" class="form-label">Loan amount</label>
<div class="input-group">
<span class="input-group-text cur">$</span>
<input type="number" min="0" step="1" v-model="lain" value="300000" placeholder="300000" class="form-control">
</div>
</div>
<div class="mb-3 divs" v-if="monthlypayment">
<label for="mpin" class="form-label">Monthly payment</label>
<div class="input-group">
<span class="input-group-text cur">$</span>
<input type="number" v-model="mpin" name="mpin" class="form-control" value="2000" placeholder="2000">
</div>
</div>
<div class="mb-3 divs">
<label for="irin" class="form-label">Annual interest rate (%)</label>
<div class="input-group">
<input type="number" min="0" step=".01" v-model="irin" name="irin" class="form-control" value="5.0" placeholder="5.0">
<span class="input-group-text">%</span>
</div>
</div>
<div class="mb-3 divs" v-if="loanterm">
<label for="ltin" class="form-label">Loan term</label>
<div class="input-group">
<input type="number" min="1" step="1" v-model="ltin" name="ltin" class="form-control" value="20" placeholder="20">

<select v-model="ltselin" class="form-select" style="max-width:160px;">
<option value="0">Years</option>
<option value="1">Months</option>
</select>
</div>
</div>
<div class="mb-3 mt-4 divs">

<button type="button" @click="calculate()" class="btn btn-success"><span>=</span> Calculate</button>
<button type="reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="mb-3 divs" v-if="firstclicked">
<label class="form-label">Monthly payment</label>
<div class="input-group input-group-lg">
<span class="input-group-text fw-semibold cur">$</span>
<input type="text" v-model="mpout" class="form-control fw-semibold" readonly>
</div>
</div>
<div class="mb-3 divs" v-if="secondcliced">
<label class="form-label">Loan amount</label>
<div class="input-group input-group-lg">
<span class="input-group-text fw-semibold cur">$</span>
<input type="text" v-model="laout" class="form-control fw-semibold" readonly>
</div>
</div>
<div class="mb-3 divs" v-if="thirdcliced">
<label class="form-label">Loan term in years</label>
<div class="input-group input-group-lg">
<input type="text" v-model="ltout" class="form-control fw-semibold" readonly>
<span class="input-group-text">Years</span>
</div>
</div>
<div class="mb-3 divs">
<label class="form-label">Loan term in months</label>
<div class="input-group input-group-lg">
<input type="text" v-model="ltmout" class="form-control fw-semibold" readonly>
<span class="input-group-text">Months</span>
</div>
</div>
<div class="mb-3 divs" v-if="loadtovalue">
<label class="form-label">Loan to value ratio</label>
<div class="input-group input-group-lg">
<input type="text" v-model="ltvout" class="form-control fw-semibold" readonly>
<span class="input-group-text fw-semibold">%</span>
</div>
</div>
<div class="mb-3 divs">
<label class="form-label">Total payments</label>
<div class="input-group input-group-lg">
<span class="input-group-text fw-semibold cur">$</span>
<input type="text" v-model="tpout" class="form-control fw-semibold" readonly>
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
              <span class="w3-large"><a class="removelink" href="/interest-calculator"> Simple interest calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/compound-interest-calculator"> Compound interest calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/effective-interest-rate-calculator"> Effective interest rate calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/gst-calculator"> Gst calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/vat-calculator"> vat calculator</a></span><br>
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
      title: 'mortgage calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Mortgage calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/mortgage-calculator'}
    ]
    }
    },
  data(){
    return {
      thirdcliced: false,
      loadtovalue: true,
      firstclicked: true,
      homeprice1: true,
      downpayment1: true,
      secondcliced: false,
      monthlypayment: '',
      secondfclicked: true,
radiotype: '0',
loanterm: true,
hpin: '',
dpin: '',
dpperin: '',
lain: '',
mpin: '',
irin: '',
ltin: '',
ltselin: '0',
mpout: '',
laout: '',
ltout: '',
ltmout: '',
ltvout: '',
tpout: '',
piechart: '',
columnchart: ''
    }
  },
  methods: {
    simpleclicked(){
      this.radiotype = "0";
      this.loanterm = true;
      this.monthlypayment = false;
      this.secondcliced = false;
      this.thirdcliced = false;
      this.homeprice1 = true;
      this.downpayment1 = true;
      this.secondfclicked = true;
      this.firstclicked = true;
      this.loadtovalue = true;
    },
simple(){
  this.radiotype = "1";
  this.loanterm = true;
  this.firstclicked = false;
  this.monthlypayment = true;
  this.secondcliced = true;
  this.thirdcliced = false;
  this.homeprice1 = false;
  this.downpayment1 = false;
  this.loadtovalue = false;
  this.secondfclicked = false;
},
simple1(){
    this.secondfclicked = true;
  this.firstclicked = false;
  this.loadtovalue = true;
  this.radiotype = "2";
  this.downpayment1 = true;
  this.homeprice1 = true;
  this.loanterm = false;
  this.monthlypayment = true;
  this.secondcliced = false;
  this.thirdcliced = true;
},
    reset(){
      this.thirdcliced = false;
      this.loadtovalue = true;
      this.firstclicked = true;
      this.homeprice1 = true;
      this.downpayment1 = true;
      this.secondcliced = false;
      this.monthlypayment = "";
      this.secondfclicked = true;
this.readiotype = "";
this.loanterm = true;
this.hpin = "";
this.dpin = "";
this.dpperin = "";
this.lain = "";
this.mpin = "";
this.irin = "";
this.ltin = "";
this.ltselin = "";
this.mpout = "";
this.laout = "";
this.ltout = "";
this.ltmout = "";
this.ltvout = "";
this.tpout = "";
this.piechart = "";
this.columnchart = "";
    },
    calculate(){
      var hpElem = this.hpin;
var dpElem = this.dpin;
var dpperElem = this.dpperin;
var pvElem = this.lain;
var mpElem = this.mpin;
var rateElem = this.irin;
var nyElem = this.ltin;
var nyselElem = this.ltselin;
var ltvElem = this.ltvout;
var tpElem = this.tpout;
var sharedivElem = this.sharediv;
var cursel=0;
var calcsel=0;
var pamount,intamount;
      var homeprice = hpElem;
var downpay = dpElem;
var pv = pvElem;
var mp = mpElem;
var rate = rateElem;
var ny = nyElem;
var nsel = nyselElem;
if( pv=='' ) pv='300000';
if( mp=='' ) mp='2000';
if( rate=='' ) rate='5';
if( ny=='' ) ny='20';
pv = parseFloat(pv);
mp = parseFloat(mp);
rate = parseFloat(rate);
ny = parseFloat(ny);
if( nsel==0 ) ny*=12;
var y;
if( this.radiotype=="0" ) {
  alert("tis")
   y=this.PayCalc(pv,rate,ny);
   this.mpout=this.numberWithCommas(y.toFixed(0));
   this.ltmout=ny;
   pamount=pv; intamount=y*ny-pv;
}
else if( this.radiotype=="1" ) {
   y=this.PVCalc(mp,rate,ny);
   this.laout=this.numberWithCommas(y.toFixed(0));
   this.ltmout=ny;
   pamount=y; intamount=mp*ny-y;
}
else {
   y=this.TermCalc(pv,mp,rate);
   if( y<=0 ) {
      //y="monthly payment < interest amount";
      this.ltout="Infinity";
    //  mpElem.style.backgroundColor = "#ffe0e0";
      return;
   }
   //mpElem.style.backgroundColor = "#ffffff";
   pamount=pv; intamount=y*mp-pv;
   this.ltout=(y/12).toFixed(1);
   this.ltmout=Math.ceil(y);
}
this.ltvout=(100.0*(pamount/homeprice)).toFixed(0);
this.tpout=this.numberWithCommas((pamount+intamount).toFixed(0));
//google.charts.load('current', {'packages':['corechart']});
//google.charts.setOnLoadCallback(drawChart);
    },
    PayCalc(p,r,n)
   {
      r=r/1200.0;
      //n=n*12;
      var x=Math.pow((1.0+r),n);
      var a=p*r*x/(x-1.0);
      return a;
   },
   PVCalc(a,r,n)
   {
      r=r/1200.0;
      //n=n*12;
      var x=Math.pow((1.0+r),n);
      var p=a*(x-1)/(r*x);
      return p;
   },
   TermCalc(p,a,r)
   {
      r=r/1200.0;
      var x=a/(a-p*r);
      if(x<0) return(-1);
      var n=Math.log(x)/Math.log(1.0+r);
      //return (n/12);
      return n;
   },
  numberWithCommas(x)
 {
    return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
 },
    CompoundCalc(PV,i,dV,n1,n2,n,iaddpay)
       {
          //FV = PV*Math.pow((1+i/100),n);
          var f;
          //var v=[];
          var prevv=PV;
          var v=[prevv];
          if( iaddpay==0 ) v[0]=prevv+dV;
          //for(var k=0; k<n; k++)
          for(var k=1; k<=n; k++)
          {
             v[k]=prevv;
             f=(k+1)/n2;
             if( f==Math.round(f) && iaddpay==0 )
                v[k]+=dV;
             f=(k+1)/n1;
             if( f==Math.round(f) )
                v[k]=v[k]*(1+i/100.0);
             f=(k+1)/n2;
             if( f==Math.round(f) && iaddpay==1 )
                v[k]+=dV;
             prevv=v[k];
          }
          return v;
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
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
