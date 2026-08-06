<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Exercício 1**
- **Exercício 2**
- **Exercício 3**
- **Exercício 4**
- **Exercício 5**
- **Exercício 6**
- **Exercício 7**
- **Exercício 8**
- **Exercício 9**
- **Exercício 10**
- **Exercício 11**
- **Exercício 12**
- **Exercício 13**
- **Exercício 14**
- **Exercício 15**
- **Exercício 16**
- **Exercício 17**
- **Exercício 18**
- **Exercício 19**
- **Exercício 20**
- **Exercício 21**
- **Exercício 22**

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

Logo of PUCRS (Pontifícia Universidade Católica do Rio Grande do Sul) featuring a coat of arms with a star and the motto 'VERVM DVCT'.

# Listas de Exercícios I

Chiara Girardi Paskulin

Inteligência Artificial – Prof<sup>a</sup>. Dr<sup>a</sup>. Silvia Maria W. Moraes

<!-- IMAGE_DESCRIPTION: datalab-2dfa6ac3edfe874f68aa0cbccaa42322_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Logo of PUCRS (Pontifícia Universidade Católica do Rio Grande do Sul) featuring a coat of arms with a star and the motto 'VERVM DVCT'.
<!-- /IMAGE_DESCRIPTION -->
## Exercício 1

(c) Autonomia – Toma as decisões e cumpre as tarefas sozinho.

As outras características não fazem de algo um agente.

Reatividade e pró-atividade são de uma classe específica de agentes.
## Exercício 2

AGENTES REATIVOS (IFs):

2 vantagens:

- Implementação mais simples e mais rápida
- Baixo processamento

2 desvantagens:

- Não consegue resolver problemas muito complexos
- Somente para ambientes completamente observáveis e com uma pouca quantidade de comportamentos para serem mapeados
## Exercício 3

Máquina de estados, autômato.
## Exercício 4

- (3) autonomia
- (1) comunicação indireta, via mudanças no ambiente -> formiga e feromônio
- (2) proatividade
- (2) adaptação
- (1) comportamento baseado apenas em estímulo-resposta
- (2) arquitetura BDI -> Belief-Desire-Intention -> crenças, desejos e intenções-> ag. cognitivo
- (2) comunicação direta entre agentes
- (2) utiliza algoritmos de raciocínio
- (1-3) percepção parcial do ambiente
- (2) conhecimento explícito sobre si mesmo e os outros agentes
## Exercício 5

- Completamente observável – Tu pode prevê tudo que possa acontecer. Informações perfeitas
- Parcialmente observável – Pode aparecer um canguru no meio da bento

{1}------------------------------------------------

- Determinístico – Autômato finito determinístico. Aconteceu X? Tu faz Y -> IF
  - Estocástico - Probabilidade, chances das coisas acontecerem
  - Episódico - Ação totalmente isolada do resto. Não tem nada a ver com ações passadas e futuras. Não se preocupa com as consequências. Ex: aspirador limpa a célula, independente da célula anterior ou a seguinte
  - Sequencial - Tudo interligado. Se preocupa com o que aconteceu antes e com o que vai acontecer depois. Manobras para estacionar o carro, palavra cruzada
  - Estático - Ambiente não muda
  - Dinâmico - Ambiente muda
  - Discreto - Passos discretos. 1,2,3,4... Passos isolados. Episódico
  - Contínuo - Ação ao longo do tempo. Aceleração do carro – Acelera ao longo do tempo
  - Mono - Um agente no ambiente
  - Multiagente - Vários carros autônomos no ambiente
- a) Aspirador de Pó  
Parcialmente observável; Determinístico; Episódico; Dinâmico; Discreto; Mono ou Multiagente.
  - b) Carro autônomo  
Parcialmente observável; Estocástico; Sequencial; Dinâmico; Contínuo; Mono ou Multiagente.
  - c) Jogo de Palavras Cruzadas  
Completamente observável; Determinístico; Sequencial; Dinâmico; Discreto; Monoagente.
  - d) Diagnóstico Médico  
Parcialmente observável; Estocástico; Sequencial; Dinâmico; Contínuo; Mono ou Multiagente.
## Exercício 6

Agente Conversacional Reativo – Switch Case. Menu de opções.

Agente Conversacional Cognitivo – Guarda contextos (não muito longos). Interpreta.
## Exercício 7

AGENTE DELIBERATIVO = Cognitivo

Raciocínio, conhecimento, comunicação com outros agentes, trabalhar em ambientes diversos, se adapta aos ambientes, aprende com o ambiente, também tem comportamentos reativos, mas não é isso que define-o.
## Exercício 8

{2}------------------------------------------------

Algoritmo de Busca com Informação – **Usa heurísticas**. Busca guiada. Ganha desempenho e ganha incerteza.

