<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Aula 05 - Agentes e Algoritmos de Busca<sup>1</sup>**
  - Sinopse
  - Sumário
  - Relembrando...
  - Algoritmos de Busca Local por Refinamentos Sucessivos
- **População Intermediária**
- **População Intermediária**
  - Outros materiais
  - Leitura para prova

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Inteligência Artificial
## Aula 05 - Agentes e Algoritmos de Busca<sup>1</sup>

Sílvia M.W. Moraes

Escola Politécnica - PUCRS

A robotic hand interacting with colorful geometric shapes (cubes and a cylinder) on a table, illustrating the concept of object recognition and manipulation.

<sup>1</sup>Este material não pode ser reproduzido ou utilizado de forma parcial sem a permissão dos autores.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-390120de4fe440c42fea8154fcaad334_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A robotic hand interacting with colorful geometric shapes (cubes and a cylinder) on a table, illustrating the concept of object recognition and manipulation.
<!-- /IMAGE_DESCRIPTION -->
### Sinopse

- Nesta aula, introduzimos **algoritmos de busca por refinamentos sucessivos: Algoritmos Genéticos**.
- Este material foi construído com base nos livros de Russel & Norvig e Luger & Stubblefield.

{2}------------------------------------------------
### Sumário

- 1 O que vimos ...
- 2 Algoritmos de Busca Local por Refinamentos Sucessivos
- 3 Algoritmo Genético
- 4 Próxima Aula

{3}------------------------------------------------
### Relembrando...

- Agentes Reativos
- Agentes Deliberativos (Cognitivos)

A close-up photograph of a white robotic hand with multiple joints and sensors, positioned over a chessboard. The hand is in the process of moving a black chess piece (a knight) from one square to another. The chessboard has a red and white checkered pattern. The background is blurred, focusing attention on the robot and the chess pieces.

A robotic hand moving a chess piece.

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-d0baec9a9191662196c3f3be304ee01c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A robotic hand moving a chess piece.
<!-- /IMAGE_DESCRIPTION -->
### Algoritmos de Busca Local por Refinamentos Sucessivos

- Os algoritmos vistos até agora exploram sistematicamente espaços de busca mantendo na memória um ou mais caminhos que levam do estado inicial do problema até o estado objetivo.
- Para muitos problemas, o caminho até a solução é irrelevante.**
  - Exemplos:** Problema das 8 rainhas, projeto de circuitos integrados, layout de instalações industriais, escalonamento de jornadas de trabalho, roteamento de veículos, alocação de recursos, etc.

|   | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|
| 1 |   |   |   |   | Q |   |   |   |
| 2 |   |   | Q |   |   |   | Q |   |
| 3 |   | Q |   |   |   |   |   |   |
| 4 |   |   |   |   |   |   | Q |   |
| 5 |   | Q |   |   |   |   |   |   |
| 6 |   |   |   |   | Q |   |   |   |
| 7 | Q |   |   |   |   |   |   |   |
| 8 |   |   |   |   |   | Q |   |   |

An 8x8 chessboard illustrating a solution to the 8-Queens problem. The queens are placed on the following squares: (1, 5), (2, 3), (3, 1), (4, 8), (5, 6), (6, 2), (7, 7), and (8, 4). The board is labeled with columns 1-8 at the top and rows 1-8 on the left and right sides.

- Para esses problemas, usamos **algoritmos de busca local por refinamentos sucessivos**.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-446fd00eff6eb62c8d5eefa8a8aa3238_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** An 8x8 chessboard illustrating a solution to the 8-Queens problem.
<!-- /IMAGE_DESCRIPTION -->
#### Características

- Algoritmos de busca local por refinamentos sucessivos, em geral:
  - **partem de soluções propostas** e tentam melhorá-las.
  - **operam sobre um único estado corrente**, ao invés de vários caminhos.
  - **se movem** apenas para os **vizinhos** desse estado.
  - **não mantêm a árvore de pesquisa** (não consideram o caminho para solução), guardam apenas os estados e suas avaliações.
  - são úteis para resolver **problemas de otimização**.

