# Khan Academy Hacks


## Tutorial (General)

1) Drag and Drop The Code into your bookmarks bar
2) Go into Khan Academy and activate the code
3) Enjoy!

OR

1) Download Tampermonkey
2) Enter the Code
3) Activate

## Code

### Answer Overwrite

```js
javascript:"undefined"==typeof originalParse&&(window.originalParse=JSON.parse),console.log("if you look in the console you WILL see a error, they save it as a question though so I'm not worried about it right now."),JSON.parse=function(o,t){let e=originalParse(o,t);try{const o=JSON.parse(e.data.assessmentItem.item.itemData);o.question&&o.question.content&&o.question.content[1]===o.question.content[1].toUpperCase()&&(console.log(o),o.question.content="pt"===location.hostname.split(".")[0]?"Selecione uma opção de resposta.":"Please select a answer choice.\n [[☃ radio 1]] [[☃ explanation 1]]",o.question.widgets={"radio 1":{options:{choices:[{content:"pt"===location.hostname.split(".")[0]?"Correcto":"Correct",correct:!0},{content:"pt"===location.hostname.split(".")[0]?"Incorrecto":"Incorrect",correct:!1}]}},"explanation 1":{options:{explanation:"discord.gg/khanacademy",hidePrompt:"",showPrompt:"Discord"}}},e.data.assessmentItem.item.itemData=JSON.stringify(o))}catch(o){}return e},location.softReload=()=>{const o=document.getElementsByTagName("html")[0].outerHTML;document.open(),document.write(o),document.close()},location.softReload(),console.error=function(){};
```  

Answer Overwrite answers the questions on the Khan Academy Lesson, and is a efficient way to complete assignments on Khan without doing it

### Energy Point Farmer

