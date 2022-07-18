<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Time calculator<hr>
          <h1 class="w3-text-teal"><b>Time calculator</b></h1>
          <p>Add and subtract time. Just select the year, month, and day to find the remaining time.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">
  <form id="thisonesi" autocomplete="off">
<div class="form-row">
<div class="form-group ml-1">
<label for="y1">Years</label>
<input type="number" min="0" v-model="y1" class="form-control" autofocus>
</div>
<div class="form-group ml-1">
<label for="mon1">Months</label>
<input type="number" min="0" v-model="mon1" name="mon1" class="form-control">
</div>
<div class="form-group ml-1">
<label for="d1">Days</label>
<input type="number" min="0" v-model="d1" name="d1" class="form-control">
</div>
<div class="form-group ml-1">
<label for="h1">Hours</label>
<input type="number" min="0" v-model="h1" name="h1" class="form-control">
</div>
<div class="form-group ml-1">
<label for="m1">Minutes</label>
<input type="number" min="0" v-model="m1" name="m1" class="form-control">
</div>
<div class="form-group ml-1">
<label for="s1">Seconds</label>
<input type="number" min="0" v-model="s1" name="s1" class="form-control">
</div>
<div class="form-group ml-1">
<label>&nbsp;</label>
<div class="input-group">
<button type="button" @click="todaydate1()" class="btn btn-sm btn-light mt-1">Now</button>
</div>
</div>
</div>
<div class="form-group">
<select v-model="op" class="form-control">
<option>+ Add</option>
<option>- Subtract</option>
</select>
</div>
<div class="form-row">
<div class="form-group ml-1">
<label for="y2">Years</label>
<input type="number" min="0" v-model="y2" name="y2" class="form-control" autofocus>
</div>
<div class="form-group ml-1">
<label for="mon2">Months</label>
<input type="number" min="0" v-model="mon2" name="mon2" class="form-control">
</div>
<div class="form-group ml-1">
<label for="d2">Days</label>
<input type="number" min="0" v-model="d2" name="d2" class="form-control">
</div>
<div class="form-group ml-1">
<label for="h2">Hours</label>
<input type="number" min="0" v-model="h2" name="h2" class="form-control">
</div>
<div class="form-group ml-1">
<label for="m2">Minutes</label>
<input type="number" min="0" v-model="m2" name="m2" class="form-control">
</div>
<div class="form-group ml-1">
<label for="s2">Seconds</label>
<input type="number" min="0" v-model="s2" name="s2" class="form-control">
</div>
<div class="form-group ml-1">
<label>&nbsp;</label>
<div class="input-group">
<button type="button" @click="todaydate2()" class="btn btn-sm btn-light mt-1">Now</button>
</div>
</div>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-primary" @click="calculate()"><span>=</span> Calculate</button>
<button type="button" @click="reset()" title="Reset" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-row">
<div class="form-group ml-1">
<label for="y">Years</label>
<input type="number" min="0" v-model="y" name="y" class="form-control" readonly>
</div>
<div class="form-group ml-1">
<label for="mon">Months</label>
<input type="number" min="0" v-model="mon" name="mon" class="form-control" readonly>
</div>
<div class="form-group ml-1">
<label for="d">Days</label>
<input type="number" min="0" v-model="d" name="d" class="form-control" readonly>
</div>
<div class="form-group ml-1">
<label for="h">Hours</label>
<input type="number" min="0" v-model="h" name="h" class="form-control" readonly>
</div>
<div class="form-group ml-1">
<label for="m">Minutes</label>
<input type="number" min="0" v-model="m" name="m" class="form-control" readonly>
</div>
<div class="form-group ml-1">
<label for="s">Seconds</label>
<input type="number" min="0" v-model="s" name="s" class="form-control" readonly>
</div>
</div>

</form>

