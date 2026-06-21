<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **DIJKSTRA'S ALGORITHM DEMO ---**
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo
  - Dijkstra's algorithm demo

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Algorithms

ROBERT SEDGEWICK | KEVIN WAYNE

The image shows the front cover of the textbook 'Algorithms, Fourth Edition' by Robert Sedgwick and Kevin Wayne. The cover is a solid dark red color. At the top right, there is a small white logo consisting of two diamonds. Below this, on the left side, is a graphic of vertical bars of varying heights, resembling a bar chart or a stylized skyline. The title 'Algorithms' is printed in a large, white, serif font, with 'FOURTH EDITION' in a smaller, white, sans-serif font directly beneath it. At the bottom of the cover, the authors' names 'ROBERT SEDGEWICK | KEVIN WAYNE' are printed in a white, sans-serif font.

Cover of the book 'Algorithms, Fourth Edition' by Robert Sedgwick and Kevin Wayne.

<http://algs4.cs.princeton.edu>

<!-- IMAGE_DESCRIPTION: datalab-30a26f2d17ca95672702bf50fb4f0242_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Cover of the book 'Algorithms, Fourth Edition' by Robert Sedgwick and Kevin Wayne.
<!-- /IMAGE_DESCRIPTION -->
## DIJKSTRA'S ALGORITHM DEMO ---

{1}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) -- 5 --> 1((1)); 0 -- 8 --> 7((7)); 0 -- 9 --> 4((4)); 1 -- 15 --> 3((3)); 1 -- 4 --> 7; 1 -- 12 --> 2((2)); 2 -- 3 --> 3; 2 -- 11 --> 6((6)); 3 -- 9 --> 6; 4 -- 9 --> 7; 4 -- 5 --> 7; 4 -- 20 --> 6; 5((5)) -- 1 --> 2; 5 -- 13 --> 6; 6 -- 3 --> 2; 6 -- 9 --> 3; 7 -- 7 --> 2; 7 -- 6 --> 5;
```

An edge-weighted digraph with 7 vertices (0-6) and various weighted edges. Vertex 0 is the source 's'. The graph shows a network of directed edges with weights. For example, 0 to 1 is 5, 0 to 4 is 9, 0 to 7 is 8, 1 to 3 is 15, 1 to 7 is 4, 1 to 2 is 12, 2 to 3 is 3, 2 to 6 is 11, 3 to 6 is 9, 4 to 5 is 5, 4 to 6 is 20, 4 to 7 is 9, 5 to 2 is 1, 5 to 6 is 13, 6 to 2 is 3, 6 to 3 is 9, 7 to 2 is 7, 7 to 5 is 6.

an edge-weighted digraph

|     |      |
|-----|------|
| 0→1 | 5.0  |
| 0→4 | 9.0  |
| 0→7 | 8.0  |
| 1→2 | 12.0 |
| 1→3 | 15.0 |
| 1→7 | 4.0  |
| 2→3 | 3.0  |
| 2→6 | 11.0 |
| 3→6 | 9.0  |
| 4→5 | 4.0  |
| 4→6 | 20.0 |
| 4→7 | 5.0  |
| 5→2 | 1.0  |
| 5→6 | 13.0 |
| 7→5 | 6.0  |
| 7→2 | 7.0  |

{2}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-aa9e46d6f962be5cebcbb5c654c9b13e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** An edge-weighted digraph with 7 vertices (0-6) and various weighted edges.
<!-- /IMAGE_DESCRIPTION -->
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

The diagram shows a directed graph with 8 vertices labeled 0 through 7. Vertex 0 is the source and is highlighted in red. The other vertices are gray. The edges are as follows: 0 → 1, 0 → 7, 0 → 4, 1 → 3, 1 → 2, 1 → 7, 2 → 3, 2 → 6, 3 → 6, 4 → 7, 4 → 5, 4 → 6, 5 → 2, 5 → 6, 6 → 7.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| → 0 | 0.0      | -        |
| 1   |          |          |
| 2   |          |          |
| 3   |          |          |
| 4   |          |          |
| 5   |          |          |
| 6   |          |          |
| 7   |          |          |

A directed graph with 8 vertices (0-7) and a table showing the state of Dijkstra's algorithm.

choose source vertex 0

{3}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-7055f51feb10ea4ea48b27c36f085286_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) and a table showing the state of Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-eefe19c5e14dc4d6c316b7f7fbb7d7d7_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of Dijkstra's algorithm on a graph with 8 vertices (0-7).
<!-- /IMAGE_DESCRIPTION -->
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 |          |          |
| 2 |          |          |
| 3 |          |          |
| 4 |          |          |
| 5 |          |          |
| 6 |          |          |
| 7 |          |          |

A directed graph illustrating Dijkstra's algorithm. The source vertex is 0 (dark red). Vertices 1, 2, 3, 4, 5, 6, and 7 are light gray. Edges from 0 are highlighted in dark red: 0 to 1 (weight 5), 0 to 7 (weight 8), and 0 to 4 (weight 9). Current distance estimates are shown above each vertex: 0 (0), 1 (infinity), 2 (infinity), 3 (infinity), 4 (infinity), 5 (infinity), 6 (infinity), 7 (infinity). A table on the right shows the state of the algorithm.

relax all edges pointing from 0

{4}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-9e6062272bbe3ddbb7c0606721d64cf0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e394c2b5c61344f6a12397f430086072_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a7d78d22e465dea388b31d0739f9d0cd_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a738993919a50143787084ee7ce6e2f2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-990567efebf979be51f56d1150012c9d_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-562f471e8153729557e6a4ee6343c32c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cfda9df1319e04207eb28bcefd1dab7b_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-e9314c83043183351ed74908e9bf2f90_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-042733dc5e8e7f5f30b60adba3266cde_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-4ee27dbf5ef12e7b58b0ef0937bc5a5e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-724c7777b608e53be38b12b6fb3c43bc_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dfe556fea00682b09a59427aaf72051c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-2b3a967f6ce4f23649be995a353e39f8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d53cd0fd1cf896a9353fd63de1505ba2_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-d734a6ea1b381280f043fcf70391b6db_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-366a77fdefb0097b3289b4a011911390_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-5a1abd59a95fa47ae192807de151e9eb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-a149b400127a3e3e50b3c98d27c5935c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-b235edb1dbe659e2782c9a0e47775ca4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-dcb5711d118ae6753b0e12f86eda37db_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-fa01531ea2c45beeb4036005da3037a4_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-318886a86a1dcc59e1fc83db6f157c60_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-cfb98c691c1af5befe32ff9442eea511_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph illustrating Dijkstra's algorithm.
<!-- /IMAGE_DESCRIPTION -->
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) -- 5 --> 1((1)); 0 -- 8 --> 7((7)); 0 -- 9 --> 4((4)); 1 --> 3((3)); 1 --> 2((2)); 1 --> 7; 7 --> 2; 7 --> 5((5)); 4 --> 7; 4 --> 5; 4 --> 6((6)); 5 --> 2; 5 --> 6; 3 --> 6; 2 --> 6;
```

