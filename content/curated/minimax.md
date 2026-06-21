<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Aula 07- Solução de Problemas (Busca Adversária)<sup>1</sup>**
  - Sinopse
  - Sumário
  - Aulas anteriores
  - Teoria dos Jogos: Conceito
  - Teoria dos Jogos
  - Teoria dos Jogos: Número de jogadores
  - Teoria dos Jogos: Objetivo do Jogo
  - Teoria dos Jogos: Informações sobre o jogo
  - Teoria dos Jogos: Algoritmos por turnos
  - Teoria dos Jogos: Árvore de Busca
  - Teoria dos Jogos: Árvore de Busca
  - Teoria dos Jogos: Árvore de Busca
  - Teoria dos Jogos: Árvore de Busca
  - Teoria dos Jogos: Árvore de Busca
  - Teoria dos Jogos: Árvore de Busca
  - Teoria dos Jogos: Algoritmo Minimax
  - Teoria dos Jogos: Algoritmo Minimax
  - Teoria dos Jogos: Algoritmo Minimax
  - Teoria dos Jogos: Algoritmo Minimax
  - Teoria dos Jogos: Algoritmo Minimax
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Teoria dos Jogos: Algoritmo Minimax**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
- **Algoritmo Minimax: Teste de Mesa**
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Minimax: Teste de Mesa
  - Algoritmo Alfa-Beta
  - Algoritmo Alfa-Beta
  - Algoritmo Alfa-Beta
  - Algoritmo Alfa-Beta
  - Algoritmo Alfa-Beta
  - Algoritmo Alfa-Beta
  - Algoritmo Alfa-Beta

<!-- EXEC_SUMMARY_END -->
<!-- DATALAB_CHUNK 1: pages 1-20 -->

{0}------------------------------------------------

# Inteligência Artificial
## Aula 07- Solução de Problemas (Busca Adversária)<sup>1</sup>

Sílvia M.W. Moraes

A large, modern, multi-story building with a light-colored facade and many windows, surrounded by trees and a clear blue sky. This is the main building of the University of Tsukuba.

<sup>1</sup>Este material não pode ser reproduzido ou utilizado de forma parcial sem a permissão dos autores.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5fb340ad68b0c71df0b56698b137e35b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A large, modern, multi-story building with a light-colored facade and many windows, surrounded by trees and a clear blue sky.
<!-- /IMAGE_DESCRIPTION -->
### Sinopse

- Nesta aula, apresentamos o **algoritmo minimax**.
- Este material foi construído com base nos capítulos:
  - 4 do livro Artificial Intelligence – a Modern Approach de Russel & Norvig
  - 4 do livro Inteligência Artificial de Luger.

{2}------------------------------------------------
### Sumário

- 1 O que vimos ...
- 2 Teoria dos Jogos
- 3 Algoritmo Minimax
- 4 Algoritmo Alfa-Beta Pruning

{3}------------------------------------------------
### Aulas anteriores

- Agente Reativos e Cognitivos
- Solução de Problemas
  - Representação, Espaço de Estados, Plano: sequência de ações
  - Busca sem informação
  - Busca com informação
    - A\*
    - Algoritmos de busca local por refinamentos sucessivos: Hill Climbing, Simulated Annealing e Algoritmos Genéticos

{4}------------------------------------------------
### Teoria dos Jogos: Conceito
### Teoria dos Jogos

"É uma disciplina da Matemática que estuda jogos idealizados e abstratos." (Ian Millington)

- Segundo esta teoria, os jogos são classificados por:
  - Número de jogadores;
  - Objetivos dos jogadores;
  - Informação que cada jogador possui do jogo.

{5}------------------------------------------------
### Teoria dos Jogos: Número de jogadores

- **Número de jogadores: 2 ou mais ?**
  - A maioria dos algoritmos de IA para jogos de tabuleiro são para dois jogadores.
    - Exemplos: jogo da velha, damas, xadrez, ...
  - Os algoritmos, na sua forma básica, podem ser adaptados para mais de dois jogadores.
  - Contudo, as otimizações destes algoritmos assumem que existe somente dois jogadores e, por isso, essas adaptações não são simples!

{6}------------------------------------------------
### Teoria dos Jogos: Objetivo do Jogo

- **Objetivo do jogo: vencer**
  - Zero-Sum Game
    - A sua vitória é a derrota do seu oponente.
    - “A soma dos *scores* de todos no final resulta em zero”.  
(Vencedor : +1, Perdedor: -1)
    - Exemplos: jogo da velha, damas, xadrez, ...
  - Non-Zero-Sum Game
    - Todos podem vencer ou perder, foco está na sua vitória e não na derrota do outro oponente.
    - “A soma dos *scores* de todos no final não é zero necessariamente”.
    - Exemplos: Chicken game, ...

{7}------------------------------------------------
### Teoria dos Jogos: Informações sobre o jogo
#### - **Informação dos jogadores sobre o jogo:**

- Em jogos de tabuleiro, ambos os jogadores conhecem tudo sobre o estado do jogo.
- Sabem qual o resultado de cada movimento irá produzir e quais opções estão disponíveis para os próximos movimentos (conhecem tudo desde o início do jogo).
- São jogos com “informações perfeitas”.
- A maioria dos jogos de estratégia por turnos, no entanto, possui algum elemento randômico que impede a previsão dos próximos movimentos. São jogos com “informações imperfeitas”. (Ex: Bridge)

{8}------------------------------------------------
### Teoria dos Jogos: Algoritmos por turnos

- Os algoritmos mais conhecidos e avançados para jogos por turnos são projetados para trabalhar com:
  - Dois jogadores;
  - Objetivo do tipo Zero-Sum;
  - “Informações perfeitas”.
- São jogos determinísticos e completamente observáveis, nos quais existem 2 jogadores cujas ações devem se alternar e que os valores de utilidade no fim do jogo são sempre iguais e opostos (ou simétricos).

{9}------------------------------------------------
### Teoria dos Jogos: Árvore de Busca

- Qualquer jogo por turno pode ser representado por uma árvore.

The diagram illustrates a game tree for a turn-based game. The tree is divided into four horizontal layers by dashed lines, representing alternating players. The layers are labeled on the left as follows: Player 1 (top), Player 2, Player 1, and Player 2 (bottom). A legend in the top right corner indicates that a circle represents a 'Terminal' position and a square represents a 'Position'. The tree starts with a single circle node at the top (Player 1). This node branches into two square nodes (Player 2). Each of these square nodes branches into two circle nodes (Player 1). The bottom-most layer consists of eight square nodes (Player 2). The first and last square nodes in this layer have a horizontal line underneath them, indicating they are terminal positions. The other six square nodes have two lines branching from them, suggesting further moves or a continuation of the game.

