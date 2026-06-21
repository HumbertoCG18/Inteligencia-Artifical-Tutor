<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Agentes e Algoritmos de Busca**
- **Agentes e Algoritmos de Busca**
  - Estados de mundo
  - Espaço de Busca
  - Algoritmo de Busca define o plano do agente
  - Atividade I
  - Atividade II
  - Atividade III
  - Espaço de Busca
  - Espaço de Busca
  - Espaço de Busca
  - Algoritmos de Busca Informada
  - Algoritmos de Busca Informada
  - Algoritmos de Busca Informada
  - Algoritmos de Busca Informada
  - Atividade IV
  - Atividade V

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Red decorative rectangleInteligência Artificial

INTRODUÇÃO À ALGORITMOS DE BUSCA HEURÍSTICA

PROF. SÍLVIA MORAES

{1}------------------------------------------------
## Agentes e Algoritmos de Busca

- ▶ A tarefa de um agente baseado em objetivo é descobrir a sequência de ações que o levará a solução do problema (seu objetivo).
- ▶ O primeiro passo no caminho que leva à solução é a definição de uma abstração de mundo que capture apenas os elementos essenciais do problema.
- ▶ Vamos considerar inicialmente alguns miniproblemas cujos ambientes são completamente observáveis, discretos e determinísticos.

{2}------------------------------------------------
## Agentes e Algoritmos de Busca

- ▶ No caso do agente-exemplo Aspirador de pó, apresentado em aulas anteriores, que é capaz de:
  - ▶ Perceber em que local está;
  - ▶ Perceber se há sujeira nesse local;
  - ▶ Mover-se para esquerda
  - ▶ Mover-se para direita;
  - ▶ Aspirar sujeira ou
  - ▶ Não fazer nada.
- ▶ é suficiente criar uma representação abstrata:
  - ▶ [Posição, Estado de A, Estado de B]

The diagram consists of two rectangular panels, labeled A and B, separated by a vertical line. Panel A shows a vacuum cleaner agent in the top right corner, facing left. Below the agent is a cluster of seven small circles representing dirt. Panel B shows the same cluster of dirt in the same position, but the vacuum cleaner agent is absent, representing a state where the agent has moved or is not present.

Diagram illustrating the vacuum cleaner agent in two states, A and B.

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7e2f2d03a5dda38b038fd4884629a2b4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the vacuum cleaner agent in two states, A and B.
<!-- /IMAGE_DESCRIPTION -->
### Estados de mundo

- ▶ Usando representação abstrata:
  - ▶ [Posição, Estado de A, Estado de B]
- ▶ Conseguimos representar os estados de mundo:
  - ▶ [A,Suja,Suja]
  - ▶ [A,Suja,Limpa]
  - ▶ [A,Limpa,Suja]
  - ▶ [A,Limpa,Limpa]
  - ▶ [B,Suja,Suja]
  - ▶ [B,Suja,Limpa]
  - ▶ [B,Limpa,Suja]
  - ▶ [B,Limpa,Limpa]

Diagram 1: A vacuum cleaner is in the left room. The left room is dirty (represented by a pile of dirt). The right room is empty and clean.

Diagram 3: A vacuum cleaner is in the left room. The left room is dirty (represented by a pile of dirt). The right room is empty and clean.

Diagram 5: A vacuum cleaner is in the left room. The right room is dirty (represented by a pile of dirt). The left room is empty and clean.

Diagram 7: A vacuum cleaner is in the left room. The left room is empty and clean. The right room is empty and clean.

Diagram 2: A vacuum cleaner is in the right room. The left room is dirty (represented by a pile of dirt). The right room is empty and clean.

Diagram 4: A vacuum cleaner is in the right room. The left room is dirty (represented by a pile of dirt). The right room is empty and clean.

Diagram 6: A vacuum cleaner is in the right room. The right room is dirty (represented by a pile of dirt). The left room is empty and clean.

