# Introdução a redes neurais

Silvia Moraes

![](content/images/introducaoredesneurais-2023-02-_page_0_Picture_2.png)

### Roteiro

- Introdução
- Conceito de Rede Neural
- Neurônio Biológico x Neurônio Artificial
- Algumas arquiteturas de Redes Neurais
- Introducao a rede neural Perceptron
- Topologias de rede

![](content/images/introducaoredesneurais-2023-02-_page_1_Picture_7.png)

Existem vários tarefas que **exigem atenção a diferentes eventos ao mesmo tempo** e o **processamento de informações variadas** para que sejam tomadas decisões e executadas ações convenientes.

![](content/images/introducaoredesneurais-2023-02-_page_2_Picture_1.png)

Tarefas até mesmo simples, como pegar um objeto, abrir uma porta ou mesmo caminhar envolvem a ação de componentes como **memória**, **aprendizado** e **coordenação**.

![](content/images/introducaoredesneurais-2023-02-_page_3_Picture_1.png)

O sistema nervoso, do qual faz parte o cérebro, é um conjunto complexo de células que determinam o funcionamento e comportamento dos seres vivos.

![](content/images/introducaoredesneurais-2023-02-_page_4_Picture_1.png)

A unidade fundamental do sistema nervoso é o neurônio.

Célula nervosa diferente das demais que se caracteriza por responder a estímulos externos e internos; e por transmitir impulsos a outras células nervosas, musculares e glandulares..

![](content/images/introducaoredesneurais-2023-02-_page_5_Picture_2.png)

0 **cérebro humano** possui cerca de **10 a 500 bilhões** de neurônios.

![](content/images/introducaoredesneurais-2023-02-_page_6_Picture_1.png)

Estima-se que esteja organizado em **1000 módulos**.

**Cada módulo** com cerca de **500 redes neurais**.

![](content/images/introducaoredesneurais-2023-02-_page_7_Picture_2.png)

Cada neurônio pode estar **conectado a centenas** ou até mesmo **milhares** de outros neurônios.

![](content/images/introducaoredesneurais-2023-02-_page_8_Picture_1.png)

As redes de neurônios trabalham de forma **massiva e paralela**, com **grande rapidez**.

O tempo de execução dos neurônios é normalmente de **0,001 segundos**.

![](content/images/introducaoredesneurais-2023-02-_page_9_Picture_2.png)

Essas capacidades e habilidades motivaram o desenvolvimento de **técnicas computacionais inspiradas no cérebro humano**.

![](content/images/introducaoredesneurais-2023-02-_page_10_Picture_1.png)

**Redes Neurais Artificiais** são sistemas computacionais distribuídos compostos de unidades simples (neurônios), densamente interconectados.

![](content/images/introducaoredesneurais-2023-02-_page_11_Picture_1.png)

Redes Neurais Artificiais podem aplicadas em várias tarefas, em diferentes paradigmas de aprendizagem a depender da sua arquitetura:

- Classificação de dados, de texto, de imagem, ...
- Reconhecimento de objetos, faces, palavras (escritas ou faladas)...
- Regressão de dados: preços futuros de taxas de câmbio ou ações, previsão de vendas, previsão de demandas, ...
- Detecção de fraudes e anomalias
- Recomendação de produtos
- · Agrupamento de dados, de objetos, de pessoas, ...
- Sumarização de dados
- Similaridade de dados

•

Qual a relação entre os neurônios biológicos e os artificiais?

![](content/images/introducaoredesneurais-2023-02-_page_13_Picture_1.png)

# Os principais componentes de um neurônio são :

- **dendritos**,
- **corpo celular** e
- **axônio**.

![](content/images/introducaoredesneurais-2023-02-_page_14_Picture_4.png)

Como esses componentes são simulados em um neurônio artificial?

![](content/images/introducaoredesneurais-2023-02-_page_15_Picture_1.png)

![](content/images/introducaoredesneurais-2023-02-_page_16_Picture_1.png)

### Neurônio Artificial

![](content/images/introducaoredesneurais-2023-02-_page_16_Picture_3.png)

#### **Dendritos:**

são prolongamentos especializados na recepção de estímulos nervosos provenientes de outros neurônios ou do ambiente.

![](content/images/introducaoredesneurais-2023-02-_page_17_Picture_3.png)

# Neurônio Artificial

**X: x<sup>1</sup> , x<sup>2</sup> , x<sup>3</sup> , ...x<sup>p</sup>**