Diagram of a game tree for a turn-based game.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e6df2733626a85205c1db682e6259c46_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a game tree for a turn-based game.
<!-- /IMAGE_DESCRIPTION -->
### Teoria dos Jogos: Árvore de Busca

- Exemplo: **Jogo da Velha** (Tic Tac Toe em inglês).
    - Posição (estado) inicial é chamada de raiz da árvore;
    - Os ramos representam os movimentos legais e os nós correspondem às novas posições.

The diagram shows a game tree for a 3x3 tic-tac-toe game. The root node is an empty 3x3 grid. It branches into 9 nodes representing the first move (X in one of the 9 cells). From the first node (X in top-left), it branches into 5 nodes representing O's possible moves. This pattern continues, showing the branching factor decreasing as the game progresses. The diagram illustrates the search space for finding a winning strategy.

Diagram illustrating a game tree for a 3x3 tic-tac-toe game. The root node is an empty 3x3 grid. It branches into 9 nodes representing the first move (X in one of the 9 cells). From the first node (X in top-left), it branches into 5 nodes representing O's possible moves. This pattern continues, showing the branching factor decreasing as the game progresses. The diagram illustrates the search space for finding a winning strategy.

{11}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-5a4e62bead259c258d069fd3663ea670_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating a game tree for a 3x3 tic-tac-toe game.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9b6b5924b48bf2fd5f347f88f06f45b3_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A search tree for the game of Tic-Tac-Toe.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cfb98c691c1af5befe32ff9442eea511_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A search tree diagram for a 3x3 Tic-Tac-Toe game.
<!-- /IMAGE_DESCRIPTION -->
### Teoria dos Jogos: Árvore de Busca

- **Fator de ramificação:** Número de sucessores de um nó.
  - É o número de transições disponíveis em cada estado (corresponde aos galhos da árvore).
  - A partir de cada jogada, vários movimentos (galhos ou ramos) são possíveis.
  - É um bom indicador de quanto será difícil para o computador escolher a sua próxima jogada.
  - Exemplos - **Fator Médio de Ramificação:**
    - Jogo da Velha: 5
    - Xadrez: 35

{12}------------------------------------------------
### Teoria dos Jogos: Árvore de Busca

- **Profundidade:** Jogos diferentes têm diferentes profundidades de árvore, ou seja, um número máximo diferente de turnos.
  - Corresponde ao número máximo de turnos (troca entre as jogadas dos jogadores)
  - Exemplos - **Profundidade:**
    - Jogo da Velha: 8 (No jogo da velha, existem 9 espaços no tabuleiro, logo haverá até 4 turnos)
    - Xadrez: ~100 (As partidas chegam com frequência até 50 movimentos por jogador).

{13}------------------------------------------------
### Teoria dos Jogos: Árvore de Busca
#### - **Árvore de Busca:**

- Jogo da Velha :  $\sim 5^8$  nodos
- Xadrez:  $\sim 35^{100}$  nodos
##### - **Transposição:**

- É a possibilidade de se ter a mesma configuração do tabuleiro a partir de seqüências diferentes de movimentos.
- Isto significa que na maioria dos jogos de tabuleiro a árvore não é uma árvore de fato, pois os galhos podem ser combinados bem como podem se dividir...

The diagram illustrates the concept of transposition in a game tree. It shows a search tree where different sequences of moves lead to the same board state. The root node is a 3x3 tic-tac-toe board. Two branches lead to intermediate nodes, which then converge to a single node representing the same board state. This demonstrates that the tree is not a simple tree but a directed acyclic graph (DAG) due to transpositions.

Diagram illustrating transposition in a game tree. It shows a search tree where different sequences of moves lead to the same board state. The root node is a 3x3 tic-tac-toe board. Two branches lead to intermediate nodes, which then converge to a single node representing the same board state. This demonstrates that the tree is not a simple tree but a directed acyclic graph (DAG) due to transpositions.

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1b5a812c8aa20fd5cba28e97001d32de_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating transposition in a game tree.
<!-- /IMAGE_DESCRIPTION -->
### Teoria dos Jogos: Árvore de Busca
##### - Redução por simetria

- No caso do jogo da velha, diminui o espaço de busca, mas o crescimento ainda é fatorial.

$$\begin{array}{|c|c|c|} \hline & & \\ \hline & & \\ \hline \times & & \\ \hline \end{array} = \begin{array}{|c|c|c|} \hline & & \\ \hline & & \\ \hline & & \times \\ \hline \end{array} = \begin{array}{|c|c|c|} \hline \times & & \\ \hline & & \\ \hline & & \\ \hline \end{array} = \begin{array}{|c|c|c|} \hline & & \times \\ \hline & & \\ \hline & & \\ \hline \end{array}$$

The diagram shows a search tree for the game of Tic-Tac-Toe. The root node is an empty 3x3 grid. It branches into three nodes representing the first move (X in center, top-left, or top-right). Each of these branches into five nodes representing O's possible responses. Each of these five nodes then branches into three nodes representing X's possible responses. Each of these nine nodes then branches into three nodes representing O's possible responses. This illustrates the exponential growth of the search space.

A search tree for the game of Tic-Tac-Toe. The root node is an empty 3x3 grid. It branches into three nodes representing the first move (X in center, top-left, or top-right). Each of these branches into five nodes representing O's possible responses. Each of these five nodes then branches into three nodes representing X's possible responses. Each of these nine nodes then branches into three nodes representing O's possible responses. This illustrates the exponential growth of the search space.

{15}------------------------------------------------
### Teoria dos Jogos: Algoritmo Minimax
#### - Algoritmo Minimax

- Os oponentes do jogo são chamados de **MIN** e **MAX**.
  - **MAX** representa o jogador tentando vencer, MAXimizando a sua vantagem.
  - **MIN** é o oponente que tenta MINimizar o *score* de MAX.
- **MIN** usa a mesma informação e tenta mover para um estado que é pior para **MAX**.

{16}------------------------------------------------
### Teoria dos Jogos: Algoritmo Minimax
#### - **Algoritmo MinMax - Características:**

