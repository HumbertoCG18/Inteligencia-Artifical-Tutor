{0}------------------------------------------------

# Lista de Exercícios I

1. Qual a característica fundamental que uma entidade virtual ou física deve possuir para ser considerada um agente ?
  - (a) Reatividade
  - (b) Pró-Atividade
  - (c) Autonomia
  - (d) Memória
  - (e) Percepção
2. A implementação de agentes reativos para resolução de problemas tem seus prós e contras. Cite ao menos 2 vantagens e 2 desvantagens referentes ao projeto e desenvolvimento de agentes reativos.
3. Que modelo matemático costuma-se usar para projetar agentes e representar os comportamentos esperados para esses agentes ?
4. Associe a coluna da esquerda com a da direita, relacionando o tipo de agente à sua característica.

|       |                   |     |                                                           |
|-------|-------------------|-----|-----------------------------------------------------------|
| ( 1 ) | Puramente Reativo | ( ) | autonomia                                                 |
| ( 2 ) | Cognitivo         | ( ) | comunicação indireta, via mudanças no ambiente            |
| ( 3 ) | Ambos             | ( ) | proatividade                                              |
|       |                   | ( ) | adaptação                                                 |
|       |                   | ( ) | comportamento baseado apenas em estímulo-resposta         |
|       |                   | ( ) | arquitetura BDI                                           |
|       |                   | ( ) | comunicação direta entre agentes                          |
|       |                   | ( ) | utiliza algoritmos de raciocínio                          |
|       |                   | ( ) | percepção parcial do ambiente                             |
|       |                   | ( ) | conhecimento explícito sobre si mesmo e os outros agentes |
5. Considerando os tipos de ambientes abaixo, defina os ambientes dos agentes mencionados a seguir:
  - Completamente observável x Parcialmente observável
  - Determinístico x Estocástico
  - Episódico x Sequencial
  - Estático x Dinâmico
  - Discreto x Contínuo
  - Mono x Multiagente
  - (a) Aspirador de Pó ?
  - (b) Carro autônomo ?

{1}------------------------------------------------

- (c) Jogo de Palavras Cruzadas ?
- (d) Diagnóstico Médico ?
6. Agentes Conversacionais são reativos ou cognitivos ? Justifique.
  7. Quais são as características de um agente deliberativo?
  8. Em que situação (ou situações) os algoritmos de busca com informação são mais interessantes que os sem informação ? Do que depende basicamente o sucesso dos algoritmos de busca com informação ? No contexto dos agentes, cite as principais aplicações desses algoritmos. (Justifique suas respostas)
  9. O que são funções heurísticas ? Diferencie os algoritmos de busca Best First e A\* quanto ao uso dessas funções.
  10. O A\* atinge a solução ótima quando a busca é em árvore e as funções heurísticas usadas são admissíveis. O que é uma função heurística admissível?
  11. Dado o problema do quebra-cabeça de peças deslizantes abaixo, defina uma função heurística admissível que poderia ser usada por um algoritmo de busca e exemplifique a função sucessor para o estado inicial apresentado.

|   |   |   |
|---|---|---|
| 7 | 2 | 4 |
| 5 |   | 6 |
| 8 | 3 | 1 |

Start State

|   |   |   |
|---|---|---|
|   | 1 | 2 |
| 3 | 4 | 5 |
| 6 | 7 | 8 |

Goal State

Diagrama de um quebra-cabeça de 3x3 com peças deslizantes. O estado inicial (Start State) tem a peça cinza vazia no centro. O estado meta (Goal State) tem a peça cinza vazia no canto superior esquerdo.

12. Quando um algoritmo de busca por refinamentos sucessivos é mais indicado para resolver um problema ? Quais as vantagens dessa abordagem de busca? Justifique.
13. Que algoritmos de refinamento possuem mecanismos para tentar escapar de máximos (ou mínimos) locais ? Ao identificar os algoritmos, explique como esses mecanismos funcionam.
14. A versão Hill Climbing “pela primeira escolha” diferencia-se da versão clássica do algoritmo em qual aspecto ? Quando essa versão é mais indicada do que a versão clássica?
15. O algoritmo Simulated Annealing é considerado uma extensão do Hill Climbing. Por que ?
16. Descreva o ciclo de execução de um algoritmo genético.

{2}------------------------------------------------

17. Considere os dois cromossomos abaixo, extraídos da população atual de um algoritmo genético, e responda os itens a seguir

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|---|---|---|---|---|---|---|
| 1 | 1 | 1 | 0 | 1 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 | 0 | 0 |

- (a) Que filhos seriam gerados se fosse aplicado o cruzamento uniponto na posição central dos cromossomos ?

(b) Que filhos seriam gerados se fosse aplicado o cruzamento uniforme que utiliza a máscara  $[1\ 0\ 0\ 0\ 1\ 1\ 1\ 0]$  ?

