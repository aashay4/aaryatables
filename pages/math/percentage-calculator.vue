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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Percentage Calculator<hr>
      <h1 class="w3-text-teal"><b>Percentage Calculator</b></h1>
      <form class="calcform">
<div>
Enter Value: <input type="text" name="a" class="form-control" v-model="number1" placeholder="Enter value: a number."> Enter Percentage: <input type="text" v-model="percentage1" name="b" class="form-control" placeholder="Percentage(%)"> ?
</div>
<div>
<button type="button" title="Calculate" class="btn btn-secondary" @click="per1()"><span>=></span> Answer</button>
<input type="text" v-model="answer1" class="form-control" readonly>
</div>
<div>
<textarea rows="1" class="form-control" readonly></textarea>
</div>
</form>
<h4>Percentage Finder</h4>
<form class="calcform">
<div>
<input type="text" v-model="number2" class="form-control"> the percent of the value
<input type="text" v-model="number3" class="form-control"> ?
</div>
<div>
<button type="button" title="Calculate" class="btn btn-secondary" @click="per2()"><span>=></span> Answer</button>
<input type="text" class="form-control" v-model="answer2" readonly> %
</div>
<div>
<textarea rows="1" class="form-control" readonly></textarea>
</div>
</form>
<h4>Percentage change</h4>
<form id="formcalculator" class="calcform">
<div>
Find the percentage:<br>from
<input type="text" v-model="number4" class="form-control">
to
<input type="text" v-model="number5" class="form-control"> ?
</div>
<div>
<button type="button" title="Calculate" class="btn btn-secondary" @click="per3()"><span>=></span> Answer</button>
<input type="text" v-model="answer4" class="form-control" readonly> %
</div>
<div>
<textarea rows="1" class="form-control" readonly></textarea>
</div>
</form>
<h4>Percent to fraction & decimal</h4>
<form id="calsstyle" class="calcform">
<table id="trstyle">
<tr>
<td>Percent:</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>Fraction:</td>
<td>&nbsp;</td>
<td>Decimal:</td>
<td>&nbsp;</td>
</tr>
<tr>
<td rowspan="2"><input type="text" v-model="number22" name="c1" class="form-control"></td>
<td rowspan="2">%</td>
<td rowspan="2"><button type="button" title="Convert" @click="per4()" class="btn btn-secondary"><span>=></span></button></td>
<td><input type="text" v-model="upperfraction" class="form-control"></td>
<td rowspan="2"><input type="text" v-model="decimalvalue" class="form-control"></td>
<td rowspan="2"><button type="reset" @click="reset()" title="Reset" class="btn btn-secondary"><span>↺</span>Reset</button></td>
</tr>
<tr>
<td><input type="text" v-model="downfraction" class="form-control"></td>
</tr>
<tr>
<td colspan="7"><button type="reset" id="resetbtn2" title="Reset" class="btn btn-secondary"><span> Reset</span></button></td>
</tr>
</table>
</form>
      </div>
      <div class="w3-padding">
        <h1>The percentage calculation</h1>
        <p>Consider an example to find the 40% of $70.</p>
        <p>The percentage calculation for this number is: 40% &times; 70.</p>
        <p>=> 40/100 &times; 70</p>
        <p>=> 28</p>
        <h2>Percentage Finder</h2><br>
        <p>20 is what percentage of 100?</p>
        <p> => 20/100 &times; 100</p>
        <p> => 20</p>
        <h2>Percentage to Fraction & Decimal.</h2>
        <p>What is the 40% to Fraction and Decimal?</p>
        <b>Fraction of 40%</b>
        <p> => 40 / 100</p>
        <p> => 2/5 </p>
        <b>Decimal of 40%</b>
        <p> => 40 / 100</p>
        <p> => 0.4 </p>
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
              <span class="w3-large"><a class="removelink" href="/math/subtraction-calculator"> Subtraction Calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
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
      title: 'Percentage Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Percentage calculator - Count percentage of numbers' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/percentage-calculator'}
    ]
    }
    },
  data(){
    return {
      number1: null,
      percentage1: null,
      answer1: '',
      number2: '',
      number3: '',
      answer2: '',
      number4: '',
      number5: '',
      answer4: '',
      number10: '',
      upperfraction: '',
      downfraction: '',
      number22: '',
      decimalvalue: ''
    }
  },
  methods: {
    reset(){
      this.number1 = null;
      this.percentage1 = null;
      this.answer1 = '';
      this.number2 = '';
      this.number3 = '';
      this.number4 = '';
      this.number5 = '';
      this.answer4 = '';
      this.number10 = '';
      this.upperfraction = '';
      this.downfraction = '';
      this.number22 = '';
      this.decimalvalue = '';
    },
    per1(){
        var ans = parseFloat(this.percentage1) * 100;
        this.answer1 = parseFloat(ans)/this.number1;
    },
    per2(){
      var ans = parseFloat(this.number2)/this.number3;
      this.answer2 = parseFloat(ans)*100
    },
    per3(){
      var ans = parseFloat(this.number5) - parseFloat(this.number4);
      var ans1 = ans/this.number4;
      this.answer4 = ans1 * 100;
    },
        per4(){
          var percent = this.number22;
          if( percent!="" ) {
  var sign = '';
  var sign2 = '+';
  var x = percent;
  var x2 = parseFloat(x/100);
  var absx = Math.abs(x2);
  //var y=Math.floor(absx);
  var y=0;
  var frac=this.roundresult(absx-y);
  if( x2<0 ) sign = sign2 = '-';
  var d = this.digits_after_period(absx);
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
  this.upperfraction = num2;
  this.downfraction = den2;
  this.decimalvalue = parseFloat(this.number22)/100;
//  document.getElementById("c4").value = roundresult(x2);
}
},
 roundresult(x) {
      var y = parseFloat(x);
      y = this.roundnum(y,10);
      return y;
   },
   digits_after_period(x)
   {
      var f = x.toString();
      var i = f.indexOf('.');
      var len = f.length-i-1;
      return len;
   },
  roundnum(x,p) {
     var i;
     var n=parseFloat(x);
     var m=n.toPrecision(p+1);
     var y=String(m);
     i=y.indexOf('e');
     if( i==-1 )	i=y.length;
    var j=y.indexOf('.');
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
      this.number1 = null;
      this.number2 = null;
      this.answer = ''
    }
  }

}
</script>

<style lang="css" scoped>
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.2rem; }
h4 { font-size:1.2rem; }
.btn span { font-size:large; font-weight:bold; }
.calcform { background:#a7c9b8; padding:15px; border-radius:7px; margin-bottom:20px; }
.calcform div { display:inline-block; }
.calcform div:nth-child(2) { margin-top:10px; }
.calcform div:nth-child(1) input[type=text] { width:100px; display:inline-block; }
.calcform div:nth-child(2) input[type=text] { width:100px; display:inline-block; margin-left:5px; }
.calcform div:nth-child(3) { display:none; margin-top:10px; }
#formcalculator input[type=text] { margin-top:10px; }
#trstyle tr:nth-child(2) td:nth-child(4) { border-bottom:2px #666 solid }
@media all and (max-width: 672px) {
   .calcform { padding:10px; }
   .calcform div:nth-child(2) { display:block; }
   .calcform input[type=text] { margin:5px 0; }
   .calcform div:nth-child(1) input[type=text] { width:90px; }
   #calsstyle { padding:10px; }
   #calsstyle button[type=reset] { float:left; }
   #resetbutton { display:none; }
}
@media all and (min-width: 673px) {
   .calcform div:nth-child(2) { margin-left:20px; }
   #resetbtn2 { display:none; }
}

</style>
