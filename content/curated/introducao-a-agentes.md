<!-- EXEC_SUMMARY_START -->
## Sumário
> *Leia antes de varrer o arquivo. Vá direto à seção relevante para a pergunta do aluno.*

- **Agentes**
  - Conceitos:
  - Agentes
  - Conceitos:
  - Agentes
  - Conceitos:
  - Agentes
  - Decorative orange circle with a purple dot and blue dashed linesCaracterística Básica
  - Exemplos de Agentes
  - Ambientes
- **Agentes como paradigma de desenvolvimento**
  - Decorative orange circle with a purple dot and blue arcsOrganizacao Classica
  - Organização segundo Russel & Norvig:
  - Agentes puramente reativos
  - Agentes puramente reativos
  - Agentes puramente reativos
  - Agentes Reativo baseado em Modelo
  - Agentes Reativos
  - Agente baseado em objetivos
  - Agente baseado em objetivos
  - Agente baseado em utilidade
  - Agente com aprendizado

<!-- EXEC_SUMMARY_END -->
{0}------------------------------------------------

# Introducao a Agentes

Abordagem Classica

Silvia Moraes – [silvia.moraes@pucrs.br](mailto:silvia.moraes@pucrs.br)

{1}------------------------------------------------
## Agentes
### Conceitos:

