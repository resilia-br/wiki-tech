<!-- VARIAVEIS -->
[funcoes-mdn]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Functions
[parametros-pre-definidos-mdn]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Functions/Default_parameters
[funcoes-guanabara-yt]: https://www.youtube.com/watch?v=mc3TKp2XzhI&ab_channel=CursoemV%C3%ADdeo
[funcoes-programador-br-yt]: https://www.youtube.com/watch?v=zNimSYkrs6w&ab_channel=ProgramadorBR
[higher-orders-functions-cod3r-yt]: https://www.youtube.com/watch?v=cGrTcnorZgs&ab_channel=Cod3rCursos
[escopo-funcao-yt]: https://www.youtube.com/watch?v=FqkSOhIuDNU&ab_channel=RogerMelo
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que é uma função?
As funções são blocos de construção fundamentais no JavaScript. A função pode ser entendida como uma funcionalidade, nada mais é que um procedimento, no qual você pode fazer diversas instruções para executar uma tarefa ou calcular.

Para declarar um função você deve usar a palavra reservada **function**, seguida de seu nome, lista de parâmetros para a função (separados por vígulas e entre parênteses) e o par de chaves para definição do escopo.

#### Sintaxe
```javascript
function saudacao(nome) {
    return `Olá ${nome}, espero que tenha um ótimo dia!`
}
```

O uso da palavra reservada `return` evidencia o retorno da função. A linha após o uso do `return` não é mais executada, quando dentro daquele escopo. Caso queira escrever um retorno em múltiplas linhas será necessário envolver o retorno em parênteses.

A função `saudacao` tem um parâmetro declarado chamado `nome` que é usado posteriormente como argumento para retornar uma `string` com uma saudação para o nome passado como argumento.

## Mas afinal, qual a diferença entre parâmetro e argumento?
O **parâmetro** é a variável que vai receber um valor em uma função (ou método), enquanto o argumento é o valor que você vai passar para a função, que pode ser originado de uma variável ou expressão.

Quando chamamos uma função não passamos parâmetros, passamos argumentos. Os parâmetros são variáveis que estão preparadas para futuros valores, e os argumentos são os valores que desejamos executar dentro do escopo da função.

```javascript
function soma(numero1, numero2) { // declaração de dois parâmetros
    return numero1 + numero2 // dois argumentos sendo utilizados para o retorno da função
}
```

Os argumentos passados para essa função poderiam ser 5 e 9, por exemplo:
```javascript
soma(5, 9)
// retorna 14
```

## Onde posso aprender mais sobre?
- [[Artigo] **Funções**][funcoes-mdn]
- [[Artigo] **Parâmetros Predefinidos**][parametros-pre-definidos-mdn]
- [[Curso, vídeo] **Funções - Curso JavaScript**][funcoes-guanabara-yt]
- [[Vídeo] **FUNÇÕES EM JAVASCRIPT**][funcoes-programador-br-yt]
- [[Vídeo] **Programador JavaScript PRECISA DOMINAR essa TÉCNICA! (Higher Order Functions)**][higher-orders-functions-cod3r-yt]
- [[Vídeo] **O que é escopo de função | JavaScript**][escopo-funcao-yt]