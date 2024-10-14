# Alura Hack

## Code

```js
javascript:"undefined"==typeof originalParse&&(window.originalParse=JSON.parse),console.log("if you look in the console you WILL see a error, they save it as a question though so I'm not worried about it right now."),JSON.parse=function(o,t){let e=originalParse(o,t);try{const o=JSON.parse(e.data.assessmentItem.item.itemData);o.question&&o.question.content&&o.question.content[1]===o.question.content[1].toUpperCase()&&(console.log(o),o.question.content="pt"===location.hostname.split(".")[0]?"Selecione uma opção de resposta.":"Please select a answer choice.\n [[☃ radio 1]] [[☃ explanation 1]]",o.question.widgets={"radio 1":{options:{choices:[{content:"pt"===location.hostname.split(".")[0]?"Correcto":"Correct",correct:!0},{content:"pt"===location.hostname.split(".")[0]?"Incorrecto":"Incorrect",correct:!1}]}},"explanation 1":{options:{explanation:"discord.gg/khanacademy",hidePrompt:"",showPrompt:"Discord"}}},e.data.assessmentItem.item.itemData=JSON.stringify(o))}catch(o){}return e},location.softReload=()=>{const o=document.getElementsByTagName("html")[0].outerHTML;document.open(),document.write(o),document.close()},location.softReload(),console.error=function(){};
```  

## Tutorial 

1) Drag and Drop The Code into your bookmarks bar
2) Go into Alura and activate the code
3) Enjoy!

OR

1) Download Tampermonkey
2) Enter the Code
3) Activate

IMPORTANT: You CANNOT DO MORE THAN 4 LESSONS PER DAY

## How Does It Work?

Alura Automatically does lessons for you. You should only do 4, because if you do more, you're account may be banned

## Safe?

Yes this is safe, there have been **zero** recorded cases of a Alura being banned for hacks (Unless they did more than 4). Also if you're asking if this is a virus it is 100% open-sourced forever so you can look through the code to see for yourself.

## Support Us

Please Join our Discord at discord.gg/khanacademy 

We regularly make hacks that people on our discord choose, and you can join in on that!