Diagram 8: A vacuum cleaner is in the right room. The left room is empty and clean. The right room is empty and clean.

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ddfe517a5ad9c77c89a57a5e780b24ca_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 1: A vacuum cleaner is in the left room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-16d86083b7ebdc40c0647a1d3d46ace7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 3: A vacuum cleaner is in the left room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b615ff07e8a0f467f0a6f4783c4463eb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 5: A vacuum cleaner is in the left room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-af8b95b7fc833cebe89ba6c8ed839984_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 7: A vacuum cleaner is in the left room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d0baec9a9191662196c3f3be304ee01c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 2: A vacuum cleaner is in the right room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-451417078c55730b2f3f9ea924407f78_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 4: A vacuum cleaner is in the right room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ab5392ddbf4af970d4ef7bff2e4df925_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 6: A vacuum cleaner is in the right room.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4b9457ad2400572dbf0c0c9f7c825643_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram 8: A vacuum cleaner is in the right room.
<!-- /IMAGE_DESCRIPTION -->
#### Estado de Mundo

- ▶ No ambiente do Aspirador de pó é apenas por meio das ações do agente que o estado do mundo pode se modificar.
- ▶ Exemplo: (estadoAtual,ação,novoEstado)
  - ▶ ([A,Suja,Suja], **aspirar**, [A,Limpa,Suja])
  - ▶ ([A,Limpa,Suja], **direita**, [B,Limpa,Suja])
  - ▶ ([B,Limpa,Suja], **aspirar**, [B, Limpa,Limpa])
- ▶ Para o estado inicial [A,Suja,Suja], a sequência de ações procurada é **aspirar, direita, aspirar**

{5}------------------------------------------------
### Espaço de Busca

- O espaço de busca pode ser organizado na forma de uma árvore ou de um grafo

![A search tree diagram for a vacuum cleaner problem. The root node is [A,Suja,Suja]. It has three children: [A,Limpa,Suja] (labeled 'aspirar'), [A,Suja,Suja] (labeled 'esquerda'), and [B,Suja,Suja] (labeled 'direita'). The node [A,Limpa,Suja] has two children: [B,Limpa,Suja] (labeled 'direita') and [A,Limpa,Suja] (labeled 'aspirar/esquerda'). The node [B,Limpa,Suja] has three children: [B,Limpa,Limpa] (labeled 'aspirar'), [B,Limpa,Suja] (labeled 'direita'), and [A,Limpa,Suja] (labeled 'esquerda'). Ellipses indicate further nodes in the tree.](a7d78d22e465dea388b31d0739f9d0cd_img.jpg)

```
graph TD; Root["[A,Suja,Suja]"] -- "aspirar" --> N1["[A,Limpa,Suja]"]; Root -- "esquerda" --> N2["[A,Suja,Suja]"]; Root -- "direita" --> N3["[B,Suja,Suja]"]; N1 -- "direita" --> N4["[B,Limpa,Suja]"]; N1 -- "aspirar/esquerda" --> N5["[A,Limpa,Suja]"]; N4 -- "aspirar" --> N6["[B,Limpa,Limpa]"]; N4 -- "direita" --> N7["[B,Limpa,Suja]"]; N4 -- "esquerda" --> N8["[A,Limpa,Suja]"]; N2 -.- Dots1["..."]; N3 -.- Dots2["..."]; N5 -.- Dots3["..."];
```

A search tree diagram for a vacuum cleaner problem. The root node is [A,Suja,Suja]. It has three children: [A,Limpa,Suja] (labeled 'aspirar'), [A,Suja,Suja] (labeled 'esquerda'), and [B,Suja,Suja] (labeled 'direita'). The node [A,Limpa,Suja] has two children: [B,Limpa,Suja] (labeled 'direita') and [A,Limpa,Suja] (labeled 'aspirar/esquerda'). The node [B,Limpa,Suja] has three children: [B,Limpa,Limpa] (labeled 'aspirar'), [B,Limpa,Suja] (labeled 'direita'), and [A,Limpa,Suja] (labeled 'esquerda'). Ellipses indicate further nodes in the tree.

```
graph TD; S1((L)) -- "S" --> S2((R)); S2 -- "S" --> S1; S1 -- "L" --> S3((L)); S3 -- "R" --> S1; S1 -- "R" --> S4((R)); S4 -- "L" --> S1; S2 -- "L" --> S5((L)); S5 -- "R" --> S2; S2 -- "R" --> S6((R)); S6 -- "L" --> S2; S3 -- "S" --> S3; S4 -- "S" --> S4; S5 -- "S" --> S5; S6 -- "S" --> S6;
```