A directed graph illustrating Dijkstra's algorithm. The source vertex is 0 (dark red). Vertices 1, 2, 3, 4, 5, 6, and 7 are gray. Edges from 0 to 1 (weight 5), 0 to 7 (weight 8), and 0 to 4 (weight 9) are highlighted in red. Current distance estimates are shown next to each vertex: 0: 0, 1: infinity (with 5 above), 2: infinity, 3: infinity, 4: infinity (with 9 below), 5: infinity, 6: infinity, 7: infinity (with 8 to its right).

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 |          |          |
| 3 |          |          |
| 4 | 9.0      | 0→4      |
| 5 |          |          |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

relax all edges pointing from 0

{5}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) --> 1((1)); 0 --> 7((7)); 0 --> 4((4)); 1 --> 3((3)); 1 --> 2((2)); 1 --> 7; 2 --> 3; 2 --> 6((6)); 3 --> 6; 4 --> 7; 4 --> 5((5)); 4 --> 6; 5 --> 2; 5 --> 6; 6 --> 6;
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertices 1, 2, 3, 4, 5, 6, and 7 are shaded gray, indicating they have been processed. Vertex 0 is white, indicating it is the current vertex being processed. Edges are shown as directed arrows. The graph structure is: 0 -> 1, 0 -> 7, 0 -> 4; 1 -> 3, 1 -> 2, 1 -> 7; 2 -> 3, 2 -> 6; 3 -> 6; 4 -> 7, 4 -> 5, 4 -> 6; 5 -> 2, 5 -> 6; 6 -> 6 (self-loop).

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 |          |          |
| 3 |          |          |
| 4 | 9.0      | 0→4      |
| 5 |          |          |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

{6}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertex 1 is highlighted in red, indicating it is the next vertex to be added to the tree. Edges from 0 to 1, 7, and 4 are shown in light gray. Other edges are solid black. The graph structure is: 0 -> 1, 7, 4; 1 -> 3, 2, 7; 2 -> 3, 6; 3 -> 6; 4 -> 7, 5, 6; 5 -> 2, 6; 7 -> 2, 5.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| → 1 | 5.0      | 0→1      |
| 2   |          |          |
| 3   |          |          |
| 4   | 9.0      | 0→4      |
| 5   |          |          |
| 6   |          |          |
| 7   | 8.0      | 0→7      |

choose vertex 1

{7}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

Graph structure and current state:

- Vertex 0: Source, distance 0.0
- Vertex 1: Current vertex, distance 5.0
- Vertex 2: Distance  $\infty$
- Vertex 3: Distance  $\infty$
- Vertex 4: Distance 9.0
- Vertex 5: Distance  $\infty$
- Vertex 6: Distance  $\infty$
- Vertex 7: Distance 8.0

Edges and weights:

