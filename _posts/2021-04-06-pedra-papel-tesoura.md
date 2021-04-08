---
layout: post
title:  "3 Pedras Ganham de 1 Papel"
description: Como um jogo tão simples pode ser tão poderoso como ferramenta.
tags: sistemas design
---

# Pedra, Papel, Sistemas e História
Pedra-Papel-Tesoura (**RPS** em inglês) é extremamente simples de se jogar, e, francamente, extremamente sem graça, mas 
que pode nos ensinar uma grande lição em game design.

Podemos desconstruir RPS em um jogo que utiliza dois sistemas:

* **Ação simultânea -** Os jogadores fazem escolhas sem conhecimento sobre a ação de seu oponente e ao mesmo tempo. 
  (Você não vê o que o seu oponente fez para decidir o que vai fazer)
* **Intransitividade -** Não existe nenhuma opção dominada. (Isto é, para todas as opções, sempre existe uma escolha 
  do oponente que faz ela vencer, e que **só** ela consegue vencer, dada a escolha do oponente: Pedra < Papel < Tesoura < Pedra.)
  
A propriedade de intransitividade faz com que RPS seja caracterizado como um Game of Pure Strategy (Jogo de estratégia 
pura, ou **GOPS**). Em um GOPS, não existe necessidade de criação de balanceamento de estratégias, pois todas as 
estratégias já são, por definição, igualmente capazes. (isso não é *exatamente* verdade, expandiremos sobre isso 
no futuro). Essa propriedade, por conta da popularidade de RPS, acaba sendo trocada desse 
nome complicado pela mais simples propriedade de **Rock-Paper-Scissors.**

# É Pau, é Pedra, é uma Trap de Noobs

Jogos modernos frequentemente possuem falta de balanceamento, para o bem ou para o mal. Isso ocorre quando, de todo 
o conjunto de ações que um jogador pode tomar, algumas delas são dominadas por outras. Em alguns casos, isso pode 
ser um problema para o jogo, e em outros pode ser uma decisão deliberada, e esse é um ponto importante: **A 
existência de opções dominadas não é, necessariamente, um problema.**

O processo de crescimento de um jogador muitas vezes *depende* do processo de usar uma estratégia, conhecer mais do 
jogo, e aprender que ela é uma estratégia dominada por outra, fazendo com que o jogador troque de estratégia; que o 
que parecia ser a melhor coisa a se fazer agora é vista como uma "noob trap". **E isso em si pode ser divertido.**

Como exemplo dessa lição, lembre-se da primeira vez que você jogou um jogo de luta. Você talvez ganhava todas as 
lutas, até que um dia você jogou contra alguém que ficava do outro lado da tela fazendo spam de Fireballs. Aquele 
Ryu que usava Hadouken o tempo todo e você não conseguia se aproximar... e quando você finalmente descobriu que é só 
pular e ir pra cima dele, você só ouvia o Ryu gritando "Shoryuken!", e aí você caía no chão e tudo começava de novo.

Depois de algumas partidas *extremamente* frustrantes, se você não desistiu de jogar, você provavelmente descobriu 
como bloquear, ou como não deixar o Ryu sequer tomar distância de você. E aí você começou a ganhar sempre... até que 
o Ryu aprendeu a lidar com sua nova estratégia, e assim continua o ciclo.

Todo esse processo pode ser divertido. **Muitas vezes algo que parecia ser uma opção dominada ganha um resignificado 
na mente do jogador**, dando à ele mais uma ferramenta pro seu arsenal estratégico, e tudo isso só acontece por conta 
desse processo de superação.

# Pedra pra Toda Obra

Como ferramenta, RPS é muito útil quando o objetivo é criar um sistema que se balanceia automaticamente. É 
impossível chegar perto do Ryu porque ele fica fazendo spam de *Hadouken*? Dê ao Ken uma habilidade que deixa ele 
evadir as *Fireballs* (por exemplo, o *Tatsumaki Senpuu Kyaku*, aquele que gira, sabe?). E agora? Ninguém mais usa 
*Hadouken* porque o *Tatsumaki* é bom demais em diminuir a distância entre o Ryu e o Ken. 