{6}------------------------------------------------
#### Características

- Algoritmos de busca local por refinamentos sucessivos
  - Vantagens:
    - ocupam **pouca memória**
    - podem **encontrar soluções razoáveis em grandes ou infinitos espaços de estados**, para os quais os algoritmos sistemáticos são inadequados.

{7}------------------------------------------------
#### Espaço de Busca

- **Topologia** consiste em:
    - **estado** (posição)
    - elevação definida pelo **valor da função** heurística (mínimo global) ou função objetivo (máximo global).

Um gráfico de uma função objetivo (eixo Y) em função do espaço de estados (eixo X). A curva vermelha apresenta um "Máximo global" no primeiro pico e um "Máximo Local" no segundo pico. Há uma "planície" (região plana) no primeiro pico. Um "Máximo local plano" é indicado no segundo pico. Um ponto no eixo X é rotulado "Estado atual", com uma seta apontando para um ponto na curva imediatamente antes do segundo pico.

Gráfico de uma função objetivo com múltiplos máximos e um estado atual.

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-ecb25d766719ce041cf4cc390791a098_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico de uma função objetivo com múltiplos máximos e um estado atual.
<!-- /IMAGE_DESCRIPTION -->
#### Espaço de Busca

- **Máximo global:** pico mais alto
- **Máximo local:** picos mais altos que os vizinhos, mas menor que o global.
- **Platôs** - planícies e máximos locais planos:
  - planície: plano em que é possível progredir.
  - máximo local plano: plano em que não há saída.

O gráfico ilustra a função objetivo em relação ao espaço de estados. A curva vermelha representa a função objetivo, com o eixo vertical rotulado 'Função objetivo' e o eixo horizontal rotulado 'Espaço de estados'. A curva apresenta um pico mais alto rotulado 'Máximo global' e um pico menor rotulado 'Máximo Local'. Há também uma região plana rotulada 'planície' e uma região plana no topo de um pico rotulada 'Máximo local plano'. Um ponto na curva é rotulado 'Estado atual'.

Gráfico da Função objetivo versus Espaço de estados, mostrando máximos globais, locais, planícies e um estado atual.

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-925f55ce69802b9d3b00546382663ee2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da Função objetivo versus Espaço de estados, mostrando máximos globais, locais, planícies e um estado atual.
<!-- /IMAGE_DESCRIPTION -->
#### Alguns Algoritmos de Busca por Refinamentos Sucessivos

- **Algoritmos Genéticos:** algoritmos baseado na teoria da evolução de Darwin. Refina soluções candidatas ao longo de sua execução.
  - **Hill-climbing** (Subida da encosta): o algoritmo tenta realizar mudanças que podem melhorar o estado corrente.
  - **Simulated annealing** (Têmpera simulada): podem realizar mudanças que podem piorar o estado corrente, temporariamente.

Figure 1: A diagram of a potential energy landscape with three peaks labeled A, B, and C. Peak B is the highest. A red dashed line with arrows shows a reaction path starting from a pink sphere in a local minimum between A and B, going up to B, and then down to another minimum between B and C.

{10}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e9b30aeb317ed964fa6de36804acf24c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Figure 1: A diagram of a potential energy landscape with three peaks labeled A, B, and C.
<!-- /IMAGE_DESCRIPTION -->
#### Algoritmo Genético: Origem

- Algoritmos de busca por refinamento sucessivo partem de soluções propostas e tentam melhorá-las.
  - **Algoritmos Genéticos:**
    - Métodos de otimização e busca inspirados nos mecanismos de evolução de populações de seres vivos.
    - Foram introduzidos por John Holland (1975) e popularizados por um dos seus alunos, David Goldberg (1989).
    - Seguem o princípio da seleção natural e sobrevivência (Charles Darwin - livro “A Origem das Espécies”, 1859): “Quanto melhor um indivíduo se adaptar ao seu meio ambiente, maior será sua chance de sobreviver e gerar descendentes” .

{11}------------------------------------------------
#### Algoritmo Genético: Ciclo

- Ciclo de execução:

```
graph TD; Inicio[Inicio] --> Inicializacao[Inicialização da População]; Inicializacao --> CalculoAptidao[Cálculo da Aptidão]; CalculoAptidao --> Decisao{Solução encontrada?}; Decisao -- Sim --> Fim[Fim]; Decisao -- Não --> Selecao[Seleção]; Selecao --> Reproducao[Reprodução]; Reproducao --> Mutacao[Mutação]; Mutacao --> CalculoAptidao;
```

The flowchart illustrates the execution cycle of a Genetic Algorithm. It begins with 'Inicio' (Start), leading to 'Inicialização da População' (Population Initialization). This is followed by 'Cálculo da Aptidão' (Fitness Calculation). A decision diamond asks 'Solução encontrada?' (Solution found?). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Não' (No), the cycle continues through 'Seleção' (Selection), 'Reprodução' (Reproduction), and 'Mutação' (Mutation), before returning to 'Cálculo da Aptidão'.

Flowchart of the Genetic Algorithm cycle.

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-27b06ec9f42b5d727a2630f61a5f1861_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Genetic Algorithm cycle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-ff0952ef692c9d960ce5f6708bcc9711_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Genetic Algorithm execution cycle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4356776ca004ecba5d599667a155d7d4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Genetic Algorithm execution cycle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-79e1709a7317ead45379cbb8ff3ba802_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Genetic Algorithm execution cycle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-90ddb84c323b956e2d50a54d3f870566_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Genetic Algorithm execution cycle.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e05b36c0d46549e681ce6581422c66b2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Flowchart of the Genetic Algorithm execution cycle.
<!-- /IMAGE_DESCRIPTION -->
#### Algoritmo Genético

- Ciclo de execução:

```
graph TD; Inicio[Inicio] --> Inicializacao[Inicialização da População]; Inicializacao --> CalculoAptidao[Cálculo da Aptidão]; CalculoAptidao --> Decisao{Solução encontrada?}; Decisao -- Sim --> Fim[Fim]; Decisao -- Não --> Selecao[Seleção]; Selecao --> Reproducao[Reprodução]; Reproducao --> Mutacao[Mutação]; Mutacao --> CalculoAptidao;
```

The flowchart illustrates the execution cycle of a Genetic Algorithm. It begins with 'Inicio' (Start), leading to 'Inicialização da População' (Population Initialization), which is highlighted with a red border. From there, the process moves to 'Cálculo da Aptidão' (Fitness Calculation). A decision diamond asks 'Solução encontrada?' (Solution found?). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Não' (No), it proceeds to 'Seleção' (Selection), then 'Reprodução' (Reproduction), and finally 'Mutação' (Mutation). The 'Mutação' step loops back to 'Cálculo da Aptidão' to re-evaluate the fitness of the new population.

Flowchart of the Genetic Algorithm execution cycle.

{13}------------------------------------------------
#### Algoritmo Genético: Inicialização da população

- **População Inicial:** conjunto de soluções geradas aleatoriamente. Corresponde à população da geração 0 (ponto de partida do algoritmo).
  - cada elemento da população é chamado de indivíduo ou cromossomo.
    - um cromossomo é formado por genes – seqüências de DNA - que servem para determinar as características da solução.
    - os cromossomos podem ser codificados em binário (mais tradicional), inteiro, real, alfabeto específico, ...
  - tamanho da população (número de soluções) é um parâmetro do algoritmo.

{14}------------------------------------------------
#### Algoritmo Genético: Inicialização da população

- **Exemplo:** Retomando o **problema das 8 rainhas** ...
  - **Objetivo:** Dispor as oito rainhas em um tabuleiro sem que uma ataque a outra.
    - Uma rainha ataca outra se esta estiver na mesma linha, coluna ou diagonal.

