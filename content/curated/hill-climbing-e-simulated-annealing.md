<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Aula 06- Solução de Problemas (Busca com Informação - Algoritmos por Refinamentos Sucessivos)<sup>1</sup>**
  - Sinopse
  - Sumário
  - Aulas anteriores

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Inteligência Artificial
## Aula 06- Solução de Problemas (Busca com Informação - Algoritmos por Refinamentos Sucessivos)<sup>1</sup>

Sílvia M.W. Moraes

Escola Politécnica - PUCRS

A photograph of a modern, multi-story building, likely the Escola Politécnica da PUCRS, with a clear blue sky and some trees in the foreground.

<sup>1</sup>Este material não pode ser reproduzido ou utilizado de forma parcial sem a permissão dos autores.

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-0538daaa5583c23e17db3a12f2281a55_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A photograph of a modern, multi-story building, likely the Escola Politécnica da PUCRS, with a clear blue sky and some trees in the foreground.
<!-- /IMAGE_DESCRIPTION -->
### Sinopse

- Nesta aula, apresentamos uma **introdução a solução de problemas por algoritmos de busca local por refinamentos sucessivos**.
- Este material foi construído com base nos capítulos:
  - 4 do livro Artificial Intelligence – a Modern Approach de Russel & Norvig
  - 4 do livro Inteligência Artificial de Luger.

{2}------------------------------------------------
### Sumário

- 1 O que vimos ...
- 2 Algoritmos de Busca Local por Refinamentos Sucessivos

{3}------------------------------------------------
### Aulas anteriores

- Agente
  - Reativos
  - Cognitivos
- Solução de Problemas
  - Representação, Espaço de Estados
  - Algoritmos de Busca:
    - A\*
    - AG

{4}------------------------------------------------
#### Algoritmos de Busca Local por Refinamentos Sucessivos

- Os algoritmos vistos até agora exploram sistematicamente espaços de busca mantendo na memória um ou mais caminhos que levam do estado inicial do problema até o estado objetivo.
- Para muitos problemas, o caminho até a solução é irrelevante.**
  - Exemplos:** Problema das 8 rainhas, projeto de circuitos integrados, layout de instalações industriais, escalonamento de jornadas de trabalho, roteamento de veículos, alocação de recursos, etc.

An 8x8 chessboard illustrating the 8-Queens problem. The board has columns and rows numbered 1 to 8. Eight queens are placed on the board such that no two queens share the same row or column. The queens are located at (4,1), (3,2), (5,3), (7,4), (1,5), (8,6), (6,7), and (2,8).

- Para esses problemas, usamos **algoritmos de busca local por refinamentos sucessivos**.

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-8e065eabc40a3645a569db7e9cd0da32_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** An 8x8 chessboard illustrating the 8-Queens problem.
<!-- /IMAGE_DESCRIPTION -->
##### Características

- Algoritmos de busca local por refinamentos sucessivos, em geral:
  - **partem de soluções propostas** e tentam melhorá-las.
  - **operam sobre um único estado corrente**, ao invés de vários caminhos.
  - **se movem** apenas para os **vizinhos** desse estado.
  - **não mantêm a árvore de pesquisa** (não consideram o caminho para solução), guardam apenas os estados e suas avaliações.
  - são úteis para resolver **problemas de otimização**.

{6}------------------------------------------------
##### Características

- Algoritmos de busca local por refinamentos sucessivos
  - Vantagens:
    - ocupam **pouca memória**
    - podem **encontrar soluções razoáveis em grandes ou infinitos espaços de estados**, para os quais os algoritmos sistemáticos são inadequados.

{7}------------------------------------------------
#### Alguns Algoritmos de Busca por Refinamentos Sucessivos

- **Algoritmo Genético:** já vimos.
- **Hill-climbing** (Subida da encosta): o algoritmo tenta realizar mudanças que podem melhorar o estado corrente.
- **Simulated annealing** (Têmpera simulada): podem realizar mudanças que podem piorar o estado corrente, temporariamente.

