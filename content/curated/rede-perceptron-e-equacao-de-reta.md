<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Neurônio e equação de reta**
- **Neurônio e equação de reta**
- **Equação da Reta**
- **Neurônio e equação de reta**
  - Estrutura Básica de um Neurônio
- **Neurônio e equação de reta**
  - Fórmula do Neurônio
- **Neurônio e equação de reta**
  - Relação Entre Pesos e a Equação da Reta
- **Neurônio e equação de reta**
- **Neurônio e equação de retas**
  - Exemplo Prático
- **Neurônio e equação de retas**
- **Conclusão**

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Decorative L-shaped black barPERCEPTRON

Relação entre neurônio e a equação de reta

Prof. Sílvia Moraes

{1}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-919a2cb85b99741a73c0c31a427236a8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decorative L-shaped black bar
<!-- /IMAGE_DESCRIPTION -->
## Neurônio e equação de reta

- Um neurônio da rede Perceptron é capaz de classificar os dados em 2 classes.
- A regra delta é quem é responsável por isso.
- Ela procura os coeficientes de uma equação de reta a partir dos dados de treino.
- Essa equação é responsável pela divisão das classes.

{2}------------------------------------------------
## Neurônio e equação de reta
## Equação da Reta

A equação da reta no plano cartesiano é dada por:

$$y=mx+b$$

onde:

- $m$  é a inclinação (coeficiente angular),
- $x$  é a variável independente (entrada),
- $b$  é uma constante.

{3}------------------------------------------------
## Neurônio e equação de reta
### Estrutura Básica de um Neurônio

- Um neurônio simples em uma rede neural recebe múltiplas entradas, cada uma associada a um peso.
- A saída do neurônio é geralmente calculada usando uma função de ativação aplicada à combinação soma ponderada entradas pelos pesos.

{4}------------------------------------------------
## Neurônio e equação de reta
### Fórmula do Neurônio

Para um neurônio com  $n$  entradas, a saída  $y$  pode ser expressa como:

$$y=f(w_1*x_1+w_2*x_2+\dots+w_n*x_n+b)$$

onde:

- $w_i$  são os pesos associados a cada entrada  $x_i$ ,
- $b$  é o bias (o peso extra),
- $f$  é a função de ativação (como a função degrau, sigmoid, etc.).

{5}------------------------------------------------
## Neurônio e equação de reta
### Relação Entre Pesos e a Equação da Reta
#### Combinação Linear:

- A parte  $w_1*x_1+w_2*x_2+\dots+w_n*x_n$  da fórmula do neurônio representa uma combinação linear das entradas, que é análoga à forma  $mx$  na equação da reta.
- Se considerarmos apenas duas entradas ( $n=2$ ), podemos simplificar a expressão para:

$$y=w_1*x_1+w_2*x_2+b$$

- Neste caso, a saída  $y$  é uma função linear das entradas  $x_1$  e  $x_2$ .

{6}------------------------------------------------
## Neurônio e equação de reta

**Inclinação e Pesos:** Quando se tem duas entradas, a inclinação da reta em relação a uma das entradas pode ser interpretada como o peso associado a essa entrada.

Por exemplo, se considerarmos  $x_1$  como a variável independente e isolarmos  $y$ :

$$y = w_1 * x_1 + w_2 * x_2 + b$$

Se  $x_2$  for mantido constante, a inclinação da reta em relação a  $x_1$  é dada pelo peso  $w_1$ . Da mesma forma, ao variarmos  $x_2$ , a inclinação em relação a  $x_2$  é dada por  $w_2$ .

{7}------------------------------------------------
## Neurônio e equação de retas

**O papel do bias (peso extra):** Ele determina onde a reta cruza o eixo y quando todas as entradas são zero.
### Exemplo Prático

Se tivermos um neurônio com duas entradas e pesos  $w_1=2$  e  $w_2=3$ , e um viés  $b=-1$ , a saída do neurônio seria:

$$y=2*x_1+3*x_2-1$$

Neste caso:

- A inclinação em relação a  $x_1$  é 2,
- A inclinação em relação a  $x_2$  é 3,
- A reta cruzará o eixo y em -1 quando  $x_1$  e  $x_2$  forem zero.

{8}------------------------------------------------
## Neurônio e equação de retas
## Conclusão

- Assim, os pesos de um neurônio em uma rede neural definem a inclinação da reta em um espaço multidimensional, enquanto o bias (peso extra  $w_0$ ) determina a posição da reta no gráfico.
- Essa relação permite que o neurônio aprenda a representar funções lineares, que são a base para a aprendizagem de padrões mais complexos em redes neurais.
