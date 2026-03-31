# PERCEPTRON

Relação entre neurônio e a equação de reta

Prof. Sílvia Moraes

- Um neurônio da rede Perceptron é capaz de classificar os dados em 2 classes.
- A regra delta é quem é responsável por isso.
- Ela procura os coeficientes de uma equação de reta a partir dos dados de treino.
- Essa equação é responsável pela divisão das classes.

### Equação da Reta

A equação da reta no plano cartesiano é dada por:

y=mx+b

#### onde:

- m é a inclinação (coeficiente angular),
- x é a variável independente (entrada),
- b é uma constante.

#### Estrutura Básica de um Neurônio

- Um neurônio simples em uma rede neural recebe múltiplas entradas, cada uma associada a um peso.
- A saída do neurônio é geralmente calculada usando uma função de ativação aplicada à combinação soma ponderada entradas pelos pesos.

### Fórmula do Neurônio

Para um neurônio com n entradas, a saída y pode ser expressa como:

```
y=f(w1*x1+w2*x2+...+wn*xn+b)
```

#### onde:

- wi são os pesos associados a cada entrada xi,
- b é o bias (o peso extra),
- f é a função de ativação (como a função degrau, sigmoid, etc.).

#### Relação Entre Pesos e a Equação da Reta

### Combinação Linear:

- A parte w1\*x1+w2\*x2+...+wn\*xn da fórmula do neurônio representa uma combinação linear das entradas, que é análoga à forma mx na equação da reta.
- Se considerarmos apenas duas entradas (n=2), podemos simplificar a expressão para:

y=w1\*x1+w2\*x2+b

■ Neste caso, a saída y é uma função linear das entradas x1 e x2.

Inclinação e Pesos: Quando se tem duas entradas, a inclinação da reta em relação a uma das entradas pode ser interpretada como o peso associado a essa entrada.

Por exemplo, se considerarmos x1 como a variável independente e isolarmos y:

$$y=w1*x1+w2*x2+b$$

Se x2 for mantido constante, a inclinação da reta em relação a x1 é dada pelo peso w1. Da mesma forma, ao variarmos x2, a inclinação em relação a x2 é dada por w2.

O papel do bias (peso extra): Ele determina onde a reta cruza o eixo y quando todas as entradas são zero.

#### Exemplo Prático

Se tivermos um neurônio com duas entradas e pesos w1=2 e w2=3, e um viés b=−1, a saída do neurônio seria:

$$y=2*x1+3*x2-1$$

#### Neste caso:

- A inclinação em relação a x1 é 2,
- A inclinação em relação a x2 é 3,
- A reta cruzará o eixo y em -1 quando x1 e x2 forem zero.

#### Conclusão

- Assim, os pesos de um neurônio em uma rede neural definem a inclinação da reta em um espaço multidimensional, enquanto o bias (peso extra w0) determina a posição da reta no gráfico.
- Essa relação permite que o neurônio aprenda a representar funções lineares, que são a base para a aprendizagem de padrões mais complexos em redes neurais.