- 0 → 1 (weight 5)
- 0 → 2 (weight 4)
- 0 → 4 (weight 9)
- 0 → 7 (weight 8)
- 1 → 3 (weight 15)
- 1 → 2 (weight 12)
- 1 → 7 (weight 4)
- 2 → 3 (weight  $\infty$ )
- 2 → 6 (weight  $\infty$ )
- 4 → 5 (weight  $\infty$ )
- 4 → 6 (weight  $\infty$ )
- 5 → 2 (weight  $\infty$ )
- 5 → 6 (weight  $\infty$ )
- 7 → 2 (weight 8)
- 7 → 5 (weight  $\infty$ )

A directed graph illustrating Dijkstra's algorithm. The source vertex is 0. Vertices 1, 2, 3, 4, 5, 6, and 7 are shown with their current distance values above them. Vertex 1 is highlighted in red, indicating it is the current vertex being processed. Edges from 1 to 3 (weight 15), 1 to 2 (weight 12), and 1 to 7 (weight 4) are highlighted in red. Other edges are black. The graph shows a network of 8 vertices and 10 directed edges.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| → 1 | 5.0      | 0→1      |
| 2   |          |          |
| 3   |          |          |
| 4   | 9.0      | 0→4      |
| 5   |          |          |
| 6   |          |          |
| 7   | 8.0      | 0→7      |

relax all edges pointing from 1

{8}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph TD; 0((0)) -- 9 --> 4((4)); 0((0)) -- 4 --> 7((7)); 4((4)) -- 4 --> 5((5)); 4((4)) -- 4 --> 6((6)); 5((5)) -- 4 --> 2((2)); 5((5)) -- 4 --> 6((6)); 7((7)) -- 8 --> 2((2)); 1((1)) -- 4 --> 7((7)); 1((1)) -- 12 --> 2((2)); 1((1)) -- 15 --> 3((3)); 2((2)) -- 4 --> 3((3)); 2((2)) -- 4 --> 6((6)); 3((3)) -- 4 --> 6((6));
```

A directed graph illustrating Dijkstra's algorithm. The graph has 8 vertices labeled 0 through 7. Vertex 0 is the source. Vertex 1 is the current vertex being processed, highlighted in dark red. Edges from 1 are highlighted in dark red: 1 to 3 (weight 15), 1 to 2 (weight 12), and 1 to 7 (weight 4). Other edges are black: 0 to 4 (weight 9), 0 to 7 (weight 4), 4 to 5 (weight 4), 4 to 6 (weight 4), 5 to 2 (weight 4), 5 to 6 (weight 4), 2 to 3 (weight 4), 2 to 6 (weight 4), 3 to 6 (weight 4), and 7 to 2 (weight 8). Current distance estimates are shown above each vertex: 0: 0.0, 1: 5.0, 2: 17.0, 3: 20.0, 4: 9.0, 5: infinity, 6: infinity, 7: 8.0. A red arrow points to vertex 1 in the table on the right.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| → 1 | 5.0      | 0→1      |
| 2   | 17.0     | 1→2      |
| 3   | 20.0     | 1→3      |
| 4   | 9.0      | 0→4      |
| 5   |          |          |
| 6   |          |          |
| 7   | 8.0 ✓    | 0→7      |

relax all edges pointing from 1

{9}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph TD; 0((0)) -- 5.0 --> 1((1)); 0((0)) -- 9.0 --> 4((4)); 0((0)) -- 8.0 --> 7((7)); 1((1)) -- 17.0 --> 2((2)); 1((1)) -- 20.0 --> 3((3)); 1((1)) -- 5.0 --> 7((7)); 2((2)) -- 17.0 --> 3((3)); 2((2)) -- 17.0 --> 6((6)); 4((4)) -- 17.0 --> 5((5)); 4((4)) -- 17.0 --> 6((6)); 5((5)) -- 17.0 --> 2((2)); 5((5)) -- 17.0 --> 6((6)); 6((6)) -- 17.0 --> 3((3)); 7((7)) -- 17.0 --> 2((2));
```

A directed graph illustrating Dijkstra's algorithm. The graph has 8 vertices labeled 0 through 7. Vertex 0 is the source. Vertices 1, 2, 3, 4, 5, 6, and 7 are shown with varying shades of gray, indicating their current status in the algorithm. Edges are shown with arrows, some in light gray and some in black. The edges and their weights are: 0 to 1 (5.0), 0 to 4 (9.0), 0 to 7 (8.0), 1 to 2 (17.0), 1 to 3 (20.0), 1 to 7 (5.0), 2 to 3 (17.0), 2 to 6 (17.0), 4 to 5 (17.0), 4 to 6 (17.0), 5 to 2 (17.0), 5 to 6 (17.0), 6 to 3 (17.0), and 7 to 2 (17.0).

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 17.0     | 1→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 |          |          |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

{10}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 17.0     | 1→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 |          |          |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertices 1, 2, 3, 4, 5, 6, and 7 are shown with their current distance from the source and the edge used to reach them. Vertex 7 is highlighted in red, indicating it is the next vertex to be added to the tree. The table on the right shows the state of the algorithm.

choose vertex 7

{11}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

