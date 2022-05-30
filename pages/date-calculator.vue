<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Date calculator<hr>
          <h1 class="w3-text-teal"><b>+/- Date Calculator</b></h1>
          <p>Add/Subtract dates.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">
  <form id="designform" autocomplete="off">

<div v-model="datediv1" class="form-group">
<label>Date</label>
<div class="form-row">
<div class="col-4 order-1">
<select v-model="m1" class="form-control">
<option>month</option>
<option value="1">January</option>
<option value="2">February</option>
<option value="3">March</option>
<option value="4">April</option>
<option value="5">May</option>
<option value="6">June</option>
<option value="7">July</option>
<option value="8">August</option>
<option value="9">September</option>
<option value="10">October</option>
<option value="11">November</option>
<option value="12">December</option>
</select>
</div>

<div v-model="daysdiv1" class="col-3 order-2">
<select v-model="d1" class="form-control">
<option>day</option>
<option>1</option>
<option>2</option>
<option>3</option>
<option>4</option>
<option>5</option>
<option>6</option>
<option>7</option>
<option>8</option>
<option>9</option>
<option>10</option>
<option>11</option>
<option>12</option>
<option>13</option>
<option>14</option>
<option>15</option>
<option>16</option>
<option>17</option>
<option>18</option>
<option>19</option>
<option>20</option>
<option>21</option>
<option>22</option>
<option>23</option>
<option>24</option>
<option>25</option>
<option>26</option>
<option>27</option>
<option>28</option>
<option>29</option>
<option>30</option>
<option>31</option>
</select>
</div>
<div class="col-3 order-3">
<input type="number" v-model="y1" placeholder="year" class="form-control">
</div>
</div>
<div class="col order-5 pl-0">
<button type="button" @click="todaydate()" class="btn btn-sm btn-light mt-1">Today</button>
</div>
</div>
<div class="form-group">
<select v-model="opsel" class="form-control">
<option value="+ Add">+ Add</option>
<option value="- Subtract">- Subtract</option>
</select>
</div>
<div id="timediv1" class="form-group">
<label>Time duration</label>
<div class="form-row">
<div class="form-group col">
<label>Years</label>
<input type="number" min="0" v-model="yt1" placeholder="years" class="form-control">
</div>
<div class="form-group col">
<label>Months</label>
<input type="number" min="0" v-model="mt1" placeholder="months" class="form-control">
</div>
<div class="form-group col">
<label>Weeks</label>
<input type="number" min="0" v-model="wt1" placeholder="weeks" class="form-control">
</div>
<div class="form-group col">
<label>Days</label>
<input type="number" min="0" v-model="dt1" placeholder="days" class="form-control">
</div>
</div>
</div>
<div class="form-group">
<button type="button" @click="answer()" class="btn btn-success"><span>=</span> Calculate</button>
<button type="reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<label>Date result</label>
<div class="form-row">
<div class="col-3 order-1">
<select v-model="wd2" readonly class="form-control">
<option>day of week</option>
<option value="2">Sun</option>
<option value="3">Mon</option>
<option value="4">Tue</option>
<option value="5">Wed</option>
<option value="6">Thu</option>
<option value="7">Fri</option>
<option value="1">Sat</option>
</select>
</div>
<div class="col-3 order-2">
<select v-model="m2" readonly class="form-control">
<option>month</option>
<option value="1">January</option>
<option value="2">February</option>
<option value="3">March</option>
<option value="4">April</option>
<option value="5">May</option>
<option value="6">June</option>
<option value="7">July</option>
<option value="8">August</option>
<option value="9">September</option>
<option value="10">October</option>
<option value="11">November</option>
<option value="12">December</option>
</select>
</div>
<div id="daysdiv2" class="col-3 order-3">
<input type="number" v-model="d2" placeholder="day" readonly class="form-control">
</div>
<div class="col-3 order-4">
<input type="number" v-model="y2" placeholder="year" readonly class="form-control">
</div>
</div>
</div>

