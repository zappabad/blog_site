---
layout: post
title:  "Três Pedras Ganham de Um Papel"
description: Como um jogo tão simples pode ser tão poderoso como ferramenta.
tags: sistemas design
---

# Pedra, Papel, Sistemas e História
Pedra-Papel-Tesoura (**RPS** em inglês) é extremamente simples de se jogar, e, francamente, extremamente sem graça, mas 
que pode nos ensinar uma grande lição em game design.

Podemos desconstruir RPS em um jogo que utiliza dois sistemas:

* **Ação simultânea -** Os jogadores fazem escolhas sem conhecimento sobre a ação de seu oponente e ao mesmo tempo. 
  (Você não vê o que o seu oponente fez para decidir o que vai fazer)
* **Intransitividade -** Não existe nenhuma opção dominada. (Isto é, todas as opções são igualmente boas: Pedra < 
  Papel < Tesoura < Pedra.)
  
A propriedade de intransitividade faz com que RPS seja caracterizado como um Game of Pure Strategy (Jogo de estratégia 
pura, ou **GOPS**). Em um GOPS, não existe necessidade de criação de balanceamento de estratégias, pois todas as 
estratégias já são, por definição, igualmente capazes. (isso não é *exatamente* verdade, expandiremos sobre isso 
AQUI COLOCAR LINKKKKKKKKKKKKKKKKK). Essa propriedade, por conta da popularidade de RPS, acaba sendo trocada desse 
nome complicado pela mais simples propriedade de **Rock-Paper-Scissors.**

# É Pau, é Pedra, é uma trap de Noobs

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

Todo esse processo pode ser divertido. Muitas vezes algo que parecia ser uma opção dominada ganha um resignificado 
na mente do jogador, dando à ele mais uma ferramenta pro seu arsenal estratégico, e tudo isso só acontece por conta 
desse processo de superação.

# Pedra pra toda obra

Como ferramenta, RPS é muito útil quando o objetivo é criar um sistema que se balanceia automaticamente. É 
impossível chegar perto do Ryu porque ele fica fazendo spam de *Hadouken*? Dê ao Ken uma habilidade que deixa ele 
evadir as *Fireballs* (por exemplo, o *Tatsumaki Senpuu Kyaku*, aquele que gira, sabe?). E agora? Ninguém mais usa 
*Hadouken* porque o *Tatsumaki* é bom demais em diminuir a distância entre o Ryu e o Ken. 

É aí que entra a Tesoura! Ao invés de mexer nos frames do *Tatsumaki* para deixar ele mais lento, ou cobrindo uma 
distância menor, ou tentar aumentar a velocidade do *Hadouken* para dificultar o Ken de desviar delas, é possível usar 
o RPS para criar uma terceira opção que ganha de *Tatsumaki*, mas perde para *Hadouken*: **Bloquear**.

Se o Ryu bloquear o *Tatsumaki*, ele ganha uma vantagem de frames que faz com que a troca (Ken *Tatsu* vs. Ryu Block) 
seja vantajosa para o Ryu. E, a peça final, claro, é que *Hadouken* possui *Chip Damage*, isto é, se você bloquear um 
*Hadouken*, a troca é neutra em termos de frames, mas quem bloqueia perde um pouco de vida.

Obviamente, esse exemplo tem suas limitações. O Ryu possui ferramentas parecidas com as do Ken, mas com detalhes 
diferentes (os frames de cada movimento deles são diferentes... O *Hadouken* do Ryu é melhor, mas o *Tatsumaki* do 
Ken é melhor que do Ryu). O ponto do exemplo é ilustrar como a filosofia de RPS pode ser usada para construir 
profundidade de estratégias.





> "This is a quote which should be followed"
> Also I think this sentence is quite long.
> more quote text to come
>   - Chris Wayne

However, these are bulletpoints:

* To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.
* another point
* that's it

However, these entries should not be styled:

1. an entry
2. another entry
3. that's another entry

<video preload="auto" poster="https://pbs.twimg.com/tweet_video_thumb/D5aj3tfW0AIiSxo.jpg" src="https://video.twimg.com/tweet_video/D5aj3tfW0AIiSxo.mp4" type="video/mp4" autoplay controls></video>

Jekyll also offers powerful support for code snippets:

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```

# An interesting fact on the economy of modern America

Pictures look like this:

![image](https://picsum.photos/200)

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

<blockquote class="twitter-tweet"><p lang="en" dir="ltr"><a href="https://twitter.com/hashtag/jekyll?src=hash&amp;ref_src=twsrc%5Etfw">#jekyll</a> <a href="https://twitter.com/hashtag/dash?src=hash&amp;ref_src=twsrc%5Etfw">#dash</a> now officially supports both, dark and light theming. Enjoy!<a href="https://t.co/4evp9pX2Ws">https://t.co/4evp9pX2Ws</a> <a href="https://t.co/vOQCZjGKic">pic.twitter.com/vOQCZjGKic</a></p>&mdash; 〽️ɪɢᴜᴇʟ (@bitbrain_) <a href="https://twitter.com/bitbrain_/status/1166440978124877827?ref_src=twsrc%5Etfw">August 27, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
