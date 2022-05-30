---
layout: post
title: "Guia definitivo de conversão de unidades"
categories: Física
tags: [pt-br, física geral]
math: true
toc: true
---

Nesses ultimos anos lecionando no ensino médio percebo muitos alunos que chegam ao colegial e não tem noções básicas de proporção. Ficam confuso quando é necessário converter unidades em física, ou perdidos em calculo esteiqueométrico. Não observei isso apenas no ensino médio. Alguns alunos de graduação e pós-graduação também apresentam tais dificuldades quando a conversão se trata de utilizar unidades adimensionais para facilitar as contas.

Enbasado nestes casos, resolvi escrever esse guia de conversão de unidades. Aqui temos a conversão de unidades da maneira mais formal até a mais intuitiva. Não pretendo apresentar algo ludico por puro preconceito. Uma vez que este texto é preparado para estudantes mais velhos e quase adultos.

Na sequencia vemos que, uma das propriedades da multiplicação é a base para que possamos converter unidades. Essa propriedade é aquela que diz que qualquer número multiplicado por $$ 1 $$ é igual à ele mesmo, ou seja,

$$ a \cdot 1 = a .$$

## O que a multiplicação por $$ 1 $$ tem a ver com a conversão de unidades?

A multiplicação pelo número $$ 1 $$ é utilizada em demasia quando calulamos a soma de fações, porem os alunos fazem tal operação sem se dar conta. Vejamos o exemplo mais simples que consigo dar sobre isso. Imaginemos que precisamos resolver a seguinte conta

$$ \frac{5}{6} + \frac{1}{2} + \frac{1}{3} = \text{?}. $$

O procedimento, para conseguir efetuar essa conta, é de conhecimento geral dos alunos. Primeiro calculamos o mínimo multiplo comum dos números que se encontram no denominador ($$ 2 $$, $$ 3 $$ e $$ 6 $$). Uma vez encontrado, que o minimo multiplo comum é 6, multiplicamos cada uma das frações em cima e em baixo por um mesmo número especifico. Cada fração tem seu número especial. Este número é aquele quando multiplicado pelo denominador resulte no minimo multiplo comum. Portanto, a primeira fração $$ 5 / 6 $$ é multiplicada pelo número $$ 1 $$, a segunda fração $$ 1 / 2 $$ é multiplicada pelo número $$ 3 $$, e a terceira fração $$ 1 / 3 $$ é multiplicada pelo número $$ 2 $$. Assim a sequencia de resolução é a seguinte:

$$ \begin{eqnarray}
\frac{5}{6}+\frac{1}{2}+\frac{1}{3} & = & \frac{5\cdot1}{6\cdot1}+\frac{1\cdot3}{2\cdot3}+\frac{1\cdot2}{3\cdot2} \\
& = & \frac{5}{6}+\frac{3}{6}+\frac{2}{6} \\
& = & \frac{5+3+2}{6} \\
& = & \frac{10}{6} \\
& = & \frac{10\div2}{6\div2} \\
& = & \frac{5}{3}.
\end{eqnarray} $$

Certo! Mas onde está essa tal multiplicação pelo número $$ 1 $$ que é tão importante? Ela é o ato de multiplicar em cima e em baixo pelo mesmo número. O que? Isso mesmo, multiplicar em cima e em baixo pelo mesmo número é multiplicar por $$ 1 $$. Deixe-me desenhar, assim é possivel visualizar melhor:

$$ 1 = \frac{1}{1} = \frac{2}{2} = \frac{3}{3} = \cdots = \frac{a}{a} .$$

O número $$ 1 $$ é qualquer fração cujo númerador seja igual ao denominador. Portanto, um procedimento intermediário está oculto nessa maneira de fazer. O procedimento é este

$$ \frac{1}{2} = \frac{1}{2} \cdot 1 = \frac{1}{2} \cdot \frac{3}{3} = \frac{1 \cdot 3}{2 \cdot 3} = \frac{3}{6} .$$

Agora que sabemos da utilidade que a multiplicação por $$ 1 $$ tem, podemos criar qualquer tipo de fração com número e unidades. Esse tipo de fração é chamada de fator de conversão, a qual é, no fim das contas, uma outra maneira de escrever o numero 1. 

## Como utilizar um fator de conversão?