```js
javascript:(function(){for(let e=0;e<1e4;e++){clearInterval(e)}document.open();document.write(` <style> body { margin: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #2c2f33;%20color:%20#ffffff;%20}%20#app%20{%20display:%20flex;%20flex-direction:%20column;%20min-height:%20100vh;%20}%20header,%20footer%20{%20background-color:%20#23272a;%20padding:%201em;%20text-align:%20center;%20}%20main%20{%20flex:%201;%20padding:%202em;%20}%20.card%20{%20background-color:%20#36393f;%20border-radius:%208px;%20padding:%201em;%20box-shadow:%200%204px%208px%20rgba(0,%200,%200,%200.2);%20}%20a%20{%20color:%20#7289da;%20text-decoration:%20none;%20}%20a:hover%20{%20text-decoration:%20underline;%20}%20input%20{%20background-color:%20#36393f;%20border-radius:%208px;%20padding:%201em;%20box-shadow:%200%204px%208px%20rgba(0,%200,%200,%200.2);%20color:%20white;%20margin-bottom:%201em;%20}%20button%20{%20background-color:%20#7289da;%20border-radius:%208px;%20padding:%201em;%20color:%20white;%20border:%20none;%20cursor:%20pointer;%20}%20button:hover%20{%20background-color:%20#5a6fb3;%20}%20p%20{%20margin:%200.5em%200;%20}%20%3C/style%3E%20%3Cdiv%20id=%22app%22%3E%20%3Cheader%3E%20%3Ch1%3EFarmer%3C/h1%3E%20%3C/header%3E%20%3Cmain%3E%20%3Csection%20class=%22card%22%3E%20%3Ch2%3EPoints,%20%3Cspan%20id=%22total%22%3E%3C/span%3E%3C/h2%3E%20%3Cp%3EPlease%20enter%20in%20a%20link%20to%20a%20unique%20Khan%20lesson%20or%20%3Ca%20href=%22/%22%3Elet%20me%3C/a%3E%20get%20one%20for%20you.%3C/p%3E%20%3C/section%3E%20%3Cinput%20id=%22input%22%20placeholder=%22URL...%22%3E%3C/input%3E%20%3Cbutton%20onclick=%22farm()%22%3EFarm%3C/button%3E%20%3Cp%3ERigs%20farming:%20%3Cspan%20id=%22lessonsFarming%22%3E0%3C/span%3E%3C/p%3E%20%3Cp%3EEP%20gained:%20%3Cspan%20id=%22pointsFarmed%22%3E0%3C/span%3E%3C/p%3E%20%3Cp%3EEP%20gained%20(1m):%20%3Cspan%20id=%22min%22%3E0%3C/span%3E%3C/p%3E%20%3C/main%3E%20%3Cfooter%3E%20%3Cp%3E&copy;%202024%20IlyTobias%3C/p%3E%20%3C/footer%3E%20%3C/div%3E%20%60);document.close();let%20o=0;let%20a=0;let%20i=0;let%20rigsFarming=0;function%20e(){let%20n=document.createElement(%22iframe%22);n.src=%22https://www.khanacademy.org/profile/me/courses%22;document.body.appendChild(n);n.onload=function(){setTimeout(function(){let%20t=%22%22;for(let%20e%20of%20n.contentWindow.document.getElementsByClassName(%22odometer-ribbon-inner%22)){t+=e.textContent}n.remove();let%20e=parseInt(t.replace(/,/g,%22%22),10);if(!isNaN(e)){let%20pointsGained=e-a;if(a===0){pointsGained=0}o=e;i+=pointsGained;document.getElementById(%22pointsFarmed%22).textContent=i;document.getElementById(%22min%22).innerText=pointsGained;document.getElementById(%22total%22).innerText=o;a=o}},3e3)}}window.farm=function(){let%20o=document.getElementById(%22input%22).value;(function(){let%20e=document.createElement(%22div%22);const%20t=Math.floor(Math.random()*1e8);e.innerHTML=%60%3Ciframe%20id=%22egg${t}%22%20style=%22display:none;%22%20src=%22${o}%22%3E%3C/iframe%3E%60;document.body.appendChild(e);let%20n=document.createElement(%22script%22);n.innerHTML=%60%20const%20de%20=%20function(e,%20t)%20{%20let%20n%20=%20document.getElementsByTagName(e);%20for%20(let%20i%20=%200;%20i%20%3C%20n.length;%20i++)%20{%20if%20(n[i].textContent.trim()%20===%20t)%20{%20return%20n[i];%20}%20}%20return%20null;%20};%20function%20e(e,%20t)%20{%20let%20n%20=%20de(e,%20t);%20if%20(n)%20{%20n.scrollIntoView();%20n.click();%20}%20}%20function%20t(e)%20{%20let%20t%20=%20document.getElementsByClassName(e)[0];%20if%20(t)%20{%20t.scrollIntoView();%20t.click();%20}%20}%20setInterval(function()%20{%20e(%22button%22,%20%22Let%E2%80%99s%20go%22);%20t(%22_ssxvf9l%22);%20e(%22button%22,%20%22Check%22);%20e(%22button%22,%20%22Try%20again%22);%20e(%22button%22,%20%22Next%20question%22);%20e(%22button%22,%20%22Show%20summary%22);%20},%203000);%20%60;document.getElementById(%22egg%22+t).contentWindow.document.body.appendChild(n);let%20a=JSON.parse;document.getElementById(%22egg%22+t).contentWindow.JSON.parse=function(e,t){let%20o=a(e,t);try{for(let%20n=0;n%3CObject.keys(o.data).length;n++){let%20e=o.data[Object.keys(o.data)[n]];let%20t=Object.keys(o.data)[n];if(t===%22assessmentItem%22){console.log(e);o.data[Object.keys(o.data)[n]].item.o='{%22answerArea%22:{%22calculator%22:false,%22chi2Table%22:false,%22periodicTable%22:false,%22tTable%22:false,%22zTable%22:false},%22hints%22:[{%22content%22:%22$\\\\begin{align}\\\\left(\\\\dfrac{z^{4}}{6^{2}}\\\\right)^{-3}&=\\\\dfrac{\\\\left(z^{4}\\\\right)^{-3}}{\\\\left(6^{2}\\\\right)^{-3}}\\\\end{align}$%22,%22images%22:{},%22replace%22:false,%22widgets%22:{}},{%22content%22:%22$\\\\begin{align}\\\\phantom{\\\\left(\\\\dfrac{z^{4}}{6^{2}}\\\\right)^{-3}}&=\\\\dfrac{z^{(4)(-3)}}{6^{(2)(-3)}}\\\\n\\\\dfrac{6^{6}}{z^{12}}\\\\end{align}$%22,%22images%22:{},%22replace%22:false,%22widgets%22:{}}],%22itemDataVersion%22:{%22major%22:0,%22minor%22:1},%22question%22:{%22content%22:%22Khan%20cheat%20made%20by%20ilyTobias[[%E2%98%83%20radio%201]]%22,%22images%22:{},%22widgets%22:{%22radio%201%22:{%22alignment%22:%22default%22,%22graded%22:true,%22options%22:{%22choices%22:[{%22content%22:%22Correct%20answer%22,%22correct%22:true},{%22content%22:%22Incorrect%20answer%22,%22correct%22:false}],%22deselectEnabled%22:false,%22displayCount%22:null,%22hasNoneOfTheAbove%22:false,%22multipleSelect%22:false,%22onePerLine%22:true,%22randomize%22:false},%22static%22:false,%22type%22:%22radio%22,%22version%22:{%22major%22:1,%22minor%22:0}}}}}'}}}catch(e){}return%20o}})();rigsFarming++;document.getElementById(%22lessonsFarming%22).textContent=rigsFarming};setInterval(e,6e4);e()})();
```  

Farmer is a efficent way to grind energy points, so if you want to get energy points, this is the strat!

This only has a 50% chance of working

## Safe?

Yes this is safe, there have been **zero** recorded cases of a Khan account being banned for hacks (at least for now). Also if you're asking if this is a virus it is 100% open-sourced forever so you can look through the code to see for yourself.

## Support Us

Please Join our Discord at discord.gg/khanacademy 

We regularly make hacks that people on our discord choose, and you can join in on that!

Support our Repo by starring it!