Diagram illustrating the Simulated Annealing algorithm. A gray mountain landscape with three peaks labeled A, B, and C. A red dot at the bottom of the valley between A and B represents the current state. A red dashed line with arrows shows a path climbing up to peak B, representing a move that improves the state. A black dashed line with arrows shows a path that would descend from the valley to a lower point, representing a move that temporarily worsens the state, which is allowed in simulated annealing.

{8}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-e0ebcd8fdcfd34b12de3601b59505fdd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram illustrating the Simulated Annealing algorithm.
<!-- /IMAGE_DESCRIPTION -->
##### Algoritmo Hill-Climbing

- **Hill-climbing** também chamado de subida da encosta, busca gulosa local ou ainda gradiente descente (função heurística).  
O algoritmo
  - consiste em um laço que continuamente move-se na direção de um valor melhor (encosta acima).
  - termina quando encontra um pico em que nenhum vizinho tem um valor mais alto.
  - não precisa manter a árvore de pesquisa, guarda apenas o estado atual e o valor da sua função objetivo (ou heurística).
  - examina apenas os estados vizinhos imediatos ao estado atual.

{9}------------------------------------------------
##### Algoritmo Hill-Climbing

```
função SUBIDA-DE-ENCOSTA() retorna um estado-solução{  
    entrada: umProblema  
    variáveis locais: nóAtual, nóVizinho  
  
    nóAtual = CRIAR-NÓ(ESTADO-INICIAL(umProblema))  
    repetir{  
        nóVizinho = um sucessor do nóAtual com melhor avaliação  
        se valor(nóVizinho) < valor(nóAtual)  
            então nóAtual = nóVizinho  
        senão retornar ESTADO(nóAtual)  
    }  
}
```

{10}------------------------------------------------
##### Algoritmo Hill-Climbing

- Precisa de uma **função heurística** para avaliar as soluções.
- O nó criado inicialmente corresponde à uma **solução gerada aleatoriamente**.
- Precisa de uma função **sucessor** que gera uma solução próxima à atual: introduz uma “perturbação” (modificação) na solução atual, gerando outra solução.
- O algoritmo executa enquanto houver uma mudança significativa.

{11}------------------------------------------------
##### Algoritmo Hill-Climbing

- Exemplo - Problema das 4 rainhas
  - Vizinhos ao estado atual

The diagram illustrates the current state and its neighbors for the 4-queens problem. The current state is a 4x4 grid with queens in the first row (R R R R), labeled with  $h=12$ . It has 12 neighbors, each with a different heuristic value ( $h$ ).

