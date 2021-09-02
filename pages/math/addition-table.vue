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
          <a href="/">Home</a> &rsaquo; <a href="/math">Math</a> &rsaquo; Addition Table <hr>
      <h1 class="w3-text-teal"><b>Addition Table</b></h1>
      <p>Use this addition table to add two numbers quickly. Click on the two and columns button to add two numbers.</p>
  <form name="additiontable" autocomplete="off">
  <table id="table3" style="margin:0 auto; border-style:none">
  <tr>
  <td><input type="text" name="num1" size="2" class="math" @change="OnButton()" v-model="firsttext"></td>
  <td><b>+</b></td>
  <td><input type="text" name="num2" id="num2" size="2" @change="OnButton1()" v-model="secondtext"></td>
  <td>=</td>
  <td><input type="text" name="result" size="2" v-model="answer" style="width:80px;"></td>
  <td><input type="reset" value="Clear" @click="reset()"></td>
  </tr>
  </table>
</form><br>
  <table id="secondtable" class="secondtable" style="border: 1px #ccc solid; border-collapse: collapse">
  <tr>
  <td class="outsideoftable"><b>+</b></td>
  <td class="outsideoftable" value="1" v-model="upnumber"><button class="w3-teal w3-hover-gray" value="1" @click="OnButton(1)">1</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="2" @click="OnButton(2)">2</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="3" @click="OnButton(3)">3</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="4" @click="OnButton(4)">4</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="5" @click="OnButton(5)">5</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="6" @click="OnButton(6)">6</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="7" @click="OnButton(7)">7</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="8" @click="OnButton(8)">8</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="9" @click="OnButton(9)">9</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="10" @click="OnButton(10)">10</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="11" @click="OnButton(11)">11</button></td>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="12" @click="OnButton(12)">12</button></td>
  </tr>
  <tr>
  <td class="outsideoftable"><button value="1" class="w3-teal w3-hover-gray" @click="OnButton1(1)">1</button></td>
  <td class="insideoftable">1</td>
  <td class="insideoftable">2</td>
  <td class="insideoftable">3</td>
  <td class="insideoftable">4</td>
  <td class="insideoftable">5</td>
  <td class="insideoftable">6</td>
  <td class="insideoftable">7</td>
  <td class="insideoftable">8</td>
  <td class="insideoftable">9</td>
  <td class="insideoftable">10</td>
  <td class="insideoftable">11</td>
  <td class="insideoftable">12</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="2" @click="OnButton1(2)">2</button></td>
  <td class="insideoftable">2</td>
  <td class="insideoftable">4</td>
  <td class="insideoftable">6</td>
  <td class="insideoftable">8</td>
  <td class="insideoftable">10</td>
  <td class="insideoftable">12</td>
  <td class="insideoftable">14</td>
  <td class="insideoftable">16</td>
  <td class="insideoftable">18</td>
  <td class="insideoftable">20</td>
  <td class="insideoftable">22</td>
  <td class="insideoftable">24</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="3" @click="OnButton1(3)">3</button></td>
  <td class="insideoftable">3</td>
  <td class="insideoftable">6</td>
  <td class="insideoftable">9</td>
  <td class="insideoftable">12</td>
  <td class="insideoftable">15</td>
  <td class="insideoftable">18</td>
  <td class="insideoftable">21</td>
  <td class="insideoftable">24</td>
  <td class="insideoftable">27</td>
  <td class="insideoftable">30</td>
  <td class="insideoftable">33</td>
  <td class="insideoftable">36</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="4" @click="OnButton1(4)">4</button></td>
  <td class="insideoftable">4</td>
  <td class="insideoftable">8</td>
  <td class="insideoftable">12</td>
  <td class="insideoftable">16</td>
  <td class="insideoftable">20</td>
  <td class="insideoftable">24</td>
  <td class="insideoftable">28</td>
  <td class="insideoftable">32</td>
  <td class="insideoftable">36</td>
  <td class="insideoftable">40</td>
  <td class="insideoftable">44</td>
  <td class="insideoftable">48</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="5" @click="OnButton1(5)">5</button></td>
  <td class="insideoftable">5</td>
  <td class="insideoftable">10</td>
  <td class="insideoftable">15</td>
  <td class="insideoftable">20</td>
  <td class="insideoftable">25</td>
  <td class="insideoftable">30</td>
  <td class="insideoftable">35</td>
  <td class="insideoftable">40</td>
  <td class="insideoftable">45</td>
  <td class="insideoftable">50</td>
  <td class="insideoftable">55</td>
  <td class="insideoftable">60</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="6" @click="OnButton1(6)">6</button></td>
  <td class="insideoftable">6</td>
  <td class="insideoftable">12</td>
  <td class="insideoftable">18</td>
  <td class="insideoftable">24</td>
  <td class="insideoftable">30</td>
  <td class="insideoftable">36</td>
  <td class="insideoftable">42</td>
  <td class="insideoftable">48</td>
  <td class="insideoftable">54</td>
  <td class="insideoftable">60</td>
  <td class="insideoftable">66</td>
  <td class="insideoftable">72</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="7" @click="OnButton1(7)">7</button></td>
  <td class="insideoftable">7</td>
  <td class="insideoftable">14</td>
  <td class="insideoftable">21</td>
  <td class="insideoftable">28</td>
  <td class="insideoftable">35</td>
  <td class="insideoftable">42</td>
  <td class="insideoftable">49</td>
  <td class="insideoftable">56</td>
  <td class="insideoftable">63</td>
  <td class="insideoftable">70</td>
  <td class="insideoftable">77</td>
  <td class="insideoftable">84</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="8" @click="OnButton1(8)">8</button></td>
  <td class="insideoftable">8</td>
  <td class="insideoftable">16</td>
  <td class="insideoftable">24</td>
  <td class="insideoftable">32</td>
  <td class="insideoftable">40</td>
  <td class="insideoftable">48</td>
  <td class="insideoftable">56</td>
  <td class="insideoftable">64</td>
  <td class="insideoftable">72</td>
  <td class="insideoftable">80</td>
  <td class="insideoftable">88</td>
  <td class="insideoftable">96</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="9" @click="OnButton1(9)">9</button></td>
  <td class="insideoftable">9</td>
  <td class="insideoftable">18</td>
  <td class="insideoftable">27</td>
  <td class="insideoftable">36</td>
  <td class="insideoftable">45</td>
  <td class="insideoftable">54</td>
  <td class="insideoftable">63</td>
  <td class="insideoftable">72</td>
  <td class="insideoftable">81</td>
  <td class="insideoftable">90</td>
  <td class="insideoftable">99</td>
  <td class="insideoftable">108</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="10" @click="OnButton1(10)">10</button></td>
  <td class="insideoftable">10</td>
  <td class="insideoftable">20</td>
  <td class="insideoftable">30</td>
  <td class="insideoftable">40</td>
  <td class="insideoftable">50</td>
  <td class="insideoftable">60</td>
  <td class="insideoftable">70</td>
  <td class="insideoftable">80</td>
  <td class="insideoftable">90</td>
  <td class="insideoftable">100</td>
  <td class="insideoftable">110</td>
  <td class="insideoftable">120</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="11" @click="OnButton1(11)">11</button></td>
  <td class="insideoftable">11</td>
  <td class="insideoftable">22</td>
  <td class="insideoftable">33</td>
  <td class="insideoftable">44</td>
  <td class="insideoftable">55</td>
  <td class="insideoftable">66</td>
  <td class="insideoftable">77</td>
  <td class="insideoftable">88</td>
  <td class="insideoftable">99</td>
  <td class="insideoftable">110</td>
  <td class="insideoftable">121</td>
  <td class="insideoftable">132</td>
  </tr>
  <tr>
  <td class="outsideoftable"><button class="w3-teal w3-hover-gray" value="12" @click="OnButton1(12)">12</button></td>
  <td class="insideoftable">12</td>
  <td class="insideoftable">24</td>
  <td class="insideoftable">36</td>
  <td class="insideoftable">48</td>
  <td class="insideoftable">60</td>
  <td class="insideoftable">72</td>
  <td class="insideoftable">84</td>
  <td class="insideoftable">96</td>
  <td class="insideoftable">108</td>
  <td class="insideoftable">120</td>
  <td class="insideoftable">132</td>
  <td class="insideoftable">144</td>
  </tr>