18. Analise as afirmações abaixo sobre as versões clássicas dos algoritmos Hill-Climbing e Simulated Annealing e assinale V para afirmação verdadeira e F para afirmação falsa.

  - Tanto o Hill-Climbing quanto o Simulated Annealing são algoritmos de refinamento.
  - Diferente do Simulated Annealing, o Hill-Climbing mantém a árvore de busca durante a sua execução.
  - O Hill-Climbing move-se sempre em direção ao melhor valor, escolhe sempre o estado vizinho sucessor melhor avaliado pela sua função heurística.
  - O Hill-Climbing, diferente do Simulated Annealing, possui um mecanismo de perturbação da solução que procura evitar máximos (ou mínimos) locais.
  - A execução do algoritmo Simulated Annealing é controlada pelo parâmetro temperatura (T). Esse parâmetro é iniciado, geralmente, com um valor elevado e é lentamente reduzido durante o processo de busca. Ao chegar a zero, o algoritmo termina.
  - O algoritmo Simulated Annealing escolhe o estado vizinho sucessor aleatoriamente.
  - O Hill-Climbing pára quando nenhum o estado vizinho sucessor tiver valor melhor que o atual.
  - O Hill-Climbing em menos de 1% dos casos aceita também soluções piores que a atual.

19. Considere o seguinte problema: Uma agência de casamento precisa de um programa que indique os casais ideais. Sabendo que o programa deve trabalhar com uma quantidade N de casais e que são listadas, para cada mulher, os homens na sua ordem de preferência, bem como, para cada homem, as mulheres em ordem de preferência. Sabendo que, no exemplo, abaixo são apresentadas as informações disponíveis para formar 4 casais ideais (as mulheres e os homens são identificados por valores de 1 a 4), responda os itens a seguir.

Image: Diagram illustrating the matching process between 4 men and 4 women. The top part shows 'Número de casais' (Number of couples) with a horizontal arrow pointing right. Below it, a table shows the preference order for women: 1 (1, 2, 3, 4), 2 (3, 1, 2, 4), 3 (4, 1, 2, 3), 4 (2, 3, 4, 1). A bracket on the right groups this table with the text 'Mulheres e os homens na ordem de preferência'. The bottom part shows a table for men: 1 (2, 1, 4, 2), 2 (2, 4, 1, 3), 3 (3, 4, 1, 2), 4 (1, 2, 4, 3). A bracket on the right groups this table with the text 'Homens e as mulheres na ordem de preferência'.

4  $\xrightarrow{\hspace{2cm}}$  Número de casais

|   |   |   |   |   |
|---|---|---|---|---|
| 1 | 1 | 2 | 3 | 4 |
| 2 | 3 | 1 | 2 | 4 |
| 3 | 4 | 1 | 2 | 3 |
| 4 | 2 | 3 | 4 | 1 |

} Mulheres e os homens na ordem de preferência

|   |   |   |   |   |
|---|---|---|---|---|
| 1 | 2 | 1 | 4 | 2 |
| 2 | 2 | 4 | 1 | 3 |
| 3 | 3 | 4 | 1 | 2 |
| 4 | 1 | 2 | 4 | 3 |

} Homens e as mulheres na ordem de preferência

- (a) Esse problema pode ser resolvido usando algoritmos genéticos. Para isso, defina:

{3}------------------------------------------------

- i. Codificação dos cromossomos
  - ii. Função de Aptidão
  - iii. Operadores de Mutação e Cruzamento
  - iv. Uma população inicial de 5 cromossomos
- (b) Esse problema pode ser resolvido usando-se apenas agentes reativos ? (Não. Por que ? Sim. Como ?) Detalhe sua resposta.
20. Analise as afirmativas abaixo sobre Algoritmos Genéticos quanto à influência das operações de mutação e cruzamento na busca de uma solução ótima, e marque a alternativa CORRETA.
- (a) A ausência da mutação aumenta as chances do algoritmo convergir para um máximo (ou mínimo) global.
  - (b) A ausência do cruzamento aumenta as chances do algoritmo convergir para um máximo (ou mínimo) global.
  - (c) A ausência da mutação aumenta as chances do algoritmo convergir para um máximo (ou mínimo) local.
  - (d) O uso intenso da mutação é diretamente responsável pela convergência prematura do algoritmo.
  - (e) O uso do cruzamento é diretamente responsável pela diversidade da população, pois ao modificar as soluções, ele aumenta as chances do algoritmo convergir para um máximo (ou mínimo) global.
21. Como funciona o algoritmo Minimax ? Em que jogos ele pode ser usado ?
22. Por que a versão alfa-beta pruning é melhor ? Explique

<!-- IMAGE_DESCRIPTION_ORPHANS -->
## Imagens Curadas

Descrições preservadas para imagens detectadas no documento, mas sem referência markdown compatível no corpo principal.

<!-- IMAGE_DESCRIPTION: datalab-9ba3dc91984c80b96f217fb1bddd5c06_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um quebra-cabeça de 3x3 com peças deslizantes.
<!-- /IMAGE_DESCRIPTION -->
<!-- /IMAGE_DESCRIPTION_ORPHANS -->
