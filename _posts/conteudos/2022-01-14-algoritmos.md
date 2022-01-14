---
layout: post
title:  "Algoritmos"
description: "Vamos falar sobre algo que você, profissional da tecnologia, vai
utilizar e criar bastante em toda a sua carreira: Algoritmos!"
categories: conteudos
tags: algoritmos
---

Salve, salve!

Vamos falar sobre algo que você vai utilizar e criar bastante em toda a sua
carreira: Algoritmos!

**Conteúdo:**

- [O que é?](#o-que-é)
- [Exemplo em pseudocódigo](#exemplo-em-pseudocódigo)
- [Exemplo em Ruby](#exemplo-em-ruby)
- [Meu primeiro algoritmo](#meu-primeiro-algoritmo)
- [Conclusão](#conclusão)

# O que é?

> _"Em matemática e ciência da computação, um
algoritmo é uma sequência finita de ações executáveis que visam obter uma
solução para um determinado tipo de problema"._

A [definição de algoritmo citada acima é encontrada na Wikipédia](https://pt.wikipedia.org/wiki/Algoritmo){:target="_blank"}.
Lá você vai encontrar muito conteúdo interessante sobre algoritmo e várias
referências bibliográficas, caso queira se aprofundar no assunto.

Mas a ideia aqui é introduzir o assunto de uma maneira simplificada, e para
isso, utilizaremos a clássica comparação entre algoritmos e receitas
culinárias.

Na citação inicial, vamos alterar a palavra "algoritmo" por "receita" e
"problema" por "comida", sendo assim, temos:

- _"Receita é uma sequência finita de ações executáveis que visam obter uma
  solução para um determinado tipo de comida"_

Ou seja, vamos dizer que o nosso problema/comida hoje é cozinhar macarrão
instantâneo.  E para isso, executaremos uma sequência de passos, nosso
algoritmo/receita, para conquistar o nosso objetivo.

# Exemplo em pseudocódigo

[Pseudocódigo](https://pt.wikipedia.org/wiki/Pseudoc%C3%B3digo){:target="_blank"}
é uma forma simplificada de representarmos o nosso algoritmo, sem preocupações
com os detalhes da linguagem de programação na qual o algoritmo será
implementado.

A ideia aqui é criar o passo a passo (_"sequência finita de ações
executáveis"_) para resolver o nosso problema; cozinhar macarrão instantâneo.
Segue abaixo o nosso algoritmo:

```
Adicionar água na panela
Colocar a panela no fogão
Acender o fogo
Aguardar a água ferver
Adicionar o macarrão instantâneo
Aguardar 3 minutos
Apagar o fogo
Adicionar o tempero
Misturar macarrão e o tempero
```

Nosso algoritmo está pronto! Executando linha por linha na sequência em que
foram escritas, teremos o nosso macarrão instantâneo pronto para ser servido ao
fim do processo.

Implementamos um algoritmo que nós, como pessoas, podemos entender e executar.
Mas e agora? Como faremos para que o nosso computador, uma máquina, entenda o
nosso algoritmo?

**Observação**: _Apesar de termos pseudocódigos que podem ser executados no
computador, como o
[Portugol](https://pt.wikipedia.org/wiki/Portugol){:target="_blank"},
seguiremos descrevendo os algoritmos em Português a fim de simplificar._

# Exemplo em Ruby

[Linguagem de programação!](https://pt.wikipedia.org/wiki/Linguagem_de_programa%C3%A7%C3%A3o){:target="_blank"}
É o que precisamos para converter o nosso pseudocódigo em algo que o nosso
computador possa entender e executar. Temos várias disponíveis, mas a que
utilizaremos aqui e em vários outros posts se chama
[Ruby](https://www.ruby-lang.org/pt/about/){:target="_blank"}.

Essa linguagem foi escolhida por ser amigável e divertida de se trabalhar,
principalmente para quem está aprendendo. Além disso, o mercado está com
bastante oportunidade em Ruby e a
[comunidade](https://community.ruby.com.br){:target="_blank"} é sensacional.

Bom, mas voltando ao nosso problema (cozinhar macarrão instantâneo), vamos
fingir que temos um robô em nossa casa e que a nossa interface de comunicação
com o mesmo se dá através do Ruby. Ou seja, o robô é capaz de fazer muitas
coisas, mas nós precisamos dizer o que fazer, passo a passo, programando em Ruby.

Assim, abstraindo os detalhes das classes, objetos e a implementação dos
métodos, temos o nosso pseudocódigo convertido em um passo a passo implementado
em Ruby, e o mais importante, capaz de ser processado por nosso robô fictício.

```ruby
panela.adicionar(agua)                    # Adicionar água na panela
boca_fogao = fogao.adicionar(panela)      # Colocar a panela no fogão
boca_fogao.acender_fogo                   # Acender o fogo
sleep(60) while(panela.nao_ferveu_ainda?) # Aguardar a água ferver
panela.adicionar(macarrao)                # Adicionar o macarrão instantâneo
sleep(3*60)                               # Aguardar 3 minutos
boca_fogao.apagar_fogo                    # Apagar o fogo
panela.adicionar(tempero)                 # Adicionar o tempero
panela.misturar                           # Misturar macarrão e o tempero
```

Não se preocupe se, de início, esse código pareceu confuso ou complexo. O
objetivo principal desse exemplo é mostrar como o nosso pseudocódigo, entendido
por nós, se tornou uma implementação entendida pela máquina. Nos próximos posts
falaremos sobre variáveis, funções, classes, objetos e muito mais. Então relaxa
que sua jornada aqui está só começando.

Porém, vale citar que foram utilizadas duas instruções do Ruby; `sleep` e `while`.

**Traduções:** _sleep_: dormir - _while_: enquanto

A função _[sleep](https://apidock.com/ruby/Kernel/sleep){:target="_blank"}_
recebe um número representando o tempo em segundos que a aplicação deve dormir
ou aguardar.  Exemplo: `sleep(2)` para dormir 2 segundos ou `sleep(1.5)` para
dormir 1 segundo e meio.

Já o `while`, é um controle de fluxo que nos permite executar uma instrução
**enquanto** uma condição for verdadeira.

Dito isso, você saberia dizer o que o robô deve fazer ao executar a instrução
abaixo?

```ruby
sleep(60) while(panela.nao_ferveu_ainda?)
```

Você acertou se pensou em algo parecido com: "Durma por 60 segundos enquanto a
panela não estiver fervendo ainda".

Ou seja, o robô vai executar a condição verificada pelo _while_
(`panela.nao_ferveu_ainda?`) e se a condição for verdadeira, o robô vai esperar
60 segundos para conferir a condição novamente.

O robô entrará em um ciclo, chamado de _loop_ em inglês, que só terminará
quando a panela estiver fervendo. Só aí que o robô executará a próxima
instrução; `panela.adicionar(macarrao)`.

É importante mencionar que não sabemos em quantos minutos a água começará a
ferver, porque depende de vários fatores como o tamanho da boca do fogão, a
quantidade de água colocada, a temperatura inicial da água, etc. Por isso que
foi interessante termos utilizado o `while` ao invés de deixarmos um tempo
fixo. A nossa solução atende tanto o cenário em que a água ferverá em 5 minutos
quanto os cenários de 8 minutos, 10 minutos, etc.

Se você reparou bem, utilizamos a função `sleep` mais de uma vez, onde na
segunda vez ela serviu para outro propósito; aguardar 3 minutos antes de apagar
o fogo.

```ruby
sleep(3*60) # 3 x 60 = 180 segundos = 3 minutos
```

# Meu primeiro algoritmo

Agora chegou a sua hora! Caso nunca tenha programado antes, hoje você resolverá
o seu primeiro problema usando algoritmos. E nada de robô fictício e outras
abstrações, mas sim um código ruby que você irá executar e conferir os
resultados.

Antes de começarmos, gostaria que você abrisse o site
[runrb.io](https://runrb.io){:target="_blank"}, é nele que executaremos o nosso
algoritmo em Ruby. Abrindo a página, teremos um pequeno código já implementado,
o famoso "Olá Mundo!". Clicando no botão central, você irá executar o código já
implementado e poderá conferir o resultado na tela preta, conforme imagem
abaixo. É assim que implementaremos e testaremos o nosso primeiro algoritmo.

![Print do site runrb.io destacando onde se escreve código, com uma seta
apontando para o botão central que executa o código escrito, com mais uma seta
apontando para a tela preta que exibe os
resultados](/imagens/2022-01-14-algoritmos/1_runrb.png)

Já temos o nosso ambiente funcionando! Então vamos ao problema que será resolvido.

**O problema**

João, seu amigo e professor, sabendo dos seus conhecimentos computacionais, te
enviou a seguinte mensagem com um pedido de ajuda.

> Minha impressora não está funcionando, parou do nada!

Brincadeira! Esse não é o problema que resolveremos hoje, ou amanhã, mas é um
pedido de ajuda real que você pode receber a qualquer momento. Enfim, vamos à
real mensagem do João:

> Preciso de ajuda para calcular a média dos alunos. Fazer tudo na calculadora
> para saber se eles foram aprovados está me dando muito trabalho e às vezes
> cometo algum pequeno erro que a média fica errada. Esses dias quase reprovei
> meu melhor aluno! rs Consegue me ajudar com algo? Ah, para passar na minha
> matéria é preciso ter a média maior ou igual à 7.0.

Olha que legal, já temos um problema real a ser resolvido, porém, antes de
começarmos a nossa implementação em Ruby, precisamos ter certeza de que
entendemos o problema.

**Entendendo o problema**

É muito importante entender todo o problema para que possamos atender às
expectativas do professor. Às vezes nos depararemos com problemas muito
grandes, tão grandes que poderão ser divididos em vários pequenos problemas,
nesses casos você até poderá iniciar a programação antes mesmo de entender tudo,
mas esse não é o caso do nosso problema atual.

O ponto principal do nosso problema é o cálculo da média. Sem entender esse
conceito será muito difícil entregarmos uma solução que atenda. Pode ser que
esse conceito esteja fresco na sua memória, mas caso não esteja, você precisará
pesquisar para tirar todas as dúvidas. Será apresentado aqui uma explicação
simples, baseada em exemplos, mas você pode encontrar na [Wikipédia conteúdos e
referências bem
detalhadas](https://pt.wikipedia.org/wiki/M%C3%A9dia){:target="_blank"}, caso
queira se aprofundar.

Se você acessou o link acima para ler mais sobre média, deve ter percebido que
existem vários tipos de média; aritmética, geométrica, harmônica, etc. Ou seja,
precisamos levantar mais requisitos e confirmar com o João qual seria a média
utilizada por ele. Depois de um contato com o João recebemos prontamente a
seguinte mensagem:

> Ahh, que bom que você vai poder me ajudar! Eu faço a média aritmética para
> calcular a nota final dos meus alunos.

Legal! A média aritmética é super simples de ser calculada, só precisamos somar
todos os valores informados e dividirmos pela quantidade de valores.

Exemplo: Quatro idosos com as idades 68, 70, 71 e 75 estão jogando dominó.
Qual é a média aritmética das idades nessa partida?

Precisamos somar todas as idades (`68 + 70 + 71 + 75 = 284`) e depois
dividirmos o resultado pela quantidade de valores (`4 idades`), resultando em
`284 / 4 = 71`. Portanto a média aritmética das idades é igual à `71`.

Entendendo bem como calcular uma média aritmética de uma lista de números,
podemos avançar para o próximo passo da criação do seu primeiro algoritmo;
rascunhar a solução.

**Rascunhando a solução**

Bom, para informarmos ao João se um aluno foi aprovado ou não, precisaremos
definir o passo a passo para resolver o problema. Sabemos que vamos precisar
ler todas as notas do aluno e também a quantidade de notas para calcular a
média do aluno. Iniciando nosso pseudo código, teremos:

```
Ler as notas
Ler a quantidade de notas
Somar as notas
Calcular a média aritmética
```

Sabendo a média aritmética, compararemos o valor com `7.0`, se for maior ou
igual, então o aluno foi aprovado, caso contrário, foi reprovado.

```
Média aritmética é maior ou igual à 7.0?
  Passou!
Senão
  Não passou.
```

Assim, temos nosso primeiro algoritmo completo em pseudo código:


```
Ler as notas
Ler a quantidade de notas
Somar as notas
Calcular a média aritmética
Média aritmética é maior ou igual à 7.0?
  Passou!
Senão
  Não passou!
```

**Implementação em Ruby**

Agora chegou a hora de implementarmos o nosso primeiro algoritmo em Ruby! Para
isso, precisaremos converter, **linha a linha**, o nosso pseudo código em Ruby. Ah,
lembre-se de deixar o [runrb.io](https://runrb.io){:target="_blank"} aberto aí
para executarmos o nosso código.

_Linha #1_

`Ler as notas`

Nessa primeira linha, nós precisaremos ler as notas e isso pode ser feito de
várias maneiras diferentes, então vamos optar pela forma mais simples:

`notas = [7.0, 8.0, 9.0]`

Criamos uma variável chamada `notas`, onde uma variável é algo que nos permite
guardar valores. Nesse caso, o valor dessa variável será à uma lista de notas
preenchidas pelo João, que nesse caso tem os valores `7.0`, `8.0` e `9.0`.

Essa nossa primeira linha já pode ser executada e testada no
[runrb.io](https://runrb.io){:target="_blank"}! O único detalhe é que nada será
impresso no terminal (parte preta do site) quando você executar essa linha.
Para verificar se está tudo certo, você pode imprimir o valor da variável
`notas` utilizando o método `puts` do Ruby, conforme exemplo abaixo:

```ruby
notas = [7.0, 8.0, 9.0]
puts notas
```

_Linha #2_

`Ler a quantidade de notas`

Nessa segunda linha precisamos ler a quantidade de notas e a maneira mais fácil
é pedir para o João informar essa quantidade em uma variável.

`quantidade_notas = 3`

Lembrando que uma variável é algo que nos permite guardar valores. Só que ao
invés de uma lista de números, guardamos apenas um número inteiro.

_Linha #3_

`Somar as notas`

Agora precisamos somar as notas que estão em nossa variável `notas`. O valor
que está guardado nessa variável foi chamado de "Lista de números", mas na
verdade, o nome dessa estrutura é conhecida como `Array`. E esse tipo de
estrutura fornece recursos interessantes para a gente, como o método `sum`,
capaz de somar todos os valores da nossa lista de notas. Portanto, a linha 3 do
nosso algoritmo será:

`soma_notas = notas.sum`

Assim como fizemos com a linha 1, você pode conferir os resultados de cada
linha com o método `puts`, conforme o exemplo abaixo:

```ruby
notas = [7.0, 8.0, 9.0]
puts notas.sum
```

O resultado da execução de `notas.sum` foi guardado na variável `soma_notas`.

_Linha #4_

`Calcular a média aritmética`

Chegamos no coração do nosso primeiro algoritmo; o cálculo da média aritmética!
Para isso, precisaremos dividir a soma das notas (`soma_notas`) pela quantidade
de notas (`quantidade_notas`), utilizando-se o operador aritmético `/`.

`media = soma_notas / quantidade_notas`

Assim, temos o resultado da divisão guardado na variável `media`.

Até o momento, o nosso primeiro algoritmo está desse jeito:

```ruby
notas = [7.0, 8.0, 9.0]               # Linha 1 - ler as notas
quantidade_notas = 3                  # Linha 2 - ler a quantidade de notas
soma_notas = notas.sum                # Linha 3 - somar as notas
media = soma_notas / quantidade_notas # Linha 4 - calcular a média aritmética
```

_Linha #5_

`Média aritmética é maior ou igual à 7.0?`

Agora precisaremos conferir se a média que acabamos de calcular é maior ou
igual à 7.0. Para responder a essa pergunta, precisaremos dos operadores
relacionais para compararmos os dois números (a `media` calculada com o valor
`7.0`).  Vamos à alguns exemplos para apresentar alguns operadores relacionais,
associando perguntas à implementação em Ruby:

O valor de x é igual a 12? `x == 12`

O valor de x é menor ou igual a 12? `x <= 12`

O valor de x é diferente de 10? `x != 10`

O valor de x é maior que 10? `x > 10`

Com base nos exemplos acima você já deve imaginar, a linha 5 do nosso algoritmo
terá a seguinte instrução:

`media >= 7.0`

O resultado dessa operação será verdadeiro (`true`) ou falso (`false`). Ou
seja, se a média for maior ou igual à `7.0`, o valor `true` será retornado,
caso contrário,  será retornado `false`.

_Linha #6_

`Passou!`

Essa parte é bem interessante, porque essa linha pode ser apenas uma impressão
na tela informando ao João que as notas foram suficientes para a aprovação,
algo como:

```ruby
puts 'Passou!'
```

Porém, nós só queremos imprimir isso na tela se a condição da linha anterior
for verdadeira, isto é, se realmente tivemos uma aprovação.

Para isso, precisamos falar sobre estruturas condicionais, recursos
importantíssimos para que possamos controlar o fluxo de nossa aplicação, em
outras palavras, decidir qual caminho nosso algoritmo deve seguir com base em
operadores como os apresentados anteriormente.

Analisando novamente as linhas 5 e 6 do nosso pseudo código, temos:

```
Média aritmética é maior ou igual à 7.0?
  Passou!
```

Ou seja, **se** a média aritmética é maior ou igual à 7.0, então temos uma
aprovação.

A estrutura condicional que precisamos nesse caso se chama `if`, que significa
"se" em inglês. E é essa estrutura que precisaremos para corrigir a linha 5.
Como resultado final, temos:

```ruby
if media >= 7.0  # Linha 5 - Média aritmética for maior ou igual a 7.0?
  puts 'Passou!' # Linha 5 - Passou!
end
```

Apenas adicionamos o `if` na linha 5. O resultado da operação `media >= 7.0`,
que será `true` ou `false`, será avaliado pelo `if`.

Desse modo, o valor "Passou!" só será impresso na dela quando o resultado da
operação for `true`.

Até o momento, o nosso primeiro algoritmo está desse jeito:

```ruby
notas = [7.0, 8.0, 9.0]               # Linha 1 - ler as notas
quantidade_notas = 3                  # Linha 2 - ler a quantidade de notas
soma_notas = notas.sum                # Linha 3 - somar as notas
media = soma_notas / quantidade_notas # Linha 4 - calcular a média aritmética

if media >= 7.0                       # Linha 5 - Média aritmética for maior ou igual a 7.0?
  puts 'Passou!'                      # Linha 6 - Passou!
end
```

_Linha #7_

`Senão`

Nessa linha utilizaremos outra estrutura condicional muito utilizada, o `else`,
que significa "senão" em inglês.

Se a média for maior ou igual a `7.0`, nós vimos que será impresso "Passou!" na
tela, caso contrário, o que acontece? Na nossa implementação atual, nada!
Porque precisamos utilizar o `else` para seguir um outro caminho nosso
algoritmo, um caminho que só será executado quando a operação `media >= 7.0`
não for verdadeira, isto é, resultar em `false`.

Portanto, nossa linha 7 ficaria algo como:

`else`

Parece meio confuso agora e talvez quebre os seus testes no
[runrb.io](https://runrb.io){:target="_blank"}, mas prometo que tudo fará
sentido na próxima linha!

_Linha #8_

`Não passou!`

Essa linha, assim como a linha 6, é apenas uma impressão na tela.

```ruby
puts 'Não passou!'
```

Porém, a gente não quer executar ela sempre, mas somente quando o resultado
operação `media >= 7.0` for `false`. E como vimos na linha anterior, é
justamente o fluxo definido pelo `else`.

Ou seja, se temos uma aprovação, tudo que está dentro do bloco do `if` será
executado, senão, todo o bloco do `else` será executado. Sendo assim, essa
parte de controle de fluxo com `if/else`, fica implementado da seguinte
maneira:

```ruby
if media >= 7.0                       # Linha 5 - Média aritmética for maior ou igual a 7.0?
  puts 'Passou!'                      # Linha 6 - Passou!
else                                  # Linha 7 - Senão
  puts 'Não passou!'                  # Linha 8 - Não passou!
end
```

Conforme prometido, agora tudo faz sentido! E finalmente terminamos o nosso
primeiro algoritmo em Ruby:

```ruby
notas = [7.0, 8.0, 9.0]               # Linha 1 - ler as notas
quantidade_notas = 3                  # Linha 2 - ler a quantidade de notas
soma_notas = notas.sum                # Linha 3 - somar as notas
media = soma_notas / quantidade_notas # Linha 4 - calcular a média aritmética

if media >= 7.0                       # Linha 5 - Média aritmética for maior ou igual a 7.0?
  puts 'Passou!'                      # Linha 6 - Passou!
else                                  # Linha 7 - Senão
  puts 'Não passou!'                  # Linha 8 - Não passou!
end
```

Agora você pode seguir brincando com o seu algoritmo no
[runrb.io](https://runrb.io){:target="_blank"}, adicionando diferentes notas e
conferindo se temos uma aprovação ou reprovação. Dando tudo certo, podemos
enviar o nosso algoritmo para o nosso amigo João!

# Conclusão

Hoje você aprendeu que um algoritmo é um passo a passo para resolver um
problema. Além disso, você aprendeu:

- É preciso entender bem o problema para criar uma solução assertiva;
- Rascunhar uma solução em pseudocódigo ajuda muito na implementação do
  algoritmo final;
- Não precisamos instalar nada em nosso computador para dar os primeiros passos
  na programação;
- Algumas instruções em Ruby: `sleep`, `while`, `if`, `else`, `sum`;
- E o principal, como resolver um problema real com programação.

É muito importante termos em mente também que, assim como temos várias receitas
diferentes de macarrão instantâneo, temos também várias e várias maneiras de se
resolver um mesmo problema. Ou ainda, podemos até entender um problema de
maneira diferente.

Por isso, é muito importante se questionar para garantir que entendeu o
problema a fundo e também questionar a pessoa que te passou o problema, para
garantir que todos os requisitos estão claros e serão atendidos.

E é isso! Esse post ficou maior do que o planejado mas espero que tenha
aprendido bastante e curtido a jornada até aqui. Aguarde os próximos posts pois
esse é apenas o primeiro de uma trilha de introdução à programação com Ruby.
Acompanhe os novos posts e discussões no
[Twitter](https://twitter.com/moaradev)!

Todo e qualquer feedback construtivo será muito bem recebido no
[GitHub](https://github.com/moaradev/moara.dev/issues) ou
[Twitter](https://twitter.com/moaradev).

Obrigado por ter chegado até aqui e até a próxima!
