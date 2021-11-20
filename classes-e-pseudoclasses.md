<!-- VARIAVEIS -->
[seletores-classe-mdn]: https://developer.mozilla.org/pt-BR/docs/Web/CSS/Class_selectors
[pseudo-classes-mdn]: https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-classes
[what-is-class-css]: https://blog.hubspot.com/website/what-is-css-class 
[guide-css-pseudo-class]: https://www.smashingmagazine.com/2016/05/an-ultimate-guide-to-css-pseudo-classes-and-pseudo-elements/
[pseudo-clasees-css-guanabara-yt]: https://www.youtube.com/watch?v=WPtRX4n0UJs 
[classes-em-css-yt]: https://www.youtube.com/watch?v=YgEp4Qt1NqE&ab_channel=MarneiCardoso
<!-- FIM DAS VARIAVEIS -->

<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que são classes no CSS?
As classes são seletores CSS, ou seja, corresponde ao(s) elemento(s) com base no conteúdo de seu atributo `class` no HTML. Para declararmos esse seletor devemos usar um ponto (.) seguido do conteúdo da classe.

#### Sintaxe
```css
.seletor {
    propriedade: valor;
}
```

Vamos ao seguinte exemplo dado este código HTML:
```html
<div class="vermelho">Primeiro elemento</div>
<!-- Para colocar mais de uma classe no HTML é necessário separá-las com espaço -->
<div class="vermelho borda-azul">Primeiro elemento</div>
```

Para estilizá-lo no CSS poderíamos selecionar as divs da seguinte maneira:
```css
/* Qualquer elemento que o conteúdo de class possua "vermelho" */
.vermelho {
    background-color: red;
}

/* Qualquer elemento <div> que o conteúdo de class possua "vermelho" */
div.vermelho {
    background-color: red;
}

/* Qualquer elemento <div> que o conteúdo de class possua "vermelho" e "borda" */
div.vermelho.borda {
    background-color: red;
    border: 1px dotted white;
}
```

# O que são pseudo-classes no CSS?

Uma pseudo-classe é uma palavra-chave (também conhecida como *palavra reservada*) que é adicionada a seletores para especificar um estado especial do(s) elemento(s) selecionado(s). Para declararmos uma pseudo-classe usamos os dois pontos (:) seguido da pseudo-classe em questão.

A pseudo-classe pode ser um evento atrelado à árvore do DOM, como a `:hover` que é aplicada quando o mouse passa sobre o elemento selecionado, mas também pode ser em relação a fatores externos, como o histórico de navegação (`:visited`) ou um campo de formulário é obrigatório (`:required`) e muito mais.

#### Sintaxe
```css
seletor:pseudo-classe {
    propriedade: valor;
}
```

## Onde posso aprender mais sobre?
- [[Artigo] **Seletores de classe**][seletores-classe-mdn]
- [[Vídeo] **Classes em CSS | O que são e como utilizar**][classes-em-css-yt]
- [[Artigo - Inglês] **The Beginner's Guide to CSS Classes**][what-is-class-css]
- [[Artigo] **Pseudo-classes**][pseudo-classes-mdn]
- [[Vídeo] **Pseudo-classes em CSS**][pseudo-clasees-css-guanabara-yt]
- [[Artigo - Inglês] **An Ultimate Guide To CSS Pseudo Classes And Pseudo Elements**][guide-css-pseudo-class]