The image contains two chessboard diagrams. The left diagram shows an 8x8 chessboard with a checkerboard pattern. It contains six red queen pieces and two white queen pieces. The red queens are located at (row, column): (1,1), (1,5), (2,3), (2,4), (3,2), (4,6), (5,4), (6,7), (7,8), and (8,8). The white queens are at (3,7) and (8,8). An arrow points from the left board to the right board. The right diagram shows an 8x8 chessboard with a checkerboard pattern, labeled with numbers 1 to 8 on both the top and left sides. It contains eight black queen pieces at the following positions: (1,4), (2,7), (3,3), (4,8), (5,2), (6,6), (7,1), and (8,5).

Two chessboard diagrams illustrating the 8-queens problem. The left board shows a partial solution with 6 red queens and 2 white queens. The right board shows a complete solution with 8 black queens.

{15}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0e240e8e4783e664047fbdb5fbd0989f_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two chessboard diagrams illustrating the 8-queens problem.
<!-- /IMAGE_DESCRIPTION -->
#### Algoritmo Genético: Inicialização da população

- **Passo 1:** Escolher a **codificação** mais indicada para o problema

- Binário: necessário 3 bits por rainha

coluna → 0 1 2 3 4 5 6 7  
 linha → 000 010 010 100 000 101 011 110

- Inteiro: valores de 0 a 7

|        |   |   |   |   |   |   |   |   |   |
|--------|---|---|---|---|---|---|---|---|---|
| coluna | → | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| linha  | → | 0 | 2 | 2 | 4 | 0 | 5 | 3 | 6 |

{16}------------------------------------------------
#### Algoritmo Genético: Inicialização da população

- **Passo 2:** Definir o tamanho da população (número de indivíduos) e gerá-la aleatoriamente.
  - recomenda-se que a população inicial contenha soluções distintas (uma diferente da outra).
  - Exemplo: **tamanho = 5**

|   | Cromossomos |   |   |   |   |   |   |   |
|---|-------------|---|---|---|---|---|---|---|
| 0 | 0           | 2 | 2 | 4 | 0 | 5 | 3 | 6 |
| 1 | 1           | 2 | 3 | 5 | 0 | 6 | 1 | 2 |
| 2 | 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
| 3 | 1           | 2 | 3 | 4 | 0 | 0 | 1 | 2 |
| 4 | 7           | 3 | 4 | 4 | 5 | 5 | 6 | 2 |

{17}------------------------------------------------
#### Algoritmo Genético: Cálculo da Aptidão

- Ciclo de execução:

```
graph TD; Inicio[Inicio] --> Inicializacao[Inicialização da População]; Inicializacao --> CalculoAptidao[Cálculo da Aptidão]; CalculoAptidao --> Decisao{Solução encontrada?}; Decisao -- Sim --> Fim[Fim]; Decisao -- Não --> Selecao[Seleção]; Selecao --> Reproducao[Reprodução]; Reproducao --> Mutacao[Mutação]; Mutacao --> CalculoAptidao;
```

The flowchart illustrates the execution cycle of a Genetic Algorithm. It begins with 'Inicio' (Start), leading to 'Inicialização da População' (Population Initialization). From there, it proceeds to 'Cálculo da Aptidão' (Fitness Calculation), which is highlighted with a red border. A decision diamond follows, asking 'Solução encontrada?' (Solution found?). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Não' (No), it continues to 'Seleção' (Selection), then 'Reprodução' (Reproduction), and 'Mutação' (Mutation), before looping back to 'Cálculo da Aptidão'.

Flowchart of the Genetic Algorithm execution cycle.

{18}------------------------------------------------
#### Algoritmo Genético: Cálculo da Aptidão

- **Passo 3:** Logo após a geração de uma população, verifica-se a aptidão dos cromossomos.
  - Aptidão: é determinada por uma função que diz o quanto os indivíduos são aptos. Ela mede a qualidade da solução.
    - Vamos usar a mesma função heurística  $h$ , usada nos exemplos anteriores, para calcular a aptidão
    - $h$ : corresponde ao número de pares de rainhas que estão atacando umas às outras, seja direta ou indiretamente.
    - objetivo é  $h = 0$ , logo, quanto menor o valor de  $h$  melhor (índivíduo mais apto).

{19}------------------------------------------------
#### Algoritmo Genético: Cálculo da Aptidão