<br>
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
              <span class="w3-large"><a class="removelink" href="/date-calculator"> Date calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/age-calculator"> Age calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/birthday-calculator"> Birthday calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/age-calculator"> Age calculator</a></span><br>
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
      title: 'Time calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Add and subtract time.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/time-calculator'}
  ],
  script: [
    {src: 'https://cdnjs.cloudflare.com/ajax/libs/dayjs/1.10.7/dayjs.min.js', integrity: 'sha512-bwD3VD/j6ypSSnyjuaURidZksoVx3L1RPvTkleC48SbHCZsemT3VKMD39KknPnH728LLXVMTisESIBOAb5/W0Q==', crossorigin: 'anonymous', referrerpolicy: 'no-referrer'},
    {src: 'https://cdn.jsdelivr.net/npm/moment@2.29.1/moment.min.js'}
  ]
    }
    },
  data(){
    return {
d1: '',
mon1: '',
h2: '',
mon2: '',
s2: '',
h1: '',
mt1: '',
dt1: '',
s1: '',
wd2: '',
m1: '',
y1: '',
d2: '',
m2: '',
y2: '',
y: '',
age: '',
day1: '',
weeks: '',
days: '',
op: '+ Add',
d: '',
mon: '',
h: '',
m: '',
s: ''
      }
  },
  methods: {
    todaydate1(){
      var now = moment();
var y=now.year();
var m=now.month()+1;
var d=now.date();
var h=now.hour();
var mm = now.minute();
var s = now.second();
this.y1 = y;

this.mon1 = m;
this.d1 = d;
this.h1 = h;
this.m1 = mm;
this.s1 = s;
    },
    todaydate2(){
      var now = moment();
var y=now.year();
var m=now.month()+1;
var d=now.date();
var h=now.hour();
var mm = now.minute();
var s = now.second();
this.y2 = y;

this.mon2 = m;
this.d2 = d;
this.h2 = h;
this.m2 = mm;
this.s2 = s;
    },
    reset(){
      this.d1 = "";
      this.mon1 = "";
      this.h2 = "";
      this.mon2 = "";
      this.s2 = "";
      this.h1 = "";
      this.mt1 = "";
      this.dt1 = "";
      this.s1 = "";
      this.wd2 = "";
      this.m1 = "";
      this.y1 = "";
      this.d2 = "";
      this.m2 = "";
      this.y2 = "";
      this.y = "";
      this.age = "";
      this.day1 = "";
      this.weeks = "";
      this.days = "";
      this.op = "+ Add";
      this.d = "";
      this.mon = "";
      this.h = "";
      this.m = "";
      this.s = "";
    },
calculate (){
  var y1= this.y1;
  var mon1=this.mon1;
  var d1=this.d1;
  var h1=this.h1;
  var m1=this.m1;
  var s1=this.s1;
  var y2=this.y2;
  var mon2=this.mon2;
  var d2=this.d2;
  var h2=this.h2;
  var m2=this.m2;
  var s2=this.s2;
  if( y1=='' ) y1='0';
  if( mon1=='' ) mon1='0';
  if( d1=='' ) d1='0';
  if( h1=='' ) h1='0';
  if( m1=='' ) m1='0';
  if( s1=='' ) s1='0';
  if( y2=='' ) y2='0';
  if( mon2=='' ) mon2='0';
  if( d2=='' ) d2='0';
  if( h2=='' ) h2='0';
  if( m2=='' ) m2='0';
  if( s2=='' ) s2='0';
  y1=parseFloat(y1);
  mon1=parseFloat(mon1);
  d1=parseFloat(d1);
  h1=parseFloat(h1);
  m1=parseFloat(m1);
  s1=parseFloat(s1);
  y2=parseFloat(y2);
  mon2=parseFloat(mon2);
  d2=parseFloat(d2);
  h2=parseFloat(h2);
  m2=parseFloat(m2);
  s2=parseFloat(s2);
  var d1=moment.duration({seconds:s1, minutes:m1, hours:h1, days:d1, months:mon1, years:y1});
  var d2=moment.duration({seconds:s2, minutes:m2, hours:h2, days:d2, months:mon2, years:y2});
  var dur;
  if( this.op=="+ Add" )
     dur=d1.add(d2);
  else
     dur=d1.subtract(d2);
  var y=dur.years();
  var mon=dur.months();
  var d=dur.days();
  var h=dur.hours();
  var m=dur.minutes();
  var s=dur.seconds();
  this.y = y;
  this.mon = mon;
  this.d = d;
  this.h = h;
  this.m = m;
  this.s = s;
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
.btn span { font-weight:bold; font-size:large; color: #ADD8E6; }

@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #thisonesi { padding:20px; max-width:600px; background:#ADD8E6; border-radius:7px; }
    .btn span { font-weight:bold; font-size:large; }
    @media all and (max-width: 800px) {
       #thisonesi { padding:10px; }
    }
 }
 h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h4 { font-size:1.2rem; }
#thisonesi { padding:20px; max-width:630px; background:#ADD8E6; }
#thisonesi input[type=number] { max-width:85px; }
.btn span { font-size:large; font-weight:bold; }
#wrapper td {
     padding-left:1px;
     padding-right:1px;
 }
</style>
