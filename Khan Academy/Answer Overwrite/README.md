# Answer Overwrite

## Code

```js
javascript:"undefined"==typeof originalParse&&(window.originalParse=JSON.parse),console.log("if you look in the console you WILL see a error, they save it as a question though so I'm not worried about it right now."),JSON.parse=function(o,t){let e=originalParse(o,t);try{const o=JSON.parse(e.data.assessmentItem.item.itemData);o.question&&o.question.content&&o.question.content[1]===o.question.content[1].toUpperCase()&&(console.log(o),o.question.content="pt"===location.hostname.split(".")[0]?"Selecione uma opção de resposta.":"Please select a answer choice.\n [[☃ radio 1]] [[☃ explanation 1]]",o.question.widgets={"radio 1":{options:{choices:[{content:"pt"===location.hostname.split(".")[0]?"Correcto":"Correct",correct:!0},{content:"pt"===location.hostname.split(".")[0]?"Incorrecto":"Incorrect",correct:!1}]}},"explanation 1":{options:{explanation:"discord.gg/khanacademy",hidePrompt:"",showPrompt:"Discord"}}},e.data.assessmentItem.item.itemData=JSON.stringify(o))}catch(o){}return e},location.softReload=()=>{const o=document.getElementsByTagName("html")[0].outerHTML;document.open(),document.write(o),document.close()},location.softReload(),console.error=function(){};
```  

## Tutorial 

1) Drag and Drop The Code into your bookmarks bar
2) Go into Khan Academy and activate the code
3) Enjoy!

## How Does It Work?

Answer Overwrite answers the questions on the Khan Academy Lesson, and is a efficient way to complete assignments on Khan without doing it

## Support Us

Please Join our Discord at discord.gg/khanacademy 

We regularly make hacks that people on our discord choose, and you can join in on that!

Support our Repo by starring it!





