<template>
  <div class="w3-white">
    <div class="w3-content" style="max-width:1400px">

<div class="w3-row">

<!-- Blog entries -->
<div class="w3-col l8 s12">
  <!-- Blog entry -->
  <div class="w3-margin w3-white">
      <div class="w3-container w3-padding">
        <a href="/">Home</a> &rsaquo; Voltage conversion<hr>
    <h1 class="w3-text-teal"><b>Online voltage conversion tools.</b></h1>
    <Adsense
    class="adsbygoogle infeed"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="4199493091"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense>
      </div>
      <ul class="w3-ul w3-hoverable w3-white">
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/voltage-conversion/volts-to-microvolts"> Volts to microvolts</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/voltage-conversion/volts-to-millivolts"> Volts to millivolts</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/voltage-conversion/volts-to-kilovolts"> Volts to kilovolts</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/voltage-conversion/volts-to-megavolts"> Volts to megavolts</a></span><br>
        </li>
        <li class="w3-padding-16">
          <span class="w3-large"><a class="removelink" href="/voltage-conversion/volts-to-gigavolts"> Volts to gigavolts</a></span><br>
        </li>
      </ul>
  </div>
  <hr>

</div>


<!-- Introduction menu -->
<!-- END GRID -->
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
import Logo from '~/components/Logo.vue'

