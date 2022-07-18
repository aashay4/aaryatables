<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; GPA calculator<hr>
          <h1 class="w3-text-teal"><b>College gpa scale</b></h1>
          <p>Calculate college gpa in grade(percentage) easily.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">

<form id="lolakhuj" autocomplete="off">
<div id="gradetypediv" class="form-group">
<div class="btn-group btn-group-toggle row ml-0" data-toggle="buttons">
<label class="btn btn-secondary">
<input type="radio" name="gradetype" id="gradetype2" checked> Grade with letters
</label>
</div>
</div>
<div class="form-group">
<table id="tbl">
<tbody>
<tr>
  <td>Assignment</td>
  <td>Grade (Percentage)</td>
  <td>Credits</td>
</tr>
<tr>
<td><input type='text' placeholder='Practical' class='form-control' autofocus></td>
<td><select v-model='lgrade' class='form-control'>
<option selected>--</option>
<option value="4.33">A+</option>
<option value="4">A</option>
<option value="3.67">A-</option>
<option value="3.33">B+</option>
<option value="3">B</option>
<option value="2.67">B-</option>
<option value="2.33">C+</option>
<option value="2">C</option>
<option value="1.67">C-</option>
<option value="1.33">D+</option>
<option value="1">D</option>
<option value="0.67">D-</option>
<option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight8' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder='e.g Assignment' class='form-control'></td>
<td><select v-model='lgrade1' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight9' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder='e.g Attendance' class='form-control'></td>
<td><select v-model='lgrade2' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight10' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder='' class='form-control'></td>
<td><select v-model='lgrade3' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight11' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder="" class='form-control'></td>
<td><select v-model='lgrade4' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight12' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder="" class='form-control'></td>
<td><select v-model='lgrade5' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight13' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder="" class='form-control'></td>
<td><select v-model='lgrade6' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight14' min='0' step='any' class='form-control'></td>
</tr>
<tr>
<td><input type='text' placeholder="" class='form-control'></td>
<td><select v-model='lgrade7' class='form-control'>
  <option selected>--</option>
  <option value="4.33">A+</option>
  <option value="4">A</option>
  <option value="3.67">A-</option>
  <option value="3.33">B+</option>
  <option value="3">B</option>
  <option value="2.67">B-</option>
  <option value="2.33">C+</option>
  <option value="2">C</option>
  <option value="1.67">C-</option>
  <option value="1.33">D+</option>
  <option value="1">D</option>
  <option value="0.67">D-</option>
  <option value="0">F</option>
</select></td>
<td><input type='number' v-model='weight15' min='0' step='any' class='form-control'></td>
</tr>
<tr id="sum">
<td>Total:</td>
<td>&nbsp;</td>
<td><input type="number" min="0" step="any" class="form-control" readonly></td>
<td><input type="number" min="0" step="any" class="form-control" placeholder="100"></td>
</tr>
</tbody>
</table>
</div>
<div id="cumdiv" class="form-group">
<label for="gpa">Include previous GPA/credits (not required)</label>
<div class="row">
<div class="col">

<input type="text" v-model="cgpa" placeholder="cumulative gpa" class="form-control">
</div>
<div class="col">

<input type="text" v-model="chours" placeholder="credits" class="form-control">
</div>
</div>
</div>

<div class="form-group">
<button type="button" title="Calculate" @click="fract1()" class="btn btn-success"><span>= ></span> Calculate</button>
<button type="button" title="Reset" @click="reset1()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<label for="avg">GPA</label>
<div class="input-group">
<input type="text" v-model="gpa" class="form-control form-control-lg mr-2" readonly>
</div>
</div>
<div class="form-group">
<label for="total">Total credits/hours</label>
<input type="number" step="any" v-model="total" class="form-control" readonly>
</div>
<div class="form-group">
<label for="area">GPA calculation</label>
<textarea rows="3" v-model="area" class="form-control" readonly></textarea>
</div>

</form><br>

</div><br>
  </div>
</div></div>

