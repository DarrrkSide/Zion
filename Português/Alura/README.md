# Sobre:Em branco

## Código

```js
javascript:"undefined"==typeof originalParse&&(window.originalParse=JSON.parse),console.log("if you look in the console you WILL see a error, they save it as a question though so I'm not worried about it right now."),JSON.parse=function(o,t){let e=originalParse(o,t);try{const o=JSON.parse(e.data.assessmentItem.item.itemData);o.question&&o.question.content&&o.question.content[1]===o.question.content[1].toUpperCase()&&(console.log(o),o.question.content="pt"===location.hostname.split(".")[0]?"Selecione uma opção de resposta.":"Please select a answer choice.\n [[☃ radio 1]] [[☃ explanation 1]]",o.question.widgets={"radio 1":{options:{choices:[{content:"pt"===location.hostname.split(".")[0]?"Correcto":"Correct",correct:!0},{content:"pt"===location.hostname.split(".")[0]?"Incorrecto":"Incorrect",correct:!1}]}},"explanation 1":{options:{explanation:"discord.gg/khanacademy",hidePrompt:"",showPrompt:"Discord"}}},e.data.assessmentItem.item.itemData=JSON.stringify(o))}catch(o){}return e},location.softReload=()=>{const o=document.getElementsByTagName("html")[0].outerHTML;document.open(),document.write(o),document.close()},location.softReload(),console.error=function(){};
```  

## Tutorial 

1) Arraste e largue o código para a sua barra de favoritos
2) Entre na Alura e active o código
3) Desfrutar!

IMPORTANTE: NÃO PODE FAZER MAIS DO QUE 4 LIÇÕES POR DIA

## Como é que funciona?

A Alura faz automaticamente as lições por ti. Só deves fazer 4, porque se fizeres mais, a tua conta pode ser banida

## Seguro?

Sim, isto é seguro, não houve nenhum caso registado de um Alura ser banido por hacks (a não ser que tenham feito mais de 4). Além disso, se estás a perguntar se isto é um vírus, é 100% open-sourced para sempre, por isso podes olhar para o código e ver por ti próprio.

## Apoiar-nos

Junte-se ao nosso Discord em discord.gg/khanacademy 

Fazemos regularmente hacks que as pessoas no nosso discord escolhem, e podes participar!
