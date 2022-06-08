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
          <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Voltage divider calculator<hr>
      <h1 class="w3-text-teal"><b>Voltage divider calculator</b></h1>
        <p>Online calculator for voltage division.</p>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
        <form id="designform" name="designform" autocomplete="off">
  <div class="form-group row">
  <label for="vin" class="col-sm-4 col-form-label">Input voltage (V<sub>in</sub>)</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="vin" class="form-control" autofocus>
  <div class="input-group-append">
  <select v-model="vinsel" class="form-control">
  <option value="0">millivolts (mV)</option>
  <option value="1">volts (V)</option>
  <option value="2">kilovolts (kV)</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label for="r1" class="col-sm-4 col-form-label">Resistance (R<sub>1</sub>)</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="r1" class="form-control">
  <div class="input-group-append">
  <select v-model="r1sel" onchange="onselchange(this,0);" class="form-control">
  <option value="0">ohms (&Omega;)</option>
  <option value="1">kiloohms (k&Omega;)</option>
  <option value="2">megaohms (M&Omega;)</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label for="r2" class="col-sm-4 col-form-label">Resistance (R<sub>2</sub>)</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="r2" class="form-control">
  <div class="input-group-append">
  <select v-model="r2sel" onchange="onselchange(this,0);" class="form-control">
  <option value="0">ohms (&Omega;)</option>
  <option value="1">kiloohms (k&Omega;)</option>
  <option value="2">megaohms (M&Omega;)</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label for="vout" class="col-sm-4 col-form-label">Output voltage (V<sub>out</sub>)</label>
  <div class="input-group col-sm-8">
  <input type="number" min="0" step="any" v-model="vout" class="form-control">
  <div class="input-group-append">
  <select v-model="voutsel" class="form-control">
  <option value="0">millivolts (mV)</option>
  <option value="1">volts (V)</option>
  <option value="2">kilovolts (kV)</option>
  </select>
  </div>
  </div>
  </div>
  <div class="form-group row">
  <label class="col-sm-4 col-form-label">&nbsp;</label>
  <div class="input-group col-sm-8">
  <button type="button" class="btn btn-primary mr-1" @click="calculate()"><span>=</span> Answer</button>
  <button type="reset" class="btn btn-secondary" onclick="setfocus()"><span>&times;</span> Reset</button>
  </div>
  </div>
  <div id="caldiv" class="form-group row">
  <label class="col-sm-4 col-form-label">Calculation</label>
  <div class="col-sm-8">
  <div style="height: 100px;" class="form-control" readonly>
{{ cal }}<br>
{{ txt1 }}<br>
{{ txt2 }}
  </div>
  </div>
  </div>
  </form>



</div><br>
    <div class="w3-padding">
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
        <h1 class=""><b>Other tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-ev"> volts to ev</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-joules"> volts to joules</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-amps"> volt sto ampere</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/electronics/volts-to-watts"> Volts to watts</a></span><br>
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
      title: 'Voltage divider calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'AN online calculator for volate devide.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/voltage-divider-calculator'}
    ]
    }
    },
  data(){
    return {
      vinsel: '1',
      vin: '',
      vout: '',
      voutsel: '1',
      r1sel: '0',
      r1: '',
      r2sel: '0',
      r2: '',
      cal: '',
      txt1: '',
      txt2: ''
      }
  },
  methods: {
    reset(){
      this.cr = 0;
      this.r = "";
      this.i = "";
      this.ci = 2;
      this.v = "";
      this.cv = 2;
      this.p = "";
      this.cp = 2;
    },
    str2num(s)
    {
       s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
       if( s=='' ) return 0;
       return Function('"use strict";return ('+s+')')();
    },
    calculate(){
      var vinElem  = this.vin;
var voutElem = this.vout;
var r1Elem = this.r1;
var r2Elem = this.r2;
var vinselElem  = this.vinsel;
var voutselElem = this.voutsel;
var r1selElem = this.r1sel;
var r2selElem = this.r2sel;
var calElem = this.cal;
var caldivElem = this.caldiv;

var vinsel = Math.pow(10,(3*vinselElem-3));
var voutsel = Math.pow(10,(3*voutselElem-3));
var r1sel = Math.pow(10,(3*r1selElem));
var r2sel = Math.pow(10,(3*r2selElem));
var vin = parseFloat(vinElem*vinsel);
var vout = parseFloat(voutElem*voutsel);
var r1 = parseFloat(r1Elem*r1sel);
var r2 = parseFloat(r2Elem*r2sel);
var txt="";
if( vin!=0 && r1!=0 && r2!=0 && vout==0 ) {
   vout = vin*r2/(r1+r2);
   this.vout = this.roundresult(vout);
   this.cal = "Vout = Vin × R2 / (R1 + R2)";
   this.txt1 = "= "+vin+"V × "+r2+"Ω / ("+r1+"Ω+"+r2+"Ω)";
   this.txt2 = "= "+this.vout+"V";
}
else if( vin!=0 && r1!=0 && r2==0 && vout!=0 ) {
   r2 = r1*vout/(vin-vout);
   this.r2 = this.roundresult(r2);
   this.cal = "R2 = R1 × Vout / (Vin - Vout)";
   this.txt1 = "= "+r1+"Ω × "+vout+"V / ("+vin+"V - "+vout+"V)";
   this.txt2 = "= " + this.r2+"Ω";
}
else if( vin!=0 && r1==0 && r2!=0 && vout!=0 ) {
   r1 = r2*(vin-vout)/vout;
   this.r1 = this.roundresult(r1);
   this.cal = "R1 = R2 × (Vin - Vout) / Vout";
   this.txt1 = "= "+r2+"Ω × ("+vin+"V - "+vout+"V) / "+vout+"V"
   this.txt2 = "= "+this.r1+"Ω";
}
else if( vin==0 && r1!=0 && r2!=0 && vout!=0 ) {
   vin = vout*(r1+r2)/r2;
   this.vin = this.roundresult(vin);
   this.cal = "Vin = Vout × (R1 + R2) / R2";
   this.txt1 = "= "+vout+"V × ("+r1+"Ω + "+r2+"Ω) / "+r2+"Ω"
   this.txt2 = "= "+this.vin+"V";
}
else {
   alert("Please enter atleast 3 values!");
   return;
}
//calElem.innerHTML = txt;

    },
    roundresult(x) {
      var y = parseFloat(x);
      y = this.roundnum(y,10);
      return y;
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
#designform {
   padding:15px;
   background:#a7c9b8;
   border:1px solid #eee;
   border-radius:7px;
   max-width:500px;
}
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
   #designform { padding:10px; }
}

</style>