*Um agente de inteligência artificial consiste em um programa de software capaz de **interagir com o ambiente, coletar dados e usar esses dados para executar tarefas** autodirecionadas que atendam a metas determinadas previamente. (AWS - <https://aws.amazon.com/what-is/ai-agents>)*

*Os agentes de IA são sistemas de software que usam a IA para **alcançar objetivos e concluir tarefas** em nome dos usuários. Eles demonstram **raciocínio, planejamento e memória, com autonomia para tomar decisões, aprender e se adaptar**. (Google - <https://cloud.google.com/discover/what-are-ai-agents?>)*

{2}------------------------------------------------
### Agentes
### Conceitos:

Os agentes são **sistemas dinâmicos e orientados a metas** que podem **raciocinar, planejar e agir** em nome dos usuários. Microsoft - <https://learn.microsoft.com/pt-br/startups/build/ai/agents/intro-agents>

*Um agente de inteligência artificial (IA) é um sistema que **realiza tarefas de forma autônoma** por meio da criação de fluxos de trabalho com as ferramentas disponíveis.*

*Os agentes de IA podem abranger uma ampla variedade de funções além do processamento de linguagem natural, inclusive tomada de decisão, resolução de problemas, interação com ambientes externos e execução de ações. (IBM - <https://www.ibm.com/br-pt/think/topics/ai-agentes>)*

{3}------------------------------------------------
### Agentes
### Conceitos:

Um **agente de IA (Inteligência Artificial)** é um sistema capaz de **perceber informações do ambiente, processá-las, tomar decisões e executar ações para atingir objetivos específicos**, com diferentes níveis de autonomia.

Em termos simples, um agente de IA não apenas responde a perguntas; ele pode **planejar, agir e adaptar seu comportamento** com base no contexto e nos resultados obtidos. (ChatGPT, 17 de junho de 2026)

"Um agente é **qualquer entidade** que percebe seu ambiente por meio de sensores e atua sobre esse ambiente por meio de atuadores." (Russel e Norvig)

{4}------------------------------------------------
### Agentes

The diagram illustrates the interaction between an agent and its environment. On the left, a yellow cloud labeled "Ambiente" represents the environment. On the right, a blue humanoid figure represents the agent. A green arrow labeled "percepção" (perception) points from the environment to the agent's head, which contains a gray box with a question mark. A label "sensores" (sensors) points to the agent's head. A label "ação" (action) points from the agent's hand back to the environment. A label "atuadores" (actuators) points to the agent's legs.

Diagram of an agent interacting with its environment.

|                                                      | Agente Humano            | Robô                                      | Sistema                                                                   |
|------------------------------------------------------|--------------------------|-------------------------------------------|---------------------------------------------------------------------------|
| <b>Sensores:</b><br>viabilizam a percepção (entrada) | Olhos, ouvidos, ..       | Câmeras, detectores de Infravermelho, ... | Teclado, microfone, BD, leitura de arquivos, câmeras, ...                 |
| <b>Atuadores:</b><br>tornam possível a ação (saída)  | Boca, mãos e pernas, ... | Motores, ...                              | Execução de um programa, auto-falante, escrita em arquivo, impressora,... |

{5}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-690fce4fb5c9cbb8beb560cb2a3fcbeb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of an agent interacting with its environment.
<!-- /IMAGE_DESCRIPTION -->
### Decorative orange circle with a purple dot and blue dashed linesCaracterística Básica

- **Autonomia**(ausência de intervenção humana, o agente executa suas ações sem ser diretamente comandado por uma pessoa): característica fundamental de um agente.

{6}------------------------------------------------

A close-up view of a smartphone mounted on a car dashboard, displaying a navigation map, representing a mobile navigation agent.

<!-- IMAGE_DESCRIPTION: datalab-a68671ef36320b8515aa85d288d82cf1_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A close-up view of a smartphone mounted on a car dashboard, displaying a navigation map, representing a mobile navigation agent.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-644ad7d112788482bbde38833226c3c9_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Decorative blue brush strokes
<!-- /IMAGE_DESCRIPTION -->
### Exemplos de Agentes

A black, circular robotic vacuum cleaner (Roomba) on a carpeted floor, representing a domestic agent.

A white Google Lexus SUV equipped with a roof-mounted sensor suite, representing a self-driving car agent.

- Anti-vírus
- Personagem não jogável (non-player character ou NPCs)
- Bot de busca de informações: Googlebot
- Bot de navegação em dispositivos móveis
- Bot de recomendação, de monitoramento, ...
- Agentes conversacionais (chatbots e assistentes)
- Eletrodomésticos, ... e
- Outros baseados em LLM

{7}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-1dba94e9a65ea5fbd805e44a5a2c8cd5_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A black, circular robotic vacuum cleaner (Roomba) on a carpeted floor, representing a domestic agent.
<!-- /IMAGE_DESCRIPTION -->

<!-- IMAGE_DESCRIPTION: datalab-c1c7af7ea36be0323047962df57d75b0_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** A white Google Lexus SUV equipped with a roof-mounted sensor suite, representing a self-driving car agent.
<!-- /IMAGE_DESCRIPTION -->
### Ambientes

- Completamente observável x Parcialmente observável
- Determinístico x Estocástico
- Episódico x Sequencial
- Estático x Dinâmico
- Discreto x Contínuo
- Mono x Multiagente

Como são os ambientes de um agente:

1. Aspirador de Pó ?
2. Carro autônomo ?
3. Jogo de Palavras Cruzadas ?
4. Diagnóstico Médico ?

{8}------------------------------------------------
## Agentes como paradigma de desenvolvimento

O diagrama ilustra a interação entre um agente e seu ambiente. À esquerda, uma nuvem amarela rotulada "Ambiente" representa o mundo externo. À direita, um agente humanoide azul, rotulado "agente" na base, representa o sistema inteligente. O agente possui um torso com um retângulo cinza contendo um ponto de interrogação "?", simbolizando o estado interno ou o processo de decisão. Uma seta verde rotulada "percepção" aponta do ambiente para o agente, indicando a entrada de dados. Uma seta preta rotulada "ação" aponta do agente de volta para o ambiente, indicando a saída de dados. No topo do agente, o rótulo "sensores" aponta para a interface de entrada. Na base do agente, o rótulo "atuadores" aponta para a interface de saída.

Diagrama de um agente interagindo com um ambiente.

Conceito de IA:

”É o estudo e projeto de agentes inteligentes, onde um agente inteligente é um sistema que percebe o seu ambiente e executa ações que maximizam suas chances de sucesso.”

(Russel&Norvig,2013)

{9}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-acfc53eca625d62b38aa2563efa95c3e_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de um agente interagindo com um ambiente.
<!-- /IMAGE_DESCRIPTION -->
### Decorative orange circle with a purple dot and blue arcsOrganizacao Classica

- Agentes **Reativos**(Não deliberativos): baseado em regras (estimulo-resposta)
- Agentes **Cognitivos**(Deliberativos): baseado em planos
- **Híbridos**

{10}------------------------------------------------
### Organização segundo Russel & Norvig:

- **Reativos**
  - Agente puramente reativo (simples)
  - Agente reativo baseado em modelo
- **Cognitivos**
  - Agente baseado em objetivos
  - Agente baseado em utilidade
  - Agente com aprendizado

{11}------------------------------------------------
### Agentes puramente reativos

- É aquele cujas ações são baseadas apenas na sua percepção atual do ambiente.
- **Reatividade:** Característica principal (responsivo).
- Capacidade de perceber seu ambiente e responder em um tempo adequado às mudanças que ocorrem no ambiente a fim de satisfazer seus objetivos.
- Consiste em mapear percepções em ações. Sua implementação, usualmente, contém uma base de regras do tipo:
  - **SE**<condição> **ENTÃO** ação
  - Exige uma definição prévia e completa do comportamento do agente (projetista).

{12}------------------------------------------------
### Agentes puramente reativos

- Outras **características básicas**:
  - **não há representação explícita de conhecimento**: conhecimento implícito, se manifesta através do comportamento do agente;
  - **não há representação do ambiente**: seu comportamento se baseia apenas no que é percebido a cada instante.
  - **não há memória das ações**: não mantêm um histórico de ações, o resultado de uma ação passada não influencia as ações futuras;
  - **organização etológica**: a forma de organização similar a dos animais, em oposição à organização social dos sistemas cognitivos;
  - **grande número de membros**: têm, em geral, um grande número de agentes, da ordem de dezenas, centenas ou mesmo milhões de agentes.

{13}------------------------------------------------
### Agentes puramente reativos

The diagram illustrates the internal structure of a purely reactive agent. The agent is represented by a grey rounded rectangle labeled "Agente" at the bottom left. It interacts with an "Ambiente" (Environment), shown as a blue vertical rectangle on the right. Data flows from the environment into the agent through "Sensores" (Sensors) at the top. Inside the agent, the input leads to a decision box asking "Qual é a aparência do mundo agora ?" (What is the current appearance of the world?). This box is connected to a "Regras condição-ação" (Condition-action rules) module, which in turn points to another decision box asking "Que ação devo executar agora ?" (What action should I execute now?). The output of this second box goes to "Atuadores" (Actuators) at the bottom, which then sends signals back to the environment. The entire process is a direct loop from perception to action without any internal state.

Diagram of a purely reactive agent architecture.

Função AgenteReativoSimples(**percepção**)

**variáveis estáticas: regras**

estado  $\leftarrow$  interpretar(estado, percepção)

regra  $\leftarrow$  buscarRegra(estado, regras)

ação  $\leftarrow$  obterAção(regra)

retorna **ação**

{14}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-b9ecbc3baefab13719e000faa6e0c7eb_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a purely reactive agent architecture.
<!-- /IMAGE_DESCRIPTION -->
### Agentes Reativo baseado em Modelo

- É aquele que usa um modelo de mundo (interno), além das percepções atuais, para definir as ações que serão executadas.
- Usa algum tipo de estado interno vinculado ao histórico de percepções que reflete alguns aspectos não observados a partir do estado atual (“controla a parte do mundo que não vê”).
- Modelo do mundo : conhecimento sobre como o “mundo funciona” (modo como o mundo evolui independentemente do agente).
  - Exemplo: Controla o posicionamento de outros agentes estimando suas localizações a partir das suas posições iniciais e da informação de como estas são atualizadas.

{15}------------------------------------------------
#### Agente Reativo baseado em Modelo

Possui alguma estrutura interna capaz de armazenar informação sobre:

- o próprio agente (estado interno). Ex: carga de energia, combustível no tanque, ...
- o ambiente (evolução, informações de controle). Ex: determinadas lixeiras podem ser mais usadas que outras, localização das lixeiras, período em que há mais lixo, ...
- ações que podem ser executadas.
- Controla o estado atual do mundo usando um modelo interno e, em seguida, escolhe uma ação da mesma maneira que o agente reativo simples.

{16}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-2b3a967f6ce4f23649be995a353e39f8_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagrama de transição de estado para um agente reativo.
<!-- /IMAGE_DESCRIPTION -->
#### Agente Reativo baseado em Modelos

The diagram illustrates the internal structure of a reactive agent. The agent is represented by a large rounded rectangle labeled 'Agente' at the bottom left. Inside, there are several components and their interactions:

- Sensores**: A label at the top with a dashed arrow pointing to the 'Estado' box and a solid arrow pointing from the 'Ambiente' to the 'Qual é a aparência do mundo agora?' box.
- Estado**: A box at the top left representing the internal state.
- Como o mundo evolui**: A box below 'Estado' with an arrow pointing to the 'Qual é a aparência do mundo agora?' box.
- O que minhas ações fazem**: A box below 'Como o mundo evolui' with an arrow pointing to the 'Qual é a aparência do mundo agora?' box.
- Regras condição-ação**: A box below 'O que minhas ações fazem' with an arrow pointing to the 'Que ação devo executar agora?' box.
- Qual é a aparência do mundo agora?**: A central box that receives input from 'Sensores', 'Como o mundo evolui', and 'O que minhas ações fazem'. It has a solid arrow pointing down to the 'Que ação devo executar agora?' box.
- Que ação devo executar agora?**: A box that receives input from 'Regras condição-ação' and 'Qual é a aparência do mundo agora?'. It has a solid arrow pointing down to the 'Atuadores' label.
- Atuadores**: A label at the bottom with a solid arrow pointing from the 'Que ação devo executar agora?' box to the 'Ambiente'.
- Ambiente**: A large blue rectangle on the right representing the environment, which interacts with the agent via 'Sensores' and 'Atuadores'.

Diagram of a reactive agent architecture based on models.

```
Função AgenteReativoComEstado(percepção) {  
    variáveis estáticas: regras, estado (interno)  
    estado ← interpretar(estado, percepção)  
    regra ← buscarRegra(estado, regras)  
    ação ← obterAção(regra)  
    estado ← atualizarEstado(estado, ação)  
    retorna ação  
}
```

{17}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-c85ded401105f62f2d6ff26b3b5eb4af_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Diagram of a reactive agent architecture based on models.
<!-- /IMAGE_DESCRIPTION -->
### Agentes Reativos

- O comportamento de um agente reativo pode ser representado por meio de uma **máquina de estados finita**.
- **Finite-State Machine (FSM)**: Modelo computacional amplamente utilizado para implementar a tomada de decisão em sistemas multiagentes. Pode variar desde algo muito simples até casos mais complexos, com hierarquias de FSMs.
- Permite a modelagem do comportamento dos agentes reativos.

The diagram consists of two separate Finite State Machine (FSM) models, each with two states represented by light blue circles.

The top FSM has two states: 'Andar' (Walk) and 'Aspirar' (Suck).

- An initial arrow points to the 'Andar' state.
- A self-loop arrow is on the 'Andar' state, labeled 'Sem sujeira' (No dirt).
- A transition arrow goes from 'Andar' to 'Aspirar', labeled 'Com sujeira' (With dirt).
- A self-loop arrow is on the 'Aspirar' state, labeled 'Com sujeira' (With dirt).
- A transition arrow goes from 'Aspirar' back to 'Andar', labeled 'Sem sujeira' (No dirt).

The bottom FSM has two states: 'Parar' (Stop) and 'Nadar' (Swim).

- An initial arrow points to the 'Parar' state.
- A transition arrow goes from 'Parar' to 'Nadar', labeled 'umidade' (humidity).
- A transition arrow goes from 'Nadar' back to 'Parar', labeled 'ausência de umidade' (absence of humidity).

Two Finite State Machine (FSM) diagrams illustrating reactive agent behavior.

{18}------------------------------------------------

<!-- IMAGE_DESCRIPTION: datalab-dfe556fea00682b09a59427aaf72051c_img.jpg -->
<!-- Tipo: generico -->
> **[Descrição de imagem]** Two Finite State Machine (FSM) diagrams illustrating reactive agent behavior.
<!-- /IMAGE_DESCRIPTION -->
#### Agentes Reativos

```
Classe Agente{
enum Estado {PATRULHAR, DEFENDER, DORMIR}
Estado estadoInicial, estadoAtual
inico(){
estadoInicial = PATRULAR
estadoAtual = estadoInicial
}
atualiza(){
If estadoAtual == PATRULHAR then{
If podeVerInimigo() then estadoAtual = DEFENDER
If cansado() then estadoAtual = DORMIR
}
else if estadoAtual== DEFENDER then{
if !podeVerInimigo() then estadoAtual = PATRULAR
}
else if estadoAtual== DORMIR then{
If !cansado() then estadoAtual = PATRULAR
}
retorna estadoAtual.getAção()
}
```

```
graph TD
    Start(( )) --> Patrulhar
    Patrulhar((Patrulhar)) -- "Pode ver o inimigo" --> Defender((Defender))
    Defender -- "Não pode ver o inimigo" --> Patrulhar
    Patrulhar -- "cansado" --> Dormir((Dormir))
    Dormir -- "descansado ou volume > 10" --> Patrulhar
```

Diagrama de transição de estado para um agente reativo. Três estados são representados por círculos azuis: Patrulhar (topo), Defender (direita) e Dormir (esquerda). Uma seta sem rótulo aponta para o estado Patrulhar. Transições rotuladas: Patrulhar para Defender com o rótulo 'Pode ver o inimigo'; Defender para Patrulhar com o rótulo 'Não pode ver o inimigo'; Patrulhar para Dormir com o rótulo 'cansado'; Dormir para Patrulhar com o rótulo 'descansado ou volume > 10'.

```
notificaRuido(int volume){
if estadoAtual == DORMIR and volume > 10
then estadoAtual = DEFENDER
}
}
```

{19}------------------------------------------------
#### Agentes Reativos
##### Vantagens

- Comportamentos reativos são normalmente simples de projetar.
- Prototipação rápida para poucos comportamentos.
- Baixo processamento.
- Fáceis de depurar quando o número de estados é pequeno;
- Intuitivos - fáceis de entender até para pessoas sem conhecimento de programação;
- Flexíveis em contexto simples – podem ser facilmente modificados.
##### Desvantagens

- O ambiente tem que ser totalmente observável, pois o agente só funciona apropriadamente se a regra correta for disparada, o que depende da percepção atual realizada.
  - Implementação de um grande conjunto de comportamentos é uma tarefa difícil ou mesmo inviável.
- ![Decorative blue brush strokes](644ad7d112788482bbde38833226c3c9_img.jpg)

{20}------------------------------------------------
### Agente baseado em objetivos

- Atua para alcançar **metas específicas**. Além de perceber o ambiente, ele considera quais ações o aproximam do objetivo desejado.
- **Características**
  - Possui um ou mais objetivos definidos.
  - Avalia possíveis ações antes de agir.
  - Utiliza planejamento e busca para atingir a meta.
  - Escolhe ações com base nos resultados futuros esperados.
- **Exemplo**
  - Um aplicativo de navegação tem como objetivo levar o usuário ao destino. Para isso, analisa diferentes rotas e escolhe aquela que melhor atende ao objetivo estabelecido.

{21}------------------------------------------------
### Agente baseado em objetivos
##### - **Vantagens**

- Possui comportamento orientado a metas específicas.
- Pode planejar ações antes de executá-las.
- É mais flexível do que agentes puramente reativos.
- Consegue encontrar diferentes caminhos para atingir o mesmo objetivo.
##### - **Desvantagens**

- O processo de planejamento pode exigir grande capacidade computacional.
- Pode demorar para tomar decisões em ambientes complexos.
- Não diferencia a qualidade entre soluções que atingem o objetivo; qualquer solução válida pode ser escolhida.
- Tem dificuldades quando há múltiplos objetivos conflitantes.

- **Exemplo:** um GPS pode encontrar várias rotas que chegam ao destino, mas um agente baseado apenas em objetivos não necessariamente escolherá a mais rápida ou econômica.

{22}------------------------------------------------
### Agente baseado em utilidade

- Um agente baseado em utilidade vai além de simplesmente alcançar um objetivo. Ele procura escolher a alternativa que gera o maior benefício ou satisfação, de acordo com as suas medidas de desempenho.
- **Características**
  - Possui uma função de utilidade que mede a qualidade dos resultados.
  - Compara diferentes alternativas.
  - Escolhe a opção que maximiza a utilidade esperada.
  - É útil em ambientes com incerteza ou múltiplas soluções possíveis.
- **Exemplo:** Um sistema de transporte pode escolher entre várias rotas que chegam ao destino. Em vez de apenas encontrar uma rota válida, ele seleciona a que oferece a melhor combinação de tempo, custo e segurança.

{23}------------------------------------------------
#### Agente Baseado em Utilidade
##### - **Vantagens**

- Escolhe a melhor alternativa entre várias opções possíveis.
- Considera fatores como custo, tempo, risco e benefício.
- Funciona bem em ambientes incertos.
- Produz decisões mais eficientes e otimizadas.
##### - **Desvantagens**

- É necessário definir uma função de utilidade adequada, o que pode ser complexo.
- Exige mais processamento para comparar alternativas.
- Pode ser difícil quantificar conceitos subjetivos, como conforto, satisfação ou segurança.
- Erros na função de utilidade podem levar a decisões inadequadas.

- **Exemplo:** um carro autônomo pode avaliar várias rotas e selecionar a que oferece melhor equilíbrio entre tempo de viagem, segurança e consumo de combustível.

{24}------------------------------------------------
### Agente com aprendizado

- é capaz de melhorar seu desempenho a partir da experiência e da interação com o ambiente.
- **Características**
  - Aprende com dados e resultados anteriores.
  - Adapta seu comportamento ao longo do tempo.
  - Pode corrigir erros e aperfeiçoar estratégias.
  - Torna-se mais eficiente à medida que acumula experiência.
- **Exemplo**
  - Um sistema de recomendação de filmes aprende as preferências dos usuários com base nos filmes assistidos e nas avaliações realizadas, melhorando gradualmente suas sugestões.

{25}------------------------------------------------
#### Agente com Aprendizado
##### - **Vantagens**

- Aprende com experiências passadas.
- Melhora continuamente seu desempenho.
- Adapta-se a mudanças no ambiente.
- Reduz a necessidade de programação manual para todas as situações.
- É adequado para ambientes dinâmicos e complexos.
#### - **Desvantagens**

- Necessita de dados e experiências para aprender.
- O treinamento pode ser demorado e custoso.
- Pode aprender padrões incorretos se os dados forem inadequados.
- O comportamento nem sempre é facilmente explicável.
- Pode exigir grande quantidade de recursos computacionais.

- **Exemplo:** um sistema de recomendação aprende os gostos dos usuários ao longo do tempo, mas pode fazer recomendações ruins se os dados coletados forem insuficientes ou enviesados.