The graph shows vertices 0 through 7. Vertex 0 is the source. Vertices 1, 2, 3, 4, 5, and 6 are gray, indicating they have been processed. Vertex 7 is dark red, indicating it is the current vertex being processed. Edges from 7 to 2 and 5 are red, indicating they are being relaxed. The table on the right shows the current state of the algorithm.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 17.0     | 1→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 |          |          |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, and 7 are white; 2, 3, 4, 5, and 6 are gray. Vertex 7 is highlighted in dark red. Edges from 7 to 2 and 5 are red. A table on the right shows the current state of the algorithm.

relax all edges pointing from 7

{12}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 15.0     | 7→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 | 14.0     | 7→5      |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

Diagram of Dijkstra's algorithm on a graph with 8 vertices (0-7). Vertex 0 is the source. Vertices 1, 2, 3, 4, 5, 6 are in the tree (grey). Vertex 7 is the current vertex being relaxed (dark red). Edges from 7 to 2 (weight 7) and 7 to 5 (weight 6) are highlighted in red. The table shows the current state of the algorithm.

relax all edges pointing from 7

{13}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph TD; 0((0)) -- gray --> 1((1)); 0((0)) -- gray --> 7((7)); 0((0)) -- gray --> 4((4)); 1((1)) -- gray --> 2((2)); 1((1)) -- gray --> 3((3)); 7((7)) -- gray --> 2((2)); 7((7)) -- gray --> 5((5)); 4((4)) -- black --> 2((2)); 4((4)) -- black --> 5((5)); 4((4)) -- black --> 6((6)); 5((5)) -- black --> 2((2)); 5((5)) -- black --> 6((6)); 2((2)) -- black --> 3((3)); 2((2)) -- black --> 6((6)); 3((3)) -- black --> 6((6));
```

A directed graph illustrating Dijkstra's algorithm. Vertices 0 and 7 are white (unprocessed), while vertices 1, 2, 3, 4, 5, and 6 are gray (processed). Edges from 0 to 1, 0 to 7, and 0 to 4 are gray, while all other edges are black.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 15.0     | 7→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 | 14.0     | 7→5      |
| 6 |          |          |
| 7 | 8.0      | 0→7      |

{14}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph TD; 0((0)) -- gray --> 1((1)); 0((0)) -- gray --> 7((7)); 0((0)) -- gray --> 4((4)); 1((1)) -- gray --> 3((3)); 1((1)) -- gray --> 2((2)); 1((1)) -- gray --> 7((7)); 7((7)) -- gray --> 2((2)); 7((7)) -- gray --> 5((5)); 4((4)) -- black --> 2((2)); 4((4)) -- black --> 5((5)); 4((4)) -- black --> 6((6)); 2((2)) -- black --> 3((3)); 2((2)) -- black --> 6((6)); 5((5)) -- black --> 6((6)); 3((3)) -- black --> 6((6));
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertices 1, 7, and 4 are white (not in the tree). Vertices 2, 3, 5, and 6 are gray (in the tree). Vertex 4 is highlighted in dark red, indicating it is the next vertex to be selected. Edges are shown as arrows, with some in gray and others in black. A red arrow points to vertex 4 in the table to the right.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 15.0     | 7→2      |
| 3   | 20.0     | 1→3      |
| → 4 | 9.0      | 0→4      |
| 5   | 14.0     | 7→5      |
| 6   |          |          |
| 7   | 8.0      | 0→7      |

select vertex 4

{15}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

![A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 7 are white; 2, 3, 5, 6 are grey; 4 is dark red. Edges from 4 are red. A table on the right shows distTo[] and edgeTo[] values.](0f985b39edc1d52ba3600c438bc8f0a5_img.jpg)

The graph shows vertices 0 through 7. Vertex 0 is the source. Vertices 2, 3, 5, and 6 are already in the tree (grey). Vertex 4 is the current vertex being processed (dark red). Red arrows indicate edges being relaxed from vertex 4: 4→7 (weight 5), 4→5 (weight 4), and 4→6 (weight 20). Other edges are shown in grey.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 15.0     | 7→2      |
| 3   | 20.0     | 1→3      |
| → 4 | 9.0      | 0→4      |
| 5   | 14.0     | 7→5      |
| 6   |          |          |
| 7   | 8.0      | 0→7      |
|     | $\infty$        |          |

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 7 are white; 2, 3, 5, 6 are grey; 4 is dark red. Edges from 4 are red. A table on the right shows distTo[] and edgeTo[] values.

relax all edges pointing from 4

{16}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

![A graph diagram illustrating Dijkstra's algorithm. The graph has 8 vertices (0-7) and 12 edges. Vertex 0 is the source. Vertices 1, 7, and 4 are white (not in the tree). Vertices 2, 3, 5, and 6 are grey (in the tree). Red arrows show the relaxation of edges from vertex 4 to vertices 7, 5, and 6. The current distance values are: 0: 0.0, 1: 5.0, 2: 15.0, 3: 20.0, 4: 9.0, 5: 13.0, 6: 29.0, 7: 8.0. The edgeTo[] values are: 0: -, 1: 0->1, 2: 7->2, 3: 1->3, 4: 0->4, 5: 4->5, 6: 4->6, 7: 0->7.](2cde062fd82833415971a8bd1a2cafab_img.jpg)

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 15.0     | 7→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 29.0     | 4→6      |
| 7 | 8.0 ✓    | 0→7      |

A graph diagram illustrating Dijkstra's algorithm. The graph has 8 vertices (0-7) and 12 edges. Vertex 0 is the source. Vertices 1, 7, and 4 are white (not in the tree). Vertices 2, 3, 5, and 6 are grey (in the tree). Red arrows show the relaxation of edges from vertex 4 to vertices 7, 5, and 6. The current distance values are: 0: 0.0, 1: 5.0, 2: 15.0, 3: 20.0, 4: 9.0, 5: 13.0, 6: 29.0, 7: 8.0. The edgeTo[] values are: 0: -, 1: 0->1, 2: 7->2, 3: 1->3, 4: 0->4, 5: 4->5, 6: 4->6, 7: 0->7.

relax all edges pointing from 4

{17}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

The graph shows 8 vertices (0-7) and their connections. Vertices 0, 1, 4, and 7 are white circles, while vertices 2, 3, 5, and 6 are gray circles. Edges from gray vertices to white vertices are light gray, and edges between gray vertices are black.

```
graph LR; 0((0)) -- light gray --> 1((1)); 0((0)) -- light gray --> 7((7)); 0((0)) -- light gray --> 4((4)); 1((1)) -- light gray --> 7((7)); 1((1)) -- light gray --> 2((2)); 1((1)) -- light gray --> 3((3)); 7((7)) -- light gray --> 2((2)); 7((7)) -- light gray --> 5((5)); 4((4)) -- light gray --> 7((7)); 4((4)) -- light gray --> 5((5)); 4((4)) -- light gray --> 6((6)); 2((2)) -- black --> 3((3)); 2((2)) -- black --> 6((6)); 5((5)) -- black --> 2((2)); 5((5)) -- black --> 6((6)); 3((3)) -- black --> 6((6));
```

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, and 7 are white (not in the tree), while vertices 2, 3, 5, and 6 are gray (in the tree). Edges from gray vertices to white vertices are light gray, and edges between gray vertices are black.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 15.0     | 7→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 29.0     | 4→6      |
| 7 | 8.0      | 0→7      |

{18}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) -- 5.0 --> 1((1)); 0 -- 9.0 --> 4((4)); 0 -- 8.0 --> 7((7)); 1 -- 10.0 --> 2((2)); 1 -- 20.0 --> 3((3)); 2 -- 15.0 --> 3; 2 -- 29.0 --> 6((6)); 4 -- 4.0 --> 5((5)); 4 -- 9.0 --> 6; 5 -- 10.0 --> 2; 5 -- 13.0 --> 6; 7 -- 15.0 --> 2; 7 -- 9.0 --> 5; style 0 fill:#fff,stroke:#333; style 1 fill:#ccc,stroke:#333; style 2 fill:#ccc,stroke:#333; style 3 fill:#ccc,stroke:#333; style 4 fill:#ccc,stroke:#333; style 5 fill:#800000,color:#fff,stroke:#333; style 6 fill:#ccc,stroke:#333; style 7 fill:#fff,stroke:#333;
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertices 1, 2, 3, 4, 6, and 7 are in the tree (shaded gray). Vertices 5 and 7 are not yet in the tree (white). Vertex 5 is the current vertex being selected. Edges from 0: 0→1 (5.0), 0→4 (9.0), 0→7 (8.0). Edges from 1: 1→2 (10.0), 1→3 (20.0). Edges from 2: 2→3 (15.0), 2→6 (29.0). Edges from 4: 4→5 (4.0), 4→6 (9.0). Edges from 5: 5→2 (10.0), 5→6 (13.0). Edges from 7: 7→2 (15.0), 7→5 (9.0).

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 15.0     | 7→2      |
| 3   | 20.0     | 1→3      |
| 4   | 9.0      | 0→4      |
| → 5 | 13.0     | 4→5      |
| 6   | 29.0     | 4→6      |
| 7   | 8.0      | 0→7      |

select vertex 5

{19}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

![A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 7 are white; 2, 3, 6 are grey; 5 is dark red. Edges from 5 to 2 and 6 are red. A table on the right shows distTo[] and edgeTo[] values.](5445597cceefaca1ac89e710fe339325_img.jpg)

The graph shows vertices 0, 1, 4, 7 as white circles, 2, 3, 6 as grey circles, and 5 as a dark red circle. Edges from 5 to 2 and 6 are highlighted in red. The table on the right shows the current state of the algorithm.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 15.0     | 7→2      |
| 3   | 20.0     | 1→3      |
| 4   | 9.0      | 0→4      |
| → 5 | 13.0     | 4→5      |
| 6   | 29.0     | 4→6      |
| 7   | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 7 are white; 2, 3, 6 are grey; 5 is dark red. Edges from 5 to 2 and 6 are red. A table on the right shows distTo[] and edgeTo[] values.

relax all edges pointing from 5

{20}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

![A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 7 are white; 2, 3, 6 are grey; 5 is dark red. Edges from 5 to 2 and 6 are red. A table on the right shows distTo[] and edgeTo[] values.](c5655e700cc3e9aac7e9f4f07f30264d_img.jpg)

The graph shows vertices 0 through 7. Vertex 0 is the source. Vertices 2, 3, and 6 are already in the tree (grey). Vertex 5 is the current vertex being processed (dark red). Red arrows indicate the relaxation of edges from vertex 5 to vertices 2 and 6. The table on the right shows the current state of the algorithm.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 14.0     | 5→2      |
| 3   | 20.0     | 1→3      |
| 4   | 9.0      | 0→4      |
| → 5 | 13.0     | 4→5      |
| 6   | 26.0     | 5→6      |
| 7   | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 7 are white; 2, 3, 6 are grey; 5 is dark red. Edges from 5 to 2 and 6 are red. A table on the right shows distTo[] and edgeTo[] values.

relax all edges pointing from 5

{21}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) --> 1((1)); 0((0)) --> 4((4)); 0((0)) --> 7((7)); 1((1)) --> 2((2)); 1((1)) --> 3((3)); 2((2)) --> 3((3)); 2((2)) --> 6((6)); 4((4)) --> 5((5)); 4((4)) --> 6((6)); 5((5)) --> 2((2)); 5((5)) --> 6((6)); 7((7)) --> 2((2)); 7((7)) --> 5((5)); style 0 fill:#fff,stroke:#333; style 1 fill:#fff,stroke:#333; style 2 fill:#ccc,stroke:#333; style 3 fill:#ccc,stroke:#333; style 4 fill:#fff,stroke:#333; style 5 fill:#fff,stroke:#333; style 6 fill:#ccc,stroke:#333; style 7 fill:#fff,stroke:#333;
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 5, and 7 are white (not in the tree). Vertices 2, 3, and 6 are gray (in the tree). Edges from 0 to 1, 4, and 7 are light gray. Edges from 1 to 2 and 3 are light gray. Edges from 2 to 3 and 6 are black. Edges from 4 to 5 and 6 are light gray. Edges from 5 to 2 and 6 are light gray. Edges from 7 to 2 and 5 are light gray.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 20.0     | 1→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 26.0     | 5→6      |
| 7 | 8.0      | 0→7      |

{22}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) --> 1((1)); 0((0)) --> 4((4)); 0((0)) --> 7((7)); 1((1)) --> 3((3)); 1((1)) --> 7((7)); 1((1)) --> 2((2)); 4((4)) --> 5((5)); 4((4)) --> 6((6)); 5((5)) --> 2((2)); 5((5)) --> 6((6)); 7((7)) --> 2((2)); 2((2)) --> 3((3)); 2((2)) --> 6((6));
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertices 3, 2, and 6 are shaded gray, indicating they are in the tree. Vertex 2 is dark red, indicating it is the current vertex being processed. Vertices 1, 4, 5, and 7 are white, indicating they are not yet in the tree. Edges are shown as arrows: 0→1, 0→4, 0→7, 1→3, 1→7, 1→2, 4→5, 4→6, 5→2, 5→6, 7→2, 2→3, 2→6.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| → 2 | 14.0     | 5→2      |
| 3   | 20.0     | 1→3      |
| 4   | 9.0      | 0→4      |
| 5   | 13.0     | 4→5      |
| 6   | 26.0     | 5→6      |
| 7   | 8.0      | 0→7      |

select vertex 2

{23}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

Graph structure and distances:

- Vertex 0:  $\text{distTo}[] = 0.0$
- Vertex 1:  $\text{distTo}[] = 5.0$
- Vertex 2:  $\text{distTo}[] = 14.0$  (highlighted)
- Vertex 3:  $\text{distTo}[] = 20.0$
- Vertex 4:  $\text{distTo}[] = 9.0$
- Vertex 5:  $\text{distTo}[] = 13.0$
- Vertex 6:  $\text{distTo}[] = 26.0$
- Vertex 7:  $\text{distTo}[] = 8.0$

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| → 2 | 14.0     | 5→2      |
| 3   | 20.0     | 1→3      |
| 4   | 9.0      | 0→4      |
| 5   | 13.0     | 4→5      |
| 6   | 26.0     | 5→6      |
| 7   | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 5, and 7 are white circles. Vertices 2, 3, and 6 are grey circles. Vertex 2 is highlighted in dark red. Edges from 2 to 3 and 2 to 6 are dark red. A red arrow points to vertex 2 in the table.

relax all edges pointing from 2

{24}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

![A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 5, and 7 are white circles. Vertices 2, 3, and 6 are grey circles. Vertex 2 is the current vertex being processed, highlighted in dark red. Edges from 2 to 3 (weight 3) and 2 to 6 (weight 11) are dark red. Other edges are grey. Current distance estimates are shown near vertices: 3 has 17 (red) and 20 (grey); 6 has 25 (red) and 26 (grey). A table on the right shows the distTo[] and edgeTo[] arrays.](552265bdbcf6d43d341fd018a9076269_img.jpg)

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| → 2 | 14.0     | 5→2      |
| 3   | 17.0     | 2→3      |
| 4   | 9.0      | 0→4      |
| 5   | 13.0     | 4→5      |
| 6   | 25.0     | 2→6      |
| 7   | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. Vertices 0, 1, 4, 5, and 7 are white circles. Vertices 2, 3, and 6 are grey circles. Vertex 2 is the current vertex being processed, highlighted in dark red. Edges from 2 to 3 (weight 3) and 2 to 6 (weight 11) are dark red. Other edges are grey. Current distance estimates are shown near vertices: 3 has 17 (red) and 20 (grey); 6 has 25 (red) and 26 (grey). A table on the right shows the distTo[] and edgeTo[] arrays.

relax all edges pointing from 2

{25}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

The diagram shows a directed graph with 8 vertices labeled 0 through 7. Vertex 0 is the source. Vertices 3, 6, and 7 are shaded gray, indicating they have been processed. The graph shows various edges between vertices, with some edges highlighted in black to show the current state of the algorithm.

```
graph LR; 0((0)) --> 1((1)); 0((0)) --> 7((7)); 0((0)) --> 4((4)); 1((1)) --> 3((3)); 1((1)) --> 7((7)); 1((1)) --> 2((2)); 7((7)) --> 2((2)); 7((7)) --> 5((5)); 4((4)) --> 7((7)); 4((4)) --> 5((5)); 4((4)) --> 6((6)); 5((5)) --> 2((2)); 5((5)) --> 6((6)); 2((2)) --> 3((3)); 2((2)) --> 6((6)); 3((3)) --> 6((6));
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertices 3, 6, and 7 are shaded gray, indicating they have been processed. The graph shows various edges between vertices, with some edges highlighted in black to show the current state of the algorithm.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 17.0     | 2→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 25.0     | 2→6      |
| 7 | 8.0      | 0→7      |