- Cada um dos indivíduos da população é avaliado pela função de aptidão ( $h$ ).

|   | Cromossomos |   |   |   |   |   |   |   | $h$ |
|---|-------------|---|---|---|---|---|---|---|-----|
| 0 | 0           | 2 | 2 | 4 | 0 | 5 | 3 | 6 | 7   |
| 1 | 1           | 2 | 3 | 5 | 0 | 6 | 1 | 2 | 9   |
| 2 | 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 | 6   |
| 3 | 1           | 2 | 3 | 4 | 0 | 0 | 1 | 2 | 14  |
| 4 | 7           | 3 | 4 | 4 | 5 | 5 | 6 | 2 | 7   |

- Esse é o momento de analisarmos se o objetivo já foi alcançado.
  - Quando isso acontece, o algoritmo pára e apresenta o cromossomo que satisfaz o objetivo como solução final.
  - Caso contrário, inicia a seleção ...

{20}------------------------------------------------
#### Algoritmo Genético: Seleção

- Ciclo de execução:

```
graph TD; Inicio[Inicio] --> Inicializacao[Inicialização da População]; Inicializacao --> Calculo[Cálculo da Aptidão]; Calculo --> Decisao{Solução encontrada?}; Decisao -- Sim --> Fim[Fim]; Decisao -- Não --> Selecao[Seleção]; Selecao --> Reproducao[Reprodução]; Reproducao --> Mutacao[Mutação]; Mutacao --> Calculo;
```

The flowchart illustrates the execution cycle of a Genetic Algorithm. It begins with 'Inicio' (Start), leading to 'Inicialização da População' (Population Initialization). This is followed by 'Cálculo da Aptidão' (Fitness Calculation). A decision diamond asks 'Solução encontrada?' (Solution found?). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Não' (No), it proceeds to 'Seleção' (Selection), which is highlighted with a red border. This is followed by 'Reprodução' (Reproduction) and 'Mutação' (Mutation). The 'Mutação' step then loops back to the 'Cálculo da Aptidão' step, completing the cycle.

Flowchart of the Genetic Algorithm execution cycle.

{21}------------------------------------------------
#### Algoritmo Genético: Seleção

- A partir desse ponto, inicia o processo de construção da **população intermediária**, ou seja, a população da próxima geração.
  - A seleção é o operador genético que escolhe indivíduos da população atual que serão usados para gerar a próxima população.
  - Há vários tipos de **seleção**. Eis alguns:
    - Seleção por **elitismo**: consiste em passar o melhor indivíduo da população atual diretamente para a próxima.
    - Seleção por **torneio**: é usada para selecionar os indivíduos da população atual com fins de cruzamento.

{22}------------------------------------------------
##### Algoritmo Genético: Seleção por Elitismo

- **Passo 4:** Aplicação da seleção por elitismo.
  - É recomendada pois melhora o desempenho do algoritmo por preservar a melhor solução encontrada até o momento.

População Atual

|   | Cromossomos |   |   |   |   |   |   |   | $h$ |
|---|-------------|---|---|---|---|---|---|---|-----|
| 0 | 0           | 2 | 2 | 4 | 0 | 5 | 3 | 6 | 7   |
| 1 | 1           | 2 | 3 | 5 | 0 | 6 | 1 | 2 | 9   |
| 2 | 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 | 6   |
| 3 | 1           | 2 | 3 | 4 | 0 | 0 | 1 | 2 | 14  |
| 4 | 7           | 3 | 4 | 4 | 5 | 5 | 6 | 2 | 7   |

População Intermediária

| Cromossomos |   |   |   |   |   |   |   |
|-------------|---|---|---|---|---|---|---|
| 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
|             |   |   |   |   |   |   |   |
|             |   |   |   |   |   |   |   |
|             |   |   |   |   |   |   |   |
|             |   |   |   |   |   |   |   |

{23}------------------------------------------------
#### Algoritmo Genético: Seleção por Torneio

