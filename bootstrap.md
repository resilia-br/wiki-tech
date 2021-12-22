<!-- VARIAVEIS -->
[navbar-bootstrap]: https://getbootstrap.com.br/docs/4.1/components/navbar/
[cards-bootstrap]: https://getbootstrap.com.br/docs/4.1/components/card/
[formularios-bootstrap]: https://getbootstrap.com.br/docs/4.1/components/forms/
[bordas-bootsrap]: https://getbootstrap.com.br/docs/4.1/utilities/borders/
[carousel-bootstrap]: https://getbootstrap.com.br/docs/4.1/components/carousel/
[documentacao-bootstrap]: https://getbootstrap.com.br/docs/4.1/getting-started/introduction/
[o-que-e-bootstrap-alura]: https://www.alura.com.br/artigos/bootstrap?gclid=Cj0KCQiAweaNBhDEARIsAJ5hwbek8InX7djTWiCKZAiXHYKhyoFdYCmT0K-EsNqCtsg99BRPna5V16waAkbpEALw_wcB
[o-que-e-bootstrap-hostinger]: https://www.hostinger.com.br/tutoriais/o-que-e-bootstrap
[o-que-e-bootstrap-hostinger-yt]: https://www.youtube.com/watch?v=jsTJL6Da5wc&ab_channel=HostingerBrasil
<!-- FIM DAS VARIAVEIS -->
<p align="center">
    <img src="./assets/images/resilia_logo.png" alt="Logo da Resilia" width="200px">
</p>

# O que é Bootstrap? 
Bootstrap é um framework gratuito para desenvolvimento front-end que fornece estruturas de **CSS, HTML e JavaScript**. Com o Bootstrap é possível criar sites e aplicações responsivas de forma rápida e simples, pois ele permite que a interface do usuário de um site seja otimizado para qualquer tamanho de tela, desde os dispositivos móveis até as telas maiores.

### Como iniciar um projeto usando Bootstrap?
1. A forma mais rápida é com o **BootstrapCDN**, primeiro você deve copiar e colar a seguinte tag `<link>` (com relação de folha de estilo) dentro da tag `<head>` do seu arquivo .html antes de todos os outros arquivos de estilo:

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
```
2. O segundo passo é colocar os seguintes `<script>` perto do final da sua página, logo antes do fechamento da tag `</body>`, nessa exata ordem:

```html
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
```

### Como funciona?
Para estilizar os componentes é necessário incluir classes específicas que podem ser vistas na documentação do Bootstrap, essas classes já possuem seus atributos e estilos prontos, mas podem ser customizáveis usando um CSS próprio.
- Exemplo 1 - Para criar um `flex container` você precisa adicionar a classe `d-flex` ao seu componente, dessa forma:

```html
  <div class="d-flex">Eu sou um flex container!</div>
```
- Exemplo 2 - Para centralizar um texto você deve usar a classe `text-center`, dessa forma:

```html
<p class="text-center">Este texto estará centralizado.</p>
```

### O que mais é possível fazer? 
O Bootstrap possui diversos componentes que podem ser utilizados em suas aplicações, com destaque para:
- [**Navbar**][navbar-bootstrap]
- [**Cards**][cards-bootstrap]
- [**Formulários**][formularios-bootstrap]
- [**Bordas**][bordas-bootsrap]
- [**Caroulsel**][carousel-bootstrap]

## Onde posso aprender mais sobre?
- [[Documentação] **Bootstrap em português**][documentacao-bootstrap]
- [[Artigo] **Bootstrap - O que é, como e quando usar?**][o-que-e-bootstrap-alura]
- [[Artigo] **O Que é Bootstrap? Guia para Iniciantes**][o-que-e-bootstrap-hostinger]
- [[Vídeo] **Bootstrap (Guia para Iniciantes)** ][o-que-e-bootstrap-hostinger-yt]

