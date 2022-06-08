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
          <a href="/">Home</a> &rsaquo; <a href="/electronics">Electronics</a> &rsaquo; Watts / Volts / Amps / Ohms calculator<hr>
      <h1 class="w3-text-teal"><b>Amps / Ohms / Watts / Volts calculator</b></h1>
        <p>An online calculator for Amps, Ohms, watts and volts.</p>
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
  <label for="r" class="col-sm-3 col-form-label">Resistance (<i>R</i>)</label>
  <div class="input-group col-sm-9">
  <input type="text" v-model="r" autofocus class="form-control">

  <select v-model="cr" class="form-control">
  <option value="0">ohms (&Omega;)</option>
  <option value="1">kiloohms (k&Omega;)</option>
  <option value="2">megaohms (M&Omega;)</option>
  </select>
  </div>
  </div>
  <div class="form-group row">
  <label for="i" class="col-sm-3 col-form-label">Current (<i>I</i>)</label>
  <div class="input-group col-sm-9">
  <input type="text" v-model="i" class="form-control">
  <select v-model="ci" class="form-control">
  <option value="0">microamps (&mu;A)</option>
  <option value="1">milliamps (mA)</option>
  <option value="2">amps (A)</option>
  <option value="3">kiloamps (kA)</option>
  <option value="4">megaamps (MA)</option>
  </select>
  </div>
  </div>
  <div class="form-group row">
  <label for="v" class="col-sm-3 col-form-label">Voltage (<i>V</i>)</label>
  <div class="input-group col-sm-9">
  <input type="text" v-model="v" class="form-control">
  <select v-model="cv" class="form-control">
  <option value="0">microvolts (&mu;V)</option>
  <option value="1">millivolts (mV)</option>
  <option value="2">volts (V)</option>
  <option value="3">kilovolts (kV)</option>
  <option value="4">megavolts (MV)</option>
  </select>
  </div>
  </div>
  <div class="form-group row">
  <label for="p" class="col-sm-3 col-form-label">Power (<i>P</i>)</label>
  <div class="input-group col-sm-9">
  <input type="text" v-model="p" class="form-control">
  <select v-model="cp" class="form-control">
  <option value="0">microwatts (&mu;W)</option>
  <option value="1">milliwatts (mW)</option>
  <option value="2">watts (W)</option>
  <option value="3">kilowatts (kW)</option>
  <option value="4">megawatts (MW)</option>
  </select>
  </div>
  </div>
  <div class="form-group row">
  <label class="col-sm-3 col-form-label">&nbsp;</label>
  <div class="col-sm-9">
  <button type="button" title="Calculate" class="btn btn-primary" @click="calculate()"><span>=</span> Calculate</button>
  <button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>&times;</span> Reset</button>
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
      title: 'Amps / Ohms / Watts / Volts calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Watts / Volts / Amps / Ohms calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/watts-volts-amps-ohms-calculator'}
    ]
    }
    },
  data(){
    return {
      cr: 0,
      r: '',
      i: '',
      ci: 2,
      v: '',
      cv: 2,
      p: '',
      cp: 2
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
      var fr = Math.pow(10,3*this.cr);
  		var fi = Math.pow(10,3*this.ci);
  		var fv = Math.pow(10,3*this.cv);
  		var fp = Math.pow(10,3*this.cp);
      var relem=this.r;
var ielem=this.i;
var velem=this.v;
var pelem=this.p;

  		var r = fr*this.str2num(relem);
  		var i = fi*this.str2num(ielem);
  		var v = fv*this.str2num(velem);
  		var p = fp*this.str2num(pelem);
  		if( r!=0 && v!=0 ) {i=v/r; p=v*i;}
  		else if( r!=0 && i!=0 ) {v=i*r; p=v*i;}
  		else if( r!=0 && p!=0 ) {v=Math.sqrt(p*r); i=p/v;}
  		else if( i!=0 && v!=0 ) {r=v/i; p=v*i;}
  		else if( i!=0 && p!=0 ) {v=p/i; r=v/i;}
  		else if( v!=0 && p!=0 ) {i=p/v; r=v/i;}
  		r /= fr;
  		i /= fi;
  		v /= fv;
  		p /= fp;
      p = p/1000000;
  		this.r = this.roundnum(r,8);
  		this.i = this.roundnum(i,8);
  		this.v = this.roundnum(v,8);
  		this.p = this.roundnum(p,8);
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