{26}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) --> 1((1)); 0 --> 4((4)); 0 --> 7((7)); 1 --> 2((2)); 1 --> 3((3)); 1 --> 7; 2 --> 3; 2 --> 6((6)); 3 --> 6; 4 --> 5((5)); 4 --> 6; 5 --> 2; 5 --> 6; 7 --> 2; 7 --> 5;
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. Vertex 3 is the current vertex being processed, highlighted in dark red. Vertex 6 is the target, highlighted in grey. Other vertices are white. Edges are shown as arrows. The graph structure is: 0 to 1, 4, 7; 1 to 2, 3, 7; 2 to 3, 6; 3 to 6; 4 to 5, 6; 5 to 2, 6; 7 to 2, 5.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 14.0     | 5→2      |
| → 3 | 17.0     | 2→3      |
| 4   | 9.0      | 0→4      |
| 5   | 13.0     | 4→5      |
| 6   | 25.0     | 2→6      |
| 7   | 8.0      | 0→7      |

**select vertex 3**

{27}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dcf37c460c66ec011dbe6ca08de44ff9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) and a target vertex 6.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-14252bcd35912bd656e98b16b2ee51c0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A directed graph with 8 vertices (0-7) and a target vertex 6.
<!-- /IMAGE_DESCRIPTION -->
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 17.0     | 2→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 25.0     | 2→6      |
| 7 | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. The graph has 8 vertices labeled 0 through 7. Vertex 0 is the source. Vertex 3 is the current vertex being processed, highlighted in dark red. Vertex 6 is the target, highlighted in grey. The graph shows edges with weights: 0 to 1 (5), 0 to 4 (9), 0 to 7 (8), 1 to 2 (14), 1 to 3 (20), 2 to 3 (9), 2 to 6 (25), 4 to 5 (13), 5 to 2 (14), 5 to 6 (25), 7 to 2 (14), and 7 to 5 (13). The table on the right shows the current state of the algorithm.