- **Estado inicial:** posição inicial do tabuleiro e identificação do jogador que fará o movimento.
- **Função sucessor:** lista de pares (movimento, estado).
- **Teste de término:** fim de jogo (estado terminal, nodo-folha).
- **Função de utilidade (ou objetivo ou de avaliação):** atribui valores numéricos aos nodos. Geralmente devolve valores inteiros (mais eficiente). Ex (nodos terminais):
  - oponente venceu: -1
  - empate: 0
  - computador venceu: +1

{17}------------------------------------------------
### Teoria dos Jogos: Algoritmo Minimax
#### - Algoritmo MinMax - Características: ...

Estado (nodo) inicial

Movimento de MAX(x)

Movimento de MIN(o)

Estados (nodos) terminais

Função Objetiva

-1 0 +1

Diagram illustrating the Minimax algorithm for a 3x3 tic-tac-toe game. The tree starts with an initial state (empty 3x3 grid). A MAX node (X's turn) branches into three possible moves. Each move leads to a MIN node (O's turn), which branches into all possible responses. The tree continues to terminal states (win, loss, or draw) where the objective function is evaluated as -1, 0, or +1.

- Solução ótima:** sequência de movimentos a partir de um estado inicial até um estado final que representa uma vitória.

{18}------------------------------------------------
### Teoria dos Jogos: Algoritmo Minimax

- Dada uma árvore de jogo, a estratégia ótima pode ser determinada examinando-se o valor *minimax* de cada nodo  $k$ :  $VALOR\_MINIMAX(k)$ .
  - Corresponde a utilidade para MAX de se encontrar um estado correspondente, supondo que ambos os jogadores têm um desempenho ótimo desse estado até o fim do jogo.

$VALOR\_MINIMAX(k)=$

- $UTILIDADE(k)$ , se  $k$  é um estado terminal;
- $\max_{s \in Sucessores(k)} VALOR\_MINIMAX(s)$ , se  $k$  é nodo MAX;
- $\min_{s \in Sucessores(k)} VALOR\_MINIMAX(s)$ , se  $k$  é nodo MIN;

{19}------------------------------------------------
### Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

The diagram shows a minimax search tree with four levels. The levels are labeled MAX, MIN, MAX, and MIN from top to bottom. The root node is a MAX node. It has three children, all MIN nodes. The left MIN node has two children, both MAX nodes. The middle MIN node has two children, both MAX nodes. The right MIN node has two children, both MAX nodes. The leaves are MIN nodes with values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The optimal path is highlighted with a solid line, starting from the root, going to the left MIN node, then to the right MAX node, then to the left MIN node, and finally to the leaf with value 9. Other paths are dashed.

A minimax search tree diagram illustrating the process of finding the optimal path. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is a MAX node. It has three children, all MIN nodes. The left MIN node has two children, both MAX nodes. The middle MIN node has two children, both MAX nodes. The right MIN node has two children, both MAX nodes. The leaves are MIN nodes with values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The optimal path is highlighted with a solid line, starting from the root, going to the left MIN node, then to the right MAX node, then to the left MIN node, and finally to the leaf with value 9. Other paths are dashed.

<!-- DATALAB_CHUNK 2: pages 21-40 -->

{20}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-81a4cbf0b3c4cbc065efdf8f800dadde_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram illustrating the process of finding the optimal path.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eb03559a4d92ea9ebd63ea9be663c50a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram illustrating the process of finding the optimal path.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ae53f90bb87d6d09e2d6b5278d7c338f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-26d664119ad25250780f554633444e54_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram illustrating the process of finding the optimal path.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-9c1d3678db4a12d5864cb2a4def1135d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-28d75f39a24203712ee907b32cf0bbe5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dd5771673aececa53d42ece89218299d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram illustrating the process of finding the optimal path.
<!-- /IMAGE_DESCRIPTION -->
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

The diagram illustrates a minimax search tree with four levels, alternating between MAX and MIN nodes. The root is a MAX node. It has three children which are MIN nodes. The first MIN node has two children which are MAX nodes; the left one is labeled '3'. The second MIN node has two children which are MAX nodes. The third MIN node has two children which are MAX nodes. The leaf nodes are labeled with values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6.

A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN. The root is a MAX node. It has three children which are MIN nodes. The first MIN node has two children which are MAX nodes; the left one is labeled '3'. The second MIN node has two children which are MAX nodes. The third MIN node has two children which are MAX nodes. The leaf nodes are labeled with values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6.

{21}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

{22}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

Diagram illustrating a minimax search tree structure. The tree is divided into levels labeled MAX and MIN. The root node is a MAX node. It has three children, all MIN nodes. The leftmost MIN node has a value of 3. It has two children, both MAX nodes. The leftmost MAX node has a value of 3, and the rightmost MAX node has a value of 9. The root node has a value of 3. The tree continues to have more levels, with values 0, 7, 4, 2, 1, 5, 6 at the leaf level. The optimal path is highlighted by a solid line from the root to the leftmost MIN node (value 3), then to the leftmost MAX node (value 3), and finally to the leftmost leaf node (value 2).

A minimax search tree diagram illustrating the process of finding the optimal path. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is a MAX node. It has three children, all MIN nodes. The leftmost MIN node has a value of 3. It has two children, both MAX nodes. The leftmost MAX node has a value of 3, and the rightmost MAX node has a value of 9. The root node has a value of 3. The tree continues to have more levels, with values 0, 7, 4, 2, 1, 5, 6 at the leaf level. The optimal path is highlighted by a solid line from the root to the leftmost MIN node (value 3), then to the leftmost MAX node (value 3), and finally to the leftmost leaf node (value 2).

{23}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

The diagram illustrates a minimax search tree with four levels: MAX, MIN, MAX, and MIN. The root node is a MAX node (square) with three children (MIN nodes, circles). The left MIN node has a value of 3 and two children (MAX nodes, circles) with values 3 and 9. The middle MIN node has a value of 0 and two children (MAX nodes, circles) with values 7 and 4. The right MIN node has two children (MAX nodes, circles) with values 2 and 1. The leaf nodes (MIN level) have values 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. Empty squares represent unvisited nodes.

A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN. The root node is a MAX node (square) with three children (MIN nodes, circles). The left MIN node has a value of 3 and two children (MAX nodes, circles) with values 3 and 9. The middle MIN node has a value of 0 and two children (MAX nodes, circles) with values 7 and 4. The right MIN node has two children (MAX nodes, circles) with values 2 and 1. The leaf nodes (MIN level) have values 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. Empty squares represent unvisited nodes.

{24}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

