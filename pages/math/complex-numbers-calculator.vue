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
          <a href="/">Home</a> &rsaquo; <a href="/math">Mathematics</a> &rsaquo; Complex Numbers Calculator<hr>
      <h1 class="w3-text-teal"><b>Complex Numbers Calculator</b></h1>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>
      <form id="dynamicccc" name="dynamicccc" autocomplete="off">
        <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('i')" value="i" class="btn btn-secondary math"><i>i</i></button>
      </div>
          <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('-')" class="btn btn-secondary">-</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('+')" class="btn btn-secondary">+</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('*')" class="btn btn-secondary">&times;</button><hr>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('/')" class="btn btn-secondary">&divide;</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('^')" class="btn btn-secondary math"><i>x <sup>y</sup></i></button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('sqrt(')" class="btn btn-secondary math">&radic;<span style="border-top:1px solid">&nbsp;&nbsp;</span></button>
        </div>
        <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('re(')" class="btn btn-secondary math">Re(<i>z</i>)</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('im(')" class="btn btn-secondary math">Im(<i>z</i>)</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('abs(')" class="btn btn-secondary math">|<i>z</i>|</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('arg(')" class="btn btn-secondary math">arg(<i>z</i>)</button>
      </div>
      <div class="form-group btn-group mt-2">
        <button type="button" @click="buttonvalue('conj(')" class="btn btn-secondary math">conj(<i>z</i>)</button>
        </div>
<div class="form-group">
<div class="input-group mt-2">
<input type="text" v-model="inputdy" class="form-control" autofocus>
<button type="button" @click="calculate()" class="btn btn-success btn-lg" style="background-color: grey">= > Ans</button>
</div>
</div>
<div class="form-group">
<textarea :class="{ buttonclicked1 : fractclicked1 }" rows="5" id="getans" class="form-control" readonly></textarea>
</div>
</form>



</div><br>
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
              <span class="w3-large"><a class="removelink" href="/math/arccos-calculator"> Arccos calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/arctan-calculator"> Arctan calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/arcsin-calculator"> Arcsin calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/math/random-number-generator"> Random number generator</a></span><br>
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
      title: 'Complex Numbers Calculator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Complex Numbers Calculator' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/math/complex-numbers-calculator'}
  ],
  script: [
    {
      src: 'https://cdnjs.cloudflare.com/ajax/libs/mathjs/9.4.3/math.min.js', integrity: 'sha512-h6sl9arHHMneDTSQwIiJ6NUSx3/wGWKr9P25MQCnwmTsPMBHIscEtk/5k/zA+IOjvGQUuvn2003cRhX2BUpgqw==', crossorigin: 'anonymous', referrerpolicy: 'no-referrer'
    }
  ]
    }
    },
  data(){
    return {
      inputdy: '',
      x: '',
      y: '',
      fractclicked1: false
    }
  },
  methods: {
    reset(){
      this.answer = '';
      this.baseinput = '';
      this.input = '';
    },
    buttonvalue(value){
      this.inputdy = value;
    },
    calculate(){
      this.fractclicked1 = true;
      setTimeout(() => this.fractclicked1 = false, 2500);
      if(this.inputdy === "")
      {alert("please enter a number")}
      else
      {
      var z=math.evaluate(this.inputdy);
if( getans.value!="" ) getans.value+="\n";
//getans.value += calcgetans.value+"\n= "+num2str(z.re)+" + "+num2str(z.im)+"i\n";
getans.value += this.inputdy+"\n= ";
getans.value+=z;
if( typeof z.im!=='undefined' ) {
   var zp = math.complex(z).toPolar();
   var phi=zp.phi*180.0/Math.PI;
   getans.value += "\n= "+zp.r+" \u2220"+phi+"\u00B0";
}
this.inputdy="";
getans.scrollTop = getans.scrollHeight;
}
    }
  }

}
</script>

<style lang="css">
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
  h1 { font-size:1.6rem; }
  h2 { font-size:1.4rem; }
  h3 { font-size:1.4rem; }
  h4 { font-size:1.2rem; }
  #dynamicccc { background:lightblue; padding:20px; }
  #getans { background:#fff; font-size:large; font-family: 'Times New Roman', Times, serif; }
  .btn-group .btn { font-size:large; }
  @media all and (max-width: 800px) {
     #dynamicccc { padding:10px; }
     .btn-group .btn { font-size:medium; }
  }


</style>