| Neighbor | Grid                                                                                                                                                                                                    | $h$ |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|---|---|---|---|---|--|---|---|--|--|--|---|--|--|--|----|
| 1        | <table><tr><td></td><td>R</td><td>R</td><td>R</td></tr><tr><td>R</td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table> |     | R | R | R | R |   |  |   |   |  |  |  |   |  |  |  | 8  |
|          | R                                                                                                                                                                                                       | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| R        |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 2        | <table><tr><td></td><td>R</td><td>R</td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td>R</td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table> |     | R | R | R |   |   |  |   | R |  |  |  |   |  |  |  | 8  |
|          | R                                                                                                                                                                                                       | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| R        |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 3        | <table><tr><td></td><td>R</td><td>R</td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td>R</td><td></td><td></td><td></td></tr></table> |     | R | R | R |   |   |  |   |   |  |  |  | R |  |  |  | 8  |
|          | R                                                                                                                                                                                                       | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| R        |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 4        | <table><tr><td>R</td><td></td><td>R</td><td>R</td></tr><tr><td></td><td>R</td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table> | R   |   | R | R |   | R |  |   |   |  |  |  |   |  |  |  | 10 |
| R        |                                                                                                                                                                                                         | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          | R                                                                                                                                                                                                       |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 5        | <table><tr><td>R</td><td></td><td>R</td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   |   | R | R |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        |                                                                                                                                                                                                         | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 6        | <table><tr><td>R</td><td></td><td>R</td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   |   | R | R |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        |                                                                                                                                                                                                         | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 7        | <table><tr><td>R</td><td></td><td>R</td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   |   | R | R |   |   |  |   |   |  |  |  |   |  |  |  | 6  |
| R        |                                                                                                                                                                                                         | R   | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 8        | <table><tr><td>R</td><td>R</td><td></td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R |   | R |   |   |  |   |   |  |  |  |   |  |  |  | 10 |
| R        | R                                                                                                                                                                                                       |     | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 9        | <table><tr><td>R</td><td>R</td><td></td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R |   | R |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        | R                                                                                                                                                                                                       |     | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 10       | <table><tr><td>R</td><td>R</td><td></td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R |   | R |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        | R                                                                                                                                                                                                       |     | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 11       | <table><tr><td>R</td><td>R</td><td></td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R |   | R |   |   |  |   |   |  |  |  |   |  |  |  | 6  |
| R        | R                                                                                                                                                                                                       |     | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 12       | <table><tr><td>R</td><td>R</td><td>R</td><td></td></tr><tr><td></td><td></td><td></td><td>R</td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table> | R   | R | R |   |   |   |  | R |   |  |  |  |   |  |  |  | 8  |
| R        | R                                                                                                                                                                                                       | R   |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     | R |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 13       | <table><tr><td>R</td><td>R</td><td>R</td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R | R |   |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        | R                                                                                                                                                                                                       | R   |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 14       | <table><tr><td>R</td><td>R</td><td>R</td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R | R |   |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        | R                                                                                                                                                                                                       | R   |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
| 15       | <table><tr><td>R</td><td>R</td><td>R</td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></table>  | R   | R | R |   |   |   |  |   |   |  |  |  |   |  |  |  | 8  |
| R        | R                                                                                                                                                                                                       | R   |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |
|          |                                                                                                                                                                                                         |     |   |   |   |   |   |  |   |   |  |  |  |   |  |  |  |    |

Diagram showing the current state and its neighbors for the 4-queens problem using Hill-Climbing. The current state is a 4x4 grid with queens in the first row. It has 12 neighbors, each with a different heuristic value (h).

{12}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-27b06ec9f42b5d727a2630f61a5f1861_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram showing the current state and its neighbors for the 4-queens problem using Hill-Climbing.
<!-- /IMAGE_DESCRIPTION -->
##### Algoritmo Hill-Climbing

- **Exemplo** - Problema das 8 rainhas
  - Versão 1 : implementação tradicional do algoritmo (sucessor melhor em amplitude, variando a linha de uma rainha)

Hill-Climbing Simple

Dimensão: 8

Ciclo: 1 - h=17      Ciclo: 2 - h=12      Ciclo: 3 - h=7

```

- - - - -
- - - - -
- - - - -
- - * - -
* - - * - -
- * - - * -
- * - - * -
- - - - -
  
```

Ciclo: 4 - h=3

Ciclo: 5 - h=2

Ciclo: 6 - h=1

```

- * - - -
- - - * -
- - - - *
- - * - -
* - - - -
- - - * -
- - * - -
- - - - *
  
```

{13}------------------------------------------------

{14}------------------------------------------------
##### Algoritmo Hill-Climbing

- **Exemplo** - Problema das  $n$  rainhas
  - Teste do algoritmo Versão 2 com quantidades diferentes de rainhas

| #rainhas | hInicial | hFinal | #ciclos |
|----------|----------|--------|---------|
| 20       | 22       | 2      | 3       |
| 50       | 64       | 2      | 4       |
| 100      | 116      | 2      | 4       |
| 200      | 215      | 2      | 4       |

{15}------------------------------------------------
##### Algoritmo Hill-Climbing

- **Variantes do algoritmo:**
  - **Subida da Encosta Estocástica:** escolhe ao acaso entre os movimentos possíveis de encosta acima.
    - A probabilidade de seleção pode variar com a declividade do movimento.
    - Em geral converge mais lentamente que a subida mais íngreme (algoritmo usual).
  - **Subida da Encosta pela primeira escolha:** gera sucessores ao acaso até ser gerado um sucessor melhor que o estado atual.
    - Boa estratégia, quando há muitos sucessores (ex: milhares).

