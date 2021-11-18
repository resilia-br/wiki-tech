<!-- VARIAVEIS -->
[conceitos-basicos-mdn]: https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox
[flex-froggy-jogo]: https://flexboxfroggy.com/
[flexbox-guia-completo]: https://origamid.com/projetos/flexbox-guia-completo/
[flexbox-w3schools]: https://www.w3schools.com/css/css3_flexbox.asp
[flexbox-na-pratica]: https://www.youtube.com/watch?v=HN1UjzRSdBk&ab_channel=Rocketseat
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que é flexbox?
Geralmente chamado de *flexbox*, o **Flexible Box Module** é um módulo do CSS que define um layout multi-coluna, o que permite definir como o conteúdo irá fluir entre as colunas, e como os vãos e regras são tratadas.

O flexbox busca lidar com o layout de maneira unidimensional, ou seja, uma dimensão de cada vez (linha e coluna).

### Flexbox e seus eixos
Quando se trata de flexbox, devemos ter em mente que todas as operações serão feitas baseadas em dois eixos: o eixo principal (*main axis*) e eixo transversal(*cross axis*). O eixo principal é definido pela propriedade `flex-direction` e tem seu valor inicial definido como `row` ("linha", em português) e o eixo transversal é diretamente perpendicular* a ele, é como se o eixo principal fosse o X do plano cartesiano (horizontal) e o eixo transversal fosse o eixo Y no plano cartesiano.

#### Eixo Principal (*main axis*)
Como já foi dito anteriormente, é definido pela propriedade `flex-direction`, que é responsável por determinar a direção do eixo e tem quatro valores possíveis, são eles:
- row (linha)
  - direção (inline) definida da esquerda para a direita, horizontalmente
- row-reverse (linha reversa)
  - direção (inline) definida da direita para a esquerda, horizontalmente
- column
  - direção (block) definida de cima para baixo, verticalmente
- column-reverse
  - direção (block) definida de cima para baixo, verticalmente

#### Eixo Transversal (*cross axis*)
O eixo transversal é perpendicular (faz ângulo de noventa graus) com o eixo principal, logo, se o eixo principal estiver na horizontal (*row* ou *row-reverse*), o eixo transversal estará na direção das colunas e se estiver na vertical(), o eixo transversal estará na direção das linhas.

### Contêiner Flex (*flex container*)
A área de um elemento que faz uso do *flexbox* é chamada de **contêiner flex**. Para iniciar essa estrutura definimos o valor da propriedade **display** como sendo `flex` ou `inline-flex` e, imediatamente, os filhos do contêiner se tornarão do tipo flex.

```css
/* exemplo de declaracao de conteiner flex */
.exemplo {
    display: flex;
}
```

Quer saber mais? Desfrute de nossa seleção de materiais :)

## Onde posso aprender mais sobre?
- [[Artigo] **Conceitos básicos de flexbox**][conceitos-basicos-mdn]
- [[Artigo] **Guia completo de Flexbox**][flexbox-guia-completo]
- [[Artigo] **CSS Flexbox**][flexbox-w3schools]
- [[Jogo] **Flexbox Froggy**][flex-froggy-jogo]
- [[Vídeo] **Desvendando o CSS Grid na prática**][flexbox-na-pratica]