<!-- VARIAVEIS -->
[increment-operator-mdn]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Increment
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que são estruturas de repetição?
Uma **estrutura de repetição** ou **laço de repetição** é responsável por repetir uma ação múltiplas vezes. No JavaScript há diferentes estruturas e mecanismos que nos permitem determinar quando um laço irá começar ou terminar. É importante pensar que tudo depende do contexto e que, uma estrutura pode ser mais recomendada que outra.

Veremos a seguir os possíveis laços:

## for
A estrutura de repetição for é repetida até que a condição especificada seja falsa.

#### Sintaxe
```javascript
for (expressaoInicial; condicao; incremento) {
    // instruções aqui
}
```

- A `expressaoInicial` é inicializada e, caso possível, executada. É comum inicializarmos um ou mais contadores nessa expressão, podendo, inclusive, conter a declaração de variáveis.
- Toda vez que o laço é executado a expressão `condicao` é avaliada e, caso seu reesultado seja verdadeiro, o laço é executado, se for falso sua execução é interrompida e, assim, terminará. Se `condicao` for omitida, é sempre assumida como verdadeira
- Depois as intruções são executadas
- E por último há a atualização da expressão `incremento`, que é executada. Essa atualização do incremento é o que define como o laço irá se repetir, por exemplo, de um em um, de dois em dois, etc.

Vamos para um exemplo:
```javascript
for (let contador = 1; contador <= 5; contador++) {
    console.log(`Número ${contador}`)
}
/* retorna:
Número 1
Número 2
Número 3
Número 4
Número 5
*/
```
Nesse exemplo, uma variável chamada contador foi declarada com o valor inicial 1 e assim o laço de repetição é inicializado. A condição é que o valor de `contador` seja menor ou igual a 5, ou seja, 5 é o valor máximo que essa variável pode assumir dentro do laço. O incremento é feito com o [operador de incremento ++][increment-operator-mdn], que adiciona 1 ao seu operando, ou seja, quando for 1 ele retorna 2, quando for 2 ele retorna 3 e assim por diante.

O que vemos no console é justamente a atualização da variável `contador`, sendo executada e posteriormente demonstrada.

Antes de seguir para outra estrutura, vamos a outro exemplo:
```javascript
const arrBaguncado = [
    'Emanuel', 21, 'Julia',
    true, 97, 'Gabriel',
    2019, 'Carolina', 'Bruno',
    { nome: 'Armando' }, 'Eduarda', 'Artur'
    ]
let apenasNomes = []

for (let i = 0; i < arrBaguncado.length; i++) {
    if(typeof arrBaguncado[i] === 'string') {
        apenasNomes.push(arrBaguncado[i])
    }
}

console.log(apenasNomes)
/* retorna:
[ 'Emanuel', 'Julia', 'Gabriel', 'Carolina', 'Bruno', 'Eduarda', 'Artur' ]
*/
```
Neste exemplo, estamos fazendo uma filtragem. Começamos com um array que contém diversos valores, entre eles algumas *strings* com nomes, valores booleanos, números e até um objeto, mas nosso objetivo é ter outro array que tenham apenas nomes.

Para essa situação vamos usar o laço de repetição `for`
- Inicialmente é importante inicializarmos com o valor `0`, porque o primeiro índice de um array é justamente o zero. 
- Também é importante ressaltar que a declaração da variável com o nome `i` é muito comum e quase uma convenção entre os programadores.
- Logo depois, a expressão passada como condição é uma tática para que não precisemos colocar o tamanho real do array, a propriedade `length` retorna o número de elemento de um array, por isso definimos como apenas **menor que** `<` e não **menor ou igual**, pois length começa sua contagem em 1, se houver elemento existente no array. Imagine que o array tem 5 elementos, length retornará 5, mas o último elemento está no índice 4.
- Novamente usamos o operador de incremento ++ e o laço está executando de um em um elemento do array.
- A cada vez que as intruções são executadas, validamos se é do tipo `string` e, se for, adicionamos no array `apenasNomes`, já que os nomes estão escritos como *strings*. Note que se não for do tipo, nada é feito.

## do...while
A instrução da estrutura `do...while` também se repetirá até que a condição seja falsa. Sua sintaxe é bem diferente do laço `for` e, em português, basicamente quer dizer que irá executar instrução enquanto a condição continue verdadeira, sua tradução literal é *faça...enquanto*.

#### Sintaxe
```javascript
do {
    // instruções aqui
} while (condicao)
```

Vamos fazer o mesmo exemplo (1° exemplo) do loop `for`, mas dessa vez usando a sintaxe do `do...while`
```javascript
let i = 0
do {
    i += 1
    console.log(`Número ${i}`)
} while (i < 5)
/* retorna:
Número 1
Número 2
Número 3
Número 4
Número 5
*/
```
O retorno desse exemplo continua sendo o mesmo. Perceba que a variável `i` teve que ser inicializada fora do escopo da estrutura `do...while` para que pudéssemos acessar dentro do bloco do `do`. Também é possível perceber o uso do operador de atribuição +=, ele é um jeito encurtado de dizermos que um operando (à esquerda, que pode ser uma variável) é igual a ele mesmo mais (+) o que está à direita. Nesse caso é o mesmo que declararmos `i = i + 1`.

## Onde posso aprender mais sobre?