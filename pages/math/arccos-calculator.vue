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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Arccos Calculator<hr>
      <h1 class="w3-text-teal"><b>Arccos Calculator</b></h1>
      <form id="calcform1" name="calcform1" autocomplete="off" class="rounded">
<div class="form-row">
<div id="log" class="col-auto">Enter Number:</div>
<div class="col">
<input type="number" id="x" name="x" v-model="number1" class="form-control">
</div>
</div>
<div id="logdiv2" class="form-row">
<div id="coefdiv2a" class="col-2">
<input type="text" id="c2" name="c2" placeholder="1" class="form-control">
</div>
<div id="coefdiv2b" class="col-auto mt-2">&times;</div>
<div id="log2" class="col-auto">log</div>
<div id="bdiv2" class="col-3 mt-4 input-group">
<input type="text" class="form-control">
<select id="btnhh" class="form-control">
<option>&nbsp;</option>
<option>2</option>
<option>e</option>
<option>10</option>
</select>
</div>
<div class="col">
<input type="text" class="form-control">
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
      title: 'Arccos Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Arccos Calculator for free online' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/arccos-calculator'}
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
  y2 = Math.acos(x);
  if( isNaN(y2) ) return;
  y1 = y2*180/Math.PI;
  y1 = this.roundnum2(y1,8);
  y2 = this.roundnum2(y2,8);
  var txt="arccos "+x+" = cos\u207B\u00B9 "+x;
  var a = Math.acos(x)*180/Math.PI;
  var deg = a>0?Math.floor(a):Math.ceil(a);
  var min = a>0?Math.floor((a-deg)*60):Math.ceil((a-deg)*60);
  var sec = (a-deg-min/60)*3600;
  var sec = this.roundnum2(sec,3);
  txt+=" = "+deg+"\u00B0 "+min+"' "+sec+"\"";
  txt+="\n= \u00B1"+y1+"\u00B0+k\u00D7360\u00B0  (k=..-1,0,1,..)";
  txt+="\n= \u00B1"+y2+"rad+k\u00D72\u03C0  (k=..-1,0,1,..)";
  txt+="\n= \u00B1"+this.roundnum2(y2/Math.PI,6)+"\u03C0rad+k\u00D72\u03C0  (k=..-1,0,1,..)";
  this.answer = y1+", -"+y1;
  this.answer1 = y2+", -"+y2;

  //document.calcform.TA1.value = txt;

    },
    reset(){
      this.number1 = null;
      this.number2 = null;
      this.answer = ''
    }
  }

}
</script>

<style lang="css">
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
#calcform1,#calcform2,#calcform3 { background:#a7c9b8; padding:20px; }
#bdiv, #bdiv2, #bdiv3 { max-width:100px; }
#b, #b2, #b3 { max-width:70px; }
#bsel,#btnhh,#b3sel { max-width:20px; padding:0; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#log, #log2, #log3 { font-size:xx-large; font-family:"Times New Roman", Times, serif; }
#txt, #txt3 { font-family:math; }
#drop, #drop2, #drop3 { background:#fff; color:#212529; }
#calcform1 button i { vertical-align: bottom; }
#coefdiv1a, #coefdiv1b span { vertical-align: bottom; }
#graph { display:none; }
/*.btn b, .btn b2 { font-size:large; }*/
#opsel { font-weight:bold; margin-top:10px; }
#coefdiv1a, #coefdiv1b, #opdiv, #logdiv2 { display:none; }
@media all and (max-width: 800px) {
   #ln { padding-right:35px; }
   #calcform1, #calcform3 { padding:10px; }
}

</style>
