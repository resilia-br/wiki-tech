<!-- VARIAVEIS -->
[arrays-mdn]: https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/Arrays
[arrays-w3schools]: https://www.w3schools.com/js/js_arrays.asp
[loopings-arrays-codigo-fonte-tv-yt]: https://www.youtube.com/watch?v=NfHVPEzo5Ik&ab_channel=C%C3%B3digoFonteTV
[tres-formas-usar-arrays-codigo-fonte-tv-yt]: https://www.youtube.com/watch?v=O9wvnvyltgs&ab_channel=C%C3%B3digoFonteTV
[manipular-arrays-e-objetos-dev-soutinho-yt]: https://www.youtube.com/watch?v=yS7AcF-xRUg&ab_channel=DevSoutinho
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que são arrays?
**Array** é um objeto do JavaScript capaz de armazenar múltiplos valores em uma lista, podendo ser armazenado em uma variável. Em tradução para o português podemos entender como uma lista, matriz ou coleção de itens.

Podem ser tratadas de maneira muito similar a outros valores, mas há suas diferenças. É possível acessar os valores dentro da lista individualmente, podemos envolver em um laço de repetição, armazenar dados que fazem sentido num dado contexto e muito mais.

Arrays servem para evitar que armazenemos valores em diversas variáveis, o que seria uma má prática já que é pouco eficiente, aumenta muito a escrita do código, além de ser mais suscetível a erros. Imagine se precisássemos armazenar 1.000 valores diferentes, esse processo seria ainda mais longo.

#### Sintaxe
É necessário colocar os valores entre colchetes (*[]*) e seus valores serão separados por vírgula.
```javascript
var laticinios = ['queijo', 'iogurte', 'manteiga', 'requeijão', 'leite condensado']
```
Aqui demos um exemplo de uma *array* armazenando uma série de laticínios, todos sendo incluídos como *string*, mas esses valores poderiam ser de tipos diferentes também (número, objeto, outra array, valor booleano, outra variável).

Para acessarmos um item específico da array é simples, apenas escrevemos a variável em que está alocada seguida de colchetes e seu índice.

O índice é o número em que aquele item se encontra e na programação é muito comum começarmos a contar do zero, com a array não podia ser diferente.

```javascript
// REPRESENTAÇÃO DOS ÍNDICES
//                  0           1          2           3               4
var laticinios = ['queijo', 'iogurte', 'manteiga', 'requeijão', 'leite condensado']

console.log(laticinios[0]) // imprime: 'queijo'
console.log(laticinios[4]) // imprime: 'leite condensado'
```

##### Ah, mas e como acesso um item de uma array dentro de outra array?
Arrays que tem como item outra array são chamadas de **arrays multidimensionais** e iremos acessar primeiro a array e logo em seguida o item dentro dessa array, vamos ao exemplo:
```javascript
var clientes = [
    ['Marcos', 32, 'Rua Fictícia'], 
    ['Giovana', 60, 'Rua de Mentirinha']
    ['Ana', 42, 'Rua do Bairro']
    ]

console.log(clientes[0]) // imprime: ['Marcos', 32, 'Rua Fictícia']
console.log(clientes[0][0]) // imprime: 'Marcos'
```
Aqui temos uma array que armazena outras arrays com nome, idade e rua de clientes. Perceba que ao usarmos apenas um par de colchetes é acessado apenas o valor daquele índice, que é a própria array. Ao colocarmos o segundo par de colchetes, é retornada a string contida no primeiro índice da array.

### Propriedade length
Podemos saber quantos itens temos na array a partir da propriedade length. Ela irá retornar quantos itens tem na array, ou seja, o comprimento.

```javascript
var numeros = [0, 1, 2, 3, 4, 5, 6]

console.log(numeros.length) // imprime: 7
```
Perceba que temos 7 itens, os números de 0 a 6. Mas é válido ressaltar que **comprimento (*length*) é diferente de índice**. Note que se `length` retornar 0 (zero) significa que a array está vazia, mas se for possível acessar o índice 0 (zero) de uma array significa que temos, pelo menos, um item.

Há muita coisa para se explorar dentro das arrays, como vários métodos possíveis, mas deixaremos isso para a boa e velha documentação :wink:

Aproveite nossa seleção de conteúdo!

## Onde posso aprender mais sobre?
- [[Artigo] **Arrays - MDN**][arrays-mdn]
- [[Artigo - inglês] **Arrays - W3Schools**][arrays-w3schools]
- [[Vídeo] **Como manipular arrays e objetos em JavaScript**][manipular-arrays-e-objetos-dev-soutinho-yt]
- [[Vídeo] **8 Formas de usar Looping em Arrays no JavaScript**][loopings-arrays-codigo-fonte-tv-yt]
- [[Vídeo] **Mais 3 Formas de Como Usar Arrays no JavaScript que Você Precisa Conhecer**][tres-formas-usar-arrays-codigo-fonte-tv-yt]