{16}------------------------------------------------
##### Algoritmo Hill-Climbing

- **Variantes do algoritmo (continuação):**
  - **Subida da Encosta com reinício aleatório:** Consiste em várias buscas (executa várias vezes o algoritmo) a partir de estados iniciais gerados ao acaso, parando quando encontrar o objetivo.
    - Diferente das versões anteriores encontra o objetivo (as anteriores podem ficar presas em máximos locais).
- De uma maneira geral, **o sucesso do algoritmo depende da topologia do espaço de estados.**

{17}------------------------------------------------
##### Algoritmo Hill-Climbing

- **Exemplo** - Problema das  $n$  rainhas
  - Teste do algoritmo com reinício aleatório com quantidades diferentes de rainhas

| #rainhas | hFinal | #execuções |
|----------|--------|------------|
| 8        | 0      | 7          |
| 20       | 0      | 20         |
| 50       | 0      | 28         |

{18}------------------------------------------------
##### Algoritmo Simulated Annealing

- Este algoritmo de busca local por refinamentos sucessivos é da década de 80 e é conhecido também como **Têmpera Simulada**.
  - **Inspiração:**
    - Têmpera: processo usado para temperar ou endurecer metais e vidros, aquecendo-os a altas temperaturas e depois resfriando-os gradualmente.
  - **A ideia é combinar o algoritmo subida da encosta com um percurso aleatório que temporariamente pode piorar a solução**, mas que, ao longo da execução, pode encontrar um máximo global.
    - Tenta resolver o problema do Algoritmo Hill Climbing: máximos locais.

{19}------------------------------------------------
##### Algoritmo Simulated Annealing

- Implementa um laço de repetição semelhante ao do algoritmo Hill Climbing.
- Diferente do algoritmo Hill Climbing, **escolhe movimento (estado vizinho) sucessor de forma aleatória.**
  - Se o estado vizinho for melhor, será aceito
  - Se o estado vizinho não for melhor, será aceito em menos de 1% dos casos
    - Essa probabilidade diminuirá exponencialmente à medida que os estados piorarem.
    - A probabilidade também diminui à medida que a “temperatura” se reduz (movimentos ruins têm mais chances de serem aceitos no início da execução).

{20}------------------------------------------------
##### Algoritmo Simulated Annealing

```
função TEMPERA-SIMULADA() retorna um estado-solução{  
    entrada: umProblema  
    escalonamento: mapeamento de tempo para “temperatura”  
    variáveis locais: nóAtual, nóProximo, T (temperatura atual)  
  
    nóAtual = CRIAR-NÓ(ESTADO-INICIAL(umProblema))  
    para  $t = 1$  até  $\infty$ {  
        T = escalonamento(t)  
        se T=0 então retornar ESTADO(nóAtual)  
        nóProximo = um sucessor do nóAtual (estado atual) gerado ao acaso  
         $\Delta E = \text{valor}(\text{nóPróximo}) - \text{valor}(\text{nóAtual})$   
        se  $\Delta E < 0$  então nóAtual = nóPróximo  
        senão se probabilidade  $e^{-\Delta E/T} > 0$   
            então nóAtual = nóPróximo  
    }  
}
```

{21}------------------------------------------------
##### Algoritmo Simulated Annealing

- $\Delta E$ : é chamado de variação de energia
- Para calcular a probabilidade pode-se a distribuição de Boltzmann-Gibbs, ou seja,  $P(\Delta E) = \exp(-\Delta E/T)$ . Relaciona energia à temperatura de moléculas.

Chances de Aceitação da Solução

Distribuição de Boltzmann-Gibbs

