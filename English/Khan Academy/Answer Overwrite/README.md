# Resposta Sobrescrever

## Código
```js
javascript:"undefined"==typeof originalParse&&(window.originalParse=JSON.parse),console.log("if you look in the console you WILL see a error, they save it as a question though so I'm not worried about it right now."),JSON.parse=function(o,t){let e=originalParse(o,t);try{const o=JSON.parse(e.data.assessmentItem.item.itemData);o.question&&o.question.content&&o.question.content[1]===o.question.content[1].toUpperCase()&&(console.log(o),o.question.content="pt"===location.hostname.split(".")[0]?"Selecione uma opção de resposta.":"Please select a answer choice.\n [[☃ radio 1]] [[☃ explanation 1]]",o.question.widgets={"radio 1":{options:{choices:[{content:"pt"===location.hostname.split(".")[0]?"Correcto":"Correct",correct:!0},{content:"pt"===location.hostname.split(".")[0]?"Incorrecto":"Incorrect",correct:!1}]}},"explanation 1":{options:{explanation:"discord.gg/khanacademy",hidePrompt:"",showPrompt:"Discord"}}},e.data.assessmentItem.item.itemData=JSON.stringify(o))}catch(o){}return e},location.softReload=()=>{const o=document.getElementsByTagName("html")[0].outerHTML;document.open(),document.write(o),document.close()},location.softReload(),console.error=function(){};
```  

## Tutorial 

1) Arraste e largue o código para a sua barra de favoritos
2) Aceda à Khan Academy e active o código
3) Divirta-se!

OU

1) Descarregar Tampermonkey
2) Introduza o código
3) Ativar

## Como funciona?

O Answer Overwrite responde às perguntas da lição da Khan Academy e é uma maneira eficiente de concluir tarefas na Khan sem fazer isso

## Seguro?

Sim, isto é seguro, houve **zero** casos registados de uma conta Khan a ser banida por hacks (pelo menos por agora). Além disso, se você está perguntando se isso é um vírus, é 100% open-sourced para sempre, então você pode olhar através do código para ver por si mesmo.

## Apoie-nos

Por favor, junte-se ao nosso Discord em discord.gg/khanacademy 

Nós fazemos regularmente hacks que as pessoas no nosso discord escolhem, e tu podes juntar-te a eles!

Apoie nosso Repo marcando-o com uma estrela!