- **Passo 5:** Aplicação da seleção por torneio para selecionar os indivíduos que serão cruzados.
  - A **seleção por torneio** consiste em
    - escolher **randomicamente dois indivíduos** da população atual e escolher o **melhor para ser o pai**.
    - escolher **randomicamente** novamente **dois indivíduos** da população atual e escolher o **melhor para ser a mãe**.

{24}------------------------------------------------
#### Algoritmo Genético: Seleção por Torneio

| População Atual |   |   |   |   |   |   |   |   |     |
|-----------------|---|---|---|---|---|---|---|---|-----|
| Cromossomos     |   |   |   |   |   |   |   |   | $h$ |
| 0               | 0 | 2 | 2 | 4 | 0 | 5 | 3 | 6 | 7   |
| 1               | 1 | 2 | 3 | 5 | 0 | 6 | 1 | 2 | 9   |
| mãe             | 2 | 0 | 3 | 3 | 5 | 7 | 4 | 3 | 6   |
|                 | 3 | 1 | 2 | 3 | 4 | 0 | 0 | 1 | 2   |
| pai             | 4 | 7 | 3 | 4 | 4 | 5 | 5 | 6 | 2   |

- **Seleção por torneio:**
    - gera randomicamente: 1 e 4, escolhe **4 para ser o pai**
    - gera randomicamente: 3 e 2, escolhe o **2 para ser a mãe**
  - O passo seguinte é o cruzamento ...

{25}------------------------------------------------
#### Algoritmo Genético: Crossover

- Ciclo de execução:

```
graph TD; Inicio[Inicio] --> Inicializacao[Inicialização da População]; Inicializacao --> CalculoAptidao[Cálculo da Aptidão]; CalculoAptidao --> Decisao{Solução encontrada?}; Decisao -- Sim --> Fim[Fim]; Decisao -- Não --> Selecao[Seleção]; Selecao --> Reproducao[Reprodução]; Reproducao --> Mutacao[Mutação]; Mutacao --> CalculoAptidao;
```

The flowchart illustrates the execution cycle of a Genetic Algorithm. It begins with 'Inicio' (Start), leading to 'Inicialização da População' (Population Initialization). This is followed by 'Cálculo da Aptidão' (Fitness Calculation). A decision diamond asks 'Solução encontrada?' (Solution found?). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Não' (No), it proceeds to 'Seleção' (Selection), then 'Reprodução' (Reproduction), and finally 'Mutação' (Mutation). The 'Reprodução' step is highlighted with a red border. The flow then loops back from 'Mutação' to 'Cálculo da Aptidão'.

Flowchart of the Genetic Algorithm execution cycle.

{26}------------------------------------------------
#### Algoritmo Genético: Crossover

- **Passo 6:** Cruzamento dos indivíduos selecionados.
  - O operador genético **crossover** é responsável por
    - cruzar a carga genética dos indivíduos escolhidos pela seleção no passo anterior
    - gerar os indivíduos da próxima geração.
  - Há vários tipos de cruzamento:
    - **$n$ -ponto:** consiste em cortar os cromossomos em  $n$  pontos. Quando  $n = 1$ , é chamado de **uniponto**. Para diferentes valores de  $n$  é chamado de multiponto.
    - **uniforme:** aplica uma máscara binária que determina como os genes serão misturados para formar os filhos.

{27}------------------------------------------------
##### Algoritmo Genético: Crossover uniponto

- No cruzamento uniponto:
  - escolhe-se o ponto de corte aleatoriamente.
  - para formar o filho1, unimos o início da mãe com o final do pai.
  - para formar o filho2, unimos o início do pai com o final da mãe.

|     |   |   |   |   |   |   |   |   |   |
|-----|---|---|---|---|---|---|---|---|---|
| mãe | 2 | 0 | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
| pai | 4 | 7 | 3 | 4 | 4 | 5 | 5 | 6 | 2 |

|         |   |   |   |   |   |   |   |   |
|---------|---|---|---|---|---|---|---|---|
| Filho 1 | 0 | 3 | 3 | 4 | 5 | 5 | 6 | 2 |
| Filho 2 | 7 | 3 | 4 | 5 | 7 | 4 | 3 | 5 |

