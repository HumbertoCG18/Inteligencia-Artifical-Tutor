<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Operações Genéticas**
  - Crossover OBX
  - Crossover OBX
  - Crossover OBX
  - Crossover PBX
  - Crossover PBX
  - Crossover PBX
  - Crossover PMX
  - Crossover PMX
  - Crossover PMX
  - Crossover PMX
  - Crossover CX
  - Crossover CX
  - Crossover CX
  - Crossover CX
  - Crossover CX
- **Mutação**

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Decorative pink barAbstract background with colorful ribbons forming a braid on the right side of the slide.Crossover & Mutação ---

Prof. Silvia

PUCRS – Escola Politécnica

{1}------------------------------------------------

## Operações Genéticas

- Operadores baseados em permutações
  - Crossover OBX
  - Crossover PBX
  - Crossover PMX
  - Crossover CX
  - Mutação

{2}------------------------------------------------

### Crossover OBX

- Order based Crossover (OBX)
  - Este crossover impõe a **ordem** durante a mistura das cargas genéticas.
- Dado 2 cromossomos selecionados para cruzamento
  - Posições:        0   **1**   2   **3**   **4**   5   6
  - Cromossomo 1: A   **B**   C   **D**   **F**   E   G
  - Cromossomo 2: C   **E**   G   **A**   **D**   F   B
- Selecione aleatoriamente ***n*** posições
  - A chance de cada posição ser selecionada é de 50%.
  - Suponha que as posições em vermelho foram selecionadas.

{3}------------------------------------------------

### Crossover OBX

#### - Continuando ...

- Posições:        0   1   2   3   4   5   6
- Cromossomo1: A   B   C   D   F   E   G
- Cromossomo2: C   E   G   A   D   F   B

#### - A seguir, copie as posições não selecionadas respeitando a disposição original:

- Posições:        0   1   2   3   4   5   6
- Filho 1        : A        C        E   G
- Filho 2        : C        G        F   B

{4}------------------------------------------------

### Crossover OBX

#### - Continuando ...

- Posições:        0   1   2   3   4   5   6
- Cromossomo 1: A   B   C   D   F   E   G
- Cromossomo 2: C   E   G   A   D   F   B

- Agora, para filho 1, insira os elementos das posições seleccionadas B-D-F, na ordem que ocorrem no cromossomo2: D – F – B.

- Faça o mesmo para o filho2, copie E-A-D na ordem que ocorrem no cromossomo 1: A – D – E.

- Posições:        0   1   2   3   4   5   6
- Filho 1        : A   D   C   F   B   E   G
- Filho 2        : C   A   G   D   E   F   B

{5}------------------------------------------------

### Crossover PBX

- Position based Crossover (PBX)
  - Este crossover impõe a **posição** durante a mistura das cargas genéticas.
- Dado 2 cromossomos selecionados para cruzamento
  - Posições:        0   1   2   3   4   5   6
  - Cromossomo 1: A   B   C   D   F   E   G
  - Cromossomo 2: C   E   G   A   D   F   B
- Da mesma forma, selecione aleatoriamente  $n$  posições
  - A chance de cada posição ser selecionada é de 50%.
  - Suponha que as posições em vermelho foram selecionadas.

{6}------------------------------------------------

### Crossover PBX

#### - Continuando ...

- Posições:        0   1   2   3   4   5   6
- Cromossomo 1: A   B   C   D   F   E   G
- Cromossomo 2: C   E   G   A   D   F   B

#### - A seguir, copie o conteúdo das posições selecionadas do cromossomo1 para filho2 e do cromossomo2 para o filho 1:

- Posições:        0   1   2   3   4   5   6
- Filho 1        :    E        A   D
- Filho 2        :    B        D   F

{7}------------------------------------------------

### Crossover PBX

#### - Continuando ...

- Posições:           0   1   2   3   4   5   6
- Cromossomo 1: A   B   C   D   F   E   G
- Cromossomo 2: C   E   G   A   D   F   B

- A seguir, copie os demais elementos para as posições vagas na ordem que aparecem nos cromossomos-pais. Cuide para não repetir. Como E-A-D já estão em filho1, faltam B-C-F-G. No caso do filho 2, faltam C-E-G-A.

- Posições:           0   1   2   3   4   5   6
- Filho 1           : B   E   C   A   D   F   G
- Filho 2           : C   B   E   D   F   G   A

{8}------------------------------------------------

### Crossover PMX

- Partially Matched Crossover (PMX)
  - Este crossover a mistura das cargas genéticas a partir de pontos de corte.
- Dado 2 cromossomos selecionados para cruzamento
  - Posições:           0   1   2   3   4   5   6
  - Cromossomo 1: A   B   C   D   F   E   G
  - Cromossomo 2: C   E   G   A   D   F   B
- Dois pontos de corte são definidos aleatoriamente, definindo uma sublista.

{9}------------------------------------------------

