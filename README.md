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
  --color-rp-base: #232136;
  --color-rp-base: #232136;
  --color-rp-surface: #2a273f;
  --color-rp-overlay: #393552;
  --color-rp-muted: #6e6a86;
  --color-rp-subtle: #908caa;
  --color-rp-text: #e0def4;
  --color-rp-love: #eb6f92;
  --color-rp-gold: #f6c177;
  --color-rp-rose: #ea9a97;
  --color-rp-pine: #3e8fb0;
  --color-rp-foam: #9ccfd8;
  --color-rp-iris: #c4a7e7;
  --color-rp-highlight-low: #2a283e;
  --color-rp-highlight-med: #44415a;
  --color-rp-highlight-high: #56526e;
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
  - title:
    - text: Manguetown
    - variant: `h1`
  - Menus:
    - Nav:
      - Home
      - Posts
      - Projects
      - Github: link to <https://github.com/oxechicao/manguetown>
- Nav
  - should receive a list of links
- Footer
  - Copyright (c) 2026 @oxechicao. All Rights Reserved.
  - Socials links:
    - Github: <https://github.com/oxechicao/manguetown>
- Cards
  - Title: `h2`
  - Description: `p`
  - Link: to the post
- Article
  - Title: `h2`
- Aside
  - A list with the: Table of content of the article

### Page templates

- Home:
  - Header
  - Main:
    - section
      - Banner in background
      - Short description of the project
      - style:
        - background: `color-surface`
        - hover, focus: `color-highlight-low`
        - border: `color-rose`
    - Cards: list of posts
  - Footer
- Blog post:
  - Header
  - Main:
    - Article
    - Aside
    - style:
      - 2 columns for desktop
      - 1 column for mobile
      - Aside should be shown before the article when media mobile
      - Table of content should be in line list instead of a list
  - Footer