Exemplo de aplicação: Dijkstra com heurística. O A\* usa uma função heurística para guiar a busca – visita em uma ordem diferente guiada para achar o resultado, que é o caminho melhor/mais rápido. O algoritmo usa os pesos para saber qual decisão tomar. **Usar os dados -> informação**.

Algoritmo de Busca sem Informação – **Sem heurísticas**. Varre a estrutura com o propósito original dele. Perde desempenho e ganha certeza.

Exemplo de aplicação: DFS. Dijkstra usa informações local das arestas, usa os pesos das arestas para achar o melhor caminho. **Distância das ruas -> dados**.
## Exercício 9

Funções heurísticas são funções matemáticas, ou seja, geram algum valor, são construídas em cima de informações sobre o domínio com o qual se está trabalhando. Estatísticas, elementos do domínio que possibilitem que tu faça uma escolha. Não é uma certeza. Auxilia em uma escolha com as informações do domínio. Processo de decisão que pode ter falhas.

Se todo mundo dobra a direita no labirinto e a maioria das pessoas que dobraram a direita chegam no final, a melhor solução é dobrar a direita. Isso não significa que tu vai chegar no final, mas vai tomar a melhor decisão daquele momento.

O A\* usa duas funções: o peso da aresta (distância real) e a estimativa que ele faz (se eu escolher esse nodo, qual distância eu estou do objetivo?).

(Best First não foi visto)
## Exercício 10

O A\* em grafo pode achar a solução, mas nem sempre é ótima.

O A\* em árvore sempre acha uma solução, se ele tem uma.

Ser admissível = função que, quando estima, não superestima. É algo que é menor ou igual.

Não estima valores maiores do que a realidade.
## Exercício 11

Função heurística: distância das peças do objetivo ou quantas peças estão no lugar certo (quanto mais, melhor)

Função sucessor é a que, a partir do estado atual, abre em amplitude os possíveis movimentos seguintes. Em seguida a função heurística decide qual vai ser o movimento escolhido a partir das possibilidades de movimentos abertas.
## Exercício 12

No algoritmo de busca por refinamento tu não constrói uma solução (tipo uma árvore). Tu começa de uma solução dentro do espaço de busca (geralmente gerada aleatoriamente) e vai refinando ela com estados vizinhos (podendo usar heurísticas) para chegar onde tu está procurando. Não é um algoritmo que está preocupado com gerar um histórico da solução (fui de X estado para Y), em saber de onde tu saiu e onde tu chegou.

Vantagens: não monta árvore (menos memória), boa estratégia para espaços de busca muito grandes (melhora o processamento e utiliza menos memória).

{3}------------------------------------------------

Exemplos: Algoritmo Genético, Hill Climbing e Simulated Annealing.

O Algoritmo Genético começa com um conjunto de soluções e vai refinando essas soluções ao longo das interações até chegar em um resultado ótimo.

Quando o Hill Climbing começa mal, ele só consegue refinar até certo ponto, pois sempre cai no máximo/mínimo local.
## Exercício 13

Algoritmos Genéticos possuem a mutação. Perturba uma solução, tira ela do espaço de busca que ela está e joga em outro estado. Tira a solução daquela área do espaço de busca e te leva pra outra área. Se ele te joga para outro local do espaço de busca, aumenta a chance de tu chegar na solução. Se for ruim, vai ser descartado, ao longo das gerações vai ser eliminado. Se for bom, não garante que tu vai encontrar a solução, mas aumenta tuas chances.

Simulated annealing - gera um sucessor aleatoriamente e, quando encontra um melhor, pega ele. De vez em quando aceita um pior, como forma de mudar a área do espaço de busca. Porém chega um ponto em que ele não aceita mais nenhum pior e só refina o que tem.
## Exercício 14

Versão clássica do Hill Climbing:

Estado atual -> abre todos vizinhos do estado atual -> avalia um por um -> escolhe o melhor, que passa a ser o atual -> recomeça o ciclo

Hill Climbing - primeira melhor escolha:

Escolhe o primeiro vizinho melhor que o atual que aparece. Melhora o processamento.

Estado atual -> achou um vizinho melhor que o atual -> esse passa a ser o atual -> recomeça o ciclo
## Exercício 15

Simulated annealing:

Introduz no início da solução mecanismos para explorar melhor o espaço de busca com o objetivo de fugir dos máximos/mínimos locais. Depois, a partir de certo momento, passa a se comportar como Hill Climbing, só refinando o que já possui.

Gera um sucessor aleatoriamente e, quando encontra um melhor, pega ele. De vez em quando aceita um pior, como forma de mudar a área do espaço de busca. Porém chega um ponto em que ele não aceita mais nenhum pior e só refina o que tem.
## Exercício 16

1º - Cria uma codificação da solução (e uma função de aptidão capaz de medir a qualidade das soluções)

