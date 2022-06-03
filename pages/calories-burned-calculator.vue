<template lang="html">
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

  <div class="w3-row">

  <!-- Blog entries -->
  <div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; Calculate burned calories <hr>
    <h1 class="w3-text-teal"><b>Calories Burned Calculator</b></h1>
<p>An online tool to calculate calories burned after doing indoor, outdoor, walking, swimming, running, training, and sports activities.</p>
<Adsense
class="adsbygoogle infeed"
style="display:block"
data-ad-client="ca-pub-6829148792481216"
data-ad-slot="4199493091"
data-ad-format="auto"
data-full-width-responsive="true">
</Adsense>
    <form id="desingiput" name="desingiput" autocomplete="off">
<div class="form-group">
<label>Select Your activity</label>
<div class="input-group-append">
<select v-model="countryprice" class="form-control" @change="cosvaluechange()">
<option>-- select --</option>
<option>Walking, swimming, running, and Cycling</option>
<option>Gym exercise</option>
<option>Training and sports</option>
<option>Outdoor activities</option>
<option>Indoor and daily activities</option>
</select>
</div><br>
<div class="form-group" v-if="walkselect === true">
<label>Select another activity:</label>
<div class="input-group-append">
  <select class="form-control" v-model="activity1" @change="cosvaluechange()">
  <option>-- select --</option>
  <option value="6.8">Slow walking</option>
  <option value="12">Fast walking</option>
  <option value="8.97">Walking Moderate</option>
  <option value="20.16">Hiking</option>
  <option value="26.86">Jogging</option>
  <option value="41.97">Running fast</option>
  <option value="34.41">Running moderate</option>
  <option value="26.86">Slow cycling</option>
  <option value="40.30">Fast cycling</option>
  <option value="33.58">Moderate cycling</option>
    <option value="28.55">Mountain cycling</option>
  <option value="20">Swimming Moderate</option>
  <option value="33">Swimming Laps</option>
  </select>
</div>
</div>
<div class="form-group" v-if="gymexercise === true">
<label>Select a Gym activity:</label>
<div class="input-group-append">
  <select class="form-control" v-model="activity2" @change="cosvaluechange()">
  <option>-- select --</option>
  <option value="33">Aerobics, Step: high impact</option>
  <option value="23">Aerobics, Step: low impact</option>
  <option value="18">Aerobics: low impact</option>
  <option value="23">Aerobics: high impact</option>
  <option value="13">Aerobics: water</option>
  <option value="23">Cycling, stationary: moderate</option>
  <option value="32">Cycling, stationary: vigorous</option>
  <option value="15">calisthenics: moderate</option>
  <option value="27">calisthenics: vigorous</option>
  <option value="26">circuit training: general</option>
  <option value="30">Elliptical trainer: general</option>
  <option value="23">Rowing, stationary: moderate</option>
  <option value="34">Rowing, stationary: vigorous</option>
  <option value="23">Ski machine: general</option>
  <option value="20">stair step machine: general</option>
    <option value="13">Stretching, Hatha Yoga</option>
    <option value="10">Weight Lifting: general</option>
    <option value="20">Weight Lifting: vigorous</option>
  </select>