export default {
  head() {
  return {
    title: 'Best online voltage conversion tool for students and professionals',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
    { hid: 'description', name: 'description', content: 'Voltage conversion tools.'}
  ],
  link: [
  {rel: 'canonical', href: 'https://www.aaryatables.com/voltage-conversion'}
  ]
  }
  },
  components: {
    Logo
  },
  data(){
    return{
        Millimeter: '',
      number1: '',
      Centimeter: '',
      Meter: '',
      Inch: '',
      Foot: '',
      Yard: '',
      Mile: '',
      convertweight: 'Millimeter:'
    }
  },
  methods: {
    reset(){
      this.Millimeter = "";
      this.number1 = "";
      this.Centimeter = "";
      this.Meter = "";
      this.Inch = "";
      this.Foot = "";
      this.Yard = "";
      this.Mile = "";
      this.convertweight = "Millimeter:";
    },
    str2num(s)
    {
       s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
       if( s=='' ) return 0;
       return Function('"use strict";return ('+s+')')();
    },
    roundresult(x) {
      var y = parseFloat(x);
      y = this.roundnum(y,10);
      return y;
    },
    roundnum(x,p) {
      var i;
      var j;
      var n=parseFloat(x);
      var m=n.toFixed(p);
      var y=String(m);
      i=y.length;
      j=y.indexOf('.');
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
    convert(){
      if(this.convertweight === "Millimeter:"){
        var x = this.str2num(this.number1);
  var y = (x/10);
  var y = this.roundresult(y);
this.Centimeter = y;
        this.Millimeter = this.number1;
        var y1 = this.roundresult(x/1000);
        this.Meter = y1;
        var y2 = (x/25.4);
var y2 = this.roundresult(y2);
this.Inch = y2;
var y3 = (x/304.8);
var y3 = this.roundresult(y3);
this.Foot = y3;
var x1 = this.str2num(this.number1);
var y4 = this.roundresult(x1*1760);
if( y4<0 ) { x1=-x1; y4=-y4; }
this.Yard = y4;
this.Mile = this.number1 * 6.213711922E-7;
      }
      else if(this.convertweight === "Centimeter:"){
        this.Centimeter = this.number1;
        var x = this.str2num(this.number1);
var y = (x*10);
var y = this.roundresult(y);
this.Millimeter = y;
var y1 = this.roundresult(x/100);
this.Meter = y1;
var y2 = (x/2.54);
var y2 = this.roundresult(y2);
this.Inch = y2;
var y3 = (x/30.48);
var y3 = this.roundresult(y3);
this.Foot = y3;
var x1= this.number1;
var y4 = this.roundresult(x1/91.44);
if( y<0 ) { x1=-x1; y4=-y4; }
this.Yard = y4;
this.Mile = this.number1 * 6.21371e-6;
      }
      else if(this.convertweight === "Meter:"){
        this.Meter = this.number1;
        var x = this.str2num(this.number1);
var y = this.roundresult(x*1000);
this.Millimeter = y;
var y1 = this.roundresult(x*160934.4);
this.Centimeter = y1;
var y2 = (x/0.0254);
var y2 = this.roundresult(y2);
this.Inch = y2;
var y3 = (x/0.3048);
var y3 = this.roundresult(y3);
this.Foot = y3;
var y4 = this.roundresult(x/0.9144);
this.Yard = y4;
var y5 = this.roundresult(x/1609.344);
this.Mile = y5;
          }
      else if(this.convertweight === "Inch:"){
        this.Inch = this.number1;
        var x = this.str2num(this.number1);
        var y = this.roundresult(x*25.4);
        this.Millimeter = y;
        var y1 = this.roundresult(x*2.54);
        this.Centimeter = y1;
        var y2 = this.roundresult(x*0.0254);
        this.Meter = y2;
        var y3 = this.roundresult(x/12);
        this.Foot = y3;
        var y4 = this.roundresult(x/36);
        this.Yard = y4;
        var y5 = this.roundresult(x/63360);
        this.Mile = y5;
          }
      else if(this.convertweight === "Foot:"){
        this.Foot = this.number1;
      var x = this.str2num(this.number1);
      var y = (x*304.8);
      this.Millimeter = y;
      var y1 = this.roundresult(x*30.48);
      this.Centimeter = y1;
      var y2 = this.roundresult(x*0.3048);
      this.Meter = y2;
      var y3 = (x*12);
var y3 = this.roundresult(y3);
this.Inch = y3;
var x1 = this.str2num(this.number1);
var y4 = this.roundresult(x1/3);
if( y4<0 ) { x1=-x1; y4=-y4; }
this.Yard = y4;
  var y5 = this.roundresult(x/5280);
  this.Mile = y5;
      }
      else if(this.convertweight === "Yard:"){
        this.Yard = this.number1;
        var x = this.str2num(this.number1);
        this.Millimeter = x*914.4;
        var y = this.roundresult(x*91.44);
        this.Centimeter = y;
        var y1 = this.roundresult(x*0.9144);
        this.Meter = y1;
        var y2 = this.roundresult(x*36);
        this.Inch = y2;
        var y3 = this.roundresult(x*3);
        this.Foot = y3;
        var y4 = this.roundresult(x/1760);
        this.Mile = y4;
      }
      else if(this.convertweight === "Mile:"){
        this.Mile = this.number1;
        var x = this.str2num(this.number1);
        this.Millimeter = x*1.609e+6;
        var y = this.roundresult(x*160934.4);
        this.Centimeter = y;
        var y1 = this.roundresult(x*1609.344);
        this.Meter = y1;
        var y2 = this.roundresult(x*63360);
        this.Inch = y2;
        var x1 = this.str2num(this.number1);
        var y3 = this.roundresult(x1*5280);
        if( y3<0 ) { x1=-x1; y1=-y1; }
	       this.Foot = y3;
         var y4 = this.roundresult(x*1760);
         this.Yard = y4;

      }
      else{
        if(this.number1 === ''){
          alert("please enter a value")
        }else
        {alert("please slect an option")}
      }
    }
  }
}
</script>

<style>
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
body,h1,h2,h3,h4,h5 {font-family: "Raleway", sans-serif}
h1 { font-size:1.6rem; }
.removelink{
    text-decoration: none;
}
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
    #designform { padding:10px; }
    #designform td input[type=number] { width:60px; }
    #designform td input[type=text] { width:60px; }
  }
</style>