### Crossover PMX

- Continuando...

|                 |   |   |   |   |   |   |   |
|-----------------|---|---|---|---|---|---|---|
| • Posições:     | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| • Cromossomo 1: | A | B | C | D | F | E | G |
| • Cromossomo 2: | C | E | G | A | D | F | B |

- Os elementos da sublista começam a ser trocados, um a um.

|                 |   |   |   |   |   |   |   |
|-----------------|---|---|---|---|---|---|---|
| • Posições:     | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| • Filho 1.....: | A | B | G | D | F | E | C |
| • Filho 2.....: | G | E | C | A | D | F | B |

{10}------------------------------------------------

### Crossover PMX

- Continuando...

|                 |   |   |   |   |   |   |   |
|-----------------|---|---|---|---|---|---|---|
| • Posições:     | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| • Cromossomo 1: | A | B | G | D | F | E | C |
| • Cromossomo 2: | G | E | C | A | D | F | B |

- Os elementos da sublista começam a ser trocados, um a um.

|                 |   |   |   |   |   |   |   |
|-----------------|---|---|---|---|---|---|---|
| • Posições:     | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| • Filho 1 ..... | D | B | G | A | F | E | C |
| • Filho 2 ..... | G | E | C | D | A | F | B |

{11}------------------------------------------------

### Crossover PMX

- Continuando...

|                 |   |   |   |   |   |   |   |
|-----------------|---|---|---|---|---|---|---|
| • Posições:     | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| • Cromossomo 1: | D | B | G | A | F | E | C |
| • Cromossomo 2: | G | E | C | D | A | F | B |

- Os elementos da sublista começam a ser trocados, um a um.

|                 |   |   |   |   |   |   |   |
|-----------------|---|---|---|---|---|---|---|
| • Posições:     | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| • Filho 1 ..... | D | B | G | F | A | E | C |
| • Filho 2 ..... | G | E | C | D | F | A | B |

{12}------------------------------------------------

### Crossover CX

- Cycle Crossover (CX)
  - Este crossover a mistura das cargas genéticas copiando elemento a elemento, estabelecendo um ciclo.
- Dado 2 cromossomos selecionados para cruzamento
  - Posições:        0   1   2   3   4   5   6
  - Cromossomo 1: A   B   C   D   F   E   G
  - Cromossomo 2: C   E   G   A   D   F   B
- Pode iniciar a cópia a partir de qualquer cromossomo.

{13}------------------------------------------------

### Crossover CX

#### - Continuando...

- Posições:           0   1   2   3   4   5   6
- Cromossomo 1: A   B   C   D   F   E   G
- Cromossomo 2: C   E   G   B   D   F   A

#### - Iniciando a cópia a partir do cromossomo1 para gerar o filho1. Para evitar duplicação, copia C (do cromossomo2) pois está na mesma posição de A (cromossomo 1).

- Posições:           0   1   2   3   4   5   6
- Filho 1.....: A           C
- Filho 2.....: C

{14}------------------------------------------------

### Crossover CX

#### - Continuando...

- Posições:           0   1   2   3   4   5   6
- Cromossomo 1: **A**   B   **C**   D   F   E   **G**
- Cromossomo 2: **C**   E   **G**   B   D   F   A

#### - Da mesma forma, copia G pois está na mesma posição de C (cromossomo 2).

- Posições:           0   1   2   3   4   5   6
- Filho 1.....: **A**           C                   G
- Filho 1.....: **C**           **G**

{15}------------------------------------------------

### Crossover CX

#### - Continuando...

- Posições:           0   1   2   3   4   5   6
- Cromossomo 1: A   B   C   D   F   E   G
- Cromossomo 2: C   E   G   B   D   F   A

#### - Termina, pois ao tentar copiar A (mesma posição de G), verifica que A já foi copiado.

- Posições:           0   1   2   3   4   5   6
- Filho 1.....: A           C                   G
- Filho 2.....: C           G                   A

{16}------------------------------------------------

### Crossover CX

#### - Continuando...

- Posições:           0   1   2   3   4   5   6
- Cromossomo 1: **A**   B   **C**   D   F   E   **G**
- Cromossomo 2: **C**   E   **G**   B   D   F   **A**

#### - A seguir, efetua uma cópia simples entre os demais elementos.

- Posições:           0   1   2   3   4   5   6
- Filho 1.....: A   **E**   C   **B**   **D**   **F**   G
- Filho 2.....: C   **B**   G   **D**   **F**   **E**   A

{17}------------------------------------------------

## Mutação

- Pode ser uma permutação simples.
  - Escolher 2 (ou mais) posições aleatoriamente
  - Trocar seus conteúdos.
    - Posições: 0 1 2 3 4 5 6
    - Cromossomo 1: A B C D F E G
  - Após a mutação:
    - Posições: 0 1 2 3 4 5 6
    - Cromossomo 1: A E C D F B G