The diagram shows a minimax search tree with four levels. The levels are labeled MAX, MIN, MAX, and MIN from top to bottom. The root node is a MAX node. It has three children, all MIN nodes. The left MIN node has two children, both MAX nodes. The middle MIN node has two children, both MAX nodes. The right MIN node has two children, both MAX nodes. The leaves are MIN nodes. The values at the leaves are 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The values at the MAX nodes are 3, 9, 0, 7, and two empty boxes. The values at the MIN nodes are 3, and two empty boxes. The root node is empty.

A minimax search tree diagram illustrating the process of finding the optimal path. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is a MAX node. It has three children, all MIN nodes. The left MIN node has two children, both MAX nodes. The middle MIN node has two children, both MAX nodes. The right MIN node has two children, both MAX nodes. The leaves are MIN nodes. The values at the leaves are 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The values at the MAX nodes are 3, 9, 0, 7, and two empty boxes. The values at the MIN nodes are 3, and two empty boxes. The root node is empty.

{25}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

MAX

MIN

MAX

MIN

2 3 5 9 0 7 4 2 1 5 6

A minimax search tree diagram illustrating the process of finding the maximum value. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is a white square. Its left child is a black circle with value 3, and its right child is a black circle with value 0. The node with value 3 has two children: a black circle with value 3 and a black circle with value 9. The node with value 0 has two children: a black circle with value 0 and a black circle with value 7. The node with value 7 has two children: a white square and a black circle with value 1. The node with value 1 has two children: a black circle with value 5 and a black circle with value 6. The leaf nodes have values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The path from the root to the leaf with value 6 is highlighted with a dashed line.

{26}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-90ddb84c323b956e2d50a54d3f870566_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram illustrating the process of finding the maximum value.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2ae3eae1bd80a90f192f568ae246a9a6_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A minimax search tree diagram illustrating the process of finding the maximum value.
<!-- /IMAGE_DESCRIPTION -->
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

Diagram illustrating a minimax search tree. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is a MAX node with a value of 3. It has three children, all MIN nodes. The left MIN node has a value of 0 and two children, both MAX nodes. The middle MIN node has a value of 7 and two children, both MAX nodes. The right MIN node has a value of 2 and two children, both MAX nodes. The leaves are MIN nodes with values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The path from the root to the leaf with value 9 is highlighted with a thick line, indicating the optimal path.

A minimax search tree diagram illustrating the process of finding the maximum value. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is a MAX node with a value of 3. It has three children, all MIN nodes. The left MIN node has a value of 0 and two children, both MAX nodes. The middle MIN node has a value of 7 and two children, both MAX nodes. The right MIN node has a value of 2 and two children, both MAX nodes. The leaves are MIN nodes with values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The path from the root to the leaf with value 9 is highlighted with a thick line, indicating the optimal path.

{27}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

The diagram illustrates a minimax search tree with four levels: MAX, MIN, MAX, and MIN. The root node is a MAX node with a value of 3. It has three children which are MIN nodes. The first MIN node has a value of 3 and two children (MAX nodes) with values 3 and 9. The second MIN node has a value of 0 and two children (MAX nodes) with values 0 and 7. The third MIN node has a value of 6 and two children (MAX nodes) with values 2 and 6. The leaf nodes (MIN level) have values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6.

| Level | Type | Value | Children (Level, Type, Value) |
|-------|------|-------|-------------------------------|
| MAX   | Root | 3     | (MIN, 3), (MIN, 0), (MIN, 6)  |
| MIN   | 3    | 3     | (MAX, 3), (MAX, 9)            |
| MIN   | 0    | 0     | (MAX, 0), (MAX, 7)            |
| MIN   | 6    | 6     | (MAX, 2), (MAX, 6)            |
| MAX   | 3    | 3     | (MIN, 2), (MIN, 3)            |
| MAX   | 9    | 9     | (MIN, 5), (MIN, 9)            |
| MAX   | 0    | 0     | (MIN, 0)                      |
| MAX   | 7    | 7     | (MIN, 7), (MIN, 4)            |
| MAX   | 2    | 2     | (MIN, 2), (MIN, 1)            |
| MAX   | 6    | 6     | (MIN, 5), (MIN, 6)            |
| MIN   | 2    | 2     | -                             |
| MIN   | 3    | 3     | -                             |
| MIN   | 5    | 5     | -                             |
| MIN   | 9    | 9     | -                             |
| MIN   | 0    | 0     | -                             |
| MIN   | 7    | 7     | -                             |
| MIN   | 4    | 4     | -                             |
| MIN   | 2    | 2     | -                             |
| MIN   | 1    | 1     | -                             |
| MIN   | 5    | 5     | -                             |
| MIN   | 6    | 6     | -                             |

A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN. The root node is a MAX node with a value of 3. It has three children which are MIN nodes. The first MIN node has a value of 3 and two children (MAX nodes) with values 3 and 9. The second MIN node has a value of 0 and two children (MAX nodes) with values 0 and 7. The third MIN node has a value of 6 and two children (MAX nodes) with values 2 and 6. The leaf nodes (MIN level) have values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6.

{28}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

MAX

MIN

MAX

MIN

2 3 5 9 0 7 4 2 1 5 6

A minimax search tree diagram with four levels: MAX, MIN, MAX, and MIN. The root node is a MAX node (square). It has three children which are MIN nodes (circles). The first MIN node has a value of 3 and two children (MAX nodes) with values 3 and 9. The second MIN node has a value of 0 and two children (MAX nodes) with values 0 and 7. The third MIN node has a value of 2 and two children (MAX nodes) with values 2 and 6. The leaf nodes (MIN level) have values: 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6.

{29}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- Exemplo:

MAX

MIN

MAX

MIN

2 3 5 9 0 7 4 2 1 5 6

A minimax search tree diagram illustrating the process of finding the optimal path. The tree has four levels: MAX (root), MIN, MAX, and MIN (leaves). The root node is labeled 3. It has three children: 3, 0, and 2. The node 3 has two children: 3 and 9. The node 0 has two children: 0 and 7. The node 2 has two children: 2 and 6. The leaf nodes are labeled 2, 3, 5, 9, 0, 7, 4, 2, 1, 5, 6. The optimal path is highlighted with a solid line, starting from the root 3, going to the left child 3, then to the right child 9, and finally to the leaf 9.

{30}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax
#### - Detalhando mais o algoritmo ...

