<template lang="html">
  <div class="w3-content" style="max-width:1400px">
    <div class="w3-row">
    <!-- Blog entries -->
    <div class="w3-col l8 s12">
      <!-- Blog entry -->
      <div class="w3-margin w3-white">


        <div class="w3-container w3-padding">
              <a href="/">Home</a> &rsaquo; Word counter<hr>
          <h1 class="w3-text-teal"><b>Count words</b></h1>
          <p>Words, characters and sentences counter oninput.</p>
          <Adsense
          class="adsbygoogle infeed"
          style="display:block"
          data-ad-client="ca-pub-6829148792481216"
          data-ad-slot="4199493091"
          data-ad-format="auto"
          data-full-width-responsive="true">
        </Adsense><br>
<div class="">
  <div class="w3-row-padding w3-margin-bottom w3-center">
    <div class="w3-quarter">
      <div class="w3-container w3-blue-grey">
        <div class="w3-center">
          <h3>Characters</h3>
        </div>
        <div class="w3-clear"></div>
        <h4>{{characters}}</h4>
      </div>
    </div>
    <div class="w3-quarter">
      <div class="w3-container w3-blue-grey">
        <div class="w3-center">
          <h3>Words</h3>
        </div>
        <div class="w3-clear"></div>
        <h4>{{words}}</h4>
      </div>
    </div>
    <div class="w3-quarter">
      <div class="w3-container w3-blue-grey">
        <div class="w3-center">
          <h3>Sentences</h3>
        </div>
        <div class="w3-clear"></div>
        <h4>{{sentences}}</h4>
      </div>
    </div>
</div>
  <div id="designform" name="designform">
    <div class="form-group">
    <textarea placeholder="Enter text here" v-model="area" rows="3" @input="fract()" style="height: 500px" class="form-control form-control-lg"></textarea>
    </div>
</div><br>
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
      title: 'An online tool to count words.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Word counter tool.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/word-counter'}
    ]
    }
    },
  data(){
    return {
      area: '',
      characters: '0',
      words: '0',
      sentences: '0'
      }
  },
  methods: {
  fract(){
    var string = this.area;
    this.sentences = '1';
    this.characters = string.length; //4
    this.words = string.split(/\b\W+\b/).length;
    const re = /[.!?]/;
    if(!string.includes('.')){
      this.sentences = 1;
    }
    else {
    this.sentences = string.split(re).length - 1;
  }
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
 #designform { padding:20px; max-width:1000px; height: 540px; background:#a7c9b8; }
 #designform td input[type=number] { width:80px; text-align: center; margin:4px auto; }
 #designform td input[type=text] { width:80px; text-align: center; margin:4px auto; }
 #designform .btn span { font-weight: bold; font-size:large; }
 #designform .btn img { filter:invert(1); }
 #wrapper td { padding-left:unset; padding-right:unset; }
@media all and (max-width: 800px) {
    .adslot_1, .adslot_2, .adslot_3 { display:none; }
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
 }
</style>
