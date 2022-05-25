<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Age calculator<hr>
          <h1 class="w3-text-teal"><b>Calculate age online</b></h1>
          <p>Enter your birth date and current date to find the accurate age.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">
  <form id="designform" name="designform" autocomplete="off">
  <div id="datediv1" class="form-group">
  <label>Enter your date of birth:</label>
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
  <div id="datediv2" class="form-group">
  <label>Enter date to calculate</label>
  <div class="form-row">
  <div class="col-4 order-1">
  <select v-model="m2" class="form-control">
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

  <div id="daysdiv2" class="col-3 order-2">
  <select v-model="d2" class="form-control">
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
  <input type="number" v-model="y2" placeholder="year" class="form-control">
  </div>
  </div>
  </div>
  <div class="form-group">
  <button type="button" title="Calculate" class="btn btn-success" @click="calcage()"><span>= ></span> Calculate</button>
  <button type="reset" title="Reset" @click="reset()" class="btn btn-secondary"><span>&times;</span> Reset</button>
  </div>
  <div class="form-group">
  <label>Age result</label>
  <textarea rows="6" v-model="age" name="age" class="form-control" readonly></textarea>
  </div>
</form><br>
  <h1 style="color: teal;">How to use this age calculator?</h1>
  <p>To use this age calculation tool, just select two dates, months and years and click on the calculate button. Once clicked on the button, you will get an answer in less than one second.</p>
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
      title: 'Age calculator - Calculate age from the birthday',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculate age with days, months, hours, minutes and seconds.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/age-calculator'}
  ],
  script: [
    {src: 'https://cdnjs.cloudflare.com/ajax/libs/dayjs/1.10.7/dayjs.min.js', integrity: 'sha512-bwD3VD/j6ypSSnyjuaURidZksoVx3L1RPvTkleC48SbHCZsemT3VKMD39KknPnH728LLXVMTisESIBOAb5/W0Q==', crossorigin: 'anonymous', referrerpolicy: 'no-referrer'}
  ]
    }
    },
  data(){
    return {
d1: '',
m1: '',
y1: '',
d2: '',
m2: '',
y2: '',
age: ''
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
    },
calcage (){
  var txt;
  var day1=this.d1;
  var month1=this.m1;
  var year1=this.y1;
if( year1=='' ) year1="1990";
  var day2=this.d2;
  var month2=this.m2;
  var year2=this.y2;
var d1 = dayjs([year1, month1, day1]);
var d2 = dayjs([year2, month2, day2]);
var years = d2.diff(d1, 'years');
var months = d2.diff(d1, 'months')-years*12;
var d3 = d1.add(years,'years').add(months,'months');
var days = d2.diff(d3, 'days');
txt = years+(years==1?" year, ":" years, ")+months+(months==1?" month, ":" months, ")+days+(days==1?" day":" days");
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'years', true)).toFixed(2)+" years";
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'months', true)).toFixed(2)+" months";
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'weeks', true)).toFixed(2)+" weeks";
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'days', true)).toFixed(0)+" days";
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'hours', true)).toFixed(0)+" hours";
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'minutes', true)).toFixed(0)+" minutes";
d1 = dayjs([year1, month1, day1]);
d2 = dayjs([year2, month2, day2]);
txt+= "\n= "+(d2.diff(d1, 'seconds', true)).toFixed(0)+" seconds";
  this.age=txt;

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
