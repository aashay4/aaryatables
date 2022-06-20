<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Birthday calculator<hr>
          <h1 class="w3-text-teal"><b>Birthday calculator</b></h1>
          <p>Calculate total months and days remaining for your birthday with this free online birth day calculator.</p>
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

  <div id="datediv1" class="form-group">
  <label>Date of birth</label>
  <div class="form-row">
  <div class="col-4 order-1">
  <select v-model="m1" class="form-control">
  <option>month</option>
  <option>January</option>
  <option>February</option>
  <option>March</option>
  <option>April</option>
  <option>May</option>
  <option>June</option>
  <option>July</option>
  <option>August</option>
  <option>September</option>
  <option>October</option>
  <option>November</option>
  <option>December</option>
  </select>
  </div>

  <div id="daysdiv1" class="col-3 order-2">
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
  </div>
  <div class="form-group">
  <button type="button" @click="calculate()" class="btn btn-success"><span>= ></span> Calculate</button>
  <button type="reset" class="btn btn-secondary"><span>&times;</span> Reset</button>
  </div>
  <div id="datediv2" class="form-group">
  <label>Date of next birthday</label>
  <div class="form-row">
  <div class="col-3 order-1">
  <select v-model="wd2" readonly class="form-control form-control-lg">
  <option>day of week</option>
  <option value="1">Sun</option>
  <option value="2">Mon</option>
  <option value="3">Tue</option>
  <option value="4">Wed</option>
  <option value="5">Thu</option>
  <option value="6">Fri</option>
  <option value="7">Sat</option>
  </select>
  </div>
  <div class="col-3 order-2">
  <select v-model="m2" readonly class="form-control form-control-lg">
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
  <input type="number" v-model="d2" placeholder="day" readonly class="form-control form-control-lg">
  </div>
  <div class="col-3 order-4">
  <input type="number" v-model="y2" placeholder="year" readonly class="form-control form-control-lg">
  </div>
  </div>
  </div>
  <div class="form-group">
  <label>Your Age at your next birthday</label>
  <input type="text" v-model="age" readonly class="form-control form-control-lg">
  </div>
  <div id="timediv1" class="form-group mb-0">
  <label>Time to next birthday</label>
  <div class="form-row">
  <div class="form-group col">
  <label>Months</label>
  <input type="number" min="0" v-model="mt1" placeholder="months" readonly class="form-control">
  </div>
  <div class="form-group col">
  <label>Days</label>
  <input type="number" min="0" v-model="dt1" placeholder="days" readonly class="form-control">
  </div>
  </div>
  </div>
  <div class="form-group">
  <label>Weeks only</label>
  <input type="text" v-model="weeks" placeholder="weeks" readonly class="form-control">
  </div>
  <div class="form-group">
  <label>Days only</label>
  <input type="text" v-model="days" placeholder="days" readonly class="form-control">
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
      title: 'An online birthday colculator tool.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculate total days remaining for your birthday.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/birthday-calculator'}
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
mt1: '',
dt1: '',
wd2: '',
m1: '',
y1: '',
d2: '',
m2: '',
y2: '',
age: '',
day1: '',
weeks: '',
days: ''
      }
  },
  methods: {
    reset(){
      this.d1 = "";
      this.m1 = "";
      this.y1 = "";
      this.d2 = "";
      this.m2 = "";
      this.y2 = "";
      this.age = "";
      this.days = "";
    },
calculate (){
  var y1= this.y1;
  var m1= this.m1;
  var d1= this.d1;
  var t1=moment().year(y1).month(m1).date(d1);
  var now = moment();
  var age = moment.duration(now.diff(t1)).add(1,'years');
  var years = moment().diff(t1, 'years');
  var adjust = (m1==now.months() && d1==now.date())?0:1;
  var t2=t1.add(years+adjust, 'years');
  this.y2 = t2.year();
  this.m2 = t2.month()+1;
  this.d2 = t2.date();
  this.wd2 = t2.day()+1;
  this.age = Math.floor(age.asYears());

  var d=moment.duration(t2.diff(now));
  this.mt1 = d.months();
  this.dt1 = d.days();
  this.weeks = d.asWeeks().toFixed(2);
  this.days = Math.round(d.asDays());
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
.btn span { font-weight:bold; font-size:large; color: #eee8d5; }

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
