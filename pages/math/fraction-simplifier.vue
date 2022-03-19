<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Simplify fractions calculator<hr>
          <h1 class="w3-text-teal"><b>Fraction Simplifier - Reduce fraction calculator</b></h1>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
          </Adsense>
<div class="">
  <form id="designpq" name="designpq" autocomplete="off">
  <div class="btn-group" data-toggle="buttons">
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simpleclicked()" checked> Simple Fractions
  </label>
  <label class="btn btn-secondary">
  <input type="radio" name="fractype" @click="simple()"> Mixed Fractions
  </label>
  </div>
  <div class="form-group mt-3">
  <table>
  <tr>
  <td rowspan="2" v-if="showleft === true"><input type="number" step="1" v-model="x1" class="form-control form-control-lg"></td>
  <td id="designpq"><input type="number" step="1" v-model="n1" class="form-control" autofocus></td>
  </tr>
  <tr>
  <td id="designpq4"><input type="number" step="1" v-model="d1" class="form-control"></td>
  </tr>
  </table>
  </div>
  <div class="form-group">
  <button type="button" title="Calculate" class="btn btn-secondary" @click="fract()"><span>= ></span> Calculate</button>
  <button type="reset" title="Reset" class="btn btn-secondary" @click="freset()"><span>&times;</span> Reset</button>
  </div>
  <div class="form-group">
  <label>Result</label>
  <table>
  <tr>
  <td><input type="text" v-model="n3" class="form-control" readonly></td>
  <td v-if="equalshow === true" rowspan="2" class="pl-2 pr-2">=</td>
  <td rowspan="2" v-if="x3if === true"><input type="text" v-model="x3" class="form-control" readonly></td>
  <td v-if="n4if === true"><input type="text" v-model="n4" class="form-control" readonly></td>
  </tr>
  <tr>
  <td><input type="text" v-model="d3" class="form-control" readonly></td>
  <td id="designpq456" v-if="d4if === true"><input type="text" v-model="d4" class="form-control" readonly></td>
  </tr>
  <tr>
  <td>Calculation:</td>
  </tr>
  <tr>
  <td><textarea rows="7" v-model="area" class="outtext" readonly></textarea>
  <input type="submit" style="display: none" /></td>
  </tr>
  </table>
  </div>
  </form>


</div><br>
<div class="">

</div>
  </div>
</div></div>

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
              <span class="w3-large"><a class="removelink" href="/math/adding-fractions-calculator"> Adding fractions calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/division-fractions-calculator"> Division fractions calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/fractions-calculator"> Fractions calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplying-fractions-calculator"> Multiplying fractions calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/subtracting-fractions-calculator"> Subtracting fractions calculator</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>

  <!-- Labels / tags -->

<!-- END Introduction Menu -->
</div>

</div>
<footer class="w3-container w3-dark-grey w3-padding-32 w3-margin-top">
  <p>© AaryaTables</p>
</footer>

</div>
</template>

