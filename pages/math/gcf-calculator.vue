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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Greatest common factor Calculator<hr>
      <h1 class="w3-text-teal"><b>GCF Calculator</b></h1>
      <p>To use this GCF calculator, just enter all the numbers in the box, separate all the numbers with a space click on the convert button.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <div id="designform" name="designform" autocomplete="off" class="rounded">
<div class="form-group row">
<label class="col-sm-3 col-form-label">Enter data values</label>
<div class="col-sm-9">
<textarea rows="3" v-model="input" class="form-control" autofocus></textarea>
</div>
</div>
<div class="form-group row">
<label class="col-sm-3 col-form-label">&nbsp;</label>
<div class="col-sm-9">
<button @click="calculate()" title="Calculate" class="btn btn-secondary"><span>=> </span> Calculate</button>
<button @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label for="avg" class="col-sm-3 col-form-label">Greatest common factor (GCF)</label>
<div class="col-sm-9">
<input type="text" v-model="avg" class="form-control form-control-lg" readonly>
</div>
</div>
<div class="form-group row">
<label for="cnt" class="col-sm-3 col-form-label">Least common multiple (LCM)</label>
<div class="col-sm-9">
<input type="text" v-model="cnt" class="form-control" readonly>
</div>
</div>
</div>
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
      title: 'Greatest Common Factor(GCF) calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Greatest Common Factor calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/gcf-calculator'}
    ]
    }
    },
  data(){
    return {
      input: '4 3 7',
      answer: '',
      answer1: '',
      cnt: '',
      avg: '',
      len: '',
      sum: '',
      txt: '',
      min: '',
      max: '',
      gmean: '',
      rms: '',
      avgcalc: '',
      med: '',
      mod: '',
      pstd: '',
      sstd: '',
      ran: ''
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
   decnum(x) {
   if(Math.floor(x) === x) return 0;
   return x.toString().split(".")[1].length || 0;
},
    calculate(){
   //var primes=[2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,101,103,107,109,113,127,131,137,139,149,151,157,163,167,173,179,181,191,193,197,199,211];
   var data = this.input;
 if( data=="" ) return;
 //data = data.match(/\d+/g);
 data = data.split(" ");
 var d,dmax=0;
 var gcf2 = function(a,b)
{
   while( a!=b ) {
      if( a>b )
         a = a-b;
      else
         b = b-a;
   }
   return a;
};
var lcm2 = function(a,b)
{
   return a*b/gcf2(a,b);
};


 for(var i=0; i<data.length; i++) {
    d = this.decnum(Math.abs(parseFloat(data[i])));
    if( d>dmax ) dmax=d;
 }
 var f=Math.pow(10,dmax);
 for(var i=0; i<data.length; i++)
    data[i] = f*Math.abs(parseInt(data[i]));
 if( data.length<2 ) return;
 var gcf,lcm;
 for(var i=0; i<data.length-1; i++) {
    if( i==0 )
       gcf = gcf2(data[0],data[1]);
    else
       gcf = gcf2(gcf,data[i+1]);
 }
 for(var i=0; i<data.length-1; i++) {
    if( i==0 )
       lcm = lcm2(data[0],data[1]);
    else
       lcm = lcm2(lcm,data[i+1]);
 }

 this.avg = gcf/f;
 this.cnt = lcm/f;
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

    reset(){


      this.input = '';
      this.avg = '';
      this.cnt = ''
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
#designform { background:#a7c9b8; padding:20px; }
#designform button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designform { padding:10px; }
}

</style>