É aí que entra a Tesoura! Ao invés de mexer nos frames do *Tatsumaki* para deixar ele mais lento, ou cobrindo uma 
distância menor, ou tentar aumentar a velocidade do *Hadouken* para dificultar o Ken de desviar delas, é possível usar 
o RPS para criar uma terceira opção que ganha de *Tatsumaki*, mas perde para *Hadouken*: **Bloquear.**

Se o Ryu bloquear o *Tatsumaki*, ele ganha uma vantagem de frames que faz com que a troca (Ken *Tatsu* vs. Ryu *Block*) 
seja vantajosa para o Ryu. E, a peça final, claro, é que *Hadouken* possui *Chip Damage*, isto é, se você bloquear um 
*Hadouken*, a troca é neutra em termos de frames, mas quem bloqueia perde um pouco de vida.

<img src="{{site.baseurl}}/assets/img/rps-skills.png">

Obviamente, esse exemplo tem suas limitações. O Ryu possui ferramentas parecidas com as do Ken, mas com detalhes 
diferentes (os frames de cada movimento deles são diferentes... O *Hadouken* do Ryu é melhor, mas o *Tatsumaki* do 
Ken é melhor que do Ryu). O ponto do exemplo é ilustrar como **a filosofia de RPS pode ser usada para construir 
profundidade de estratégias.**


# La Casa de Pedra, Papel, Tesoura, ...

Diferentes escalas de RPS podem ser empregadas no processo de design. Em uma micro-escala temos o exemplo do Ken e 
Ryu, no qual o sistema é empregado para o balanço de "mini-jogos" que acontecem a cada segundo. É como se fossem 
jogados vários jogos seguidos de RPS, onde cada vitória representa uma pequena vantagem de pontos de vida. Usar 
um *Hadouken* quando seu oponente bloqueia dá 2% de dano *on block*, por exemplo. O vencedor do *round* é, portanto, 
aquele que primeiro vence uma série de várias rodadas de RPS.

Também é possível usar o RPS em uma macro-escala. No *Street Fighter*, por exemplo, existem grupos de personagens 
que se encaixam, em diferentes quantidades, em uma de três caixas: *Grappler*, *Zoner* ou *Rusher*. 
*Grapplers* são aqueles que se beneficiam de lutas à curta distância, mas que possuem dificuldade em se aproximar de 
suas vítimas; *Rushers* são personagens que dependem da sua mobilidade boa para se aproximar dos seus inimigos ... 
são velozes, porém frágeis; e *Zoners*, que são aqueles que possuem mobilidade reduzida, mas são ótimos 
em punir aqueles que dão tempo para eles carregarem seus movimentos (daí o nome *Zoner*)... eles são bons em reagir e 
manter a distância, mas se ficarem de cara com seus inimigos, rapidamente sucumbem.

<img src="{{site.baseurl}}/assets/img/rps-matchups.png">

Fica bem claro que, nesse caso, **existem vantagens mesmo antes da partida começar**, dependendo do *match-up* que é 
selecionado. Os *Grapplers* possuem muita dificuldade de se aproximar dos *Zoners*, que se beneficiam 
dessa distância, normalmente por possuir algum projétil bom que impede o lento e furioso *Grappler* de colar nele.
Os *Rushers* adoram jogar contra *Zoners*, pois, assim que conseguirem se aproximar (graças à sua 
mobilidade aumentada), a luta fica à seu favor, já que os *Zoners* não podem se beneficiar de suas habilidades à 
longa distância. E, finalmente, os *Grapplers* ficam tranquilos ao lutar contra *Rushers*, pois não precisam se 
preocupar em se aproximar deles... é só esperar que a *Chun-Li* (uma clássica *Rusher*) venha pra cima de você, 
afinal, ela depende de ficar próxima pra lutar, e assim que a luta ficar no mano-a-mano, o poder devastador de um 
*Grappler* consegue atropelar a fragilidade de seu oponente.