A state transition graph for a vacuum cleaner problem. The graph consists of 8 states represented by boxes. Each box contains a vacuum cleaner icon and a set of dots representing dirt. The states are arranged in a 3x3 grid. Transitions are labeled with 'L' (left), 'R' (right), and 'S' (suck). The graph shows a complex set of transitions between states, including self-loops labeled 'S'.

{6}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-88b0f3f4393228e9ea4d6542aef7c399_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A state transition graph for a vacuum cleaner problem.
<!-- /IMAGE_DESCRIPTION -->
#### Formalizando...

- ▶ Um problema pode ser definido formalmente por quatro componentes:
  - ▶ **estado inicial**: estado de mundo em que o agente começa a sua execução.
  - ▶ **descrição das ações**: define as ações possíveis do agente.
    - ▶ Em geral, usa uma função sucessor para gerar os estados válidos.
    - ▶ Dado um estado  $x$ , a função  $\text{sucessor}(x)$  retorna o conjunto de pares
  - ▶ **teste de objetivo**: usada para verificar se um dado estado é o estado objetivo.
  - ▶ **custo do caminho**: define o custo numérico a cada caminho que leva o estado inicial ao estado objetivo.

{7}------------------------------------------------
#### Formalizando...

- ▶ Exemplo Aspirador de pó
  - ▶ **estado inicial**: pode ser qualquer um, tal como [A,sujo,sujo].
  - ▶ descrição das ações: **aspirar, direita e esquerda**.
    - ▶ **sucessor**([A,sujo,sujo]) = { (aspirar, [A,limpo,sujo]), (esquerda, [A,sujo,sujo]), (direita,[B,sujo,sujo]) }
  - ▶ teste de objetivo: verifica se todos os locais estão limpos, ou seja, se atingiu um dos estados **[A,limpo,limpo]** ou **[B,limpo,limpo]**.
  - ▶ custo do caminho: cada passo custa 1, logo é o número de passos do caminho.

{8}------------------------------------------------
### Algoritmo de Busca define o plano do agente

- ▶ A tarefa do agente é dentro do espaço de busca encontrar a **sequência de ações que o leva do estado inicial ao estado objetivo**.
- ▶ Para isso, são usados algoritmos de busca.
- ▶ No exemplo, o agente poderia encontrar os seguintes **planos**:
  - ▶ **[aspirar, direita, aspirar]** tem custo 3.
  - ▶ **[direita, aspirar, esquerda, aspirar]** tem custo 4

{9}------------------------------------------------
### Atividade I

- ▶ Para os estados inicial [B,Suja,Limpa] a seguir, quais os planos que o agente poderia encontrar ?

{10}------------------------------------------------
### Atividade II

- ▶ Se o problema fosse estendido para mais salas, da seguinte forma: 2 salas no térreo, 2 salas no primeiro piso, acesso às salas pelo corredor e um elevador para viabilizar o deslocamento entre os andares
  - ▶ Sabendo que as operações disponíveis são:
    - ▶ Subir: do térreo para o primeiro piso desde que esteja no corredor
    - ▶ Descer: do primeiro piso para o térreo desde que esteja no corredor
    - ▶ Entrar na Sala 1: o agente deve estar no corredor do andar da Sala 1
    - ▶ Entrar na Sala 2: o agente deve estar no corredor do andar da Sala 2
    - ▶ Sair: o agente sai para o corredor do andar atual.
    - ▶ Aspirar: agente limpa a sala em que está posicionado.
1. Como representar ?
  2. Como seria um plano para limpar todas as salas ?

{11}------------------------------------------------
### Atividade III

- ▶ Considerando o estado atual do jogo da velha abaixo, monte o espaço de busca

|   |   |   |   |
|---|---|---|---|
| ▶ | X | O |   |
| ▶ |   | X |   |
| ▶ |   |   | O |

{12}------------------------------------------------
### Espaço de Busca

- ▶ Durante o processo de busca existe a possibilidade de desperçarmos tempo expandindo espaços que já foram encontrados e expandidos antes.
- ▶ Para alguns problemas, essa possibilidade nunca surge. O espaço de estados é uma árvore e só existe um caminho até cada estado. Ex: Problema das  $n$  rainhas.