relax all edges pointing from 3

{28}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 17.0     | 2→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 25.0 ✓   | 2→6      |
| 7 | 8.0      | 0→7      |

A directed graph illustrating Dijkstra's algorithm. The graph has 8 vertices labeled 0 through 7. Vertex 0 is the source. Vertex 3 is highlighted in dark red, indicating it is the current vertex being processed. Vertex 6 is highlighted in grey, indicating it is the next vertex to be processed. The graph shows edges from 0 to 1, 4, and 7; from 1 to 2 and 3; from 2 to 3 and 6; from 4 to 5 and 6; from 5 to 2 and 6; from 7 to 2 and 5. A table to the right shows the current state of the algorithm.

relax all edges pointing from 3

{29}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) -- 5 --> 1((1)); 0 -- 9 --> 4((4)); 0 -- 8 --> 7((7)); 1 -- 14 --> 2((2)); 1 -- 17 --> 3((3)); 1 -- 5 --> 7; 2 -- 17 --> 3; 2 -- 25 --> 6((6)); 3 -- 25 --> 6; 4 -- 13 --> 5((5)); 4 -- 25 --> 6; 5 -- 14 --> 2; 5 -- 13 --> 6; 7 -- 14 --> 2; 7 -- 13 --> 5; style 6 fill:#ccc
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. The graph shows the state after processing vertices 0 through 7. Vertex 6 is shaded, indicating it is the next vertex to be processed. The edges and their weights are: 0→1 (5), 0→4 (9), 0→7 (8), 1→2 (14), 1→3 (17), 1→7 (5), 2→3 (17), 2→6 (25), 3→6 (25), 4→5 (13), 4→6 (25), 5→2 (14), 5→6 (13), 7→2 (14), 7→5 (13).

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 17.0     | 2→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 25.0     | 2→6      |
| 7 | 8.0      | 0→7      |