</div>
</div>
<div class="form-group" v-if="sportsshow === true">
<label>Select a Gym activity:</label>
<div class="input-group-append">
  <select class="form-control" v-model="activity3" @change="cosvaluechange()">
  <option>-- select --</option>
  <option value="13">Badminton</option>
  <option value="27">Basketball</option>
  <option value="8">Billiards</option>
  <option value="10">Bowling</option>
  <option value="30">Boxing</option>
  <option value="10">Dancing slow</option>
  <option value="20">Dancing fast</option>
  <option value="21">Fencing</option>
  <option value="30">Football</option>
  <option value="10">Frisbee</option>
  <option value="18">Golf</option>
  <option value="13">Gymnastics</option>
  <option value="40">Handball</option>
  <option value="27">Hockey</option>
  <option value="7">Horse Riding</option>
    <option value="23">Ice skating</option>
    <option value="17">Kayaking</option>
    <option value="23">Racquetball</option>
    <option value="27">Rock climbing: Rappelling</option>
    <option value="26">Rock climbing: ascending</option>
    <option value="36">Rollerblading</option>
    <option value="39">Skating</option>
    <option value="40">Fast Rope Jumping</option>
    <option value="27">Slow Rope Jumping</option>
    <option value="34">Rugby</option>
    <option value="24">Scuba diving</option>
    <option value="17">Skateboarding</option>
    <option value="23">Skiing</option>
    <option value="23">Sledding</option>
    <option value="27">Snow shoeing</option>
    <option value="24">Soccer</option>
    <option value="13">Tai Chi</option>
    <option value="23">Tennis</option>
    <option value="27">Beach Volleyball</option>
    <option value="10">General play Volleyball</option>
    <option value="34">Water polo</option>
    <option value="20">Water Skiing</option>
    <option value="10">Water Volleyball</option>
    <option value="17">Whitewater rafting</option>
    <option value="20">Wrestling</option>
    </select>
</div>
</div>
<div class="form-group" v-if="outdoor === true">
<label>Select an Outdoor activity:</label>
<div class="input-group-append">
  <select class="form-control" v-model="activity4" @change="cosvaluechange()">
  <option>-- select --</option>
  <option value="17">Carrying wood</option>
  <option value="20">Chopping wood</option>
  <option value="15">Fishing</option>
  <option value="16">Gardening</option>
  <option value="18">Mowing Lawn Hand</option>
  <option value="15">Mowing Lawn Machine</option>
  <option value="14">Operate snow Blower</option>
  <option value="14">Raking lawn</option>
  <option value="20">Shoveling snow</option>
    </select>
</div>
</div>
<div class="form-group" v-if="indoor === true">
<label>Select an indoor/daily activity:</label>
<div class="input-group-append">
  <select class="form-control" v-model="activity5" @change="cosvaluechange()">
  <option>-- select --</option>
  <option value="7">Cooking</option>
  <option value="10">Food shopping</option>
  <option value="15">Heavy Cleaning: car wash etc</option>
  <option value="23">Moving: Carrying boxes</option>
  <option value="20">Moving furniture</option>
  <option value="17">Paint, remodel</option>
  <option value="13">Playing with kids</option>
  <option value="4">Reading and Sitting</option>
  <option value="2">Sleeping</option>
  <option value="4">Standing in queue</option>
  <option value="3.1">Watching TV</option>
    </select>