<div class="w3-col l4">
  <!-- About Card -->
  <div class="w3-margin">
    <div class="w3-container w3-white">
      <div class="w3-margin w3-white">
          <div class="w3-container w3-padding">
        <h1 class=""><b>Other tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/final-grade-calculator"> Final grade calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/gpa-to-letter-grade"> GPA to letter grade</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/grade-calculator"> Grade calculator</a></span><br>
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
      title: 'College gpa calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'An easy to use college gpa calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/gpa-calculator'}
    ]
    }
    },
  data(){
    return {
      chours: null,
      cgpa: null,
      gpa: null,
      total: null,
lgrade: null,
xxdd: null,
yydd: null,
gradefmt2: null,
gradepoints: null,
gradepoints1: null,
gradepoints2: null,
gradepoints3: null,
gradepoints4: null,
gradepoints5: null,
gradepoints6: null,
gradepoints7: null,
weightpoint: null,
weightpoint1: null,
weightpoint2: null,
weightpoint3: null,
weightpoint4: null,
weightpoint5: null,
weightpoint6: null,
weightpoint7: null,
grade: null,
weight: null,
lgrade1: null,
grade1: null,
weight1: null,
lgrade2: null,
grade2: null,
weight2: null,
lgrade3: null,
grade3: null,
weight3: null,
lgrade4: null,
grade4: null,
weight4: null,
lgrade5: null,
grade5: null,
weight5: null,
lgrade6: null,
grade6: null,
weight6: null,
lgrade7: null,
grade7: null,
weight7: null,
weight8: null,
weight9: null,
weight10: null,
weight11: null,
weight12: null,
weight13: null,
weight14: null,
weight15: null,
counter: 0,
rgrade: '',
avg: null,
avg1: null,
avglet: null,
avglet1: null,
area: '',
fg: null,
fglet: null,
gradefmt: 2,
gradefmt1: 2,
avg42: null,
avglet42: null
      }
  },
  methods: {
    reset2(){
      this.gradepoints = null;
       this.gradepoints1 = null;
       this.gradepoints2 = null;
       this.gradepoints3 = null;
      this.gradepoints4 = null;
       this.gradepoints5 = null;
       this.gradepoints6 = null;
       this.gradepoints7 = null;
       this.weightpoint = null;
       this.weightpoint1 = null;
       this.weightpoint2 = null;
       this.weightpoint3 = null;
       this.weightpoint4 = null;
       this.weightpoint5 = null;
       this.weightpoint6 = null;
       this.weightpoint7 = null;
    },
    fract2(){
var pointsum, maxsum;
var gradepoints = this.gradepoints;
var gradepoints1 = this.gradepoints1;
var gradepoints2 = this.gradepoints2;
var gradepoints3 = this.gradepoints3;
var gradepoints4 = this.gradepoints4;
var gradepoints5 = this.gradepoints5;
var gradepoints6 = this.gradepoints6;
var gradepoints7 = this.gradepoints7;
var weightpoint = this.weightpoint;
var weightpoint1 = this.weightpoint1;
var weightpoint2 = this.weightpoint2;
var weightpoint3 = this.weightpoint3;
var weightpoint4 = this.weightpoint4;
var weightpoint5 = this.weightpoint5;
var weightpoint6 = this.weightpoint6;
var weightpoint7 = this.weightpoint7;
if(this.gradepoints === null){
  this.gradepoints = null;
  gradepoints = 0;
}
if(this.gradepoints1 === null){
  this.gradepoints1 = null;
  gradepoints1 = 0;
}
if(this.gradepoints2 === null){
  this.gradepoints2 = null;
  gradepoints2 = 0;
}
if(this.gradepoints3 === null){
  this.gradepoints3 = null;
  gradepoints3 = 0;
}
if(this.gradepoints4 === null){
  this.gradepoints4 = null;
  gradepoints4 = 0;
}
if(this.gradepoints5 === null){
  this.gradepoints5 = null;
  gradepoints5 = 0;
}
if(this.gradepoints6 === null){
  this.gradepoints6 = null;
  gradepoints6 = 0;
}
if(this.gradepoints7 === null){
  this.gradepoints7 = null;
  gradepoints7 = 0;
}
if(this.weightpoint === null){
  this.weightpoint = null;
  weightpoint = 0;
}
if(this.weightpoint1 === null){
  this.weightpoint1 = null;
  weightpoint1 = 0;
}
if(this.weightpoint2 === null){
  this.weightpoint2 = null;
  weightpoint2 = 0;
}
if(this.weightpoint3 === null){
  this.weightpoint3 = null;
  weightpoint3 = 0;
}
if(this.weightpoint4 === null){
  this.weightpoint4 = null;
  weightpoint4 = 0;
}
if(this.weightpoint5 === null){
  this.weightpoint5 = null;
  weightpoint5 = 0;
}
if(this.weightpoint6 === null){
  this.weightpoint6 = null;
  weightpoint6 = 0;
}
if(this.weightpoint7 === null){
  this.weightpoint7 = null;
  weightpoint7 = 0;
}
var grade = parseFloat(gradepoints) + parseFloat(gradepoints1) + parseFloat(gradepoints2) + parseFloat(gradepoints3) + parseFloat(gradepoints4) + parseFloat(gradepoints5) + parseFloat(gradepoints6) + parseFloat(gradepoints7);
var point = parseFloat(weightpoint) + parseFloat(weightpoint1) + parseFloat(weightpoint2) + parseFloat(weightpoint3) + parseFloat(weightpoint4) + parseFloat(weightpoint5) + parseFloat(weightpoint6) + parseFloat(weightpoint7);
this.xxdd = grade;
this.yydd = point;
pointsum = grade;
maxsum = point;
if( pointsum==0 || maxsum==0 )
{
   alert("Please enter grade points");
   return;
}
var avg=pointsum/maxsum*100;
avg=avg.toFixed(this.gradefmt2);
var avglet=this.GetLetterFromPercent(avg);
this.avg42=avg;
this.avglet42=avglet;

    },
    reset1(){
       this.weight8 = null;
       this.weight9 = null;
       this.weight10 = null;
       this.weight11 = null;
       this.weight12 = null;
       this.weight13 = null;
       this.weight14 = null;
       this.weight15 = null;
       this.lgrade = null;
       this.lgrade1 = null;
       this.lgrade2 = null;
       this.lgrade3 = null;
       this.lgrade4 = null;
       this.lgrade5 = null;
       this.lgrade6 = null;
       this.lgrade7 = null;
       this.chours = null;
       this.cgpa = null;
       this.gpa = null;
this.total = null;
this.area = null;
    },

    fract1(){
      var avg=0;
var sum=0;
var txt="";
var tavg="";
var tsum="";
var weight8 = this.weight8;
var weight9 = this.weight9;
var weight10 = this.weight10;
var weight11 = this.weight11;
var weight12 = this.weight12;
var weight13 = this.weight13;
var weight14 = this.weight14;
var weight15 = this.weight15;
var lgrade = this.lgrade;
var lgrade1 = this.lgrade1;
var lgrade2 = this.lgrade2;
var lgrade3 = this.lgrade3;
var lgrade4 = this.lgrade4;
var lgrade5 = this.lgrade5;
var lgrade6 = this.lgrade6;
var lgrade7 = this.lgrade7;
//alert(this.weight8)
if(this.weight8 === null || this.lgrade === null ){
  this.weight8 = null;
  this.lgrade = null;
  weight8 = 0;
  lgrade = 0;
}
if(this.weight9 === null || this.lgrade1 === null ){
  this.weight9 = null;
  this.lgrade1 = null;
  weight9 = 0;
  lgrade1 = 0;
}
if(this.weight10 === null || this.lgrade2 === null ){
  this.weight10 = null;
  this.lgrade2 = null;
  weight10 = 0;
  lgrade2 = 0;
}
if(this.weight11 === null || this.lgrade3 === null ){
  weight11 = 0;
  lgrade3 = 0;
  this.weight11 = null;
  this.lgrade3 = null;
}
if(this.weight12 === null || this.lgrade4 === null ){
  weight12 = 0;
  lgrade4 = 0;
  this.weight12 = null;
  this.lgrade4 = null;
}
if(this.weight13 === null || this.lgrade5 === null ){
  weight13 = 0;
  lgrade5 = 0;
  this.weight13 = null;
  this.lgrade5 = null;
}
if(this.weight14 === null || this.lgrade6 === null ){
  this.weight14 = null;
  this.lgrade6 = null;
  weight14 = 0;
  lgrade6 = 0;
}
if(this.weight15 === null || this.lgrade7 === null ){
  this.weight15 = null;
  this.lgrade7 = null;
  weight15 = 0;
  lgrade7 = 0;
}

var glook=[-1,4.33,4.00,3.67,3.33,3.00,2.67,2.33,2.00,1.67,1.33,1.00,0.67,0,-1,-1];
var gpa=0;
var sum=0;
var txt1="";
var txt2="";
var el,hour,igrade,grade;
   el=(parseFloat(weight8) * parseFloat(lgrade)) + (parseFloat(weight9) * parseFloat(lgrade1)) + (parseFloat(weight10) * parseFloat(lgrade2)) + (parseFloat(weight11) * parseFloat(lgrade3)) + (parseFloat(weight12) * parseFloat(lgrade4)) + (parseFloat(weight13) * parseFloat(lgrade5)) + (parseFloat(weight14) * parseFloat(lgrade6)) + (parseFloat(weight15) * parseFloat(lgrade7));
   var hours=el;
   hours = parseFloat(hours);
   el=parseFloat(weight8) + parseFloat(weight9) + parseFloat(weight10) + parseFloat(weight11) + parseFloat(weight12) + parseFloat(weight13) + parseFloat(weight14) + parseFloat(weight15);
   igrade=el;
   grade = glook[igrade];
   if( hours>0 && grade>=0 )
   {
      gpa+=hours*grade;
      sum+=hours;
      txt1+=hours+"\u00D7"+grade+"+";
      txt2+=hours+"+";
   }
var cgpa=this.cgpa;
var chours=this.chours;
cgpa = parseFloat(cgpa);
chours = parseFloat(chours);
if( cgpa>=0 && chours>0 )
{
   gpa+=chours*cgpa;
   sum+=chours;
   txt1+=chours+"\u00D7"+cgpa+"+";
   txt2+=chours+"+";
}
gpa/=sum;
gpa=gpa.toFixed(2);
txt1=txt1.slice(0, -1);
txt2=txt2.slice(0, -1);
var txt="("+txt1+") / ("+txt2+") = "+gpa;
this.gpa=gpa;
this.total=sum;
this.area=txt;
//var percent=25*gpa;
//if( percent>100 ) percent=100;
//$("#gpacircle").percircle({percent: percent,text: gpa});
//$("#gpacircle").show();
},
   GetLetterFromGPA(gpa)
 {
    var letter="F";
    var lettertbl=['A+','A','A-','B+','B','B-','C+','C','C-','D+','D','D-','F'];
    var gpatbl=[4.165,3.835,3.5,3.165,2.835,2.5,2.165,1.835,1.5,1.165,0.835,0.335];
    for(var i=0; i<gpatbl.length; i++)
       if( gpa>=gpatbl[i] )
       {
          letter = lettertbl[i];
          break;
       }
    return letter;
 },
    metricclicked(){
        this.showmetric = true;
      this.showunits = false;
this.isMetric = true;
    },
     roundresult(x) {
   var y=parseFloat(x);
   y=this.roundnum(y,10);
   return y;
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

 GetLetterFromPercent(percent)
{
   var letter="";
   var lettertbl=['A+','A','A-','B+','B','B-','C+','C','C-','D+','D','D-','F'];
   var percenttbl=[97,93,90,87,83,80,77,73,70,67,63,60,0];
   for(var i=0; i<percenttbl.length; i++)
      if( percent>=percenttbl[i] )
      {
         letter = lettertbl[i];
         break;
      }
   return letter;
},
reset(){
  this.grade = null;
  this.weight = null;
  this.grade1 = null;
  this.weight1 = null;
  this.grade2 = null;
  this.weight2 = null;
  this.grade3 = null;
  this.weight3 = null;
  this.grade4 = null;
  this.weight4 = null;
  this.grade5 = null;
  this.weight5 = null;
  this.grade7 = null;
  this.weight7 = null;
  this.grade6 = null;
  this.weight6 = null;
},
  fract(){
    var avg=0;
    var sum=0;
    var txt="";
    var tavg="";
    var tsum="";
    if(this.grade === null || this.weight === null){
this.grade = 0;
this.weight = 0;
this.counter++;
    }
    if(this.grade1 === null || this.weight1 === null){
this.grade1 = 0;
this.weight1 = 0;
this.counter++;
    }
    if(this.grade2 === null || this.weight2 === null){
this.grade2 = 0;
this.weight2 = 0;
this.counter++;
    }
    if(this.grade3 === null || this.weight3 === null){
this.grade3 = 0;
this.weight3 = 0;
this.counter++;
    }
    if(this.grade4 === null || this.weight4 === null){
this.grade4 = 0;
this.weight4 = 0;
this.counter++;
    }
    if(this.grade5 === null || this.weight5 === null){
this.grade5 = 0;
this.weight5 = 0;
this.counter++;
    }
    if(this.grade6 === null || this.weight6 === null){
this.grade6 = 0;
this.weight6 = 0;
this.counter++;
    }
    if(this.grade7 === null || this.weight7 === null){
this.grade7 = 0;
this.weight7 = 0;
this.counter++;
    }
    var totalgrade = parseInt(this.grade1) + parseInt(this.grade) + parseInt(this.grade2) + parseInt(this.grade3) + parseInt(this.grade4) + parseInt(this.grade5) + parseInt(this.grade6) + parseInt(this.grade7);
    var totalweight = parseInt(this.weight1) + parseInt(this.weight) + parseInt(this.weight2) + parseInt(this.weight3) + parseInt(this.weight4) + parseInt(this.weight5) + parseInt(this.weight6) + parseInt(this.weight7);
//    alert(totalgrade)
  //  alert("Counter: " + this.counter)
    avg = (this.grade * this.weight) + (this.grade1 * this.weight1) + (this.grade2 * this.weight2) + (this.grade3 * this.weight3) + (this.grade4 * this.weight4) + (this.grade5 * this.weight5) + (this.grade6 * this.weight6) + (this.grade7 * this.weight7)
  //  alert(avg)
sum = parseInt(this.weight) + parseInt(this.weight1) + parseInt(this.weight2) + parseInt(this.weight3) + parseInt(this.weight4) + parseInt(this.weight5) + parseInt(this.weight6) + parseInt(this.weight7);
//alert("Sum: " +sum)

    if( avg==0 || sum==0 )
    {
       alert("Please enter grades & weights");
       return;
    }
    var topsum=avg;
    avg/=sum;
    avg=avg.toFixed(this.gradefmt);
    txt="("+tavg+") / ("+tsum+") = "+this.roundresult(topsum)+" / "+this.roundresult(sum)+" = "+avg;
    var avglet=this.GetLetterFromPercent(avg);
    var rgrade=this.rgrade;
    if( rgrade=="" ) this.rgrade=80;
    var final = (100*this.rgrade-sum*avg)/(100-sum);
    final = final.toFixed(this.gradefmt);
    var finallet = this.GetLetterFromPercent(final);
    this.avg=avg;
    this.avglet=avglet;
    this.area=txt;
    this.fg=final;
    this.fglet=finallet;
    if( avg==Math.floor(avg) ) avg=Math.floor(avg);
    //var url="final-grade-calculator.html?grade="+avg+"&weight="+sum;
    //if( sum<=0 || sum>=100 ) url=undefined;
    //SetFinalURL(url);
    var percent=avg;
    if( percent>100 ) percent=100;

    }
}
}
</script>

<style lang="css" scoped>
.buttonclicked{
  background-color: Violet;
}
.buttonclicked1{
  background-color: Violet;
}
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
 #wrapper td { padding-left:3px; padding-right:3px; }
 #lolakhuj, #lolakhuj2 { max-width:414px; padding:15px; background:#a7c9b8; border:1px solid #e0e0e0; border-radius:7px; }
 .btn span { font-weight:bold; font-size:large; }
 #gradecircle { display:none; margin: 0 auto; float:none; }
 #tbl td { padding-bottom:3px; background:#a7c9b8; }
 /*#tbl tr td:first-child { width:60px; }*/
 #tbl tr:first-child td { height:45px; }
 #tbl input[type=number], #tbl select { width:100px; }
 #sum { display:none; }
 #sum td:first-child { padding-left:0; }
@media all and (max-width: 600px) {
 .nav-tabs { display:none; }
 #tbl input[type=number], #tbl select { width:85px; }
}
.btn span { font-weight:bold; font-size:large; }

@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
 }
</style>
