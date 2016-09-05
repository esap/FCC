# FCC
|序|算法题名称|行数|代码片段（单行省略return)|
|:----|:--|:--|:--|
|1|Reverse a String|1|```str.split('').reverse().join('');```|
|2|Factorialize a Number|1|```num<2 ? (num || 1) : num*factorialize(num-1);```|
|3|Check for Palindromes|2|```str=str.toLowerCase().replace(/[^0-9a-z]/g,'');  return str==str.split('').reverse().join(''); ```|
|4|Find the Longest Word in a String|1|```Math.max(...str.split(' ').map(v => v.length));```|
|5|Title Case a Sentence|1|```str.toLowerCase().replace(/(^|\s)\w/g, v => v.toUpperCase());```|
|6|Return Largest Numbers in Arrays|1|```arr.map(v => Math.max(...v));```|
|7|Confirm the Ending|1|```RegExp(target+'$').test(str);```|
|8|Repeat a string repeat a string|1|```Array(num<0 ? 0 : num+1).join(' ').replace(/\s/g, str);```|
|9|Truncate a string|1|```(num<str.length) ? (num<=3 ? str.slice(str, num-str.length) : str.slice(str, num-str.length-3))+... : str;```|
|10|Chunky Monkey|1|```arr.reduce((p, c, i, a) => (i%size===0 ? p.concat([a.slice(i, i+size)]) : p), []);```|
|11|Slasher Flick|1|```arr.slice(howMany);```|
|12|Mutations|1|```!arr[1].replace(RegExp('['+arr[0]+'[]','gi'),);```|
|13|Falsy Bouncer|1|```arr.filter(Boolean);```|
|14|Seek and Destroy|1|```arr.filter(v => Array.from(arguments).slice(1).indexOf(v)<0);```|
|15|Where do I belong|1|```arr.filter(v => v<num).length;```|
|16|Caesars Cipher|1|```str.replace(/[A-Z]/g, v => String.fromCharCode(v.charCodeAt()<78 ? v.charCodeAt()+13 : v.charCodeAt()-13));```|
|17|Sum All Numbers in a Range|1|```arr.reduce((p, c) => (p+c)*(Math.abs(p-c)+1)/2);```|
|18|Diff Two Arrays|1|```arr1.concat(arr2).filter(v => arr1.indexOf(v)<0 || arr2.indexOf(v)<0);```|
|19|Roman Numeral Converter|2|```var table=[['I','II','III','IV','V','VI','VII','VIII','IX'],['X','XX','XXX','XL','L','LX','LXX','LXXX','XC'],['C','CC','CCC','CD','D','DC','DCC','DCCC','CM'], ['M','MM','MMM','MV','V','VM','VMM','VMMM','MX']]; return String(num).split('').map((v, i, a) => table[a.length-i-1][v-1]).join('');```|
|20|Where art thou|1|```collection.filter(v => { for (var p in source) if (v[p] != source[p]) return false; return true; });```|
|21|Search and Replace|1|```str.replace(RegExp(before,'g'), v => before.charCodeAt(0)<90 ? after.replace(/^\w/g, (v) => v.toUpperCase()) : after);```|
|22|Pig Latin|1|```(str.match(/[^aeiou]*/)=='' ? str + w : str.replace(/([^aeiou]*)([aeiou]\w*)/,$2$1)) + ay;```|
|23|DNA Pairing|1|```str.split('').map(v => (v+{ A:'T', T:'A', C:'G', G:'C' }[v]).split(''));```|
|24|Missing letters|2|```var letter = str.split('').map(v => v.charCodeAt()+1).filter((v, i, a)=>v+1!=a[i+1] && i+1<a.length); return letter !=  ? String.fromCharCode(letter) : undefined;```|
|25|Boo who|1|```typeof bool=='boolean';```|
|26|Sorted Union|1|```Array.from(arguments).reduce((p, c) => p.concat(c)).reduce((p,c) => p.indexOf(c)<0 ? p.concat([c]) : p, []);```|
|27|Convert HTML Entities|2|```t ={&: &amp;, <: &lt;, >: &gt;, '': &quot;, ': &apos;}; return str.replace(/[&<>']/g, v => t[v]);```|
|28|Spinal Tap Case|1|```str.replace(/(\W|_)/g, '-').replace(/\w(?=[A-Z])/g, v => v+'-').toLowerCase();```|
|29|Sum All Odd Fibonacci Numbers|4|```var fb=[1, 1]; for (var i=2; fb[i-1]+fb[i-2]<=num; i++)  fb[i]=fb[i-1]+fb[i-2]; return eval(fb.filter(v => v%2).join(+));```|
|30|Sum All Primes|1|``` eval(Array(num).join(' ').split('').map((v, i) => i+2).filter(v => { for(var j=2;j<v;j++)   if (v%j===0) return false;    return true; }).join('+'));```|
|31|Smallest Common Multiple|2|```var [min, max] = arr.sort((a, b) => a-b);  return Array(max-min+2).join(' ').split('').map((v, i) => i+min).reduce((p, c) => {for(var i=1;; i++) if ((c*i)%p===0) return c*i;);```|
|32|Finders Keepers|1|```arr.filter(func)[0];```|
|33|Drop it|1|```(!arr.length || arr.slice(0,1).filter(func).length) ? arr : drop(arr.slice(1), func);```|
|34|Steamroller|1|```eval([ + JSON.stringify(arr).replace(/[\[\]]/g,).replace(/,,/g,,) + ]);```|
|35|Binary Agents|1|```str.split( ).map(v=>String.fromCharCode(parseInt(v,2))).join();```|
|36|Everything Be True|1|```collection.reduce((p, c, i, a) => c[pre] ? p+1 : p, 0)==collection.length;```|
|37|Arguments Optional|3|```for (var i=0;i<arguments.length;i++) if (!(arguments[i]===+arguments[i])) return undefined; return (arguments.length==1) ? (v => v===+v ? v+arguments[0] : undefined) : eval(Array.from(arguments).join('+'));```|
|38|Validate US Telephone Numbers|1|```/^(1\s?)?(\(\d{3}\)|\d{3})[\s\-]?\d{3}[\s\-]?\d{4}$/.test(str);```|
|39|Symmetric Difference|1|```Array.from(arguments).reduce((p, c) => p.concat(c).filter((v, i, a) => v!=a[i+1] && (p.indexOf(v)<0 || c.indexOf(v)<0)));```|
|40|Exact Change|14|```var change=[], i, cid2={};  var list={TWENTY: 20, TEN: 10, FIVE: 5, ONE: 1, QUARTER:0.25,DIME: 0.1, NICKEL: 0.05,PENNY:0.01};  var [c, r] = [cid.slice().reduce((p, c) => p+c[1], 0), cash-price];  if(c==r) return Closed;  if(c<r) return Insufficient Funds;  cid.map(v => {cid2[v[0]]=v[1]; });  for (var k in list) {    if (r>=list[k]) {      i=Math.min(r-r%list[k], cid2[k]); if (i > 0) { change.push([k, i]); r=(r-i).toFixed(2);}}}  if (r > 0) return Insufficient Funds;    return change;```|
|41|Inventory Update|1|```arr1.concat(arr2).sort((x, y) => x[1].localeCompare(y[1])).reduce((p, c, i, a) => {      if (i<a.length-1 && c[1]==a[i+1][1]) return p.concat([[c[0]+a[i+1][0],c[1]]]);      if (i>0 && c[1]==a[i-1][1]) return p;      return p.concat([c]);    },[]);```|
|42|No repeats please|9|```var collection = [];  var pmt = (str, arr) => {    if (arr.length==1) {      collection.push(str + arr[0]);    } else {      for (var i=0; i<arr.length; i++) {            arr2 = arr.slice();                pmt(str + arr2.splice(i,1)[0], arr2);      }    }     };  pmt('', str.split(''));  return collection.filter(v => !v.match(/(.)\1+/g)).length;```|
|43|Friendly Date Ranges|20|```var monName =[January, February, March, April, May, June, July, August, September, October, November, December];  var dayChg = v => {    if (v==1) return 1st;    if (v==2) return 2nd;    if (v==3) return 3rd;    return v+th;  };  arr = arr.map(v => v.split(-).map(v => +v));  var today = new Date();  var flagYear = arr.reduce((p,c) => c[0]*365+c[1]*30+c[2]-p,0);  var flagMon = (arr[0][1]==arr[1][1]);  var flagThisYear = (arr[0][0]==(today.getFullYear()));  arr = arr.map(v => [monName[v[1]-1],dayChg(v[2]),v[0]]);  if (flagYear===0) {    arr.splice(1,1);  } else if (flagYear<365) {    arr[1].splice(2,1);    if (flagThisYear) arr[0].splice(2,1);    if (flagMon && flagYear<300) arr[1].splice(0,1);   }     arr.forEach(v => v.length>2?v[1]=v[1]+,:v[1]);  return arr.map(v => v.join(' '));```|
|44|Make a Person|7|```var [f,l] = name.split( );  this.getFirstName = () => { return f; };  this.getLastName = () =>  { return l; };  this.getFullName = () =>  { return f +  + l; };  this.setFirstName = (first) => { f= first; };  this.setLastName = (last) => { l= last;  };  this.setFullName = (name) => { [f,l] = name.split( ); };  ```|
|45|Map the Debris|1|```arr.map(v => {v.orbitalPeriod=Math.round(2*Math.PI*Math.sqrt(Math.pow(earthRadius+v.avgAlt ,3)/GM));    delete v.avgAlt;    return v;  });```|
|46|Pairwise|1|```arr.reduce( (p, c, i, arr) => {    var myWife = arr.slice(i+1).indexOf(arg-c);    if (myWife>=0) {      p+=i+i+1+myWife;      arr.splice(myWife+1+i,1,arg+1);      arr.splice(i,1,arg+1);      }    return p;  },0);```|