```
função Minimax( tabuleiro, profundidade )  
    se FimDeJogo( tabuleiro ) ou profundidade == 0  
        retorne CalcularScore( tabuleiro )  
    se OponenteEstáJogando( tabuleiro ) {  
        valor = 9999999  
        para todas ramificações do tabuleiro  
            valor = mínimo(valor,Minimax(ramificação,profundidade -  
1))  
    }  
    senão {  
        valor = -9999999  
        para todas ramificações do tabuleiro  
            valor = máximo(valor,Minimax(ramificação,profundidade -  
1))  
    }  
    retornar valor
```

{31}------------------------------------------------
## Teoria dos Jogos: Algoritmo Minimax

- **Atividade II:** Testar o algoritmo minimax com a função objetivo  $f(k)$ , considerando que a jogada inicial do oponente foi:

|   |   |   |   |
|---|---|---|---|
| 1 | o | x | x |
|   |   | x |   |
|   |   | o |   |
| 2 | o | x | x |
|   |   | o |   |
|   |   |   | x |

{32}------------------------------------------------
## Algoritmo Minimax: Teste de Mesa

- Testar o algoritmo Minimax, considerando o tabuleiro abaixo, para definir a próxima jogada do computador (O):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

chamada inicial: **minimax**(tabuleiro, 4)

{33}------------------------------------------------
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating a Minimax search tree for a 3x3 Tic-Tac-Toe game. The tree shows the progression from the initial state (depth 4) down to the leaf nodes (depth 1), alternating between the computer (MAX) and the opponent (MIN).

**Profundidade** (Depth) is indicated on the right side of the tree.

**Estado inicial – oponente (MIN)** (Initial state – opponent (MIN)) is at depth 4.

**computador (MAX)** (computer (MAX)) is at depth 3.

**oponente (MIN)** (opponent (MIN)) is at depth 2.

**computador (MAX)** (computer (MAX)) is at depth 1.

**Fim de Jogo: +1** (End of Game: +1) is indicated at the bottom left.

```

graph TD
    D4["Estado inicial – oponente (MIN)"] --> D3_1["computador (MAX)"]
    D4 --> D3_2["computador (MAX)"]
    D4 --> D3_3["computador (MAX)"]
    D4 --> D3_4["computador (MAX)"]
    D3_1 --> D2_1["oponente (MIN)"]
    D3_1 --> D2_2["oponente (MIN)"]
    D3_2 --> D2_3["oponente (MIN)"]
    D3_2 --> D2_4["oponente (MIN)"]
    D3_3 --> D2_5["oponente (MIN)"]
    D3_3 --> D2_6["oponente (MIN)"]
    D3_4 --> D2_7["oponente (MIN)"]
    D3_4 --> D2_8["oponente (MIN)"]
    D2_1 --> D1_1["computador (MAX)"]
    D2_1 --> D1_2["computador (MAX)"]
    D2_2 --> D1_3["computador (MAX)"]
    D2_2 --> D1_4["computador (MAX)"]
    D2_3 --> D1_5["computador (MAX)"]
    D2_3 --> D1_6["computador (MAX)"]
    D2_4 --> D1_7["computador (MAX)"]
    D2_4 --> D1_8["computador (MAX)"]
    D2_5 --> D1_9["computador (MAX)"]
    D2_5 --> D1_10["computador (MAX)"]
    D2_6 --> D1_11["computador (MAX)"]
    D2_6 --> D1_12["computador (MAX)"]
    D2_7 --> D1_13["computador (MAX)"]
    D2_7 --> D1_14["computador (MAX)"]
    D2_8 --> D1_15["computador (MAX)"]
    D2_8 --> D1_16["computador (MAX)"]
    D1_1 --> Win["+1"]
  
```

A search tree diagram for a 3x3 Tic-Tac-Toe game. The root node is at depth 4, labeled 'Estado inicial – oponente (MIN)'. It has four children at depth 3, labeled 'computador (MAX)'. Each of these has two children at depth 2, labeled 'oponente (MIN)'. Each of those has two children at depth 1, labeled 'computador (MAX)'. Red arrows trace a path from the root down to a leaf node at depth 1, which is a win for the computer (+1).

{34}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8f7c0bf0c75a31fee6b0c7392ff57c39_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating a minimax search tree for a 3x3 tic-tac-toe game.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation process.

**Profundidade (Depth):** 4, 3, 2, 1, 0

**Estado inicial – oponente (MIN):**

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

**computador (MAX):**

Four branches from the initial state lead to depth 3 states:

- Branch 1 (Red arrow):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |

- Branch 2:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

- Branch 3:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
|   |   |   |

- Branch 4:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O | O |

**oponente (MIN):**

From the first depth 3 state, two branches lead to depth 2 states:

  - Branch 1 (Red arrow):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
|   |   |   |

  - Branch 2:

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |

**computador (MAX):**

From the first depth 2 state, two branches lead to depth 1 states:

  - Branch 1 (Red arrow):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
| O | O |   |

  - Branch 2 (Blue arrow):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
|   | O | O |

**oponente (MIN):**

From the second depth 1 state, a branch leads to a depth 0 state:

  - Branch 1 (Blue arrow):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
| X | O | O |

**Fim de Jogo:**

At depth 0, the game is over. The value is +1 for the first state and -1 for the second state.

**Evaluation:**

The value of the second depth 1 state is calculated as  $\text{minimo}(9999999, -1) = -1$ .

{35}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-4356776ca004ecba5d599667a155d7d4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the Minimax algorithm for a 3x3 tic-tac-toe game.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-789ee0a267b24f34bd1f45313e86c9a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a Minimax tree for Tic-Tac-Toe.
<!-- /IMAGE_DESCRIPTION -->
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of the game state.

The game state is represented by a 3x3 grid. The initial state is labeled "Estado inicial – oponente (MIN)".

The search tree shows the progression of the game, with levels labeled by "Profundidade" (Depth) from 4 to 1.

The tree structure is as follows:

- Depth 4 (Estado inicial – oponente (MIN)):** Initial state:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   |   |   |
- Depth 3 (computador (MAX)):** Four possible moves from the initial state:

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   |   | O |
- Depth 2 (oponente (MIN)):** Three possible moves from the first state at Depth 3:

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |
- Depth 1 (computador (MAX)):** Two possible moves from the first state at Depth 2:

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
|   | O | O |

The evaluation of the game state at Depth 1 is shown:

- The first state (O, X, X; O, X, X; O, O, ) is evaluated as **+1**.
- The second state (O, X, X; O, X, X; , O, O) is evaluated as **-1**.

