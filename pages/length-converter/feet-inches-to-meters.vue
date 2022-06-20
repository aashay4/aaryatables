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
          <a href="/">Home</a> &rsaquo; <a href="/length-converter">Length</a> &rsaquo; Feet+Inches to Meter<hr>
      <h1 class="w3-text-teal"><b>Feet+Inches to Meters</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <form id="designstyle" autocomplete="off">

<div class="form-row">
<div class="form-group col">
<label for="ft">Feet</label>
<div class="input-group">
<input type="text" v-model="ft" name="ft" class="form-control" autofocus>
<div class="input-group-append">
<span class="input-group-text">ft</span>
</div>
</div>
</div>
<div class="form-group col">
<label for="inch">Inches</label>
<div class="input-group">
<input type="text" v-model="inch" name="inch" class="form-control">
<div class="input-group-append">
<span class="input-group-text">in</span>
</div>
</div>
</div>
</div>
<div class="form-group">
<button type="button" @click="calculate()" class="btn btn-success"><span>= ></span> Convert</button>
<button type="button" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<label for="cm1">Meters</label>
<div class="input-group">
<input type="number" v-model="m1" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">m</span>
</div>
</div>
</div>
<div class="form-row">
<div class="form-group col">
<label for="m2">Meters</label>
<div class="input-group">
<input type="number" v-model="m2" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">m</span>
</div>
</div>
</div>
<div class="form-group col">
<label for="cm2">Centimeters</label>
<div class="input-group">
<input type="number" v-model="cm2" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">cm</span>
</div>
</div>
</div>
</div>
<div class="form-group">
<label for="TA">Calculation</label>
<textarea v-model="ta" rows="2" class="form-control" readonly></textarea>
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
    title: 'Convert feet and inches to Meters.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: 'Feet+Inches to Meter.'}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/weight-converter/feet-inches-to-meters'}
  ]
  }
  },
  data(){
    return {
      ft: null,
      inch: null,
      answer: '',
      m1: '',
      m2: '',
      cm2: '',
      ta: ''
    }
  },
  methods: {
    calculate(){
      var ft = this.ft;
      var inch = this.inch;
      if( ft=="" ) ft="0";
      if( inch=="" ) inch="0";
      ft = parseFloat(ft);
      inch = parseFloat(inch);
      var inch2 = 12*ft+inch;
      var m1 = this.roundresult(0.0254*inch2);
      var m2 = Math.floor(m1);
      var cm2 = this.roundresult((m1-m2)*100);
      var txt=ft+"ft \u00D7 0.3048 + "+inch+"in \u00D7 0.0254\n";
      txt+="= "+m1+'m';
      this.m1 = m1;
      this.m2 = m2;
      this.cm2 = cm2;
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
      this.ft = null;
      this.inch = null;
      this.answer = "";
      this.m1 = "";
      this.m2 = "";
      this.cm2 = "";
      this.ta = "";
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
