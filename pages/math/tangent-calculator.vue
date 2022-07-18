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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Tangent and Tan inverse Calculator<hr>
      <h1 class="w3-text-teal"><b>Tan (x) calculator</b></h1>
      <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>
      <form id="inputdesign" autocomplete="off">
<div class="form-inline">
<span class="h1 math">tangent</span>
<input type="text" v-model="x" class="form-control col-sm-7 ml-2" autofocus>
<select v-model="degtype" class="form-control math h1 ml-1 mb-0">
<option value="0">&deg;</option>
<option value="1">rad</option>
</select>
<button type="button" @click="updatepi()" class="btn btn-light ml-1 math">&pi;</button>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-success" @click="calculate()"><span>=</span> Calculate</button>
<button type="button" title="Reset" class="btn btn-secondary" @click="reset()"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<input type="text" v-model="y" class="form-control" readonly>
</div>
</form><br>
<h2>tangent expression calculator</h2>
<p>An easy to use tangent expression calculator.</p>

<form id="inputdesign" name="calcform2">
<div class="form-inline">
<span class="h1 math">tan<sup class="h4">-1</sup></span>
<input type="text" v-model="x2" class="form-control col-sm-9 ml-2">
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-success" @click="calculate2()"><span>=</span> Calculate</button>
<button type="reset" title="Reset" class="btn btn-secondary" onclick="setfocus()"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<label>Angle in degrees</label>
<div class="input-group">
<input type="text" v-model="y2" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">&deg;</span>
</div>
</div>
</div>
<div class="form-group">
<label>Angle in radians</label>
<div class="input-group">
<input type="text" v-model="y3" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">rad</span>
</div>
</div>
</div>
<div class="form-group">
<label>Angle in radians</label>
<div class="input-group">
<input type="text" v-model="y4" class="form-control" readonly>
<div class="input-group-append">
<span class="input-group-text">rad</span>
</div>
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
      title: 'Tangent converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/tangent-calculator'}
    ]
    }
    },
  data(){
    return {
      x: '',
      y: '',
      degtype: '0',
      x2: '',
      y2: '',
      y3: '',
      y4: ''
        }
  },
  methods: {
    reset(){
      this.x = "";
      this.y = "";
    },
    updatepi(){
      if(this.x.includes("π")){
        this.x = this.x;
      }
      else{
      this.x = this.x + 'π';
}
    },
    reset2(){
      this.x2 = "";
this.ydeg1 = "";
this.ydeg2 = "";
this.yrad1 = "";
this.yrad2 = "";
    },
    calculate2(){
      var x=this.str2num(this.x2);
      var y3=Math.atan(x);
      var y2=y3*180/Math.PI;
      y2 = this.roundnum2(y2,8);
      var y4 = this.roundnum2(y3/Math.PI,8);
      y3 = this.roundnum2(y3,8);
      this.y2 = y2;
      this.y3 = y3;
      this.y4 = y4+"\u03C0";
    },
    calculate(){
      var x=this.x;
      x=x.replace(/(\d)(\u03C0)/gm,"$1*\u03C0");
      x=x.replace(/\u03C0/g,"3.141592653589793");
      x=this.str2num(x);
      var degtype=this.degtype;
      var i=degtype;
      if( i==0 )
         x*=Math.PI/180;
      var y = Math.tan(x);
      y = this.roundnum2(y,8);
      this.y = y;
    },
    removeAt(s,i) {
      s = s.substring(0,i)+s.substring(i+1,s.length);
      return s;
    },
    roundnum2(x,p) {
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
    str2num(s)
    {
       s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
       if( s=='' ) return 0;
       return Function('"use strict";return ('+s+')')();
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
#inputdesign { background:#a7c9b8; padding:20px; }
#inputdesign button i { vertical-align: bottom; }
@media all and (max-width: 800px) {

}

</style>
