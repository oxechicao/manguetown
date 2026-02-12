+++
title = "COOKBOOK: Aprendendo com testes"
sort_by = "date"
page_template = "post.html"
+++

Objetivo deste documento é aprender RUST através de testes: unitários, integração etc.

Por mais que testes automatizados seja um tópico relativamente avançado, adquirir uma cultura de testes é essencial para qualquer pessoa desenvolvedora.  
Então, porque não começar com os testes? ~~Porque é coisa de doido~~

Uma vez ouvi um colega dizer para mim:

> "Eu dificilmente subo minha aplicação. Geralmente é a ultima etapa, só para ter certeza. Eu sempre utilizo os testes unitários para executar meu código"

Isso mudou mais uma vez meu estilo de programação. Apesar de muitos considerar que testes atrasam uma entrega. Eu digo que testes postergam problemas. O prazo de entrega pode aumentar algund dias, enquanto um prazo de debug tendem a demorar semanas.

Utilizar TDD (Test Driven Development, Desenvolvimento Orientado a Teste) exige prática, e no começo vai parecer ser bem sem sentido, mas continue firme na prática, isso mudará seu jeito de pensar em como entregar o mínimo.  
Resumidamente, no TDD primeiro você escreve o teste, para aquilo que não existe, isso deve falhar, do contrário, ou o teste está errado, ou a implementação já existe e você não sabia :D.  
A implementação segue um ciclo: Escreve o teste, Faz o teste passar, Refatore o código.

## {% mmd() %}

## title: Ciclo TDD

stateDiagram-v2
state "Escreva o Teste" as a
state "Escreva o código que passe no teste" as b
state "Refatore o código" as c
[*] --> a: Início da iteração
a --> b: falhou
b --> c: passou
c --> a: próxima iteração
{% end %}

Os exemplos abaixo foram surgindo de acordo com a minha necessidade e meu aprendizado. Não estão necessariamente em alguma ordem.

> **NOTA:**
> Nem tudo deve ser testado, nem todos os testes abaixo devem ser realmente implementados.
> O objetivo deste documento é o aprendizado,
