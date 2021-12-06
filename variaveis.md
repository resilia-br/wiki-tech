<!-- VARIAVEIS -->
[variables-mdn]: https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/Variables
[cases-betterprogramming]: https://betterprogramming.pub/string-case-styles-camel-pascal-snake-and-kebab-case-981407998841
[var-let-const-diferenca-alura]: https://www.alura.com.br/artigos/entenda-diferenca-entre-var-let-e-const-no-javascript
[var-let-const-diferenca-linkedin-gabriel]: https://www.linkedin.com/pulse/qual-diferen%C3%A7a-entre-var-let-e-const-javascript-gabriel-de-jesus/?originalSubdomain=pt
[var-let-const-diferenca-programador-br-yt]: https://www.youtube.com/watch?v=ZOx7iTnBqFQ&ab_channel=ProgramadorBR
[var-let-const-diferenca-marco-bruno-yt]: https://www.youtube.com/watch?v=EFoEqHIwxqY&ab_channel=MarcoBruno
[const-let-var-website]: https://constletvar.com/
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que são variáveis?
Uma **variável** é uma forma de armazenamento de dados muito comum nas linguagens de programação. Nada mais é que um espaço na memória do computador destinado ao armazenamento de um dado. No JavaScript temos algumas formas de declarar variáveis e iremos explorá-las neste documento.

Para se declarar uma variável é preciso declarar sua palavra reservada, que no JavaScript são três (`var`, `let` e `const`) e em seguida nomeá-la, e pronto, sua declaração está feita. Após isso, é possível atribuir um valor à variável usando o símbolo de igual e logo em seguida seu valor.

#### camelCase vs snake_case
Antes de nos aprofundarmos no assunto, é importante falar que há uma convenção no nome de variáveis, geralmente vemos as variáveis serem nomeadas seguindo a convenção **camelCase**, que a primeira letra é escrita em minúsculo e a letra inicial das palavras seguintes (se existirem) é escrita em maiúsculo, recebe esse nome pois a aparência visual do nome da variável lembra corcovas de camelo.

Os palavras que seguem a convenção **snake_case** são todas escritas em minúsculo e separadas por um subtraço, também conhecido popularmente como *underline* e recebe esse nome pois sua aparência lembra a segmentação de uma cobra.

Ambas as convenções são aceitas, mas no Javascript a convenção **camelCase** é mais popular e disseminada, então há forte recomendação de ser seguida. Vale frisar que também é seguida na declaração de funções, metódos e até nos próprios métodos nativos da linguagem.

## var
A palavra reservada `var` define uma variável e foi a primeira a existir no Javascript. Vejamos alguns exemplos:
```javascript
var idade
var nomeESobrenome = 'Marcos Silva'

console.log(idade) // retorna undefined
console.log(nomeESobrenome) //  retorna 'Marcos Silva'
```

Na primeira linha a variável `idade` foi apenas declarada, então retorna `undefined` (indefinido), que basicamente explicita que ela está declarada, mas nenhum valor lhe foi atribuída. A segunda retorna a *string* que armazenamos na variável `nomeESobrenome`

A variável `var` permite a reatribuição de um valor, redeclarando-se e assim assumindo um novo valor (atualização) e há duas formas de fazer isso. Vamos aos exemplos:
```javascript
var cor = 'amarelo'
var cor = 'verde'
```
ou
```javascript
var cor = 'amarelo'
cor = 'verde'
```
Essa forma de redeclarar a variável implica em um dos problemas que as variáveis declaradas com `var` têm. E vamos abordá-lo a seguir, pense no seguinte cenário
```javascript
var nome = 'Yara'
var sabeNome = true
var saudacao = 'Oi, tudo bem?'

if (sabeNome) {
    var saudacao = `Oi ${nome}, tudo bem?`
}

console.log(saudacao) // retorna 'Oi Yara, tudo bem?'
```
Imagine que você está trabalhando em um código que já está ocupando 400 linhas e não percebeu que já havia declarado a variável `saudacao`, isso passa a ser um problema, já que você não percebeu que ela já havia sido definida antes, talvez até já tenha um valor atribuído.

## let
Após o lançamento do ES6 (EcmaScript 6), duas novas formas de declarar variáveis foram estabelecidas e uma delas é o `let`. Acabou se tornando extremamente recomendável seu uso, já que resolve alguns problemas antes existentes com a palavra-chave `var`. Um desses problemas é o de escopo. Com o `let` o escopo está limitado ao bloco, isso significa que se for definido dentro de uma função, por exemplo, estará disponível dentro daquele bloco. Vamos ver:

```javascript
let instituicao = 'Resilia'
function linguagemELogs() {
    let linguagem = 'JavaScript'

    console.log('1. ', instituicao)
    console.log('2. ', linguagem)
}

linguagemELogs()

console.log('3. ', instituicao)
console.log('4. ', linguagem)

/* no console iremos ter impresso:
1. Resilia
2. JavaScript
3. Resilia
linguagem is not defined
*/
```
O quarto *log* diz que `linguagem` não está definido, pois naquele escopo a variável sequer existe, fica limitada ao escopo da função `linguagemELogs`.

## const
Ainda que a declaração feita com `let` já resolva muita coisa, ainda quando ela é inicializada lhe é atribuído o valor `undefined`, e como podemos uma variável com um valor padrão? A palavra-chave `const` veio para solucionar isso.
Com esta variável podemos ter constantes no Javascript, o que não permite a alteração posterior do valor que foi inicializado.
```javascript
const nome = 'Allan'
console.log(nome) // retorna 'Allan'
nome = 'Carlos' // erro: Assignment to constant variable.
```
O erro na terceira linha evidencia o que foi explicado, não é possível atribuir novos valores à variável.

```javascript
const idade = 19
const escolaridade // erro: Missing initializer in const declaration
```
O erro nesta segunda linha se explica pelo fato da constante não ter sido devidamente inicializada, ou seja, nenhum valor lhe foi atribuído.

Aqui vai um resumo da diferença entre essas declarações, disponível no site [constletvar.com][const-let-var-website], traduzido:
| Palavra reservada | var | let | const |
|-------------------|-----|-----|-------|
| Escopo global | SIM | não | não |
| Escopo de função | SIM | SIM | SIM |
| Escopo de bloco | não | SIM | SIM |
| Pode ser reatribuído | SIM | SIM | não |

## Onde posso aprender mais sobre?
- [[Artigo] **Armazenando as informações que você precisa — Variáveis**][variables-mdn]
- [[Artigo - inglês] **Case Styles: Camel, Pascal, Snake, and Kebab Case**][cases-betterprogramming]
- [[Artigo] **Entenda a diferença entre var, let e const no JavaScript**][var-let-const-diferenca-alura]
- [[Artigo] **Qual a diferença entre var, let e const no JavaScript?**][var-let-const-diferenca-linkedin-gabriel]
- [[vídeo] **Var, Let, Const - Tudo o que você precisa saber**][var-let-const-diferenca-programador-br-yt]
- [[vídeo] **Como funciona o var, let e const?**][var-let-const-diferenca-marco-bruno-yt]