</form><br>

  <h4>Get total days between 2 dates</h4>
  <p>To calculate days between 2 dates, select date, year and month. Once selected, just click on the calculate button.</p>
  <form id="designform" autocomplete="off">

  <div class="form-group">
  <label>First date</label>
  <div class="form-row">
  <div class="col-4 order-1">
  <select v-model="m3" class="form-control">
  <option>month</option>
  <option value="1">January</option>
  <option value="2">February</option>
  <option value="3">March</option>
  <option value="4">April</option>
  <option value="5">May</option>
  <option value="6">June</option>
  <option value="7">July</option>
  <option value="8">August</option>
  <option value="9">September</option>
  <option value="10">October</option>
  <option value="11">November</option>
  <option value="12">December</option>
  </select>
  </div>
  <div class="col-3 order-2">
  <select v-model="d3" class="form-control">
  <option>day</option>
  <option>1</option>
  <option>2</option>
  <option>3</option>
  <option>4</option>
  <option>5</option>
  <option>6</option>
  <option>7</option>
  <option>8</option>
  <option>9</option>
  <option>10</option>
  <option>11</option>
  <option>12</option>
  <option>13</option>
  <option>14</option>
  <option>15</option>
  <option>16</option>
  <option>17</option>
  <option>18</option>
  <option>19</option>
  <option>20</option>
  <option>21</option>
  <option>22</option>
  <option>23</option>
  <option>24</option>
  <option>25</option>
  <option>26</option>
  <option>27</option>
  <option>28</option>
  <option>29</option>
  <option>30</option>
  <option>31</option>
  </select>
  </div>
  <div class="col-3 order-3">
  <input type="number" v-model="y3" placeholder="year" class="form-control">
  </div>
  </div>
  <div class="col order-5 pl-0">
  <button type="button" @click="todaydate1()" class="btn btn-sm btn-light mt-1">Today</button>
  </div>
  </div>
  <div class="form-group">
  <label>Second date</label>
  <div class="form-row">
  <div class="col-4 order-1">
  <select v-model="m4" class="form-control">
  <option>month</option>
  <option value="1">January</option>
  <option value="2">February</option>
  <option value="3">March</option>
  <option value="4">April</option>
  <option value="5">May</option>
  <option value="6">June</option>
  <option value="7">July</option>
  <option value="8">August</option>
  <option value="9">September</option>
  <option value="10">October</option>
  <option value="11">November</option>
  <option value="12">December</option>
  </select>
  </div>
  <div class="col-3 order-2">
  <select v-model="d4" class="form-control">
  <option>day</option>
  <option>1</option>
  <option>2</option>
  <option>3</option>
  <option>4</option>
  <option>5</option>
  <option>6</option>
  <option>7</option>
  <option>8</option>
  <option>9</option>
  <option>10</option>
  <option>11</option>
  <option>12</option>
  <option>13</option>
  <option>14</option>
  <option>15</option>
  <option>16</option>
  <option>17</option>
  <option>18</option>
  <option>19</option>
  <option>20</option>
  <option>21</option>
  <option>22</option>
  <option>23</option>
  <option>24</option>
  <option>25</option>
  <option>26</option>
  <option>27</option>
  <option>28</option>
  <option>29</option>
  <option>30</option>
  <option>31</option>
  </select>
  </div>
  <div class="col-3 order-3">
  <input type="number" v-model="y4" placeholder="year" class="form-control">
  </div>
  </div>
  <div class="col order-5 pl-0">
  <button type="button" @click="todaydate2()" class="btn btn-sm btn-light mt-1">Today</button>
  </div>
  </div>
  <div class="form-group">
  <button type="button" @click="finddays()" class="btn btn-success"><span>= ></span> Calculate</button>
  <button type="reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
  </div>
  <div id="timediv2" class="form-group">
  <label>Result for total time duration.</label>
  <div class="form-row">
  <div class="form-group col mb-0">
  <label>Years</label>
  <input type="text" v-model="yt2" placeholder="years" readonly class="form-control">
  </div>
  <div class="form-group col mb-0">
  <label>Months</label>
  <input type="text" v-model="mt2" placeholder="months" readonly class="form-control">
  </div>

  <div class="form-group col mb-0">
  <label>Days only</label>
  <input type="text" v-model="dt2" placeholder="days" readonly class="form-control">
  </div>
  </div>
  </div>
  <div class="form-group">
  <label>Days</label>
  <input type="text" v-model="days" placeholder="Answer in days" readonly class="form-control">
  </div>
  <div class="form-group">
  <label>Hours</label>
  <input type="text" v-model="hours" placeholder="Answer in hours" readonly class="form-control">
  </div>
  <div class="form-group">
  <label>Seconds</label>
  <input type="text" v-model="seconds" placeholder="Answer in seconds" readonly class="form-control">
  </div>
  </form>

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
              <span class="w3-large"><a class="removelink" href="/unit-conversion"> Unit Conversion</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/random-letter-generator"> Random letter generator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/word-counter"> Word counter</a></span><br>
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
      title: 'Date calculator for free.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Date calculator.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/date-calculator'}
  ],
  script: [
    {src: 'https://cdn.jsdelivr.net/npm/moment@2.29.1/moment.min.js'}
  ]
    }
    },
  data(){
    return {
datediv1: '',
m1: '',
daysdiv1: '',
d1: '',
y1: '',
y2: '',
m2: '',
d2: '',
wd2: '',
yt1: '',
mt1: '',
  wt1: '',
  dt1: '',
  y3: '',
  m3: '',
  d3: '',
  y4: '',
  m4: '',
  d4: '',
  yt2: '',
  mt2: '',
  dt2: '',
  days: '',
  hours: '',
  seconds: '',
  picker1btn: '',
  picker3btn: '',
  picker4btn: '',
    now1: '',
    now3: '',
      now4: '',
      opsel: '+ Add'
      }
  },
  methods: {
    reset(){
      this.datediv1 = "";
      this.m1 = "";
      this.daysdiv1 = "";
      this.d1 = "";
      this.y1 = "";
      this.y2 = "";
      this.m2 = "";
      this.d2 = "";
      this.wd2 = "";
      this.yt1 = "";
      this.mt1 = "";
        this.wt1 = "";
        this.dt1 = "";
        this.y3 = "";
        this.m3 = "";
        this.d3 = "";
        this.y4 = "";
        this.m4 = "";
        this.d4 = "";
        this.yt2 = "";
        this.mt2 = "";
        this.dt2 = "";
        this.days = "";
        this.hours = "";
        this.seconds = "";
        this.picker1btn = "";
        this.picker3btn = "";
        this.picker4btn = "";
          this.now1 = "";
          this.now3 = "";
            this.now4 = "";
            this.opsel = "+ Add";
    },
    todaydate1(){
      var now = moment();
var y=now.year();
var m=now.month()+1;
var d=now.date();
this.m3 = m;
this.d3 = d;
this.y3 = y;
    },
    finddays(){
      var y3=this.y3;
var m3=this.m3;
var d3=this.d3;
var y4=this.y4;
var m4=this.m4;
var d4=this.d4;
var time1=moment().year(y3).month(m3).date(d3);
var time2=moment().year(y4).month(m4).date(d4);
var duration = moment.duration(Math.abs(time1.diff(time2))+1);
this.yt2 = duration.years();
this.mt2 = duration.months();
this.dt2 = duration.days();
this.days = Math.round(duration.asDays());
this.hours = Math.round(duration.asHours());
this.seconds = Math.round(duration.asSeconds());

    },
    todaydate2(){
      var now = moment();
var y=now.year();
var m=now.month()+1;
var d=now.date();
this.m4 = m;
this.d4 = d;
this.y4 = y;
    },
    unitclicked(){
        this.showunits = true;
        this.showmetric = false;
        this.isMetric = false;
    },
    metricclicked(){
        this.showmetric = true;
      this.showunits = false;
this.isMetric = true;
    },
    todaydate(){
      var now = moment();
var y=now.year();
var m=now.month()+1;
var d=now.date();
this.m1 = m;
this.d1 = d;
this.y1 = y;
    },
    answer(){
    var y1=this.y1;
    var m1=this.m1;
    var d1=this.d1;
    var t=moment().year(y1).month(m1).date(d1);
    var y2=this.yt1;
    var m2=this.mt1;
    var w2=this.wt1;
    var d2=this.dt1;
    var i=this.opsel;
    if( i=="+ Add" )
    {
       t.add(y2, 'years').add(m2, 'months').add(w2, 'weeks').add(d2, 'days');
}
    else
    {
       t.subtract(y2, 'years').subtract(m2, 'months').subtract(w2, 'weeks').subtract(d2, 'days');
     }
    this.y2 = t.year();
    this.m2 = t.month();
    this.d2 = t.date();
    this.wd2 = t.day();
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
 #wrapper td { padding:.75rem; }
#designform {
   padding:15px;
   background:#a7c9b8;
   border:1px solid #eee;
   border-radius:7px;
   max-width:500px;
}
.btn span { font-weight:bold; font-size:large; }

@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #calcform, #calcform2 { padding:20px; max-width:600px; background:#eee8d5; border-radius:7px; }
    #picker1btn img, #picker3btn img, #picker4btn img { opacity:0.7; }
    #picker1txt, #picker3txt, #picker4txt { display:none; }
    #wrapper TD { padding-left:unset; padding-right:unset; }
    .qs-datepicker-container { top:40px !important; left:-225px !important; }
    .btn span { font-weight:bold; font-size:large; }
    @media all and (max-width: 800px) {
       #calcform, #calcform2 { padding:10px; }
    }

 }
</style>
