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
          <a href="/">Home</a> &rsaquo; <a href="/length-converter">Length</a> &rsaquo; Meters to Feet+Inches<hr>
      <h1 class="w3-text-teal"><b>Meter to Feet and Inches</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <form id="designstyle" autocomplete="off">
        <label class="btn btn-secondary active">
<input type="radio" name="options" id="option1" @click="meters()" checked> Meters
</label>
<label class="btn btn-secondary">
<input type="radio" name="options" id="option2" @click="cms()"> Meters+Centimeters
</label>

      <div class="form-row">
      <div class="form-group col">
      <label for="m">Meters</label>
      <div class="input-group">
      <input type="number" min="0" step="any" v-model="m" class="form-control" autofocus>
      <div class="input-group-append">
      <span class="input-group-text">m</span>
      </div>
      </div>
      </div>
      <div v-if="showcm" class="form-group col">
      <label for="m">Centimeters</label>
      <div class="input-group">
      <input type="number" min="0" step="any" v-model="cm" class="form-control" autofocus>
      <div class="input-group-append">
      <span class="input-group-text">cm</span>
      </div>
      </div>
      </div>
      </div>
      <div class="form-group">
      <button type="button" class="btn btn-success" @click="calculate()">=> Convert</button>
      <button type="button" @click="reset()" class="btn btn-secondary"> Reset</button>
      </div>
      <div class="form-row">
      <div class="form-group col">
      <label for="ft">Feet</label>
      <div class="input-group">
      <input type="text" v-model="ft" class="form-control" readonly>
      <div class="input-group-append">
      <span class="input-group-text">ft</span>
      </div>
      </div>
      </div>
      <div class="form-group col">
      <label for="inch1">Inches</label>
      <div class="input-group">
      <input type="text" v-model="inch1" class="form-control" readonly>
      <div class="input-group-append">
      <span class="input-group-text">in</span>
      </div>
      </div>
      </div>
      </div>
      <div class="form-group">
      <label for="inch2">Inches decimal result</label>
      <div class="input-group">
      <input type="text" v-model="inch2" class="form-control" readonly>
      <div class="input-group-append">
      <span class="input-group-text">in</span>
      </div>
      </div>
      </div>
      <div class="form-group">
      <label for="inch3">Inches fractional result</label>
      <div class="input-group">
      <input type="text" v-model="inch3" class="form-control" readonly>
      <div class="input-group-append">
      <span class="input-group-text">in</span>
      </div>
      </div>
      </div>
      <div class="form-group">
      <label for="TA">Calculation</label>
      <textarea v-model="ta" rows="4" class="form-control" readonly></textarea>
      </div>
      </form>

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
        <h1 class=""><b>Other tools tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/length-converter/meters-to-feet"> Meters to Feet</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/length-converter/meters-to-inches"> Meters to inches</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/length-converter/meters-to-km"> Meters to kilometers</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/length-converter/meters-to-miles"> Meters to Miles</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/length-converter/meters-to-mm"> Meters to Mm</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/length-converter/meters-to-yards"> Meters to Yards</a></span><br>
            </li>
            </ul>
      </div>
    </div>
  </div>

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
  return {
    title: 'Translate Meters to feet and inches.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: 'Meters to feet+inches.'}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/weight-converter/meters-to-feet-inches'}
  ]
  }
  },
  data(){
    return {
      m: null,
      inch2: '',
      inch3: '',
      cm: null,
      ft: null,
      inch1: null,
      answer: '',
      cm1: '',
      m2: '',
      cm2: '',
      ta: '',
      showcm: false
    }
  },
  methods: {
    meters(){
      this.showcm = false;
    },
    cms(){
      this.showcm = true;
    },
    digits_after_period(x)
{
  var f = x.toString();
  var i = f.indexOf('.');
  var len = f.length-i-1;
  return len;
},
    dec2frac(x) {
      var y = parseFloat(x);
      y = Math.round(y*64)/64;
      var absy=Math.abs(y);
      var yy=Math.floor(absy);
      var frac=this.roundresult(absy-yy);
      //if( x2<0 ) sign = sign2 = '-';
      var d = this.digits_after_period(absy);
      var den = Math.round(Math.pow(10,d));
      var num = Math.round(frac*den);
      var len=num.toString().length;
      var f=false;
      if( len>8 ) f=true;
      var gcd2 = function(a, b, f) {
     if( f )
     {
         if ( b<=1 )
             return a;
       }
       else
     {
         if ( !b )
             return a;
       }
       return gcd2(b, a % b, f);
    };

      var g = gcd2(num,den,f);
      var num2 = Math.round(num/g);
      var den2 = Math.round(den/g);
      y = yy;
      if( num2!=0 ) y+=" "+this.getFracString(num2,den2);
      return(y);
   },
   getFracString(num,den)
   {
      var s="";
      num=num.toString();
      den=den.toString();
      var ulook=["\u2070","\u00B9","\u00B2","\u00B3","\u2074","\u2075","\u2076","\u2077","\u2078","\u2079"];
      var dlook=["\u2080","\u2081","\u2082","\u2083","\u2084","\u2085","\u2086","\u2087","\u2088","\u2089"];
      for(var i=0; i<num.length; i++)
         s+=ulook[num[i]];
      s+="/";
      for(var i=0; i<den.length; i++)
         s+=dlook[den[i]];
      return s;
   },
    calculate(){
      var m = this.m;
      var cm = this.cm;
      if( m==null ) m="0";
      if( cm==null ) cm="0";
      m = parseFloat(m);
      cm = parseFloat(cm);
      var cm2 = 100*m+cm;
      var inch = this.roundresult(cm2/2.54);
      var ft2 = Math.floor(inch/12);
      var inch2 = this.roundresult(inch-ft2*12);
      var inch3 = this.dec2frac(inch);
      var txt="length = ";
      if( m!=0 )
         txt+="100\u00D7"+m+"m/2.54 + ";
      txt+=cm+"cm/2.54 = "+inch+"in\n";
      txt+="feet = floor("+inch+"in/12) = "+ft2+"ft\n";
      txt+="inch = "+inch+"in - 12\u00D7"+ft2+"ft = "+inch2+"in\n";
      txt+="length = "+ft2+"ft+"+inch2+"in";
      this.ft = ft2;
      this.inch1 = inch2;
      this.inch2 = inch;
      this.inch3 = inch3;
      this.ta = txt;

        },
    str2num(s)
    {
       s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
       if( s=='' ) return 0;
       return Function('"use strict";return ('+s+')')();
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
    },
    reset(){
      this.m = null;
      this.inch2 = "";
      this.inch3 = "";
      this.cm = null;
      this.ft = null;
      this.inch1 = null;
      this.answer = "";
      this.cm1 = "";
      this.m2 = "";
      this.cm2 = "";
      this.ta = "";
      this.showcm = false;
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
#designstyle { background:#a7c9b8; padding:20px; }
#designstyle button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designstyle { padding:10px; }
}

</style>