</table><br>
  <h2>Addition quiz</h2>
  <p>Use the addition table to solve this quiz or solve it on your own. Do not forget the check answers from the table or click on the check answers button.</p>
  <form id="quizform">
  <table id="quiz">
  <tbody>
  <tr>
  <td>{{quiznumber1}}</td>
  <td>+</td>
  <td>{{quiznumber2}}</td>
  <td>=</td>
  <td><input v-model="quizanswer1" type="number" min="0" step="1"></td>
  <td>{{result1}}</td>
  </tr>
  <tr>
  <td>{{quiznumber3}}</td>
  <td>+</td>
  <td>{{quiznumber4}}</td>
  <td>=</td>
  <td><input v-model="quizanswer2" type="number" min="0" step="1"></td>
  <td>{{result2}}</td>
  </tr>
  <tr>
  <td>{{quiznumber5}}</td>
  <td>+</td>
  <td>{{quiznumber6}}</td>
  <td>=</td>
  <td><input type="number" v-model="quizanswer3" min="0" step="1"></td>
  <td>{{result3}}</td>
  </tr>
  <tr>
  <td>{{quiznumber7}}</td>
  <td>+</td>
  <td>{{quiznumber8}}</td>
  <td>=</td>
  <td><input type="number" v-model="quizanswer4" min="0" step="1"></td>
  <td>{{result4}}</td>
  </tr>
  <tr>
  <td>{{quiznumber9}}</td>
  <td>+</td>
  <td>{{quiznumber10}}</td>
  <td>=</td>
  <td><input type="number" v-model="quizanswer5" min="0" step="1"></td>
  <td>{{result5}}</td>
  </tr>
  <tr>
  <td>{{quiznumber11}}</td>
  <td>+</td>
  <td>{{quiznumber12}}</td>
  <td>=</td>
  <td><input type="number" v-model="quizanswer6" min="0" step="1"></td>
  <td>{{result6}}</td>
  </tr>
  <tr>
  <td>{{quiznumber13}}</td>
  <td>+</td>
  <td>{{quiznumber14}}</td>
  <td>=</td>
  <td><input type="number" min="0" v-model="quizanswer7" step="1"></td>
  <td>{{result7}}</td>
  </tr>
  <tr>
  <td>{{quiznumber15}}</td>
  <td>+</td>
  <td>{{quiznumber16}}</td>
  <td>=</td>
  <td><input type="number" min="0" v-model="quizanswer8" step="1"></td>
  <td>{{result8}}</td>
  </tr>
  <tr>
  <td>{{quiznumber17}}</td>
  <td>+</td>
  <td>{{quiznumber18}}</td>
  <td>=</td>
  <td><input type="number" min="0" v-model="quizanswer9" step="1"></td>
  <td>{{result9}}</td>
  </tr>
  <tr>
  <td>{{quiznumber19}}</td>
  <td>+</td>
  <td>{{quiznumber20}}</td>
  <td>=</td>
  <td><input type="number" min="0" v-model="quizanswer10" step="1"></td>
  <td>{{result10}}</td>
  </tr>
  </tbody>