The diagram illustrates the search space for the N-Queens problem using a tree structure of 4x4 chessboards. The root node is an empty board. It has three children, each with one queen in a different column. The first child has two children of its own, each with two queens. The second child has one child with two queens. The third child has one child with two queens. The fourth level shows four boards with three queens each. The first three boards have a queen in the first column and are marked with a large 'X', indicating they are invalid. The fourth board has a queen in the first column and is also marked with a large 'X', indicating it is invalid. This illustrates that the search space is a tree where each state is reached by a unique path, and invalid states are pruned.

Diagram illustrating the search space for the N-Queens problem. It shows a tree structure of 4x4 chessboards. The root node is an empty board. It has three children, each with one queen in a different column. The first child has two children of its own, each with two queens. The second child has one child with two queens. The third child has one child with two queens. The fourth level shows four boards with three queens each. The first three boards have a queen in the first column and are marked with a large 'X', indicating they are invalid. The fourth board has a queen in the first column and is also marked with a large 'X', indicating it is invalid. This illustrates that the search space is a tree where each state is reached by a unique path, and invalid states are pruned.

{13}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-eefe19c5e14dc4d6c316b7f7fbb7d7d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the search space for the N-Queens problem.
<!-- /IMAGE_DESCRIPTION -->
### Espaço de Busca

- ▶ Para outros, os estados repetidos são inevitáveis.
- ▶ Inclui problemas de localização de rotas ou quebra-cabeças deslizantes.
- ▶ As árvores de busca para esses problemas são infinitas (presença de ciclos).

O Mundo de blocos

Diagram of a robotic arm in a block world environment. The arm is positioned over a table with three stacks of blocks. The left stack has a blue block 'A'. The middle stack has a green block 'B' with an orange block 'C' on top. The right stack has a blue block 'A' with a green block 'B' on top, and an orange block 'C' on top of that. The arm is currently holding the orange block 'C' from the middle stack.

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 | 8 | 5 |
| 6 |   | 2 |

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 | 8 | 5 |
| 6 | 2 |   |

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 | 8 | 5 |
|   | 6 | 2 |

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 |   | 5 |
| 6 | 8 | 2 |

A search tree diagram for a 3x3 sliding tile puzzle. The root node is a 3x3 grid with tiles 1, 3, 4 in the top row; 7, 8, 5 in the middle row; and 6, an empty space (orange square), and 2 in the bottom row. Three arrows point to three child nodes. The left child has the empty space at the bottom-right. The middle child has the empty space at the bottom-middle. The right child has the empty space at the middle-right.

Diagram of a Tower of Hanoi puzzle. Three vertical pegs are labeled A, B, and C. A stack of five colored disks is on peg A. From top to bottom, the disks are red (labeled 1), orange (labeled 2), yellow (labeled 3), green (labeled 4), and blue (labeled 5).

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7832324609ad3cc688064e0341612b32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a robotic arm in a block world environment.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a33da0f14e456f92539ce3e9b7d81f9a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A search tree diagram for a 3x3 sliding tile puzzle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-df6babe297323feb1575ba89f5cf3b09_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a Tower of Hanoi puzzle. Three vertical pegs are labeled A, B, and C. A stack of five colored disks is on peg A. From top to bottom, the disks are red (labeled 1), orange (labeled 2), yellow (labeled 3)...
<!-- /IMAGE_DESCRIPTION -->
### Espaço de Busca

- ▶ O que fazer ?
  - ▶ Podar alguns estados para reduzir a árvore a um tamanho finito (ex. profundidade máxima fixa).
  - ▶ Memorizar os estados visitados. Relação inversamente proporcional espaço x tempo. “Algoritmos que esquecem sua história estão condenados a repeti-la”.
  - ▶ Em problemas com muitos estados repetidos, Busca-Em-Grafo é mais eficiente do que Busca-Em-Árvores

O diagrama ilustra o espaço de busca para o problema das 3-disk Tower of Hanoi. Os estados são representados por pilhas de blocos A, B e C. O estado inicial (labeled 'initial state') é uma pilha com A na base, B no meio e C no topo. O estado objetivo (labeled 'goal state') é uma pilha com A na base, C no meio e B no topo. As transições entre estados são representadas por setas bidirecionais, cada uma rotulada com uma operação de movimento de disco (ex: 'move A to B', 'move B to C', etc.). O diagrama mostra como o espaço de busca pode se expandir a partir do estado inicial, com muitos estados repetidos (como a pilha A-B-C) aparecendo em diferentes partes da árvore de busca.

