# 🦈 Tony Shark: O Rei Tubarão Parte 1

## por [Prof. Anderson Rodrigues]

Neste tutorial, vamos criar um jogo simples no MakeCode Arcade com um tubarão nadando em um cenário submarino e se alimentando de peixes e  com um pescador maluco querendo caça-lo.

---

## Passo 1: Configurar a cor de fundo que representará a água

Vamos começar definindo a cor de fundo (água azul)

* :tree: Na categoria **Scene** (Cena), arraste o bloco **set background color to [ ]** para dentro do bloco **on start**.

* :paint brush: Clique no campo de cor e escolha o **tom azul claro (cor 9)** para representar a água.

```blocks
scene.setBackgroundColor(9)
```
---

## Passo 2: Criar o Cenário de Fundo

Vamos começar a desenhar o cenário com algas, bolhas e o movimento da água.

* :tree: Na categoria **Scene** (Cena), arraste o bloco **set background image to [ ]** para dentro do bloco **on start** abaixo do **set background color to [ ]**

* :pencil: Clique no quadrado cinza para abrir o editor e desenhe com algas, bolhas e o movimento da água ou o que desejar, e coloque o nome de **Cenario**.

```blocks
scene.setBackgroundColor(9)
scene.setBackgroundImage(assets.image`Cenario`)
```
---

## Passo 3: Criar o Tubarão (Sprite do Jogador)

Vamos adicionar o nosso personagem principal e chamá-lo de Tony_Shark.

* :paper plane: Na categoria **Sprites**, arraste o bloco **set [mySprite] to sprite [ ] of kind [Player]** para dentro do bloco **on start** abaixo do **scene.setBackgroundImage(assets.image`Cenario`)**.

* :mouse pointer: Renomeie a variável clicando em mySprite e **Rename Variable** e digite **Tony_Shark**.

* :pencil: Clique no quadrado cinza para abrir o editor e desenhe o seu sprite de tubarão ou pegue ele na galeria.

```blocks
scene.setBackgroundColor(9)
scene.setBackgroundImage(assets.image`Cenario`)
let Tony_Shark = sprites.create(assets.image`Tony_Shark`, SpriteKind.Player)
```
---

## Passo 4: Adicionar Movimento ao Tony_Shark

Vamos permitir que o jogador mova o Tony_Shark

* :controller: Na categoria **Controller** (Controle), arraste o bloco **move [mySprite] with buttons(+)** e encaixe-o no bloco **on start** abaixo do **set Tony_Shark to sprite [] of kind Player)**.

* :mouse pointer: Selecione Tony_Shark na lista suspensa de variáveis de Sprites.

```blocks
scene.setBackgroundColor(9)
scene.setBackgroundImage(assets.image`Cenario`)
let Tony_Shark = sprites.create(assets.image`Tony_Shark`, SpriteKind.Player)
controller.moveSprite(Tony_Shark)
```

## Passo 5: Impedir que o Tony_Shark saia da tela.

* :paper plane: Na categoria **Sprites**, arraste o bloco **set [mySprite] stay in screen (on)** para dentro do bloco **on start** abaixo do **move [mySprite] with buttons(+)**.

* :white check mark: Troque a variável de mySprite para Tony_Shark e altere o valor para **(ON)** caso ela esteja em **(OFF)**.

```blocks
scene.setBackgroundColor(9)
scene.setBackgroundImage(assets.image`Cenario`)
let Tony_Shark = sprites.create(assets.image`Tony_Shark`, SpriteKind.Player)
controller.moveSprite(Tony_Shark)
Tony_Shark.setStayInScreen(true)
```
---

## Fim!

**Parabéns! Você concluiu a configuração básica do jogo do Tony_Shark- O Rei Tubarão.**

Na próxima aula vamo criar as falas e avisos do nosso jogo e deixar ele mais interativo.

Aula 01 - https://arcade.makecode.com/#tutorial:46777-87047-84535-20520