The evaluation is calculated as: **computador (MAX) : maximo(+1, -1) = +1**.

{36}------------------------------------------------
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating a Minimax search tree for a 3x3 Tic-Tac-Toe game. The tree shows the progression from the initial state to terminal states, with levels labeled by depth (Profundidade).

**Estado inicial – oponente (MIN)** (Depth 4):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   |   |   |

**computador (MAX)** (Depth 3):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
|   |   | O |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | O |

**oponente (MIN)** (Depth 2):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| X | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | X |   |

**Fim de Jogo:**

**+1** (Red arrow pointing to the first terminal state)

**-1** (Blue arrow pointing to the second terminal state)

**Profundidade** (Depth) is indicated on the right side of the tree.

{37}------------------------------------------------
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation process.

**Profundidade (Depth):** 4, 3, 2, 1, 0

**Estado inicial – oponente (MIN):**

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

**computador (MAX) (Depth 3):**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
|   |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

**oponente (MIN) (Depth 2):**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | X | O |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O | X |

**computador (MAX) (Depth 1):**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | O |
|   | O | X |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O | O |

**oponente (MIN) (Depth 0):**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | O |
| X | O | X |

**Fim de Jogo:** -1

**computador (MAX) (Depth 1):** 1

**oponente (MIN):**  $\min(9999999, -1) = -1$

**Evaluation:**

- Red arrows indicate the path chosen by the computer (MAX) and the opponent (MIN).
- Blue arrow indicates the path chosen by the computer (MAX).
- Green arrow indicates the path chosen by the opponent (MIN).
- Red arrow indicates the path chosen by the computer (MAX).

{38}------------------------------------------------
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of the game state.

**Estado inicial – oponente (MIN)** (Profundidade 4):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

**computador (MAX)** (Profundidade 3):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | O |

**oponente (MIN)** (Profundidade 2):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| X | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | X |   |

**computador (MAX)** (Profundidade 1):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | O |
| O | X |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | O | X |

**Fim de Jogo:**

Red arrows indicate the path chosen by the computer (MAX) to maximize its score. The final score is  $\text{máximo}(-1, +1) = +1$ .

{39}------------------------------------------------
## Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of the initial state.

**Profundidade** (Depth) is indicated on the right, ranging from 4 to 2.

**Estado inicial – oponente (MIN)** (Initial state – opponent (MIN)) is at depth 4:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Arrows from the initial state lead to the **computador (MAX)** level (depth 3):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | O |

Arrows from the computer level lead to the **oponente (MIN)** level (depth 2):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| X | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | X |   |

Evaluation values for the depth 2 states:

- First state: **+1** (red arrow)
- Second state: **-1** (blue arrow)
- Third state: **+1** (green arrow)

The evaluation for the third state is calculated as: **oponente (MIN) mínimo(+1,-1,+1) = -1**.

<!-- DATALAB_CHUNK 3: pages 41-60 -->

{40}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the final state.

**Estado inicial – oponente (MIN)**

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Profundidade

**computador (MAX)**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | O |

**oponente (MIN)**

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |

**computador (MAX)**

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O | O | O |

**oponente (MIN)**

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| O | O | X |

**Fim de Jogo : 0**

mínimo(9999999,0) = 0

{41}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating a Minimax search tree for a 3x3 tic-tac-toe game. The tree shows the progression from the initial state (depth 4) down to the terminal state (depth 0).

**Profundidade** (Depth) is indicated on the right side of the tree.

**Estado inicial – oponente (MIN)** (Initial state – opponent (MIN)) is at depth 4. The board is:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

A red arrow points to the first empty cell (row 1, column 1) as a potential move for the computer (MAX).

**computador (MAX)** (computer (MAX)) branches are at depth 3. The boards are:

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O | O |

**oponente (MIN)** (opponent (MIN)) branches are at depth 2. The boards are:

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O | X |

A blue arrow points to the value **-1** associated with the first opponent branch.

**computador (MAX)** (computer (MAX)) branches are at depth 1. The boards are:

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
|   | O | O |

A dashed arrow points from the value **maximo(0,+1) = +1** to the first computer branch.

**Fim de Jogo: +1** (Game Over: +1) is at depth 0. The board is:

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| O | O |   |

The value **0** is shown below the final board.

{42}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of the initial state.

**Estado inicial – oponente (MIN)** (Profundidade 4):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

**computador (MAX)** (Profundidade 3):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

**oponente (MIN)** (Profundidade 2):

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |

**computador (MAX)** (Profundidade 1):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X | X |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O | O | O |

**Fim de Jogo: +1 Fim de Jogo: +1**

**Profundidade** (4, 3, 2, 1)

**Labels and Annotations:**

- 1**: Value assigned to the first MAX node (O X X).
- +1**: Value assigned to the first MIN node (O X X).
- máximo(+1,+1) = +1**: Calculation for the final MAX node.

{43}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating a Minimax search tree for a 3x3 Tic-Tac-Toe game. The tree shows the progression from the initial state to terminal states, alternating between the computer (MAX) and the opponent (MIN).

**Estado inicial – oponente (MIN)**

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Profundidade

**computador (MAX)**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | O |

**oponente (MIN)**

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O | O |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |

**computador (MAX)**

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | O | X |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O | O | X |

Fim de Jogo: +1

Annotations: A red arrow points to the first MAX node. A blue "-1" is below the first MIN node. A "+1" is below the first MAX node. A "+1" is below the second MIN node. A "+1" is below the second MAX node.

{44}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating a Minimax search tree for a 3x3 Tic-Tac-Toe game. The tree shows the alternating levels of the computer (MAX) and the opponent (MIN), with the depth (Profundidade) indicated on the right.

**Estado inicial – oponente (MIN)** (Profundidade 4):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Arrows from the initial state point to four possible moves for the computer (MAX) at depth 3:

**computador (MAX)** (Profundidade 3):

- Move 1 (highlighted with a red arrow):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O |   |
- Move 2:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |
- Move 3:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
|   | O |   |
- Move 4:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O | O |