<script>
export default {
  head() {
    // sets document title
    return {
      title: 'Fraction Simplifier - reduce fraction calculator to lowerst term',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Looking for the best converter to simplify fractions? Try out fraction simplifier calculator to perform the same action.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/fraction-simplifier'}
    ]
    }
    },
  data(){
    return {
      equalshow: false,
      x3if: false,
      n4if: false,
      d4if: false,
      showleft: false,
      showright: false,
      n1: '',
      thrrepiece: '',
      minusvalue: false,
      d1: '',
      n2: '',
      d2: '',
      x1: '',
      x2: '',
      n3: '',
      d3: '',
      d4: '',
      n4: '',
      sign: '',
      x2: '',
      x3: '',
      n31: '',
      selected: '+',
      area: ''
    }
  },
  methods: {
    freset(){
      this.area = "";
      this.x3if = false;
      this.n4if = false;
      this.d4if = false;
      this.showleft = false;
      this.showright = false;
      this.n1 = '';
      this.thrrepiece = '';
      this.minusvalue = false;
      this.d1 = '';
      this.equalshow = '';
      this.n2 = '';
      this.d2 = '';
      this.x1 = '';
      this.x2 = '';
      this.n3 = '';
      this.d3 = '';
      this.d4 = '';
      this.n4 = '';
      this.sign = '';
      this.x2 = '';
      this.x3 = '';
      this.n31 = '';
      this.selected = '+';
    },
    simple(){
this.showleft = true;
this.showright = true;
    },
    simpleclicked(){
      this.showleft = false;
      this.showright = false;
    },
    reset(){
      this.n1 = '',
      this.thrrepiece = '';
      this.minusvalue = false;
      this.d1 = '';
      this.n2 = '';
      this.d2 = '';
      this.n3 = '';
      this.d3 = '';
      this.d4 = '';
      this.n4 = '';
      this.sign = '-';
      this.n31 = '';
      this.x2 = '';
      this.x3 = '';
      this.selected = '';
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
  fract(){
    var out1 = '';
    var out2 = '';
    var s=1;
    var w = this.x1;
    var n = this.n1;
    var d = this.d1;
    if( n=='' || d=='' )
    {
       alert("Please enter fraction values");
       return;
    }
    if( w=='-' ) { s=-1; w='0'; }
    if( w=='' ) w='0';
    w = parseInt(w);
    n = parseInt(n);
    d = parseInt(d);
    if( w==0 && (n/d)<0 ) s=-1;
    n = Math.abs(n);
    d = Math.abs(d);
    if( w!=0 )
    {
       this.n1 = n;
       this.d1 = d;
    }
    if( w<0 ) { s=-1; w=-w; }
    //y = s*(w+n/d);
    var n1 = n+d*w;
    var g = this.gcd(n1,d);
    var sign='';
    if(s==-1 ) sign = '-';

    var out = '('+n1+','+d+') = '+g;
    out += '\n';
    if( w!=0 ) out+=w+' ';
    out += n+'/'+d;
    if( w!=0 )
    {
       out += '\n= ';
       out += sign+n1+'/'+d;
    }
    var n2=n1;
    var d2=d;
    //$('#td32').hide();
    //$('#td33').hide();
    //$('#td34').hide();
    //$('#designpq456').hide();
    this.x3if = false;
    this.n4if = false;
    this.d4if = false;
    this.equalshow = false;
    if( g>1 )
    {
       out += '\n= ';
       out += sign+'('+n1+'/'+g+')/('+d+'/'+g+')';
       n2 = n1/g;
       d2 = d/g;
       out += '\n= ';
       out += sign+n2+'/'+d2;
    }
    if( n1>d )
    {
       var i=Math.floor(n1/d);
       var j = Math.abs(n2)-Math.abs(i*d2);
       if( j!=0 ) {
          out += '\n= ';
          out += sign+i+' '+j+'/'+d2;
          //$('#td32').show();

          //$('#td33').show();
          this.x3if = true;
          this.n4if = true;
          this.d4if = true;
          this.equalshow = true;
          //$('#td34').show();
          //$('#designpq456').show();
          var t = sign+i;
          //$('#td33 input').val(t);
          this.x3 = t;
          //$('#td34 input').val(j);
          this.n4 = j;
          //$('#designpq456 input').val(d2);
          this.d4 = d2;
       }
    }
    this.n3 = sign+n2;
    this.d3 = d2;
    out += '\n= ';
    out += sign+this.roundresult(n2/d2);
    out += '\n= ';
    out += sign+this.roundresult(n2/d2*100)+'%';
    this.area = out;
    var obj = document.getElementById("frac");
},
  gcd(x, y){
  if ((typeof x !== 'number') || (typeof y !== 'number'))
    return false;
  x = Math.abs(x);
  y = Math.abs(y);
  while(y) {
    var t = y;
    y = x % y;
    x = t;
  }
  return x;
  }
}
}
</script>

<style lang="css" scoped>
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
.adslot_1 { display:none; }
 h1 { font-size:1.6rem; }
 h2 { font-size:1.4rem; }
 h3 { font-size:1.4rem; }
 h4 { font-size:1.2rem; }
 #designpq { padding:20px; max-width:500px; background:#a7c9b8; }
 #designpq td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #designpq td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #designpq .btn span { font-weight: bold; font-size:large; }
 #designpq .btn img { filter:invert(1); }
 #op { font-weight:bold; }
#designpq { padding-bottom:0px; }
#designpq4, #tabetd1455, #designpq456 { border-top:#666 3px solid; padding-top:1px; }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designpq { padding:10px; }
    #designpq td input[type=number] { width:60px; }
    #designpq td input[type=text] { width:60px; }
 }
</style>