</div>
</div>
<div class="form-group">
<label>Enter time:</label>
<div class="input-group">
<input type="number" v-model="hours" class="form-control" placeholder="Hours" required>
<div class="input-group-append">
<input type="number" v-model="minutes" class="form-control" placeholder="Minutes" required>
</div>
</div>
</div>
<div class="form-group">
<label>Body weight:</label>
<div class="input-group">
<input type="number" v-model="bodyweight" class="form-control" required>
<div class="input-group-append">
<select v-model="weighttype" class="form-control">
<option selected>KG</option>
<option>Pounds</option>
</select>
</div>
</div>
</div>
</div>
<div class="form-group">
<button type="button" title="Calculate" class="btn btn-secondary" @click="cosvaluechange()"><span>=></span> Answer</button>
</div>
<div class="form-group">
<label>Total calories burned:</label>
<div class="input-group">
<input type="text" v-model="answer" class="form-control" readonly>
</div>
</div>
</form><br>
      </div>
        </div>
  <hr>

  </div>


  <!-- Introduction menu -->

  <!-- END GRID -->
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
  </div><br>

  <!-- END w3-content -->
  </div>

  <!-- Footer -->
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
      title: 'Calories burned calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Calculate how much calories did you burn after doing different activites like training, sports, gyming, walking, running, swimming, cycling.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/electronics/calories-burned-calculator'}
    ]
    }
    },
  data(){
    return {
      sportsshow: false,
      indoor: false,
      activity5: '',
      outdoor: false,
      activity4: '',
      activity3: '',
      activity2: '',
      walkselect: false,
      hours: null,
      minutes: null,
      countryprice: '',
      activity1: '',
      currenttype: 'DC',
      powerfactor: false,
      threephase: false,
      amperselect: 'A',
      voltagechange: 'Watts',
      kw: '',
      w: '',
      mw: '',
      number1: '',
      number2: '',
      powerfactorinput: '',
      voltagetype: 'Line to line voltage',
      cosvalue: '',
      bodyweight: null,
      weighttype: 'KG',
      hours: null,
      minutes: null,
      answer: null,
      gymexercise: false
    }
  },
  methods: {
    cosvaluechange(){
      if(this.weighttype === "Pounds"){
        this.bodyweight = 0.453592*this.bodyweight;
        this.weighttype === "KG";
      }
      if(this.countryprice === "Walking, swimming, running, and Cycling"){
      this.walkselect = true;
      this.gymexercise = false;
      this.sportsshow = false;
      this.outdoor = false;
        this.indoor = false;
      var activity1 = this.activity1;
      var bodyweight = this.bodyweight;
      var weighttype = this.weighttype;
var hours = this.hours;
var minutes = this.minutes;
var totaltime = parseFloat(hours * 60) + parseFloat(minutes);
var answer = totaltime * activity1 * bodyweight;
this.answer = answer/200;
}
else if(this.countryprice === "Gym exercise"){
this.walkselect = false;
this.gymexercise = true;
this.outdoor = false;
this.sportsshow = false;
  this.indoor = false;
var activity1 = this.activity2;
var bodyweight = this.bodyweight;
var weighttype = this.weighttype;
var hours = this.hours;
var minutes = this.minutes;
var totaltime = parseFloat(hours * 60) + parseFloat(minutes);
var answer = totaltime * activity1 * bodyweight;
this.answer = answer/200;
}
else if(this.countryprice === "Training and sports"){
  this.walkselect = false;
  this.gymexercise = false;
  this.sportsshow = true;
  this.outdoor = false;
    this.indoor = false;
  var activity1 = this.activity3;
  var bodyweight = this.bodyweight;
  var weighttype = this.weighttype;
  var hours = this.hours;
  var minutes = this.minutes;
  var totaltime = parseFloat(hours * 60) + parseFloat(minutes);
  var answer = totaltime * activity1 * bodyweight;
  this.answer = answer/200;
}
else if(this.countryprice === "Outdoor activities"){
  this.walkselect = false;
  this.gymexercise = false;
  this.sportsshow = false;
  this.outdoor = true;
  this.indoor = false;
  var activity1 = this.activity4;
  var bodyweight = this.bodyweight;
  var weighttype = this.weighttype;
  var hours = this.hours;
  var minutes = this.minutes;
  var totaltime = parseFloat(hours * 60) + parseFloat(minutes);
  var answer = totaltime * activity1 * bodyweight;
  this.answer = answer/200;
}
else if(this.countryprice === "Indoor and daily activities"){
  this.walkselect = false;
  this.gymexercise = false;
  this.sportsshow = false;
  this.outdoor = false;
  this.indoor = true;
  var activity1 = this.activity5;
  var bodyweight = this.bodyweight;
  var weighttype = this.weighttype;
  var hours = this.hours;
  var minutes = this.minutes;
  var totaltime = parseFloat(hours * 60) + parseFloat(minutes);
  var answer = totaltime * activity1 * bodyweight;
  this.answer = answer/200;
}
    },
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

#desingiput { background:#a7c9b8; padding:20px; }
.btn span { font-weight: bold; font-size:large; }
/*.btn b, .btn b2 { font-size:large; }*/
@media all and (max-width: 800px) {
}
</style>