{28}------------------------------------------------
##### Algoritmo Genético: Crossover uniponto

- Os indivíduos gerados (filhos) são colocados na população intermediária.
- O processo de seleção e cruzamento (passos 4 e 5) devem ser repetidos até completar a população.
  - Observação: toda a população tem sempre a mesma quantidade de elementos.

População Intermediária

| Cromossomos |   |   |   |   |   |   |   |
|-------------|---|---|---|---|---|---|---|
| 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
| 0           | 3 | 3 | 4 | 5 | 5 | 6 | 2 |
| 7           | 3 | 4 | 5 | 7 | 4 | 3 | 5 |
|             |   |   |   |   |   |   |   |
|             |   |   |   |   |   |   |   |

{29}------------------------------------------------
##### Algoritmo Genético: Crossover multiponto

- Exemplo de cruzamento  $n$ -ponto, para  $n = 2$ .
  - Os pontos de corte são escolhidos aleatoriamente.
  - É mais interessante para cromossomos longos.

|     |   |   |   |   |   |   |   |   |   |
|-----|---|---|---|---|---|---|---|---|---|
| mãe | 2 | 0 | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
| pai | 4 | 7 | 3 | 4 | 4 | 5 | 5 | 6 | 2 |

|         |   |   |   |   |   |   |   |   |
|---------|---|---|---|---|---|---|---|---|
| Filho 1 | 0 | 3 | 4 | 4 | 5 | 5 | 3 | 5 |
| Filho 2 | 7 | 3 | 3 | 5 | 7 | 4 | 6 | 2 |

{30}------------------------------------------------
##### Algoritmo Genético: Crossover uniforme

- No cruzamento **uniforme**, é necessário inicialmente gerar uma máscara binária.
  - A máscara determina como os genes deve ser copiados para formar os filhos.
    - Filho1: contém os genes do pai cuja posição na máscara é 1 e os genes da mãe cuja posição na máscara é 0.
    - Filho2: o oposto.

|       |   |         |   |   |   |   |   |   |   |            |
|-------|---|---------|---|---|---|---|---|---|---|------------|
|       |   | máscara |   |   |   |   |   |   |   |            |
|       |   | 1       | 0 | 0 | 1 | 0 | 1 | 1 | 0 |            |
| 2     |   | 0       | 3 | 3 | 5 | 7 | 4 | 3 | 5 | mãe<br>pai |
| 4     |   | 7       | 3 | 4 | 4 | 5 | 5 | 6 | 2 |            |
| Filho | 1 | 7       | 3 | 3 | 4 | 7 | 5 | 6 | 5 |            |
| Filho | 2 | 0       | 3 | 4 | 5 | 5 | 4 | 3 | 2 |            |

{31}------------------------------------------------
#### Algoritmo Genético: mutação

- Ciclo de execução:

```
graph TD; Inicio[Inicio] --> Inicializacao[Inicialização da População]; Inicializacao --> CalculoAptidao[Cálculo da Aptidão]; CalculoAptidao --> Decisao{Solução encontrada?}; Decisao -- Sim --> Fim[Fim]; Decisao -- Não --> Selecao[Seleção]; Selecao --> Reproducao[Reprodução]; Reproducao --> Mutacao[Mutação]; Mutacao --> CalculoAptidao;
```

The flowchart illustrates the execution cycle of a Genetic Algorithm. It begins with 'Inicio' (Start), leading to 'Inicialização da População' (Population Initialization). This is followed by 'Cálculo da Aptidão' (Fitness Calculation). A decision diamond asks 'Solução encontrada?' (Solution found?). If 'Sim' (Yes), the process ends at 'Fim' (End). If 'Não' (No), it proceeds to 'Seleção' (Selection), then 'Reprodução' (Reproduction), and finally 'Mutação' (Mutation). The 'Mutação' step is highlighted with a red border. An arrow from 'Mutação' loops back to 'Cálculo da Aptidão', completing the cycle.

Flowchart of the Genetic Algorithm execution cycle.

{32}------------------------------------------------
#### Algoritmo Genético: mutação