Primeiro de tudo é preciso se atentar de que unidades de medidas seguem as regras da algebra, ou seja, podemos dividi-las, multiplica-las, soma-las e subtrai-las. A partir de uma relação entre unidades de medidas criamos dois fatores de conversão, um que leva da unidade A para a unidade B, e o outro que leva da unidade B para a unidade A.

Peguemos como exemplo a conversão relação entre as unidades de enegia caloria e Joules, em que $$ 1 \text{ cal} = 4.184 \text{ J} $$. Se dividirmos os dois lados dessa igualdade por $$ 4.184 \text{ J} $$ obtemos uma fração que tem valor $$ 1 $$, ou seja,

$$ \frac{1 \text{ cal}}{4.184 \text{ J}} = 1 .$$

Portanto, esta fração é o fator de conversão de Joules para calorias

$$ f_1 = \frac{1 \text{ cal}}{4.184 \text{ J}} ,$$

e sua inversa inversa é o fator de conversão de calorias para Joules

$$ f_2 = \frac{4.184 \text{ J}}{1 \text{ cal}} .$$

Para converter qualquer quantidade de Joules em calorias basta multiplica-la por $$ f_1 $$, por exemplo:

$$ \begin{eqnarray}
1000 \text{ J} & = & 1000 \text{ J} \cdot 1 \\
& = & 1000 \text{ J} \cdot f_1 \\
& = & 1000 \text{ J} \cdot \frac{1 \text{ cal}}{4.184 \text{ J}} \\
& = & 1000 \cancel{\text{ J}} \cdot \frac{1 \text{ cal}}{4.184 \cancel{\text{ J}}} \\
& = & \frac{1000}{4.184} \cdot 1 \text{ cal} \\
& = & 239 \cdot 1 \text{ cal} \\
& = & 239 \text{ cal}.
\end{eqnarray} $$

Para converter qualquer quantidade de calorias em Joules basta multiplica-la for $$ f_2 $$, por exemplo:

$$ \begin{eqnarray}
1000 \text{ cal} & = & 1000 \text{ cal} \cdot 1 \\
& = & 1000 \text{ cal} \cdot f_2 \\
& = & 1000 \text{ cal} \cdot \frac{4.184 \text{ J}}{1 \text{ cal}} \\
& = & 1000 \cancel{\text{ cal}} \cdot \frac{4.184 \text{ J}}{1 \cancel{\text{ cal}}} \\
& = & 1000 \cdot 4.184 \text{ J} \\
& = & 4184 \text{ J}.
\end{eqnarray} $$

Vamos formalizar isso!

Dadas duas quantidades distintas $$ x_A $$ e $$ y_B $$, cujas unidades $$ A $$ e $$ B $$ são de mesma natureza porem igualmente distintas. Um vez que a igualdade $$ x_A = y_B $$ é verdadeira, o fator de conversão $$ A \rightarrow B $$ é definido como

$$ f_{AB} = \frac{y_B}{x_A} , $$

enquanto o fator de conversão de conversão $$ B \rightarrow A $$ é definido como

$$ f_{BA} = \frac{x_A}{y_B} . $$

Portanto temos que suas aplicações são dadas, respectivamente, da seguinte maneira:

$$ \begin{eqnarray} 
[{\text{quantidade}}]_A \cdot f_{AB} = [{\text{quantidade}}]_B , \\
[{\text{quantidade}}]_B \cdot f_{BA} = [{\text{quantidade}}]_A .
\end{eqnarray} $$

## Posso converter unidades por substituição direta?

Certamente, também podemos converter unidades por substituição direta. Como seria isso? Vamos usar a conversão de velocidade entre $$ \text{km/h} $$ e $$ \text{m/s} $$, já que esta é uma das mais, senão a mais, usual operação de conversão de unidades encontrada nos exercicios de ensino médio.

Sabe-se que para converter entre tais unidades, dividimos a quantidade em $$ \text{km/h} $$ por $$ 3.6 $$, e o oposto é feito com a operação de multiplicação, ou seja, a quantidade em $$ \text{m/s} $$ é multiplicada por $$ 3.6 $$ a fins de se obter seu equivalente em $$ \text{km/h} $$.

Para fazer essas operaçãoes por substituição direta, devemos usar estas seguintes igualdades:

+ $$ 1 \text{ km} = 1000 \text{ m} $$,
+ $$ 1 \text{ h} = 60 \text{ min} $$,
+ $$ 1 \text{ min} = 60 \text{ s} $$.

Comecemos por converter uma quantidade $$ x $$ em $$ \text{km/h} $$ para $$ \text{m/s} $$, e veremos o fator de $$ 3.6 $$ aparecer no denominador de divisão:

$$ \begin{eqnarray}
x \text{ km/h} & = & x \cdot \frac{1 \text{ km}}{1 \text{ h}} \\
& = & x \cdot \frac{1000 
\text{ m}}{60 \text{ min}} \\
& = & x \cdot \frac{1000 \text{ m}}{60 \cdot 1 \text{ min}} \\
& = & x \cdot \frac{1000 \text{ m}}{60 \cdot 60 \text{ s}} \\
& = & x \cdot \frac{1000 \text{ m}}{3600 \text{ s}} \\
& = & x \cdot \frac{1000 \text{ m} \div 1000}{3600 \text{ s} \div 1000} \\
& = & x \cdot \frac{1 \text{ m}}{3.6 \text{ s}} \\
& = & \frac{x}{3.6} \cdot \frac{1 \text{ m}}{1 \text{ s}} \\
& = & \frac{x}{3.6} \text{ m/s}
\end{eqnarray} $$

Agora, faremos o mesmo para uma quantidade $$ y $$ em $$ \text{m/s} $$, e veremos o fator de $$ 3.6 $$ aparecer como produto de multiplicação:

$$ \begin{eqnarray}
y \text{ m/s} & = & y \cdot \frac{ 1 \text{ m}}{1 \text{ s}} \\
& = & y \cdot \frac{(1 / 1000) \text{ km}}{(1/60) \text{ min}} \\
& = & y \cdot \frac{(1 / 1000) \cdot 1 \text{ km}}{(1/60) \cdot 1 \text{ min}} \\
& = & y \cdot \frac{(1 / 1000) \cdot 1 \text{ km}}{(1/60) \cdot (1/60) \text{ h}} \\
& = & y \cdot \frac{(1 / 1000) \cdot 1 \text{ km}}{(1/60) \cdot (1/60) \cdot 1 \text{ h}} \\
& = & y \cdot \frac{(1 / 1000) \cdot 1 \text{ km}}{(1/3600) \cdot 1 \text{ h}} \\
& = & y \cdot \frac{1/1000}{1/3600} \cdot \frac{1 \text{ km}}{1 \text{ h}} \\
& = & y \cdot \frac{1}{1000} \cdot \frac{3600}{1} \cdot \frac{1 \text{ km}}{1 \text{ h}} \\
& = & y \cdot \frac{3600}{1000} \cdot \frac{1 \text{ km}}{1 \text{ h}} \\
& = & y \cdot 3.6 \cdot \frac{1 \text{ km}}{1 \text{ h}} \\
& = & 3.6 y \text{ km/h}
\end{eqnarray} $$

Portanto, se conhecemos a relação entre duas unidades, então conseguimos converter unidades compostas sem, necessariamente, usar um fator de conversão.

Aqui se enserra o básico de conversão de unidade. O que é necessário para se saber caso esteja no ensino médio, ou cursando engenharia e afins.

## O que são unidades admensionais? Quando e como usa-las?

Os tópicos daqui por diante são avançados e destinados a alunos de iniciação cientifica, mestrado e doutorado. Apesar que estes dois ultimos já devem saber trabalhar com unidades admensionais.

Bom, mas o que são essas tais unidades admensionais?

Elas são unidades sem dimensão física, e não me refiro à coeficientes que não possuem unidades, como é o caso do coeficiente de atrito $$ \mu $$. Não não! Me refiro a trabalhar com grandezas físicas que usualmente tem dimensão, como é o caso do comprimento. Assim, se eu trocar a palavra "unidades" por "comprimento", a pergunta se torna "O que são comprimentos admensionais?". Estranho isso, não? Sim, parece estranho, porém é um artificio matemático muito útil dependendo o sistema que estamos estudando.

- [x] aviso
- [] Intro
- [] Tamanho padrão.
- [] Ex com atomo de atomo de hidrogenio

## Por que alguns livros ou artigos de fisica teoria fazem $$ \hbar = c = 1 $$?

- [] intro
- [] unidades naturais
- [] exemplo com hamiltoniano