{30}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

The diagram shows a directed graph with 8 vertices labeled 0 through 7. Vertex 6 is the target and is highlighted in dark red. The graph has the following edges: 0→1, 0→7, 0→4, 1→3, 1→7, 1→2, 2→3, 2→6, 3→6, 4→7, 4→5, 4→6, 5→2, 5→6, 7→2. The edges 2→6 and 4→5 are highlighted in red, corresponding to the current state of the algorithm.

A directed graph with 8 vertices (0-7) and a target vertex 6. Vertex 6 is highlighted in dark red. The graph shows various edges connecting the vertices, with some edges highlighted in red to show the current state of the algorithm.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 14.0     | 5→2      |
| 3   | 17.0     | 2→3      |
| 4   | 9.0      | 0→4      |
| 5   | 13.0     | 4→5      |
| → 6 | 25.0     | 2→6      |
| 7   | 8.0      | 0→7      |

**select vertex 6**

{31}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

The graph shows vertices 0 through 7. Vertex 6 is the target and is highlighted in dark red. The table to the right shows the current state of the algorithm, with vertex 6 highlighted in red.

| v   | distTo[] | edgeTo[] |
|-----|----------|----------|
| 0   | 0.0      | -        |
| 1   | 5.0      | 0→1      |
| 2   | 14.0     | 5→2      |
| 3   | 17.0     | 2→3      |
| 4   | 9.0      | 0→4      |
| 5   | 13.0     | 4→5      |
| → 6 | 25.0     | 2→6      |
| 7   | 8.0      | 0→7      |

