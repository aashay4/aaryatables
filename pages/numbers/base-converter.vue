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
          <a href="/">Home</a> &rsaquo; <a href="/numbers">Numbers</a> &rsaquo; base Converter<hr>
      <h1 class="w3-text-teal"><b>Base converter</b></h1>
      <p>Convert base of almost every numbering system with just one click.</p>
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="4199493091"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <form id="designstyle" autocomplete="off">
<div class="form-group">
<label for="x">Enter number that you want to convert:</label>
<input type="text" v-model="x" class="form-control form-control-lg" required autofocus>
</div>
<div class="form-group">
<label for="sel1">From Base</label>
<select name="sel1" v-model="sel1" class="form-control">
<option value="2">2 (binary)</option>
<option value="3">3</option>
<option value="4">4</option>
<option value="5">5</option>
<option value="6">6</option>
<option value="7">7</option>
<option value="8">8 (octal)</option>
<option value="9">9</option>
<option value="10" selected>10 (decimal)</option>
<option value="11">11</option>
<option value="12">12</option>
<option value="13">13</option>
<option value="14">14</option>
<option value="15">15</option>
<option value="16">16 (hex)</option>
<option value="17">17</option>
<option value="18">18</option>
<option value="19">19</option>
<option value="20">20</option>
<option value="21">21</option>
<option value="22">22</option>
<option value="23">23</option>
<option value="24">24</option>
<option value="25">25</option>
<option value="26">26</option>
<option value="27">27</option>
<option value="28">28</option>
<option value="29">29</option>
<option value="30">30</option>
<option value="31">31</option>
<option value="32">32</option>
<option value="33">33</option>
<option value="34">34</option>
<option value="35">35</option>
<option value="36">36</option>
</select>
</div>
<div class="form-group">
<label>To base</label>
<select v-model="sel2" class="form-control">
  <option value="2">2 (binary)</option>
  <option value="3">3</option>
  <option value="4">4</option>
  <option value="5">5</option>
  <option value="6">6</option>
  <option value="7">7</option>
  <option value="8">8 (octal)</option>
  <option value="9">9</option>
  <option value="10" selected>10 (decimal)</option>
  <option value="11">11</option>
  <option value="12">12</option>
  <option value="13">13</option>
  <option value="14">14</option>
  <option value="15">15</option>
  <option value="16">16 (hex)</option>
  <option value="17">17</option>
  <option value="18">18</option>
  <option value="19">19</option>
  <option value="20">20</option>
  <option value="21">21</option>
  <option value="22">22</option>
  <option value="23">23</option>
  <option value="24">24</option>
  <option value="25">25</option>
  <option value="26">26</option>
  <option value="27">27</option>
  <option value="28">28</option>
  <option value="29">29</option>
  <option value="30">30</option>
  <option value="31">31</option>
  <option value="32">32</option>
  <option value="33">33</option>
  <option value="34">34</option>
  <option value="35">35</option>
  <option value="36">36</option>
</select>
</div>
<div class="form-group">
<button type="button" title="Convert" class="btn btn-success" @click="calculate()"><span>= ></span> Convert</button>

<button type="reset" title="Reset" class="btn btn-secondary" @click="reset()"><span>&times;</span> Reset</button>
</div>
<div class="form-group">
<label for="y">Result number</label>
<textarea rows="2" v-model="y" class="form-control form-control-lg" readonly></textarea>
</div>
</form>


