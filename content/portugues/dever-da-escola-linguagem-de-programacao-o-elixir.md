---
title: "Dever da Escola - Linguagem programacao: O Elixir"
date: 2024-11-05T20:52:01-03:00
draft: false
---

# Origem 

Elixir e uma linguagem de programacao criado por Jose Valim, um paulista que atualmente mora na Europa. A linguagem foi criado em 2011, pois a sua criacao foi motivado e inspirado por Ruby, uma outra linguagem programacao japones. A idea do seu criado era melhorar o desempenho do Ruby, mas encontrou algumas dificuldades. Porem, ele conseguiu achar uma linguagem que poderia substituir o Ruby e Ruby on Rails para o desenvolvimento de backend, que e o Erlang. A problema e, o Erlang nao tive alguns característicos que o Jose precisava, ele resolveu cria uma linguagem nova, o qual tem um sintaxe parecido com Ruby, mas com a mesma maquina virtual do Erlang(BEAM).

# Caracteristicas

## Introducao

Elixir e uma linguagem de programacao, que e considerado dinamico, strong typing e funcional. 

## Funcional

Funcional e uma paradigma mais antigo do que a paradigma OOP(ou POO, que significa programacao orientado ao objeto). Os seus principais beneficios sao a consistência do dado e transferencia referencial. Ele e baseado em dois conceitos essencial: funcao pura e estrutura de dado imutável.

### Funcao pura

 Funcao pura nada mais e uma funcao matematica, mas na programacao. Portanto, ele nao ha nenhum side effect, que e qualquer efeito que nao e somente calculacao. Por examplo, ligar a lâmpada, conectar ao servidor, etc. 

### Estrutura de dado imutavel

Estrutura de dado imutavel, como o nome diz, e um tipo de estrutura de dado, mas imutavel. Essa cacteristica trouxe uma grande consistência na programacao, pois os dados nunca mudam, eles somente se produzem em um dado novo baseado nele. Assim, os dados nao mudam sincronizado, mas requere o programador mudar com a sua intenção.

### Exemplos

#### If/Else

Porem, o elixir nao forca voce usa esses conceitos supracitados, pois ele te dar um ambiente confortável e conviniente para a sua necessidade de programação funcional. Na linguagem, qualquer bloco de codigo e uma expressão. Por examplo, if/else da linguagem retorna valor: 
```elixir
if age < 18 do
    "menor de  idade"
else
    "maior de idade"
end
```

Nessa expressao se age e maior do que 18, retornaria `"menor de idade"`. Com isso, podemos escrever codigo como assim. 

```elixir

mensagem = if age < 18 do
    "menor de  idade"
else
    "maior de idade"
end

IO.puts(mensagem)
```

Dessa forma, o programador pensa mais no dado, em vez do comando, o qual e uma outra forma de pensar que eu acho que e melhor do que pensar mais em comando nas maiorias das situacoes.

#### Recursao

Recursao e um dos conceitos fundamental da matematica, tambem em programacao funcional. Assim, o elixir fornece bastante ferramentas para a sua experiencia de programacao funcional. Em outras linguagens, o uso de recursao poderia causar _stack overflow_, que e uma problema onde o stack foi preenchido com dados inecessarios ate um momento que ele nao conseguiu mais arguentar. Nesse caso, o Elixir fez uma optimizacao contra essa problema. Dessa forma, nas maiorias situacoes, o uso de recursao e aceitavel na linguagem, pois nao recomendo usar devido aos alternativas mais claras de interpretar mesma logica. Dado isso, podemos implementar o classico funcao recursiva, o famoso fibonacci com recursao:

```Elixir
defmodule Fib do
  def fib(0), do: 0
  def fib(1), do: 1
  def fib(x), do: fib(x - 1) + fib(x - 2)
end
```

> No Elixir, para escrever uma funcao e necessario definir o modulo

Esse codigo e equivalente a:

```python
def fib(x):
    if x == 0:
        return 0
    elif x == 1:
        return 1
    else:
        return fib(x - 1) + fib(x - 2)
```