Diagrama de um espaço de busca para o problema das 3-disk Tower of Hanoi, mostrando estados como pilhas de blocos A, B e C e transições entre eles.

{15}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-724c7777b608e53be38b12b6fb3c43bc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um espaço de busca para o problema das 3-disk Tower of Hanoi, mostrando estados como pilhas de blocos A, B e C e transições entre eles.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmos de Busca Informada

- ▶ A busca em um espaço de estados é o processo de procurar um caminho de solução iniciando no estado inicial até alcançar o estado objetivo.
- ▶ Algoritmos de Busca
  - ▶ sem informação (ou busca cega)
    - ▶ Busca em largura ou amplitude ou extensão
    - ▶ Busca em profundidade
  - ▶ com informação ou informada (usam funções heurísticas)

{16}------------------------------------------------
### Algoritmos de Busca Informada

- ▶ Busca com informação (ou heurística) utiliza conhecimento específico do problema para encontrar a solução. Pode ser mais eficiente que a busca cega, pois não visita todos os nodos.
- ▶ Usa uma função de avaliação, heurística:  $f(n) = h(n)$
- ▶ Heurística:
  - ▶ probabilidade ou suposição a respeito da resolução de um problema
  - ▶ regra para escolher aqueles ramos em um espaço de estado que têm maior probabilidade de levarem a uma solução aceitável.

{17}------------------------------------------------
### Algoritmos de Busca Informada

- ▶ Razões para usá-la:
  - ▶ O problema não tem uma solução exata por causa das ambiguidades na formalização do problema ou nos dados disponíveis. Ex: diagnóstico médico
  - ▶ O problema tem solução exata, mas o custo computacional é proibitivo. Ex: jogo de xadrez

{18}------------------------------------------------
### Algoritmos de Busca Informada

- ▶ Algoritmo A\*, IDA\*
- ▶ Hill Climbing
- ▶ Simulated Annealing
- ▶ Algoritmos Genéticos

A close-up, low-angle photograph of a complex wooden maze. The maze is constructed from dark wood blocks, creating a series of interconnected paths and dead ends. The perspective is from above, looking down into the maze, which recedes into the background. A solid red rectangular block is positioned in the upper right corner of the image.

{19}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1630bfd9ebf9b95faec11ae6cdfd9c0a_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up, low-angle photograph of a complex wooden maze.
<!-- /IMAGE_DESCRIPTION -->
### Atividade IV

- ▶ Para responder as questões abaixo, consulte o capítulo 3 do livro do Russel e Norvig.
- 1. Qual a diferença entre um algoritmo de busca em extensão de um algoritmo de custo uniforme ?
- 2. Qual a diferença entre um algoritmo de busca em profundidade de um algoritmo com busca limitada ou iterativa ? Todos podem alcançar a solução ótima ?
- 3. Como funciona uma busca bidirecional ? Ela é sempre aplicável ? O que é necessário para aplicá-la ?
- 4. Quem consome mais memória os algoritmos de busca em extensão ou em profundidade ?

{20}------------------------------------------------
### Atividade V

- Considerando que o estado final desejado seja os números ordenados, a partir da primeira célula, pense em funções heurísticas que poderiam ajudar a escolher o estado seguinte.

The diagram illustrates a state transition in a 3x3 grid puzzle. The initial state is a 3x3 grid with the following values:

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 | 8 | 5 |
| 6 |   | 2 |

Three arrows point from the initial state to three possible successor states, each represented by a 3x3 grid:

- Left successor state:

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 | 8 | 5 |
| 6 | 2 |   |
- Middle successor state:

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 | 8 | 5 |
|   | 6 | 2 |
- Right successor state:

|   |   |   |
|---|---|---|
| 1 | 3 | 4 |
| 7 |   | 5 |
| 6 | 8 | 2 |

Diagram showing a 3x3 grid state and its three possible successor states in a 3x3 grid puzzle.

<!-- IMAGE_DESCRIPTION: datalab-c5655e700cc3e9aac7e9f4f07f30264d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing a 3x3 grid state and its three possible successor states in a 3x3 grid puzzle.
<!-- /IMAGE_DESCRIPTION -->