O gráfico ilustra a probabilidade de aceitação de uma solução durante o processo de Simulated Annealing. O eixo horizontal representa a Temperatura, variando de 0 a 100. O eixo vertical representa a Aceitação, variando de 0 a 1.2. A curva começa em (0,0), sobe rapidamente, atingindo aproximadamente 0.85 em T=5, 0.92 em T=10, e estabiliza-se próximo a 1.0 para temperaturas superiores a 20. Isso indica que, à medida que a temperatura diminui, a probabilidade de aceitar uma solução pior (com maior energia) também diminui, convergindo para 1.0 quando a temperatura é alta o suficiente.

| Temperatura | Aceitação |
|-------------|-----------|
| 0           | 0.00      |
| 5           | 0.85      |
| 10          | 0.92      |
| 20          | 0.97      |
| 30          | 0.98      |
| 40          | 0.99      |
| 50          | 0.995     |
| 60          | 1.00      |
| 70          | 1.00      |
| 80          | 1.00      |
| 90          | 1.00      |
| 100         | 1.00      |

Gráfico da Distribuição de Boltzmann-Gibbs mostrando a probabilidade de aceitação de uma solução em função da temperatura.

{22}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c4c8cd9c58f395c25a2a2b217ca7c2fb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Gráfico da Distribuição de Boltzmann-Gibbs mostrando a probabilidade de aceitação de uma solução em função da temperatura.
<!-- /IMAGE_DESCRIPTION -->
##### Algoritmo Simulated Annealing

- Em altas temperaturas, cada estado tem (praticamente) a mesma chance de ser o estado corrente;
- Em baixas temperaturas, somente estados com baixa energia têm alta probabilidade de se tornar o estado corrente;
- O método termina quando
  - nenhuma melhora significativa é alcançada,
  - um número fixo de iterações foi efetuado, ou
  - a temperatura  $T$  atingiu seu valor mínimo.
- O parâmetro  $T$  é iniciado com um valor elevado e é lentamente reduzido durante o processo de busca.
  - Geralmente, implementa-se um decrescimento geométrico para  $T$ , tal como  $T = k \times T$ .  $k$  tipicamente pertence a  $[0;1]$ .

{23}------------------------------------------------
##### Algoritmo Simulated Annealing

- **Exemplo** - Retomando o problema das  $n$  rainhas
  - $T_0 = 100$
  - $T = k \times T$ , onde  $k = 0.8$
  - Critérios de parada:
    - 50.000 iterações
    - ausência de melhora

| #rainhas | #iteraões |
|----------|------------|
| 4        | 4          |
| 6        | 901        |
| 8        | 108        |
| 10       | 1462       |
| 20       | 4271       |
| 40       | 9166       |

{24}------------------------------------------------
##### Algoritmo Simulated Annealing
##### - 6 Rainhas:

- Ciclo: 1- Temperatura: 100.0 -  $h=4$
- Ciclo: 2- Temperatura: 80.0 -  $h=4$
- Ciclo: 3- Temperatura: 64.0 -  $h=6$
- Ciclo: 4- Temperatura: 51.2 -  $h=6$
- Ciclo: 5- Temperatura: 40.96000000000001 -  $h=4$
- Ciclo: 6- Temperatura: 32.76800000000001 -  $h=5$
- ...
- Ciclo: 10- Temperatura: 13.421772800000006 -  $h=5$
- Ciclo: 11- Temperatura: 10.737418240000006 -  $h=6$
- Ciclo: 12- Temperatura: 8.589934592000004 -  $h=6$
- Ciclo: 13- Temperatura: 6.871947673600004 -  $h=9$
- ...
- ...
- Ciclo: 20- Temperatura: 1.4411518807585602 -  $h=5$
- Ciclo: 21- Temperatura: 1.1529215046068482 -  $h=4$
- Ciclo: 22- Temperatura: 0.9223372036854786 -  $h=3$
- Ciclo: 23- Temperatura: 0.7378697629483829 -  $h=2$
- ...
- Ciclo: 67- Temperatura: 4.0173451106474905E-5 -  $h=1$
- ...
- Ciclo: 901- Temperatura: 6.039323489882099E-86 -  $h=0$
