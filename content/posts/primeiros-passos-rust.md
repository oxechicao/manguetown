+++
title = "Primeiros passos: O Borrow Checker"
date = 2024-05-20
description = "Entendendo como o Rust gerencia memória sem Garbage Collector e minhas primeiras lutas com o compilador."
+++

Hoje comecei a estudar o conceito mais famoso (e temido) do Rust: o **Ownership**.

Vindo de linguagens como JavaScript, onde o _Garbage Collector_ faz tudo, ou C, onde `malloc` e `free` são manuais, o Rust propõe um meio-termo interessante.

## O que é Ownership?

O sistema de ownership é um conjunto de regras que o compilador verifica em tempo de compilação. Nenhuma dessas regras impõe overhead em tempo de execução.

### As 3 Regras

1. Cada valor em Rust tem um proprietário (owner).
2. Só pode haver um proprietário por vez.
3. Quando o proprietário sai de escopo, o valor é descartado.

## O problema da String

Tentei fazer isso e o compilador gritou comigo:

```rust
let s1 = String::from("olá");
let s2 = s1;

println!("{}, mundo!", s1); // Erro aqui!
```