A directed graph with 8 vertices (0-7) and a target vertex 6. Vertex 6 is highlighted in dark red. A table to the right shows the current state of the algorithm, with vertex 6 highlighted in red.

relax all edges pointing from 6

{32}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) -- 5 --> 1((1)); 0 -- 9 --> 4((4)); 0 -- 8 --> 7((7)); 1 -- 14 --> 2((2)); 1 -- 17 --> 3((3)); 1 -- 5 --> 7; 2 -- 2 --> 3; 2 -- 25 --> 6((6)); 3 -- 13 --> 6; 4 -- 13 --> 5((5)); 4 -- 25 --> 6; 5 -- 14 --> 2; 5 -- 13 --> 6; 7 -- 14 --> 2; 7 -- 13 --> 5;
```

A directed graph with 8 vertices (0-7) illustrating Dijkstra's algorithm. Vertex 0 is the source. The graph shows the state after processing vertices 0 through 7. Edges and their weights are: 0→1 (5), 0→4 (9), 0→7 (8), 1→2 (14), 1→3 (17), 1→7 (5), 2→3 (2), 2→6 (25), 3→6 (13), 4→5 (13), 4→6 (25), 5→2 (14), 5→6 (13), 7→2 (14), 7→5 (13).

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 17.0     | 2→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 25.0     | 2→6      |
| 7 | 8.0      | 0→7      |

{33}------------------------------------------------
### Dijkstra's algorithm demo

- Consider vertices in increasing order of distance from  $s$  (non-tree vertex with the lowest  $\text{distTo}[]$  value).
- Add vertex to tree and relax all edges pointing from that vertex.

```
graph LR; 0((0)) --> 1((1)); 0((0)) --> 7((7)); 0((0)) --> 4((4)); 1((1)) --> 2((2)); 1((1)) --> 7((7)); 2((2)) --> 3((3)); 2((2)) --> 6((6)); 3((3)) --> 6((6)); 4((4)) --> 5((5)); 4((4)) --> 7((7)); 5((5)) --> 2((2)); 5((5)) --> 6((6)); 6((6)) --> 2((2)); 7((7)) --> 2((2));
```

A directed graph illustrating Dijkstra's algorithm. The graph has 8 vertices labeled 0 through 7. Vertex 0 is the source, marked with a red 's'. The shortest-path tree is highlighted with thick black arrows, showing the path from 0 to 4, 0 to 1, 0 to 7, 4 to 5, 5 to 2, 2 to 3, and 2 to 6. Light gray arrows represent other edges in the graph: 1 to 2, 1 to 7, 2 to 6, 3 to 6, 4 to 7, 5 to 6, and 7 to 2.

| v | distTo[] | edgeTo[] |
|---|----------|----------|
| 0 | 0.0      | -        |
| 1 | 5.0      | 0→1      |
| 2 | 14.0     | 5→2      |
| 3 | 17.0     | 2→3      |
| 4 | 9.0      | 0→4      |
| 5 | 13.0     | 4→5      |
| 6 | 25.0     | 2→6      |
| 7 | 8.0      | 0→7      |

shortest-paths tree from vertex  $s$