</div><br>
<div class="w3-padding w3-raw w3-align">
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
        <h1 class=""><b>Other Numbers tools</b></h1>
      </div><hr>
          <ul class="w3-ul w3-hoverable w3-white">
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-hexadecimal"> Binary to Hexadecimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-translator"> Binary code translator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/binary-to-decimal"> Binary to Decimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-binary"> Decimal to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/decimal-to-hexadecimal"> Decimal to Hexadecimal</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-binary"> Hexadecimal to Binary</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/hexadecimal-to-decimal"> Hexadecimal calculator</a></span><br>
            </li>
            <li class="w3-padding-16">
              <span class="w3-large"><a class="removelink" href="/numbers/text-to-binary"> Text to Binary</a></span><br>
            </li>
          </ul>
      </div>
    </div>
  </div>


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
//import { BigNumber } from 'bignumber.js'
export default {
  head() {
    // sets document title
    return {
      title: 'Base Converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Base converter tool online.' }
  ],
    link: [
    {rel: 'canonical', href: 'https://www.aaryatables.com/numbers/base-converter'}
  ],
  script: [
    {src: 'https://www.rapidtables.com/lib/bignumber/bignumber9.0.0.min.js'},
    {src: 'https://cdnjs.cloudflare.com/ajax/libs/mathjs/10.1.1/math.min.js', integrity: 'sha512-o7l/Uxf+iFLa5H6VpPjFdrY+bF+JtYI47FXfYJp6zlCRhs8K8sO1EVyEiS/1FeEvw1b6HeK6oXT3Plza8L/NIQ=='}
  ]
    }
    },
  data(){
    return {
      base: '10',
      cal2result: '',
      cal2dec: '',
      cal2tbl: '',
      cal1txt: '',
      sel1: '10',
      b2txt: '',
      sel2: '2',
      x: '',
      op: '0',
      x2: '',
      y: '',
      b1txt: ''
    }
  },
  methods: {
    calculate(){

      var x = this.x;
var b1 = parseFloat(this.sel1);
var b2 = parseFloat(this.sel2);

try {
  var y = new BigNumber(x, b1);
  //$("#x").css("background-color", "white");
    // xelem.style.background = "white";
}
catch(err) {
     //xelem.style.background = "#fff0f0";
     y = "";
  return;
}
  var dec = y.toString(10);
  y = y.toString(b2).toUpperCase();
this.y = y;
  this.b1txt = b1;
  this.b2txt = b2;
  this.base2decimal(x,dec,b1);
  this.decimal2base(dec,y,b2);
//  if( b1==10 ) cal1elem.style.display="none"; else cal1elem.style.display="block";
//  if( b2==10 ) cal2elem.style.display="none"; else cal2elem.style.display="block";
//  calgroup.style.display="block";
},
base2decimal(x, dec, b) {
		var txt="("+x+")<sub>"+b.toString()+"</sub> = ";
		var d,e,minus=false;
		var len=x.length;
		if( x[0]=="-" ) { txt+="-["; x=x.substr(1); len--; minus=true; }
		var idot=x.indexOf(".");
		if( idot>=0 ) { x=x.substring(0,idot)+x.substring(idot+1,len); len--; }
		else idot=len;
		for(var i=0; i<len; i++) {
         d = parseInt(x[i],b);
			e = idot-i-1;
			e=e.toString();
			txt+="("+d+" \u00D7 "+b+"<sup>"+e+"</sup>)";
			if( i<len-1 ) txt+=" + ";
		}
		if( minus ) txt+="]";
		txt+=" = ("+dec+")<sub>10</sub>";
      this.cal1txt = txt;
   },
   decimal2base(dec, y, b) {
      var row,txt="";
      //$("#cal2tbl tbody tr").remove();
      this.cal2tbl = "";
      if( dec<0 ) dec=-dec;
      dec=dec.toString();
      var id=dec.indexOf(".");
      var nd=y.length-y.indexOf(".")-1;
      if( nd>6 ) nd=6;
      if( id>=0 && nd>0) {
         txt="Multiply the number with the destination base raised to the power of decimals of the result (up to 6 digits resolution):<br>";
         txt+="floor("+dec+"&times;"+b+"<sup>"+nd+"</sup>) = ";
         dec=Math.floor(dec*Math.pow(b,nd));
         txt+=dec;
      }
      this.cal2dec = txt;
      for(var n=dec,k=0; n>=1; k++) {
         row = "<tr>";
         row+="<td>"+n+"/"+b+"</td>";
         row+="<td>"+Math.floor(n/b)+"</td>";
         row+="<td>"+(n%b).toFixed()+"</td>";
         row+="<td>"+k+"</td>";
         row+="</tr>";
         n = Math.floor(n/b);
         //$("#cal2tbl tbody").append(row);
         var tableRef = this.cal2tbl;
        // var newRow = tableRef.insertRow(k);
         //newRow.innerHTML = row;
      }
      this.cal2result="= ("+y+")<sub>"+b+"</sub>";
   },
reset(){
  this.base = '10',
  this.cal2result = '',
  this.cal2dec = '',
  this.cal2tbl = '',
  this.cal1txt = '',
  this.sel1 = '10',
  this.b2txt = '',
  this.sel2 = '2';
  this.x = '';
  this.op = '0';
  this.x2 = '';
  this.y = '';
  this.b1txt = "";
},
    bintodecimal(){
      this.fa = parseInt(this.number1)
      var cc = new BigNumber(parseInt(this.number1, 2))
      if (isNaN(cc)) {
        this.base10 = 'This number cannot be converted into Decimal'
      } else {
        this.base10 = cc
      }
    },
     bintohexadecimal(){
       var bin = this.number1;
             var m = new  BigNumber(bin, 2)
             var binn = m.toString(16).toUpperCase();
             this.base16 = binn;
    },
     bintooctal(){
       this.xxx = parseInt(this.number1)
         var bintooct = parseInt(this.xxx, 2).toString(8)
         if (isNaN(bintooct)) {
           this.base8 = 'This number cannot be converted into Octal'
         } else {
           this.base8 = bintooct
         }
    },
  }

}
</script>

<style lang="css">
#cal2tbl th { font-weight: normal; }
#cal2tbl td { line-height:1; }
#cal2tbl th p { word-break: break-all; }
#cal2tbl p { line-height:1; }
#cal2tbl tbody tr td:nth-child(3) { background:#f8f8f8; border:dashed 1px #333; }
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
#designstyle { background:#a7c9b8; padding:20px; }
#designstyle button i { vertical-align: bottom; }
@media all and (max-width: 800px) {
   #designstyle { padding:10px; }
}
#cal { background:#a7c9b8; height:auto; }


</style>
