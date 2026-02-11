# Da Lama Ao Caos

> Este site foi criado com [Zola](https://getzola.org), um projeto para gerar site estático em rust.

O objetivo deste projeto é documentar da forma mais didática possível meu aprendizado em rust. Já iniciei esse aprendizado diversas vezes e sempre tive as mesmas dificuldade quando tento aprender na prática.

Do velho ditado: `ta achando ruim faz você`. Criei este site para fazer da minha maneira, explicar o que estou aprendendo com Rust. A ideia é sempre demonstrar os conceitos da linguagem implementando alguma coisa, útil ou não, sem esquecer da maior dor de todo dev, os testes.

Escrevendo exemplos de códigos, cookbooks, etc, através de TDD, procuro tomar nota do meu entendimento de como fazer as coisas em Rust.

Por conta disso, uma postagem hoje, pode ser atualizada com o tempo. Pode se tornar inútil, mas, para mim, o importante é que eu transcreva meu aprendizado, porque assim eu consigo aprender também.

## Sobre o nome

`Da lama ao Caos` é uma música do grandioso Chico Science e Nação Zumbi. Além da música e composição ser magnífica, a ideia é fazer um trocadilho com o mascote não oficial do rust, o carangueiro Ferris, e um dos lares dos carangueijos, o mangue.

![ferrir-crab](image.png)

## Sobre o site

Desenvolvido usando Zola, utiliza [Tera Templates](https://keats.github.io/tera/docs/#templates) como html-engine-builder.

As cores do projeto são as do [rose pine moon theme](https://rosepinetheme.com/palette/ingredients/)

```css
:root {
  --color-base: #232136;
  --color-base: #232136;
  --color-surface: #2a273f;
  --color-overlay: #393552;
  --color-muted: #6e6a86;
  --color-subtle: #908caa;
  --color-text: #e0def4;
  --color-love: #eb6f92;
  --color-gold: #f6c177;
  --color-rose: #ea9a97;
  --color-pine: #3e8fb0;
  --color-foam: #9ccfd8;
  --color-iris: #c4a7e7;
  --color-highlight-low: #2a283e;
  --color-highlight-med: #44415a;
  --color-highlight-high: #56526e;
}
```

## TODO

Criar templates usando Tera template engine.

### Styles

- General definitions:
  - background: `color-base`
  - text: `color-text`
  - fonts:
    - 100: `static/fonts/webfont/MartianGrotesk-WdTh.woff2`
    - 400: `static/fonts/webfont/MartianGrotesk-WdRg.woff2`
    - 700: `static/fonts/webfont/MartianGrotesk-WdBd.woff2`
    - 1000: `static/fonts/webfont/MartianGrotesk-WdUlt.woff2`
    - fallback: `sans-serif`
- link:
  - text: `color-foam`
  - hover, focus: color-foam underscore
- heading:
  - text: color-iris
  - hover, focus: underscore
- paragraph, list item:
  - focus, hover:
    - background color-hightlight-med
- header and footer:
  - background: color-surface
  - border: `color-pine`
  - focus,hover: color-hightlight-low
- cards:
  - background: color-surface
  - border: color-rose
  - hover, focus:
    - border: color-gold
    - background: color-highlight-low
- article:
  - background: color-surface
  - border: color-rose
  - hover, focus:
    - background: color-highlight-low
- aside:
  - background: color-surface
  - border: color-gold
  - hover, focus:
    - background: color-highlight-low

### Components

Os templates de páginas serão:

- Header
  - title: Manguetown
  - Menus:
    - Nav:
      - Home
      - Posts
      - Projects
      - Socials: deve ser um anchor para o footer
- Nav
  - Lista de links
- Footer
  - Copyright (c) 2026 @oxechicao. All Rights Reserved.
  - Socials links:
    - Github
    - LinkedIn
- Cards
  - Title
  - Description
  - Link
- Article
- Aside
  - Table of content of the article
