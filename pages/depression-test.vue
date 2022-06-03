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
          <a href="/">Home</a> &rsaquo; Depression test<hr>
      <h1 class="w3-text-teal"><b>Depression self-assessment test</b></h1>
      <p>Most accurate Depression test. Just answer seven quick questions to find out whether you are suffering from depression or not.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
    </Adsense>

    <div class="w3-white w3-card">
            <h2 class="w3-padding-16"><i class="fa-fw w3-margin-right w3-xxlarge w3-text-teal"></i>Depression test questions</h2>
            <div class="w3-container" v-if="step == 1">
              <h5 class="w3-opacity"><b>Question 1 - Do you sometimes feel hopeless in your life?</b></h5>
              <hr>
                <input type="radio" id="yes" value="yes" v-model="size">
          <label for="10">yes</label><br>
          <input type="radio" id="no" value="no" v-model="size">
          <label for="12">no</label><br>
            </div>
            <div class="w3-container" v-if="step == 2">
                <h5 class="w3-opacity"><b>Question 2 - Do you have unusual sleeping cycle? Either sleeping too much or very less?</b></h5>
                <hr>
                <input type="radio" id="yes" value="yes" v-model="price">
              <label for="yes">yes</label><br>
              <input type="radio" id="no" value="no" v-model="price">
              <label for="no">no</label><br>
            </div>

            <div class="w3-container" v-if="step == 3">
                <h5 class="w3-opacity"><b>Question 3 - Do you feel tired all the time or have a little energy before starting any new task?</b></h5>
                <hr>
                <input type="radio" id="yes" value="yes" v-model="reason">
          <label for="radio">yes</label><br>
          <input type="radio" id="no" value="no" v-model="reason">
        <label for="radio">no</label><br>
              </div>

              <div class="w3-container" v-if="step == 4">
                  <h5 class="w3-opacity"><b>Question 4 - Do you have poor appetite or over-eat?</b></h5>
                  <hr>
                  <input type="radio" id="yes" value="yes" v-model="os">
            <label for="Chrome">yes</label><br>
                  <input type="radio" id="no" value="no" v-model="os">
            <label for="Windows">no</label><br>
                </div>

                <div class="w3-container" v-if="step == 5">
                    <h5 class="w3-opacity"><b>Question 5 - Do you feel, you have let any of your closed-one down?</b></h5>
                    <hr>
                    <input type="radio" id="yes" value="yes" v-model="twoinone">
              <label for="radio">yes</label><br>
              <input type="radio" id="no" value="no" v-model="twoinone">
              <label for="radio">no</label><br>
                  </div>
                  <div class="w3-container" v-if="step == 6">
                      <h5 class="w3-opacity"><b>Question 6 - Do you have trouble focusing?</b></h5>
                      <hr>
                      <input type="radio" id="yes" value="yes" v-model="focus">
                <label for="radio">yes</label><br>
                <input type="radio" id="no" value="no" v-model="focus">
                <label for="radio">no</label><br>
                    </div>
                    <div class="w3-container" v-if="step == 7">
                        <h5 class="w3-opacity"><b>Question 7 - Do you have any thoughts of giving pain or any other harmful thoughts towards yourself?</b></h5>
                        <hr>
                        <input type="radio" id="yes" value="yes" v-model="harm">
                  <label for="radio">yes</label><br>
                  <input type="radio" id="no" value="no" v-model="harm">
                  <label for="radio">no</label><br>
                      </div>
                      <div class="w3-margin-left">
            <button class="w3-margin-bottom w3-button w3-padding-large w3-teal w3-border" v-if="step != totalsteps" @click.prevent="nextstep"><b>Next Step &raquo;</b></button>
            <button class="w3-margin-bottom w3-button w3-padding-large w3-orange w3-border" v-if="step != 1" @click.prevent="previousstep"><b>&laquo; Previous Step</b></button>
            <button class="w3-margin-bottom w3-button w3-padding-large w3-green w3-border" v-if="step == 7" @click.prevent="findit()"><b>Get report &raquo;</b></button>
          </div>
          </div><br>
          <div v-if="result === true" class="w3-container fl-porto" ref="porto">
            <h1 style="color: teal;">Test Results based on your choices:</h1>
  <div v-if="less2 === true">
    <h3 style="color: green;">It is highly unlikely you are suffering from depression.</h3>
    <h3>You can avoid depression by doing a few following ways!</h3>
    <ul><li>Exercise regularly even on the Sundays as well</li>
    <li>Spend less amount of time on social media apps</li>
    <li>Spend more time on strong relationships. Spend time with the people whom you trust the most</li>
    <li>Reduce stress by doing Yoga for a few minutes</li>
    <li>Get enough sleep every day. Get around 7 to 9 hours of sleep every night</li>
    <li>Distance yourself from the toxic people.</li></ul>
  </div>
  <div v-if="less4 === true">
    <p>It is likely that you are suffering from a mild depression. Although you have nothing to worry about and this is something that you can easily snap out of by proper support and guidance.</p>
    <h3>You can avoid depression by doing a few following ways!</h3>
    <ul><li>Exercise regularly even on the Sundays as well</li>
    <li>Spend less amount of time on social media apps</li>
    <li>Spend more time on strong relationships. Spend time with the people whom you trust the most</li>
    <li>Reduce stress by doing Yoga for a few minutes</li>
    <li>Get enough sleep every day. Get around 7 to 9 hours of sleep every night</li>
    <li>Distance yourself from the toxic people.</li></ul>
  </div>
  <div v-if="less7 === true">
    <p>It is highly likely that you are extreamely depressed and you need a consultation.</p>
    <h3>You can avoid depression by doing a few following ways!</h3>
    <ul><li>Exercise regularly even on the Sundays as well</li>
    <li>Spend less amount of time on social media apps</li>
    <li>Spend more time on strong relationships. Spend time with the people whom you trust the most</li>
    <li>Reduce stress by doing Yoga for a few minutes</li>
    <li>Get enough sleep every day. Get around 7 to 9 hours of sleep every night</li>
    <li>Distance yourself from the toxic people.</li></ul>
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
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/case-converter"> Case Converter</a></span><br>
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
      title: 'Free Depression test',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'With the help of this Depression test app, you can find your mental health state.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/depression-test'}
    ]
    }
    },
  data(){
    return {
      articles : [],
      step: 1,
      totalsteps: 7,
      size: '',
      reason: '',
      price: '',
      os: '',
      twoinone: '',
      review: '',
      percentage: '',
      focus: '',
      harm: '',
      less2: false,
      less4: false,
      less7: false,
      result: false
    }
  },
  methods: {
    scrollMeTo(refName) {
    var element = this.$refs[refName];
 var top = element.offsetTop;

    window.scrollTo(0, top);
  },
  percentclick(){
    this.review = 'yea1';
  },
    nextstep()
        {
            this.step++;
        },
        previousstep()
        {
            this.step--;
        },
        findit(){
          this.result = true;
var yes = 0;
var no = 0;
if(this.size === "yes"){
  yes ++;
}
if(this.size === "no"){
  no ++;
}
if(this.price === "yes"){
  yes ++;
}
if(this.price === "no"){
  no ++;
}
if(this.reason === "yes"){
  yes ++;
}
if(this.reason === "no"){
  no ++;
}
if(this.os === "yes"){
  yes ++;
}
if(this.os === "no"){
  no ++;
}
if(this.twoinone === "yes"){
  yes ++;
}
if(this.twoinone === "no"){
  no ++;
}
if(this.harm === "yes"){
  yes ++;
}
if(this.harm === "no"){
  no ++;
}
if(this.focus === "yes"){
  yes ++;
}
if(this.focus === "no"){
  no ++;
}
if(yes <= 2){
this.less2 = true;
  this.less4 = false;
  this.less7 = false;
}
if(yes > 2 && yes <= 4){
  this.less4 = true;
  this.less2 = false;
  this.less7 = false;
}
if(yes > 4){
  this.less7 = true;
  this.less2 = false;
    this.less4 = false;
}
      },
  async secondbutton()
  {
    const data = await this.$axios.$get('/api/articles/filtera')
    this.articles = data
  },
  async sendvalues()
  {
   await this.$axios.$post('/api/articles/filter', {
     author: this.author
   })
   .then((response) => {
    this.articles = response
  })
  }
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
