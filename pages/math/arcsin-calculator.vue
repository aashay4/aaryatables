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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Arcsin calculator<hr>
      <h1 class="w3-text-teal"><b>Arcsin calculator</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>

      <form id="designvoc" name="designvoc" autocomplete="off" class="rounded">
<div class="form-row">
<div class="col-auto">Enter Number:</div>
<div class="col">
<input type="number" v-model="number1" class="form-control">
</div>
</div>
<div class="form-group mt-4">
<button @click="calculate()" type="button" class="btn btn-secondary"><span></span> Calculate</button>
<button @click="reset()" type="reset" class="btn btn-secondary"><span></span> Reset</button>
</div>
<div class="form-group">
<div class="input-group mb-3">
<input type="text" v-model="answer" readonly class="form-control form-control-lg"><p>Degree</p>
</div>
</div>
<div class="form-group">
<div class="input-group mb-3">
<input type="text" v-model="answer1" readonly class="form-control form-control-lg"><p>Rad</p>
</div>
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
        <h1 class=""><b>Other Number tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/addition-table"> Addition Table</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/logarithm-calculator"> Logarithm Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/sum-calculator"> Sum Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
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
      title: 'Arcsin calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Arcsin calculator online' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/arcsin-calculator'}
    ]
    }
    },
  data(){
    return {
      number1: null,
      number2: null,
      answer: '',
      answer1: ''
    }
  },
  methods: {
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
    },
    calculate(){
      var y1,y2,y,y12,y22;
  var x=this.number1;
    x=this.str2num(x);
  y2 = Math.asin(x);
  if( isNaN(y2) ) return;
  y1 = y2*180/Math.PI;
  y1 = this.roundnum2(y1,8);
  y2 = this.roundnum2(y2,8);
  y12 = this.roundnum2(180-y1,8);
  y22 = this.roundnum2(Math.PI-y2,8);

  var txt="arcsin "+x+" = sin\u207B\u00B9 "+x;
  var a = Math.asin(x)*180/Math.PI;
  var deg = a>0?Math.floor(a):Math.ceil(a);
  var min = a>0?Math.floor((a-deg)*60):Math.ceil((a-deg)*60);
  var sec = (a-deg-min/60)*3600;
  sec = this.roundnum2(sec,3);
  txt+=" = "+deg+"\u00B0 "+min+"' "+sec+"\"";
  txt+="\n= "+y1+"\u00B0 + k\u00D7360\u00B0";
  txt+="\n, "+y12+"\u00B0 + k\u00D7360\u00B0  (k=..-1,0,1,..)"; //\n= ";
  txt+="\n= "+y2+"rad + k\u00D72\u03C0";
  txt+="\n, "+y22+"rad + k\u00D72\u03C0  (k=..-1,0,1,..)";
  txt+="\n= "+this.roundnum2(y2/Math.PI,6)+"\u03C0rad + k\u00D72\u03C0";
  txt+="\n, "+this.roundnum2(y22/Math.PI,6)+"\u03C0rad + k\u00D72\u03C0  (k=..-1,0,1,..)";
  this.answer = y1+", "+y12;
  this.answer1 = y2+", "+y22;

    },
    reset(){
      this.answer = "";
      this.number1 = null;
      this.number2 = null;
      this.answer1 = "";
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
#designvoc { background:#a7c9b8; padding:20px; }
#designvoc button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designvoc { padding:10px; }
}

</style>
