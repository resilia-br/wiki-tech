<!-- VARIAVEIS -->
[callback-mdn]: https://developer.mozilla.org/pt-BR/docs/Glossary/Callback_function
[entendendo-callback-medium]: https://medium.com/totvsdevelopers/entendendo-fun%C3%A7%C3%B5es-callback-em-javascript-7b500dc7fa22
[callback-js-marco-bruno-yt]: https://www.youtube.com/watch?v=0haWgdHFuJw&ab_channel=MarcoBruno
[callback-codigo-fonte-tv-yt]: https://www.youtube.com/watch?v=zUtqTM6_-PM&ab_channel=C%C3%B3digoFonteTV
[callback-em-formulario-allan-kildare]: https://codepen.io/allankildare/pen/gOGaqRV
[callback-hell]: http://callbackhell.com/
[javascript-callbacks-js-tutorial]: https://www.javascripttutorial.net/javascript-callback/
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que é uma função callback?
Uma **função callback** é uma função passada como argumento para outra função. Essa função é invocada dentro da função externa para executar uma rotina ou ação.

No JavaScript as *funções callback* são um recurso bastante utilizado, inclusive nativamente na própria linguagem, sendo geralmente funções assíncronas que executam quando algum evento acontece ou algum estado é atingido.

Vamos a um simples exemplo:

```javascript
function soma(arrNumeros) {
  // soma feita usando uma função redutora
  let somaDosNumeros = arrNumeros.reduce((acumulador, valorAtual) => {
    return acumulador + valorAtual
  })
  
  // transformação da array em string, com números separados pelo operador +
  const expressaoDaOperacao = arrNumeros.join(' + ')

  // exibição do resultado
  console.log(`${expressaoDaOperacao} = ${somaDosNumeros}`)
}

function processaSoma(callback) {
  const numeros = [2, 7, 6, 9] // numeros para somar
  const strNumeros = numeros.join(', ') // string com todos os números da array
  console.log(`Vamos somar os números ${strNumeros}`)
  callback(numeros)
}

processaSoma(soma)
/* retorna:
Vamos somar os números 2, 7, 6, 9
2 + 7 + 6 + 9 = 24
*/
```

Neste exemplo a função `processaSoma` é responsável por exibir no console um texto informando quais números irão ser somados e em seguida chama outra função, que é uma chamada de retorno ou *callback*, ela é responsável por exibir a soma de acordo com os números passados na função `processaSoma`. Ao invocarmos a função note que passamos a função `soma` como argumento, evidenciando uma função callback.

### Uso de callback em formulários
Ok, ok, o exemplo acima é bom para entender do que se trata, mas você sabe mesmo como usar na prática? Vamos a um exemplo com um simples formulário.

Vamos imaginar que temos uma página HTML com um formulário apenas para envio do seu nome para uma lista de uma festa. Poderíamos estruturá-lo assim:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário e uso de callback</title>
</head>
<body>
    <form id="feedbackForm">
        <label>Nome completo</label>
        <input type="text" name="" id="nameInput">
        
        <button type="submit">Enviar</button>
      </form>
</body>
</html>
```

E que tal lidarmos com a validação desse campo?
Nesse caso iremos apenas validar se este campo está vazio, mas poderiam ser feitas outras checagens.
```javascript
// elementos no DOM
const feedbackForm = document.getElementById("feedbackForm")
const nameInput = document.getElementById("nameInput")

function validaFormulario(event) {
  // previne comportamento padrão do evento
  event.preventDefault()

  // retorna true se o campo está vazio e false caso tenha pelo menos um caractere
  const campoNomeEstaVazio = nameInput.value === ""

  // testa se o campo está vazio
  if (campoNomeEstaVazio) {
    alert("Você deixou o campo de nome vazio, favor preenchê-lo")
  } else {
    alert("Seu nome foi enviado com sucesso!")
  }
}

// método addEventListener recebe a função validaFormulario como callback
feedbackForm.addEventListener("submit", validaFormulario)
```
Este exemplo mostra um caso real de como podemos usar uma função callback para lidar com formulários. O método usado é o `addEventListener` e ele basicamente fica "escutando" o evento que lhe é passado como argumento, no nosso caso o evento passado foi o próprio onSubmit, passado como uma *string* escrita "submit".

A função `validaFormulario` é a responsável por lidar com o que será feito antes da submissão do formulário, neste caso checamos se o campo está vazio ou não, exibindo um `alert` de falha ou sucesso dependendo do caso.

Poderíamos usar uma função responsável por fazer uma requisição enviando os dados dos possíveis campos após a validação por exemplo, o que seria outra callback já que uma função invoca a outra. Porém tome cuidado, ficar invocando uma sequência de funções dentro da outra pode resultar em um caso de ***Callback Hell***, muito comum quando estamos falando de programação assíncrona e você pode aprender mais sobre [neste link][callback-hell].

Você pode ver um exemplo de formulário um pouco mais complexo [neste Pen][callback-em-formulario-allan-kildare] do Allan Kildare, nosso Resiliente.

E aí, gostou do nosso conteúdo? Desfrute do nosso material selecionado!
## Onde posso aprender mais sobre?
- [[Artigo] **Callback - MDN**][callback-mdn]
- [[Vídeo] **Callback // Dicionário do Programador**][callback-codigo-fonte-tv-yt]
- [[Artigo] **Entendendo funções callback em JavaScript**][entendendo-callback-medium]
- [[Vídeo] **Callback no JavaScript**][callback-js-marco-bruno-yt]
- [[Website] **Callback Hell**][callback-hell]
- [[Artigo - inglês] **JavaScript Callback**][javascript-callbacks-js-tutorial]