From the first move (highlighted), the tree continues to depth 2 (opponent's turn):

**oponente (MIN)** (Profundidade 2):

- Move 1 (highlighted with a blue arrow and labeled -1):

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
| O | O |   |
- Move 2:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O | O |   |
- Move 3:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |

From the first move at depth 2, the tree continues to depth 1 (computer's turn):

**computador (MAX)** (Profundidade 1):

- Move 1 (highlighted with a blue arrow and labeled +1):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | O | X |
- Move 2:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O | O | X |

From the first move at depth 1, the tree continues to depth 0 (opponent's turn):

**oponente (MIN)** (Profundidade 0):

- Move 1 (highlighted with a blue arrow and labeled +1):

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| O | O | X |

**Fim de Jogo: 0**

{45}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 tic-tac-toe game, showing the search tree and the evaluation of the initial state.

**Profundidade** (Depth) is indicated on the right, ranging from 4 to 1.

**Estado inicial – oponente (MIN)** (Initial state – opponent (MIN)) is at depth 4:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Arrows from the initial state point to the four possible moves at depth 3, labeled **computador (MAX)**:

**computador (MAX)** (Depth 3):

- Move 1 (Red arrow): 

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O |   |   |
- Move 2: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |
- Move 3: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |
- Move 4: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | O |

Arrows from the MAX nodes point to the possible moves at depth 2, labeled **oponente (MIN)**:

**oponente (MIN)** (Depth 2):

- From Move 1: 

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
| O | O |   |

 (Value: **+1**)
- From Move 2: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | X |
| O | O |   |

 (Value: **+1**)
- From Move 3: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |
- From Move 4: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |

Arrows from the MIN nodes point to the possible moves at depth 1, labeled **computador (MAX)**:

**computador (MAX)** (Depth 1):

- From Move 1: 

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O | O | X |

 (Value: **+1**)
- From Move 2: 

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O | X |

 (Value: **0**)

The final evaluation for the initial state is: **máximo(+1,0) = +1**.

{46}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of the initial state.

**Estado inicial – oponente (MIN)** (Profundidade 4):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

**computador (MAX)** (Profundidade 3):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O |   |

**oponente (MIN)** (Profundidade 2):

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
| O | O |   |

**Profundidade** (indicated by arrows):

- 4: Estado inicial – oponente (MIN)
- 3: computador (MAX)
- 2: oponente (MIN)

**Evaluation and Pruning:**

- The initial state is evaluated as  $-1$  (indicated by a red arrow).
- The state reached by the computer (MAX) is evaluated as  $+1$  (indicated by a blue arrow).
- The state reached by the oponente (MIN) is evaluated as  $+1$  (indicated by a blue arrow).
- The final evaluation is  $\text{mínimo}(+1, +1, +1) = +1$ .

{47}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of the game state.

**Profundidade** (Depth) is indicated on the right, ranging from 0 to 4.

**Estado inicial – oponente (MIN)** (Initial state – opponent (MIN)) is at depth 4:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   |   | O |

**computador (MAX)** (computer (MAX)) moves at depth 3:

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O |   |   |

**oponente (MIN)** (opponent (MIN)) moves at depth 2:

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
|   |   |   |

**computador (MAX)** (computer (MAX)) moves at depth 1:

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| O | O |   |

**oponente (MIN)** (opponent (MIN)) moves at depth 0:

|   |   |   |
|---|---|---|
| O | X | X |
| X | X | O |
| X | O | O |

**Fim de Jogo: 0** (Game over: 0) and **Fim de Jogo: -1** (Game over: -1) are shown at the bottom.

The diagram also shows the evaluation of the game state at depth 0, where the value 0 is calculated as  $\text{Máximo}(0, -1) = 0$ .

Arrows indicate the flow of the search tree, showing the path taken by the algorithm.

{48}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

{49}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating a minimax search tree for a 3x3 tic-tac-toe game. The tree structure shows the progression from the initial state (Estado inicial - oponente (MIN)) through the computer's move (computador (MAX)) and the opponent's move (oponente (MIN)) to the final state (Profundidade 4).

The initial state (Level 0) is a 3x3 grid:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Level 1 (computador (MAX)) shows four possible moves for 'O' (indicated by red arrows):

- Move 1: O at (1,1), X at (1,2), X at (2,2). Value: -1.
- Move 2: O at (1,1), X at (1,2), X at (2,2). Value: +1.
- Move 3: O at (1,1), X at (1,2), X at (2,2). Value: -1.
- Move 4: O at (1,1), X at (1,2), X at (2,2). Value: -1.

Level 2 (oponente (MIN)) shows the opponent's possible moves for 'X' from the first MAX node:

- Move 1: X at (1,1), X at (1,2), O at (2,2). Value: 0.
- Move 2: X at (1,1), X at (1,2), O at (2,2). Value: -1.
- Move 3: X at (1,1), X at (1,2), O at (2,2). Value: 0.

Level 3 (Profundidade 4) shows the final state of the game after the opponent's move. The value -1 is calculated as the minimum of the values from the opponent's moves:  $\text{Mínimo}(0, -1, 0) = -1$ .

Diagram illustrating a minimax search tree for a 3x3 tic-tac-toe game. The tree has four levels: Level 0 (Estado inicial - oponente (MIN)), Level 1 (computador (MAX)), Level 2 (oponente (MIN)), and Level 3 (Profundidade 4). The root node is a 3x3 grid with 'O' at (1,1), 'X' at (1,2), and 'X' at (2,2). Arrows show the search path: from the root to the first MAX node, then to the first MIN node, and finally to the leaf node with value -1. The leaf node is reached by playing 'O' at (2,3). The value -1 is propagated up to the MAX node, which then propagates +1 to the root. Other branches are shown but not fully evaluated.

{50}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game, showing the search tree and the evaluation of states.

**Profundidade** (Depth) is indicated on the right, ranging from 0 to 4.

**Estado inicial – oponente (MIN)** (Initial state – opponent (MIN)) is at depth 4. The board is:

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Arrows lead to the **computador (MAX)** level (depth 3), showing four possible moves:

- Move 1 (Red arrow): Board with O at (3,1). Value: **-1**.
- Move 2: Board with O at (2,3). Value: **+1**.
- Move 3: Board with O at (3,3). Value: **-1**.
- Move 4: Board with O at (3,2).

Arrows lead to the **oponente (MIN)** level (depth 2), showing four possible moves:

- Move 1 (Blue arrow): Board with X at (1,2). Value: **+1**.
- Move 2: Board with X at (2,2).
- Move 3: Board with X at (3,2).
- Move 4: Board with X at (3,1).

Arrows lead to the **computador (MAX)** level (depth 1), showing four possible moves:

- Move 1: Board with O at (1,2). Value: **Máximo(-1, +1) = +1**.
- Move 2: Board with O at (2,2). Value: **Máximo(-1, +1) = +1**.
- Move 3: Board with O at (3,2). Value: **Fim de Jogo: -1**.
- Move 4: Board with O at (3,1). Value: **Fim de Jogo: +1**.

Arrows lead to the **oponente (MIN)** level (depth 0), showing four possible moves:

- Move 1: Board with X at (1,1). Value: **Fim de Jogo: +1**.
- Move 2: Board with X at (2,1). Value: **Fim de Jogo: -1**.
- Move 3: Board with X at (3,1). Value: **Fim de Jogo: -1**.
- Move 4: Board with X at (3,2). Value: **Fim de Jogo: +1**.

{51}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating a Minimax search tree for a 3x3 tic-tac-toe game. The tree shows the progression from the initial state (depth 4) down to the leaf nodes (depth 2).

**Estado inicial – oponente (MIN)** (Depth 4):

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

**Profundidade** (Depth) is indicated on the right side of the tree.

**computador (MAX)** (Depth 3):

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
|   | O |   |

**oponente (MIN)** (Depth 2):

|   |   |   |
|---|---|---|
| O | X | X |
| X | X |   |
|   | O | O |

**Values and Pruning:**

- At Depth 2, the values **+1**, **+1**, and **-1** are shown below the boards.
- At Depth 3, the values **-1**, **+1**, and **-1** are shown below the boards.
- A dashed line indicates a pruning path from the initial state to the leaf node with value **-1** at Depth 2.

**oponente (MIN) Minimo(+1,+1,-1) = -1**

{52}------------------------------------------------
### Algoritmo Minimax: Teste de Mesa

Diagram illustrating the Minimax algorithm for a 3x3 Tic-Tac-Toe game.

**Initial State (Profundidade 4):**

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
|   | O |   |

Estado inicial – oponente (MIN)

**Computer's Turn (Profundidade 3):**

computer (MAX)

|   |   |   |
|---|---|---|
| O | X | X |
| O | X |   |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O | O |   |

+1

|   |   |   |
|---|---|---|
| O | X | X |
|   | X | O |
| O |   |   |

|   |   |   |
|---|---|---|
| O | X | X |
|   | X |   |
| O |   | O |

**Calculation:**

Máximo(-1,+1,-1,-1) = +1

**Jogada Escolhida**

**Profundidade**

Diagram showing a Minimax tree for Tic-Tac-Toe. The root node is at depth 4 (initial state, opponent's turn). It branches to four nodes at depth 3 (computer's turn). The first node is circled in red, and its value +1 is shown below it. A red arrow points from the text 'Jogada Escolhida' to this node. The other three nodes have values -1 below them. The text 'Máximo(-1,+1,-1,-1) = +1' is shown, indicating the computer chooses the move that maximizes its score. Arrows indicate the flow from the initial state to the depth 3 nodes.

{53}------------------------------------------------
### Algoritmo Alfa-Beta

- A **poda alfa-beta** (*alpha-beta pruning*) é uma técnica que permite descartar ramificações que não influenciarão na decisão final.
- Retorna o mesmo resultado que a versão padrão do minimax, mas visitando menos nodos;
- Pode ser aplicado em árvores com qualquer profundidade;

{54}------------------------------------------------
### Algoritmo Alfa-Beta
#### Princípio da técnica

”Considere um nó  $n$  da árvore, tal que o computador tenha que escolher um movimento até este nó. Se o computador tiver uma escolha melhor  $m$  no nó pai de  $n$  ou em qualquer ponto adicional acima dele, então  $n$  nunca será alcançado em um jogo real. E, assim, poderemos podá-lo.”

{55}------------------------------------------------
### Algoritmo Alfa-Beta
#### - *Exemplo:*

- $$\begin{aligned}\text{minimax} &= \max \{ \min\{3, 12, 8\}, \min\{2, x, y\}, \min\{14, 5, 2\} \} \\ &= \max \{3, z, 2\}, z \leq 2 \\ &= 3\end{aligned}$$

{56}------------------------------------------------
### Algoritmo Alfa-Beta

- O algoritmo recebeu esse nome em razão de dois parâmetros (limites sobre os valores propagados de volta) :
  - $\alpha$  : o valor da melhor escolha (valor mais alto) ao longo do caminho para MAX.
  - $\beta$  : o valor da melhor escolha (valor mais baixo) ao longo do caminho para MIN.

{57}------------------------------------------------
### Algoritmo Alfa-Beta

- Os valores de  $\alpha$  e  $\beta$  são atualizados a medida que a busca ocorre.
  - $\alpha$  : não pode diminuir.
  - $\beta$  : não pode aumentar.
- As ramificações são podadas (recursão encerrada) tão logo se sabe que o valor do nó atual é pior que o valor corrente de  $\alpha$  ou  $\beta$  para MAX ou MIN, respectivamente.
- A efetividade a técnica é altamente dependente da ordem em que os sucessores são examinados.

{58}------------------------------------------------
### Algoritmo Alfa-Beta

```
ação função busca_alfa_beta(estado, profundidade){  
    v = VALORMAX(estado, -9999999, +9999999, profundidade)  
    retorna a ação em SUCESSORES(estado) com valor v  
}  
int função VALORMAX(estado, alfa, beta, profundidade){  
    se fimDeJogo(estado) ou profundidade=0  
    então retorna UTILIDADE(estado)  
    v = -9999999  
    para cada s em SUCESSORES(estado) faça{  
        v = MAXIMO(v, VALORMIN(estado, alfa, beta, profundidade-1))  
        se v >= beta então retornar v  
        alfa = MAXIMO(alfa, v)  
    }  
    retornar v  
}  
...
```

{59}------------------------------------------------
### Algoritmo Alfa-Beta

```
...
int função VALORMIN(estado, alfa, beta, profundidade){
    se fimDeJogo(estado) ou profundidade=0
        então retorna UTILIDADE(estado)
    v = +9999999
    para cada s em SUCESSORES(estado) faça{
        v = MINIMO(v, VALORMAX(estado, alfa, beta, profundidade-1))
        se v <= alfa então retornar v
        beta = MINIMO(beta, v)
    }
    retornar v
}
```

<!-- DATALAB_CHUNK 4: pages 61-61 -->

{60}------------------------------------------------

# Desempenho dos Algoritmos

|           | Complexidade                  |
|-----------|-------------------------------|
| minimax   | $O(b^m)$                      |
| alfa-beta | $O(b^{m/2})$ com ordenação    |
|           | $O(b^{3m/4})$ ordem aleatória |

- $m$  é profundidade máxima
- $b$  é ramificação média