</table><br>
  <button type="button" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" @click="checkanswers()">Check results</button>
  <button type="button" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" @click="newquiz()"> New quiz</button><br>
  <p v-if="validate === 1">Your score is {{score}}/10
  </p>
  </form>

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
              <span class="w3-large"><a class="removelink" href="/math/multiplication-table"> Multiplication Table</a></span><br>
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
      title: 'Addition Table',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Addition Table' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/addition-table'}
    ]
    }
    },
  data(){
    return {
      firsttext: 0,
      score: 0,
      validate: 0,
      upnumber: '',
      secondtext: 0,
      answer: '',
      quiznumber1: '',
      quiznumber2: '',
      quizanswer1: '',
      quizanswer2: '',
      quizanswer3: '',
      quizanswer4: '',
      quizanswer5: '',
      quizanswer6: '',
      quizanswer7: '',
      quizanswer8: '',
      quizanswer9: '',
      quizanswer10: '',
      quiznumber3: '',
      quiznumber4: '',
      quizanswer2: '',
      result1: '',
      result2: '',
      result3: '',
      result4: '',
      result5: '',
      result6: '',
      result7: '',
      result8: '',
      result9: '',
      result10: '',
      quiznumber5: '',
      quiznumber6: '',
      quizanswer3: '',
      quiznumber7: '',
      quiznumber8: '',
      quizanswer4: '',
      quiznumber9: '',
      quiznumber10: '',
      quizanswer5: '',
      quiznumber11: '',
      quiznumber12: '',
      quizanswer6: '',
      quiznumber13: '',
      quiznumber14: '',
      quizanswer7: '',
      quiznumber15: '',
      quiznumber16: '',
      quizanswer8: '',
      quiznumber17: '',
      quiznumber18: '',
      quizanswer9: '',
      quiznumber19: '',
      quiznumber20: '',
      quizanswer10: ''
    }
  },
  methods: {
    OnButton(value){
      if(value){
      this.upnumber = value;
      this.firsttext = value;
      this.answer = parseInt(this.firsttext) + parseInt(this.secondtext);
    }
    else{
      this.answer = parseInt(this.firsttext) + parseInt(this.secondtext);
    }
    },
    OnButton1(value){
      if(value){
        this.upnumber = value;
        this.secondtext = value;
        this.answer = parseInt(this.firsttext) + parseInt(this.secondtext);
      }
      else{
        this.answer = parseInt(this.firsttext) + parseInt(this.secondtext);
      }
    },
    reset(){
      this.upnumber = null;
      this.secondtext = null;
    },
    newquiz(){
      this.result1= '',
      this.result2= '',
      this.result3= '',
      this.result4= '',
      this.result5= '',
      this.result6= '',
      this.result7= '',
      this.result8= '',
      this.result9= '',
      this.result10= ''
      this.validate = 0,
      this.quizanswer1 = '',
      this.quiznumber2 = '',
      this.quiznumber3 = '',
      this.quiznumber4 = '',
      this.quiznumber5 = '',
      this.quiznumber6 = '',
      this.quiznumber7 = '',
      this.quiznumber8 = '',
      this.quiznumber9 = '',
      this.quiznumber10 = '';
      this.quizanswer2 = null;
      this.quizanswer3 = null;
      this.quizanswer4 = null;
      this.quizanswer5 = null;
      this.quizanswer6 = null;
      this.quizanswer7 = null;
      this.quizanswer8 = null;
      this.quizanswer9 = null;
      this.quizanswer10 = null;
    this.quiznumber()
        },
    quiznumber(){
      var x = Math.floor(Math.random() * 10);
      this.quiznumber1 = x;
      var y = Math.floor(Math.random() * 10);
      this.quiznumber2 = y;
      var z = Math.floor(Math.random() * 10);
      this.quiznumber3 = z;
      var a = Math.floor(Math.random() * 10);
      this.quiznumber4 = a;
      var b = Math.floor(Math.random() * 10);
      this.quiznumber5 = b;
      var c = Math.floor(Math.random() * 10);
      this.quiznumber6 = c;
      var d = Math.floor(Math.random() * 10);
      this.quiznumber7 = d;
      var e = Math.floor(Math.random() * 10);
      this.quiznumber8 = e;
      var f = Math.floor(Math.random() * 10);
      this.quiznumber9 = f;
      var g = Math.floor(Math.random() * 10);
      this.quiznumber10 = g;
      var h = Math.floor(Math.random() * 10);
      this.quiznumber11 = h;
      var i = Math.floor(Math.random() * 10);
      this.quiznumber12 = i;
      var j = Math.floor(Math.random() * 10);
      this.quiznumber13 = j;
      var k = Math.floor(Math.random() * 10);
      this.quiznumber14 = k;
      var l = Math.floor(Math.random() * 10);
      this.quiznumber15 = l;
      var m = Math.floor(Math.random() * 10);
      this.quiznumber16 = m;
      var n = Math.floor(Math.random() * 10);
      this.quiznumber17 = n;
      var o = Math.floor(Math.random() * 10);
      this.quiznumber18 = o;
      var p = Math.floor(Math.random() * 10);
      this.quiznumber19 = p;
      var q = Math.floor(Math.random() * 10);
      this.quiznumber20 = q;
    },
    checkanswers(){
      var ans = this.quiznumber1 + this.quiznumber2;
      var ans2 = this.quiznumber3 + this.quiznumber4;
      var ans3 = this.quiznumber5 + this.quiznumber6;
      var ans4 = this.quiznumber7 + this.quiznumber8;
      var ans5 = this.quiznumber9 + this.quiznumber10;
      var ans6 = this.quiznumber11 + this.quiznumber12;
      var ans7 = this.quiznumber13 + this.quiznumber14;
      var ans8 = this.quiznumber15 + this.quiznumber16;
      var ans9 = this.quiznumber17 + this.quiznumber18;
      var ans10 = this.quiznumber19 + this.quiznumber20;
      if(this.quizanswer1 == ans){
        this.result1 = "right answer"
        this.score++;
      }
      else{
        this.result1 = "wrong answer"
      }
      if(this.quizanswer2 == ans2){
        this.result2 = "right answer"
        this.score++;
      }
      else{
        this.result2 = "wrong answer"
      }
      if(this.quizanswer3 == ans3){
        this.result3 = "right answer"
        this.score++;
      }
      else{
        this.result3 = "wrong answer"
      }
      if(this.quizanswer4 == ans4){
        this.result4 = "right answer"
        this.score++;
      }
      else{
        this.result4 = "wrong answer"
      }
      if(this.quizanswer5 == ans5){
        this.result5 = "right answer"
        this.score++;
      }
      else{
        this.result5 = "wrong answer"
      }
      if(this.quizanswer6 == ans6){
        this.result6 = "right answer"
        this.score++;
      }
      else{
        this.result6 = "wrong answer"
      }
      if(this.quizanswer7 == ans7){
        this.result7 = "right answer"
        this.score++;
      }
      else{
        this.result7 = "wrong answer"
      }
      if(this.quizanswer8 == ans8){
        this.result8 = "right answer"
        this.score++;
      }
      else{
        this.result8 = "wrong answer"
      }
      if(this.quizanswer9 == ans9){
        this.result9 = "right answer"
        this.score++;
      }
      else{
        this.result9 = "wrong answer"
      }
      if(this.quizanswer10 == ans10){
        this.result10 = "right answer"
        this.score++;
      }
      else{
        this.result10 = "wrong answer"
      }
      this.validate = 1;
    }
  },
  beforeMount(){
   this.quiznumber()
}

}
</script>

<style lang="css">
h1 { font-size:1.6rem; }
h2 { font-size:1.4rem; }
h3 { font-size:1.2rem; }
h4 { font-size:1.2rem; }
.insideoftable {
			background:#fff;
			padding:3px;
			border: 1px #ccc solid;
			text-align:center;
			font-family:Arial, Helvetica, sans-serif;
			font-size: 1.2em; }
      .outsideoftable {
			background:#ccc;
			padding:3px;
			border:0px #ccc solid;
			text-align:center;
			font-family:Arial, Helvetica, sans-serif;
			font-size: 1.2em; }
      @media all and (max-width: 576px) {
}
@media all and (min-width: 577px) {
	#secondtable { table-layout: fixed; }
	#secondtable td button { width:36px; height:26px; }
}

</style>
