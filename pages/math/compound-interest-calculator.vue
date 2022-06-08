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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Compound Interest Calculator<hr>
      <h1 class="w3-text-teal"><b>Compound Interest Calculator</b></h1>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
        <form id="formnumber1" name="formnumber1" autocomplete="off">
  <div class="form-group">
  <label for="Text1">Enter Value</label>
  <div class="input-group">
  <input type="number" min="0" step="any" v-model="Text1" class="form-control" autofocus>
  </div>
  </div>
  <div class="form-group">
  <label for="Text2">Enter Annual interest rate %</label>
  <div class="input-group">
  <input type="number" step="any" v-model="Text2" class="form-control">
  <div class="input-group-append">
  <span class="input-group-text">%</span>
  </div>
  <div class="input-group-append ml-1">
  <select v-model="Select2" class="form-control">
  <option value="0">compounded monthly</option>
  <option value="1">compounded quarterly</option>
  <option value="2">compounded yearly</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group">
  <label for="Text4">Time duration</label>
  <div class="input-group">
  <input type="number" min="1" step="any" v-model="Text4" class="form-control">
  <div class="input-group-append ml-1">
  <select v-model="Select4" name="Select4" class="form-control">
  <option value="0">Days</option>
  <option value="1">Weeks</option>
  <option value="2">Months</option>
  <option value="3">Quarters</option>
  <option value="4">Years</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group">
  <label for="Text3">Any other payments (optional)</label>
  <div class="input-group">
  <input type="number" step="any" v-model="Text3" class="form-control">
  <div class="input-group-append ml-1">
  <select v-model="Select3" class="form-control">

  <option value="0">monthly</option>
  <option value="1">quarterly</option>
  <option value="2">yearly</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group mb-3">
  <label for="addpay-start" class="row ml-0">Compounding period</label>
  <div class="btn-group btn-group-toggle row ml-0" data-toggle="buttons">
  <label>
  <input type="radio" id="start" value="start" v-model="addpaydiv" checked> start
  </label>
  <label>
  <input type="radio" id="end" value="end" v-model="addpaydiv"> end
  </label>
  </div>
  </div>
  <div class="form-group mt-4">
  <button type="button" @click="calculate()" class="btn btn-success"><span>=</span> Calculate</button>
  <button type="button" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
  </div>
  <div class="form-group">
  <label>Future value</label>
  <div class="input-group">
  <input type="text" v-model="Text7" class="form-control" readonly>
  </div>
  </div>
  <div class="form-group">
  <label>Total deposits amount</label>
  <div class="input-group">
  <input type="text" v-model="Text5" class="form-control" readonly>
  </div>
  </div>
  <div class="form-group">
  <label>Total interest amount</label>
  <div class="input-group">
  <input type="text" v-model="Text6" class="form-control" readonly>
  </div>
  </div>
  <div class="form-group">
  <label>Total yield</label>
  <div class="input-group">
  <input type="text" v-model="Text8" class="form-control" readonly>
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
              <span class="w3-large"><a class="removelink" href="/math/addition-table"> Addition Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/percentage-calculator"> Percentage Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/division-calculator"> Division Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/fractions-calculator"> Fractions Calculator</a></span><br>
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
      title: 'Compound interest calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'compound interest calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/compound-interest-calculator'}
    ]
    }
    },
  data(){
    return {
      Text8: '',
      Text7: '',
      Text6: '',
      Text1: '',
      Text5: '',
      Text2: '',
      input: '',
      Select2: 2,
      Text3: '',
      Select3: 2,
      Text4: '',
      Select4: 4,
      addpaydiv: 'start'
    }
  },
  methods: {
    reset(){
      this.Text8 = "";
      this.Text7 = "";
      this.Text6 = "";
      this.Text1 = "";
      this.Text5 = "";
      this.Text2 = "";
      this.input = "";
      this.Select2 = 2;
      this.Text3 = "";
      this.Select3 = 2;
      this.Text4 = "";
      this.Select4 = 4;
      this.addpaydiv = "start";
    },
    calculate(){
      var x0 = this.Text1;
      var rate = this.Text2;
      var i1 = this.Select2;
      var x1 = this.Text3;
      var i2 = this.Select3;
      var period = this.Text4;
      var i3 = this.Select4;
      var iaddpay = this.addpaydiv;
      if(iaddpay === "start"){
        iaddpay = 0;
      }
      if(iaddpay === "end"){
        iaddpay = 1;
      }
      if( x0=='' ) x0='1000';
      if( x1=='' ) x1='0';
      if( rate=='' ) rate='4';
      if( period=='' ) period='10';

      var x0 = parseFloat(x0);
      var x1 = parseFloat(x1);
      if(x0==0) x0=x1;
      rate = parseFloat(rate);
      period = parseFloat(period);
      i1 = parseInt(i1);
      i2 = parseInt(i2);
      i3 = parseInt(i3);
      if( x1==0 ) i2=2;

      //var rlook=[52,12,4,1];
      var rlook=[12,4,1];
      var rlook4=[365,52,12,4,1];
      var n1 = rlook[i1];
      var n2 = rlook[i2];
      var n3 = rlook4[i3];
      period /= n3; // convert to years
      var period1 = period*n1;
      var period2 = period*n2;
      rate /= n1;
      var ratio=n2/n1;
      var maxperiod = period1>period2?period1:period2;
      var f1=12/n1;
      var f2=12/n2;
      if( (f1>=f2) && ((f1/f2)==Math.round(f1/f2)) ) { f1/=f2; f2=1; }
      else if( (f2>f1) && ((f2/f1)==Math.round(f2/f1)) ) { f2/=f1; f1=1; }
      var v = this.CompoundCalc(x0,rate,x1,f1,f2,maxperiod,iaddpay);
      var y2=v[v.length-1];
      var y0 = x0+x1*period2;
      var p = y2-y0;
      var total;
      if( y0>0 )
         total = y2/y0*100.0-100.0;
      else
         total = 0;

      y0 = y0.toFixed(2);
      p  = (Math.round(100*p)/100).toFixed(2);
      y2 = y2.toFixed(2);
      total = (Math.round(100*total)/100).toFixed(2);

      var depamount=parseFloat(y0);
      var intamount=parseFloat(p);

      y0 = this.numberWithCommas(y0);
      p  = this.numberWithCommas(p);
      y2 = this.numberWithCommas(y2);
      total = this.numberWithCommas(total);
      this.Text5 = y0;
      this.Text6 = p;
      this.Text7 = y2;
      this.Text8 = total;
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