2º - Cria uma população inicial (geração 0) = conjunto gerado aleatoriamente de soluções candidatas

3º - Faz elitismo na população atual – vê qual a melhor solução da população atual a partir da função de aptidão e copia para a população intermediária (futura geração 1)

4º - Faz o torneio e crossover – Torneio: randomiza duas soluções da população atual e escolhe a melhor pra ser o pai. Randomiza mais duas soluções da população atual e escolhe a melhor pra ser a mãe. Crossover: cruza o pai e a mãe de acordo com algum operador genético de crossover. Gera 2 filhos. Adiciona os dois na população intermediária.

{4}------------------------------------------------

5° - Repete torneio e crossover até completar a população intermediária.

6° - População intermediária (geração 1) sobrescreve a geração 0, se tornando a população atual

7° - Reinicia no passo 3.

8° - Parada – o algoritmo para depois de várias gerações (é estabelecido um número de parada); se tu sabe qual o valor ótimo da solução, para quando achá-lo; pelo critério de convergência, ou seja, quando a partir de 90% das soluções da população tem o mesmo valor da função de aptidão.

De tempos em tempos, conforme a taxa de mutação, é aplicada uma mutação: escolhe aleatoriamente uma das soluções para fazer uma alteração.
## Exercício 17

a) Cruzamento uniponto:

Filho 1: 1 1 1 0 1 1 0 0

Filho 2: 0 1 0 1 1 0 1 1

b) Cruzamento uniforme que utiliza a máscara [ 1 0 0 0 1 1 1 0 ]

[ 1 0 0 0 1 1 1 0 ] -> quando for 1, traz do pai; quando for 0, traz da mãe

Filho 1: 1 1 0 1 1 0 1 0

[ 1 0 0 0 1 1 1 0 ] -> quando for 0, traz do pai; quando for 1, traz da mãe

Filho 2: 0 1 1 0 1 1 0 1
## Exercício 18

(V) Tanto o Hill-Climbing quanto o Simulated Annealing são algoritmos de refinamento.

(F) Diferente do Simulated Annealing, o Hill-Climbing mantém a árvore de busca durante a sua execução. **Nenhum dos dois gera árvore.**

(V) O Hill-Climbing move-se sempre em direção ao melhor valor, escolhe sempre o estado vizinho sucessor melhor avaliado pela sua função heurística.

(F) O Hill-Climbing, diferente do Simulated Annealing, possui um mecanismo de perturbação da solução que procura evitar máximos (ou mínimos) locais. **É o contrário.**

(V) A execução do algoritmo Simulated Annealing é controlada pelo parâmetro temperatura (T). Esse parâmetro é iniciado, geralmente, com um valor elevado e é lentamente reduzido durante o processo de busca. Ao chegar a zero, o algoritmo termina.

(V) O algoritmo Simulated Annealing escolhe o estado vizinho sucessor aleatoriamente.

(V) O Hill-Climbing pára quando nenhum o estado vizinho sucessor tiver valor melhor que o atual.

(F) O Hill-Climbing em menos de 1% dos casos aceita também soluções piores que a atual. **Simulated annealing que aceita de vez em quando um pior. O Hill-Climbing só sobe.**
## Exercício 19

a)

i. Codificação dos cromossomos e iv. Uma população inicial de 5 cromossomos:

Índice do vetor: 1 2 3 4 (mulheres)

2 3 2 4 -> formaria os casais: (1,2) (2,3) (3,1) (4,4)

3 1 2 4 -> formaria os casais: (1,3) (2,1) (3,2) (4,4)

4 1 2 3

3 2 4 1

{5}------------------------------------------------

1 4 3 2

- ii. Função de aptidão: os casais mais próximos com as preferências das pessoas
- iii. Operadores de Mutação e Cruzamento: pega duas posições (da mesma linha) e troca de lugar.

b) Sim, seria possível utilizando cadeias de IFs.
## Exercício 20

Alternativa correta: c

Sobre a alternativa E, não é o cruzamento que diversifica a população, é a mutação (insere algo novo).
## Exercício 21

O algoritmo Minimax pode ser utilizado em jogos com ambientes determinísticos e observáveis e com 2 jogadores, onde um vence e outro perde. Ex: jogos de tabuleiro.

O computador é se coloca em nível de max (para maximizar a chance dele de ganhar) e coloca o usuário em nível de min (para minimizar a chance dele de ganhar). É necessário ter uma função que defina se tu ganhou ou perdeu. O computador monta a árvore com os possíveis movimentos a partir do estado atual e escolhe as folhas que retornam vitória ou empate.
## Exercício 22

Ela é melhor pois ela não visita todos os ramos. As constantes de alfa e beta fazem com que o algoritmo corte alguns ramos desnecessários e não visite toda a árvore, deixando o algoritmo mais eficiente.