O vetor X de dados simula os dendritos. Representa a entrada. X pode ser os dados de entrada da rede ou o sinal de saída de outros neurônios.

![](content/images/introducaoredesneurais-2023-02-_page_17_Picture_7.png)

#### **Dendritos:**

são prolongamentos especializados na recepção de estímulos nervosos provenientes de outros neurônios ou do ambiente.

# Neurônio Artificial

**X: x<sup>1</sup> , x<sup>2</sup> , x<sup>3</sup> , ...x<sup>p</sup>**

O vetor X de dados simula os dendritos. Representa a entrada. X pode ser os dados de entrada da rede ou **o sinal de saída de outros neurônios**.

![](content/images/introducaoredesneurais-2023-02-_page_18_Figure_6.png)

#### **Dendritos:**

são prolongamentos especializados na recepção de estímulos nervosos provenientes de outros neurônios ou do ambiente. **Recebem sinais com intensidade e frequência diferentes.**

![](content/images/introducaoredesneurais-2023-02-_page_19_Picture_3.png)

# Neurônio Artificial

**W: w<sup>1</sup> , w<sup>2</sup> , w<sup>3</sup> , ...w<sup>p</sup>**

O vetor de pesos sinápticos W simula as intensidades diferentes do sinal. Esses valores ponderam as entradas simulando variações na intensidade do sinal.

![](content/images/introducaoredesneurais-2023-02-_page_19_Picture_7.png)

#### **Corpo Celular:**

Recebe os estímulos dos dendritos , os combina e os processa.

![](content/images/introducaoredesneurais-2023-02-_page_20_Picture_3.png)

### Neurônio Artificial

#### **$\Sigma$ :** Responsável por combinar os valores de entrada. Realiza uma soma das entradas ponderadas pelos pesos.

![](content/images/introducaoredesneurais-2023-02-_page_20_Picture_6.png)

#### **Axônio:**

Prolongamento do neurônio, responsável pela condução de impulsos elétricos gerados pelo corpo celular até outro local mais distante, geralmente outros neurônios. Em um adulto pode ter até 1m.

![](content/images/introducaoredesneurais-2023-02-_page_21_Picture_3.png)

### Neurônio Artificial

**Função de transferência (ou ativação):**

Responsável pela modulação do sinal propagado., gera valores excitatórios (positivos) ou inibitórios (negativos).

![](content/images/introducaoredesneurais-2023-02-_page_21_Picture_7.png)

#### **Axônio:**

O contato entre a terminação de um axônio e o dentrito de outro neurônio e chamado de **Sinapse**.

As sinapses mediam as interações entre os neurônios, podendo ser excitatórias ou inibitórias.

#### **Função de transferência (ou ativação):**

Responsável pela modulação do sinal propagado., gera valores excitatórios (positivos) ou inibitórios (negativos).

![](content/images/introducaoredesneurais-2023-02-_page_22_Picture_6.png)

#### **Axônio:**

O contato entre a terminação de um axônio e o dentrito de outro neurônio e chamado de **Sinapse**.

As sinapses mediam as interações entre os neurônios, podendo ser excitatórias ou inibitórias.

![](content/images/introducaoredesneurais-2023-02-_page_23_Picture_4.png)

**Função de transferência (ou ativação):**

Responsável pela modulação do sinal propagado., gera valores excitatórios (positivos) ou inibitórios (negativos).

Se o neurônio estiver em uma camada de saída da rede, o sinal gerado corresponde a saída da rede.

![](content/images/introducaoredesneurais-2023-02-_page_23_Picture_8.png)

Como é a propagação de um sinal em um neurônio em uma rede artificial?

![](content/images/introducaoredesneurais-2023-02-_page_24_Picture_1.png)

![](content/images/introducaoredesneurais-2023-02-_page_25_Picture_1.png)

![](content/images/introducaoredesneurais-2023-02-_page_26_Picture_1.png)

Recebendo os dados de entrada X

![](content/images/introducaoredesneurais-2023-02-_page_27_Picture_1.png)

Ponderando as entradas X pelos pesos W: x<sub>i</sub> \* w<sub>ij</sub>

![](content/images/introducaoredesneurais-2023-02-_page_28_Picture_1.png)

Combinando os sinais: soma=  $x_1 * w_{1j} + x_2 * w_{2j} + x_3 * w_{3j} + ... x_n * w_{nj}$ 

![](content/images/introducaoredesneurais-2023-02-_page_29_Picture_1.png)

Gerando o sinal de saida:  $y_1 = f(soma)$
