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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; variance calculator<hr>
      <h1 class="w3-text-teal"><b>variance calculator</b></h1>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>
      <div id="designvoc" name="designvoc" autocomplete="off" class="rounded">
<div class="form-group row">
<label class="col-sm-3 col-form-label">Enter data values</label>
<div class="col-sm-9">
<textarea rows="3" v-model="input" class="form-control" autofocus></textarea>
</div>
</div>
<div class="input-group-append">
  <label class="col-sm-3 col-form-label">Select an option</label>
<select v-model="countryprice" class="form-control" @change="cosvaluechange()">
<option value="0">Whole population data</option>
<option value="1">Sampled data</option>
</select>
</div><br>
<div class="form-group row">
<label class="col-sm-3 col-form-label">&nbsp;</label>
<div class="col-sm-9">
<button @click="calculate()" title="Calculate" class="btn btn-secondary"><span>=> </span> Calculate</button>
</div>
</div>
<div class="form-group row">
<label for="avg" class="col-sm-3 col-form-label">Standard deviation:</label>
<div class="col-sm-9">
<input type="text" v-model="Text1" class="form-control form-control-lg" readonly>
</div>
</div>
<div class="form-group row">
<label for="cnt" class="col-sm-3 col-form-label">Variance:</label>
<div class="col-sm-9">
<input type="text" v-model="Text2" class="form-control" readonly>
</div>
</div>
<div class="form-group row">
<label for="sum" class="col-sm-3 col-form-label">Mean:</label>
<div class="col-sm-9">
<input type="text" v-model="Text3" class="form-control" readonly>
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
      title: 'variance calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Find variance, standard deviation, sample size n, mean and sum of squares with this tool.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/variance-calculator'}
    ]
    }
    },
  data(){
    return {
      Text1: '',
      Text2: '',
      Text3: '',
      countryprice: '0',
      input: '1,2,7',
      answer: '',
      answer1: '',
      pstd: '',
sstd: '',
pvar: '',
svar: '',
mean: ''
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
      var num = new Array();
			var txt = this.input;
			var index1 =  this.countryprice;
			if( txt=="" ) txt="1 3 5";
			txt = txt.replace(/\054/g," ");
			txt = txt.replace(/\r\n/g," ");
			txt = txt.replace(/\n/g," ");
			if( txt.charAt(txt.length-1)==" " )
				txt = txt.substring(0,txt.length-1);
			var n = txt.split(" ");
			for(var i=0; i<n.length; i++)
				num[i] = parseFloat(n[i]);
			var m = 0;
			for(i=0; i<num.length; i++)
				m += num[i];
			m /= num.length;
			var v = 0;
			for(i=0; i<num.length; i++)
				v += (num[i]-m)*(num[i]-m);
			if( index1==0 )
				v /= num.length;
			else
				v /= (num.length-1);
			var std = Math.sqrt(v);
			this.Text1 = this.roundresult(std);
			this.Text2 = this.roundresult(v);
			this.Text3 = this.roundresult(m);
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
      this.input = "1,2,7";
      this.answer = "";
      this.answer1 = "";
      this.cnt = "";
      this.avg = "";
      this.len = "";
      this.sum = "";
      this.txt = "";
      this.min = "";
      this.max = "";
      this.gmean = "";
      this.rms = "";
      this.avgcalc = "";
      this.med = "";
      this.mod = "";
      this.pstd = "";
      this.sstd = "";
      this.ran = "";
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
