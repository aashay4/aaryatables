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
          <a href="/">Home</a> &rsaquo; Height converter<hr>
      <h1 class="w3-text-teal"><b>Height converter</b></h1>
        <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="4199493091"
        data-ad-format="auto"
        data-full-width-responsive="true">
      </Adsense><br>
      <p>All height conversion units are available. Convert between feet, inches, meters, and centimeters.</p>
      <form id="formnumber1" autocomplete="off">
<table>
<tr>
<td><label for="ftin1">Feet+Inches</label></td>
<td>&nbsp;</td>
</tr>
<tr>
<td class="form-group">
<div class="form-row">
<div class="col">
<input type="text" v-model="ftin1" class="form-control" @input="ConvertFtin()" autofocus>
</div>
<span class="mt-2">ft</span>
<div class="col">
<input type="text" v-model="ftin2" class="form-control" @input="ConvertFtin()">
</div>
</div>
</td>
<td>in</td>
</tr>
<tr>
<td><label for="ft">Feet</label></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><input type="text" v-model="ft" class="form-control" @input="ConvertFt()"></td>
<td>ft</td>
</tr>
<tr>
<td><label for="in">Inches</label></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><input type="text" v-model="inc" class="form-control" @input="ConvertIn()"></td>
<td>in</td>
</tr>
<tr>
<td><label for="mcm1">Meters+Centimeters</label></td>
<td>&nbsp;</td>
</tr>
<tr>
<td>
<div class="form-row">
<div class="col">
<input type="text" v-model="mcm1" class="form-control" @input="ConvertMcm()">
</div>
<span class="mt-2">m</span>
<div class="col">
<input type="text" v-model="mcm2" class="form-control" @input="ConvertMcm()">
</div>
</div>
</td>
<td>cm</td>
</tr>
<tr>
<td><label for="m">Meters</label></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><input type="text" v-model="m" class="form-control" @input="ConvertM()"></td>
<td>m</td>
</tr>
<tr>
<td><label for="cm">Centimeters</label></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><input type="text" v-model="cm" class="form-control" @input="ConvertCm()"></td>
<td>cm</td>
</tr>
<tr>
<td><button type="button" @click="reset()" title="Reset" class="btn btn-secondary mt-2"><span>&times;</span> Reset</button></td>
<td>&nbsp;</td>
</tr>
</table>
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
      title: 'Height converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'All units height converter.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/height-converter'}
    ]
    }
    },
  data(){
    return {
      ftin1: '',
      ftin2: '',
      ft: '',
      inc: '',
      mcm1: '',
      mcm2: '',
      m: '',
      cm: ''
    }
  },
  methods: {
    reset(){
      this.ftin1 = "";
      this.ftin2 = "";
      this.ft = "";
      this.inc = "";
      this.mcm1 = "";
      this.mcm2 = "";
      this.m = "";
      this.cm = "";
    },
    roundnum(x,p) {
      var i;
      var n=parseFloat(x);
      var m=n.toPrecision(p+1);
      var y=String(m);
      i=y.indexOf('e');
      if( i==-1 )	i=y.length;
      var j=y.indexOf('.');
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
     ConvertCm()
    {
       var d = this.cm;
       if( d=='' ) return;
       d = this.str2num(d);
       var mcm1 = Math.floor(d/100);
       var d2 = d/2.54;
      var ftin1 = Math.floor(d2/12);
       //document.calcform.cm.value		= this.roundnum(d,		6);
       this.m		= this.roundnum(d/100,		6);
       this.inc		= this.roundnum(d/2.54,	6);
       this.ft		= this.roundnum(d/2.54/12,6);
       this.mcm1	= this.roundnum(mcm1,		6);
       this.mcm2	= this.roundnum(d-mcm1*100,6);
       this.ftin1	= this.roundnum(ftin1,		6);
       this.ftin2	= this.roundnum(d2-ftin1*12,6);
    },
    str2num(s)
    {
       s=s.toString().trim().replace(/(\d)(\s+)(?=\d)/gm,"$1+").replace(/,(?=[^,]*$)/, '.').replace(/[^-()e\d/*+.]/g, '');
       if( s=='' ) return 0;
       return Function('"use strict";return ('+s+')')();
    },
     ConvertM()
    {
       var d = this.m;
       if( d=='' ) return;
       d = this.str2num(d);
       var cm = d*100;
       var d1 = Math.floor(cm/100);
       var d2 = d/0.0254;
       var ftin1 = Math.floor(d2/12);
       this.cm		= this.roundnum(d*100,		6);
       //document.calcform.m.value		= this.roundnum(d,			6);
       this.inc		= this.roundnum(d/0.0254,	6);
       this.ft		= this.roundnum(d/0.0254/12,	6);
       this.mcm1	= this.roundnum(d1,			6);
       this.mcm2	= this.roundnum(cm-d1*100,	6);
       this.ftin1	= this.roundnum(ftin1,		6);
       this.ftin2	= this.roundnum(d2-ftin1*12,	6);
    },

     ConvertMcm()
    {
       var d1 = this.mcm1;
       var d2 = this.mcm2;
       if( d1=='' && d2=='' ) return;
       if( d1=='' ) d1='0';
       if( d2=='' ) d2='0';
       d1 = this.str2num(d1);
       d2 = this.str2num(d2);
       cm = d1*100+d2;
       var d3 = cm/2.54;
       var ftin1 = Math.floor(d3/12);
       this.cm		= this.roundnum(d1*100+d2,	6);
       this.m		= this.roundnum(d1+d2/100,	6);
       this.inc		= this.roundnum(cm/2.54,		6);
       this.ft		= this.roundnum(cm/2.54/12,	6);
       //document.calcform.mcm1.value	= this.roundnum(d1,			6);
       //document.calcform.mcm2.value	= this.roundnum(d2,			6);
       this.ftin1	= this.roundnum(ftin1,		6);
       this.ftin2	= this.roundnum(d3-ftin1*12,	6);
    },
  ConvertIn()
    {
       var d = this.inc;
       if( d=='' ) return;
       d = this.str2num(d);
       var d1 = Math.floor(d/12);
       var cm = d*2.54;
       var d2 =  Math.floor(cm/100);
       this.cm		= this.roundnum(d*2.54,		6);
       this.m		= this.roundnum(d*0.0254,	6);
       //document.calcform.in.value		= this.roundnum(d,			6);
       this.ft		= this.roundnum(d/12,		6);
       this.mcm1	= this.roundnum(d2,			6);
       this.mcm2	= this.roundnum(cm-d2*100,	6);
       this.ftin1	= this.roundnum(d1,			6);
       this.ftin2	= this.roundnum(d-d1*12,		6);
    },
     ConvertFt()
    {
       var d = this.ft;
       if( d=='' ) return;
       d = this.str2num(d);
       var d1 = Math.floor(d);
       var cm = d*30.48;
       var d2 =  Math.floor(cm/100);
       this.cm		= this.roundnum(d*30.48,		6);
       this.m		= this.roundnum(d*0.3048,	6);
       this.inc		= this.roundnum(d*12,		6);
       //document.calcform.ft.value		= this.roundnum(d,			6);
       this.mcm1	= this.roundnum(d2,			6);
       this.mcm2	= this.roundnum(cm-d2*100,	6);
       this.ftin1	= this.roundnum(d1,			6);
       this.ftin2	= this.roundnum((d-d1)*12,	6);
    },
     ConvertFtin()
    {
       var d1 = this.ftin1;
       var d2 = this.ftin2;
       if( d1=='' && d2=='' ) return;
       if( d1=='' ) d1='0';
       if( d2=='' ) d2='0';
       d1 = this.str2num(d1);
       d2 = this.str2num(d2);
       var cm = d1*30.48+d2*2.54;
       var d3 = Math.floor(cm/100);
       this.cm		= this.roundnum(cm,			6);
       this.m		= this.roundnum(cm/100,	6);
       this.inc		= this.roundnum(d1*12+d2,	6);
       this.ft		= this.roundnum(d1+d2/12,	6);
       this.mcm1	= this.roundnum(d3,			6);
       this.mcm2	= this.roundnum(cm-d3*100,6);
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
#formnumber1 { background:#a7c9b8; padding:20px; }
.calc, table.calc td { background:#a7c9b8; }
.btn span { font-weight: bold; font-size:large; }
#formnumber1 button i { vertical-align: bottom; }
/*.btn b, .btn b2 { font-size:large; }*/
@media all and (max-width: 800px) {
   #formnumber1 { padding:10px; }
}

</style>