- **Passo 7: Aplicação da operação de mutação**
  - O operador genético mutação consiste em uma mudança genética em cromossomos da população.
  - A taxa de mutação deve ser baixa.
    - Escolhe randomicamente um dos filhos recém gerados pelo cruzamento e um dos seus genes para mutar.
    - Substitui o gene escolhido por outro, também gerado aleatoriamente.

{33}------------------------------------------------
#### Algoritmo Genético: mutação
##### - Exemplo:

- Indivíduo escolhido aleatoriamente: 2
  - Gene escolhido aleatoriamente: 4 (posição)

Antes
## População Intermediária

|   | Cromossomos |   |   |   |   |   |   |   |
|---|-------------|---|---|---|---|---|---|---|
| 0 | 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
| 1 | 0           | 3 | 3 | 4 | 5 | 5 | 6 | 2 |
| 2 | 7           | 3 | 4 | 5 | 7 | 4 | 3 | 5 |
| 3 |             |   |   |   |   |   |   |   |
| 4 |             |   |   |   |   |   |   |   |

Depois
## População Intermediária

| Cromossomos |   |   |   |   |   |   |   |
|-------------|---|---|---|---|---|---|---|
| 0           | 3 | 3 | 5 | 7 | 4 | 3 | 5 |
| 0           | 3 | 3 | 4 | 5 | 5 | 6 | 2 |
| 7           | 3 | 4 | 5 | 0 | 4 | 3 | 5 |
|             |   |   |   |   |   |   |   |
|             |   |   |   |   |   |   |   |

{34}------------------------------------------------
#### Algoritmo Genético

- Uma vez preenchida a população intermediária,
  - ela se transforma na população atual (geração+1) e
  - o ciclo reinicia no passo 3.
- **Critérios de parada**
  - solução ótima
  - número de gerações
  - convergência: 98 a 99% dos indivíduos representam a mesma solução.

{35}------------------------------------------------
#### Algoritmo Genético: exercícios

- **Atividade I:** Um projeto possui **10 tarefas** que precisam ser distribuídas entre 2 pessoas da equipe. Para cada tarefa foi estimado o número de horas necessário para concluí-la.
  - 1 Como poderíamos realizar a distribuição de tarefas entre as duas pessoas de forma harmônica ?
    - Para responder à questão, considere as tarefas e sua carga (em horas);

|    |    |    |    |    |    |    |    |    |     |
|----|----|----|----|----|----|----|----|----|-----|
| t1 | t2 | t3 | t4 | t5 | t6 | t7 | t8 | t9 | t10 |
| 5  | 10 | 15 | 3  | 10 | 5  | 2  | 16 | 9  | 7   |
  - 2 Como poderíamos codificar as soluções ?
  - 3 Qual seria a função de aptidão mais apropriada ?

{36}------------------------------------------------
#### Algoritmo Genético: exercícios

- **Atividade II:** O problema das rotas entre 6 cidades apresentado nas aulas anteriores poderia ser resolvido usando algoritmos genéticos ?
  - Como poderíamos codificar as soluções ?
  - Qual seria a função de aptidão mais apropriada ?

{37}------------------------------------------------
### Outros materiais

- <http://www.obitko.com/tutorials/genetic-algorithms/portuguese/index.php>
- [http://pt.wikipedia.org/wiki/Algoritmo\\_gen%C3%A9tico](http://pt.wikipedia.org/wiki/Algoritmo_gen%C3%A9tico)
- <http://iaufes20092.pbworks.com/w/page/8625598/AG%20-%20Quadro%20Cognitivo%207>
- [http://rednuht.org/genetic\\_cars\\_2/](http://rednuht.org/genetic_cars_2/)
- <https://www.youtube.com/watch?v=Hp6bhARBGc4>
- <https://www.youtube.com/watch?v=xclBoPuNliw>
- <https://www.youtube.com/watch?v=eZ14la6zttM>

{38}------------------------------------------------
### Leitura para prova

- RUSSELL, S. J. & Norvig, P. Artificial Intelligence – a Modern Approach
  - Capítulos 1, 2, 3 e 4