Em micro-escala, vencer uma rodada de RPS significava uma pequena vitória em pontos de vida, e em macro-escala, 
ganhar um RPS ao escolher um estilo de personagem bom contra o seu oponente significa começar a série já com algumas 
rodadas vencidas... o seu oponente vai ter que fazer hora extra pra compensar a desvantagem de *match-up* que ele 
escolheu tomar.

# ... Lizard e Spock

Os sistemas de RPS em macro-escala podem acontecer em diferentes magnitudes. Por um lado, pode ser uma parte 
importante do que faz o jogo ficar "justo" por ser um sistema de cheques e balanças que é integral para que o jogo 
possua alguma noção de *counterplay*. Por outro, pode causar uma sensação de injustiça e desamparo para os jogadores 
que podem achar que já começam perdendo mesmo antes do jogo começar.

Como exemplo, pense na fase de escolha de personagem, ou *draft*, no *League of Legends.* Como background, nessa 
fase são escolhidos 10 personagens (totalizando cinco por time, cada um controlado por um jogador) que serão utilizados até o
final da partida. Cada personagem possui distintos pontos fortes e pontos fracos, que podem ser exploitados pelos outros 
personagens.

O *draft* procede com cada time podendo escolher alguns personagens para serem banidos durante a partida, dentre o 
elenco de mais de 100 opções. Depois disso, os times intercalam, escolhendo um personagem por turno, até que se 
complete a escolha de todos eles.

Dessa forma, um personagem forte **A** têm chance de ser "controlado" por personagem **B** inimigo que, por mais que 
não tão objetivamente forte, possui um bom *match-up* contra **A**. E da mesma forma, um personagem **C** então pode 
ser escolhido para complementar **A** e ajudar no combate contra **B**, e assim sucessivamente. **As escalas em que 
essas escolhas impactam o jogo então podem ser ajustadas meticulosamente por mudanças pequenas em *match-ups* 
específicos.**

# Pedra, Papel, Tesoura e Tesouros

**Em jogos modernos, RPS, como vemos, é uma ferramenta que é usada mais "em espírito" do que de forma literal na 
criação de sistemas de jogo.** É claro que o *Zangief* possui uma chance de ganhar de um *Guile*, por mais que *Grapplers* 
tenham uma suposta vantagem contra *Zoners*. Do contrário, o jogo terminaria na escolha de personagens, sem 
necessidade da luta acontecer e, consequentemente, sem necessidade do *Street Fighter* existir.

Pense no seguinte "jogo experimento", **Pedra, Papel, Tesouro e tesouros**:

* Jogadores escolhem entre Pedra, Papel e Tesoura como em RPS tradicional, mas...
* Cada jogador começa também com **10 "tesouros"**. Ao mostrarem suas mãos com sua escolha de RPS, os jogadores também 
  escolhem e falam, simultaneamente, **um** ou **três** tesouros, pagando-os ao retirá-los de seu total de tesouros.

Normalmente, Pedra perde para Papel, mas, se quem escolheu Pedra pagar **três tesouros**, e quem escolheu Papel 
pagou somente **um tesouro,** vence a rodada quem escolheu Pedra. Isto é:

* As regras de RPS se aplicam para decidir quem ganha normalmente, **mas três tesouros sempre ganham de um 
  tesouro**, independente da escolha feita no RPS. Do contrário (ou seja, três contra três tesouros, ou um contra um 
  tesouro), vence quem venceria a rodada de RPS.
* Perde quem perder cinco rodadas primeiro, ou quem não tiver tesouros sobrando para pagar mais rodadas, o que vier 
  primeiro.

Pense nesse jogo. Pense nas estratégias que são possíveis dada essa modificação simples ao jogo de RPS. É sério, vou 
te dar um tempo pra pensar... e na semana que vem falaremos mais sobre ele.









