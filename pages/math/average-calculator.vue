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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Average Calculator<hr>
      <h1 class="w3-text-teal"><b>Average Calculator</b></h1>
      <p>To use this average calculator, just enter all the numbers by separating them with a comma. For example, if you want to find the average of numbers like 4, 5, and 7 then enter these numbers in this way in the box and click on the convert button.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <div id="calcform1" name="calcform1" autocomplete="off" class="rounded">
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
<button @click="reset()" type="reset" title="Reset" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
</div>
<div class="form-group row">
<label for="avg" class="col-sm-3 col-form-label">Average (mean)</label>
<div class="col-sm-9">
<input type="text" v-model="avg" class="form-control form-control-lg" readonly>
</div>
</div>
<div class="form-group row">
<label for="cnt" class="col-sm-3 col-form-label">Count</label>
<div class="col-sm-9">
<input type="text" v-model="cnt" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="sum" class="col-sm-3 col-form-label">Sum</label>
<div class="col-sm-9">
<input type="text" v-model="sum" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="avgcalc" class="col-sm-3 col-form-label">Average calculation steps</label>
<div class="col-sm-9">
<textarea rows="3" v-model="avgcalc" class="form-control" readonly></textarea>
</div>
</div>
<div class="form-group row">
<label for="gmean" class="col-sm-3 col-form-label">Geometric mean</label>
<div class="col-sm-9">
<input type="text" v-model="gmean" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="rms" class="col-sm-3 col-form-label">Root mean square (RMS)</label>
<div class="col-sm-9">
<input type="text" v-model="rms" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="med" class="col-sm-3 col-form-label">Median</label>
<div class="col-sm-9">
<input type="text" v-model="med" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="mod" class="col-sm-3 col-form-label">Mode</label>
<div class="col-sm-9">
<input type="text" v-model="mod" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="pstd" class="col-sm-3 col-form-label">Population SD</label>
<div class="col-sm-9">
<input type="text" v-model="pstd" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="sstd" class="col-sm-3 col-form-label">Sample SD:</label>
<div class="col-sm-9">
<input type="text" v-model="sstd" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="min" class="col-sm-3 col-form-label">Min value</label>
<div class="col-sm-9">
<input type="text" v-model="min" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="max" class="col-sm-3 col-form-label">Max value</label>
<div class="col-sm-9">
<input type="text" v-model="max" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="ran" class="col-sm-3 col-form-label">Range</label>
<div class="col-sm-9">
<input type="text" v-model="ran" class="form-control" readonly>
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
      title: 'Average Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Average Calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/average-calculator'}
    ]
    }
    },
  data(){
    return {
      input: '1,2,7',
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
    calculate(){
      var txt = this.input;
      //var del = document.getElementById("del").value;
      txt = txt.trim();
      //var num = txt.split(del);
      //var num = txt.match(/(\d|\/|\.|-|\+)+/g);
      var num = txt.split(",");
      //console.log(num);
      //return;

      if( !num ) return;
      var len=num.length;
		if( len==0 ) return;
      //num=num.map(Number);
      for (var i=0; i<len; i++) {
         num[i]=num[i].trim();
         num[i]=this.str2num(num[i]);
      }

      var sum=0;
      for(var i=0; i<len; i++)
         sum+=num[i];
      var avg=this.roundresult(sum/len);
      txt="Sum / Count = (";
      for(var i=0; i<len-1; i++)
         txt+=num[i]+"+";
      txt+=num[len-1]+") / "+len+" = "+sum+"/"+len+" = "+avg;
      this.avg = avg;
      this.cnt = len;
      this.sum = this.roundresult(sum);
      this.avgcalc = txt;

      var prod=1;
      for(var i=0; i<len; i++)
         prod*=num[i];
      var gmean = Math.pow(prod,(1/len));
      var rms=0;
      for(var i=0; i<len; i++)
         rms+=num[i]*num[i];
      rms = Math.sqrt(rms/len);

      //var min=Math.min(...num);
      //var max=Math.max(...num);
      var min="";
      var max="";
      var num0,dist,avg;
      var num0=num.slice();
      num.sort(function(a,b) { return a-b; }); //96% browser support
      min = num[0];
      max = num[len-1];
      dist=[];
      var prevnum=null;
      for(var i=0,k=-1; i<len; i++) {
         if( num[i]!=prevnum ) {
            prevnum = num[i];
            k++;
            dist[k]={};
            dist[k].num = num[i];
            dist[k].count=1;
         }
         else
            dist[k].count++;
      }
		var countmax=-1;
      for(var i=0; i<dist.length; i++) {
         if( dist[i].count>countmax )
            countmax = dist[i].count;
		}
		var mod="";
      for(var i=0; i<dist.length; i++) {
         if( dist[i].count==countmax )
            mod+=dist[i].num+", ";
		}
		mod=mod.slice(0,-2);
		var std=0;
      for(var i=0; i<dist.length; i++) {
		   std+=dist[i].count*Math.pow((dist[i].num-avg),2);
		}
		var pstd=this.roundresult(Math.sqrt(std/len));
		var sstd=this.roundresult(Math.sqrt(std/(len-1)));
      var i1=Math.floor((len+1)/2)-1;
      var i2=Math.floor((len+2)/2)-1;
      var med=this.roundresult((num[i1]+num[i2])/2);
      var range=this.roundresult(max-min);
      this.min = min;
      this.max = max;
      this.gmean = gmean;
      this.rms = rms;
      this.med = med;
      this.mod = mod;
      this.pstd = pstd;
      this.sstd = sstd;
      this.ran = range;

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

    },
    reset(){
      this.number1 = null;
      this.number2 = null;
      this.answer = ''
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
