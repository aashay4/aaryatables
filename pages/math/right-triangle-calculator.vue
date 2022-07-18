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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Right triangle calculator<hr>
      <h1 class="w3-text-teal"><b>Right triangle calculator</b></h1>
      <p>An easy to use tool to calculate right triangle. You just need to enter one side to get the right answer.</p>
      <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>
      <form id="inputdesign" autocomplete="off">
<div class="form-group row">
<label for="a" class="col-sm-3 col-form-label">Side a</label>
<div class="col-sm-9">
<input type="text" v-model="a" class="form-control" autofocus>
</div>
</div>
<div class="form-group row">
<label for="b" class="col-sm-3 col-form-label">Side b</label>
<div class="col-sm-9">
<input type="text" v-model="b" class="form-control">
</div>
</div>
<div class="form-group row">
<label for="c" class="col-sm-3 col-form-label">Side c</label>
<div class="col-sm-9">
<input type="text" v-model="c" class="form-control">
</div>
</div>
<div class="form-group row">
<label for="anglea" class="col-sm-3 col-form-label">Angle A</label>
<div class="input-group col-sm-9">
<input type="text" v-model="anglea" name="anglea" class="form-control">
<div class="input-group-append">
<select v-model="degtype1" class="form-control">
<option value="0">&deg;</option>
<option value="1">rad</option>
</select>
</div>
</div>
</div>
<div class="form-group row">
<label for="angleb" class="col-sm-3 col-form-label">Angle B</label>
<div class="input-group col-sm-9">
<input type="text" v-model="angleb" name="angleb" class="form-control">
<div class="input-group-append">
<select v-model="degtype2" class="form-control">
<option value="0">&deg;</option>
<option value="1">rad</option>
</select>
</div>
</div>
</div>
<div class="form-group">
<label class="col-sm-3 col-form-label">&nbsp;</label>
<button type="button" title="Calculate" class="btn btn-secondary" @click="calculate()"><span>=</span> Calculate</button>
<button type="reset" title="Reset" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
</div>
<div class="form-group">
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
      title: 'Right triangle calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Right triangle calculator online and learn how to convert.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/right-triangle-calculator'}
    ]
    }
    },
  data(){
    return {
      a: '',
b: '',
c: '',
anglea: '',
degtype1: '0',
angleb: '',
degtype2: '0'
    }
  },
  methods: {
    reset(){
      this.a = "";
      this.b = "";
      this.c = "";
      this.anglea = "";
      this.degtype1 = "0";
      this.angleb = "";
      this.degtype2 = "0";
    },
    calculate(){
      var i1 = this.degtype1;
  var i2 = this.degtype2;
  var a = this.str2num(this.a);
  var b = this.str2num(this.b);
  var c = this.str2num(this.c);
  var anglea = this.str2num(this.anglea);
  var angleb = this.str2num(this.angleb);
  //var area = document.getElementById("area").value;
  if( anglea!="" && i1==0 ) anglea*=Math.PI/180.0;
  if( angleb!="" && i2==0 ) angleb*=Math.PI/180.0;
  if( angleb && !anglea ) anglea=Math.PI/2-angleb;
  if( anglea && !angleb ) angleb=Math.PI/2-anglea;
  if( a && b ) {
    c=Math.sqrt(a*a+b*b);
  }
  else if( a && c ) {
    b=Math.sqrt(c*c-a*a);
  }
  else if( b && c ) {
    a=Math.sqrt(c*c-b*b);
  }
  else if( a && anglea ) {
    b=a/Math.tan(anglea);
    c=Math.sqrt(a*a+b*b);
  }
  else if( b && anglea ) {
    a=b*Math.tan(anglea);
    c=Math.sqrt(a*a+b*b);
  }
  else if( c && anglea ) {
    a=c*Math.sin(anglea);
    b=c*Math.cos(anglea);
  }
  anglea=Math.atan(a/b);
  angleb=Math.atan(b/a);
  if( i1==0 ) anglea*=180.0/Math.PI;
  if( i2==0 ) angleb*=180.0/Math.PI;
  this.a = this.roundnum(a,6);
  this.b = this.roundnum(b,6);
  this.c = this.roundnum(c,6);
  this.anglea = this.roundnum(anglea,6);
  this.angleb = this.roundnum(angleb,6);
  //document.gethis.tElementById("area").value = area;

    },
    removeAt(s,i) {
      s = s.substring(0,i)+s.substring(i+1,s.length);
      return s;
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
