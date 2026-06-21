---
entry_id: "analise-exploratoria-dos-dados-exemplo-2"
title: "Analise Exploratória dos Dados - Exemplo 2"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/analise-exploratoria-dos-dados-exemplo-2.ipynb"
---
# Analise Exploratória dos Dados - Exemplo 2

> **Linguagem:** jupyter

## Célula 1 — Markdown

# **Aula 02 - Preparação de Dados : Análise**
Sílvia Moraes
---
Nesse exemplo usamos o **profiling** do Pandas para realizar a análise de alguns datasets


*   **Facilidade de uso**: com poucas linhas de código gera-se um relatório abrangente
*   **Economia de tempo**: ampla gama de informações sobre um conjunto de dados com o mínimo de esforço
*   **Relatórios HTML interativos**: o perfil do Pandas gera relatórios HTML interativos que são fáceis de analisar e entender.

No entanto, **desempenho com grandes conjuntos de dados pode ser ineficiente**. À medida que o volume de dados cresce, o tempo de geração do relatório aumenta consideravelmente

## Célula 2 — Markdown

Instale o pacote, se necessário

## Célula 3 — Código

```python
!pip install typing-extensions==4.7.0
!pip install ydata-profiling


import pandas as pd
from ydata_profiling import ProfileReport
```

**Saída:**

```text
Collecting typing-extensions==4.7.0
  Downloading typing_extensions-4.7.0-py3-none-any.whl.metadata (3.1 kB)
Downloading typing_extensions-4.7.0-py3-none-any.whl (33 kB)
Installing collected packages: typing-extensions
  Attempting uninstall: typing-extensions
    Found existing installation: typing_extensions 4.15.0
    Uninstalling typing_extensions-4.15.0:
      Successfully uninstalled typing_extensions-4.15.0
[31mERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
plum-dispatch 2.5.7 requires typing-extensions>=4.9.0, but you have typing-extensions 4.7.0 which is incompatible.
wandb 0.21.3 requires typing-extensions<5,>=4.8, but you have typing-extensions 4.7.0 which is incompatible.
typeguard 4.4.4 requires typing_extensions>=4.14.0, but you have typing-extensions 4.7.0 which is incompatible.
typing-inspection 0.4.1 requires typing-extensions>=4.12.0, but you have typing-extensions 4.7.0 which is incompatible.
openai 1.106.1 requires typing-extensions<5,>=4.11, but you have typing-extensions 4.7.0 which is incompatible.
fastapi 0.116.1 requires typing-extensions>=4.8.0, but you have typing-extensions 4.7.0 which is incompatible.
torch 2.8.0+cu126 requires typing-extensions>=4.10.0, but you have typing-extensions 4.7.0 which is incompatible.
google-genai 1.33.0 requires typing-extensions<5.0.0,>=4.11.0, but you have typing-extensions 4.7.0 which is incompatible.
pydantic 2.11.7 requires typing-extensions>=4.12.2, but you have typing-extensions 4.7.0 which is incompatible.
starlette 0.47.3 requires typing-extensions>=4.10.0; python_version < "3.13", but you have typing-extensions 4.7.0 which is incompatible.
pydantic-core 2.33.2 requires typing-extensions!=4.7.0,>=4.6.0, but you have typing-extensions 4.7.0 which is incompatible.
alembic 1.16.5 requires typing-extensions>=4.12, but you have typing-extensions 4.7.0 which is incompatible.
altair 5.5.0 requires typing-extensions>=4.10.0; python_version < "3.14", but you have typing-extensions 4.7.0 which is incompatible.[0m[31m
[0mSuccessfully installed typing-extensions-4.7.0
Collecting ydata-profiling
  Downloading ydata_profiling-4.16.1-py2.py3-none-any.whl.metadata (22 kB)
Collecting scipy<1.16,>=1.4.1 (from ydata-profiling)
  Downloading scipy-1.15.3-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (61 kB)
[2K     [90m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m62.0/62.0 kB[0m [31m3.4 MB/s[0m eta [36m0:00:00[0m
[?25hRequirement already satisfied: pandas!=1.4.0,<3.0,>1.1 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (2.2.2)
Requirement already satisfied: matplotlib<=3.10,>=3.5 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (3.10.0)
Requirement already satisfied: pydantic>=2 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (2.11.7)
Requirement already satisfied: PyYAML<6.1,>=5.0.0 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (6.0.2)
Requirement already satisfied: jinja2<3.2,>=2.11.1 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (3.1.6)
Collecting visions<0.8.2,>=0.7.5 (from visions[type_image_path]<0.8.2,>=0.7.5->ydata-profiling)
  Downloading visions-0.8.1-py3-none-any.whl.metadata (11 kB)
Requirement already satisfied: numpy<2.2,>=1.16.0 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (2.0.2)
Collecting htmlmin==0.1.12 (from ydata-profiling)
  Downloading htmlmin-0.1.12.tar.gz (19 kB)
  Preparing metadata (setup.py) ... [?25l[?25hdone
Collecting phik<0.13,>=0.11.1 (from ydata-profiling)
  Downloading phik-0.12.5-cp312-cp312-manylinux_2_24_x86_64.manylinux_2_28_x86_64.whl.metadata (5.6 kB)
Requirement already satisfied: requests<3,>=2.24.0 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (2.32.4)
Requirement already satisfied: tqdm<5,>=4.48.2 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (4.67.1)
Requirement already satisfied: seaborn<0.14,>=0.10.1 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (0.13.2)
Collecting multimethod<2,>=1.4 (from ydata-profiling)
  Downloading multimethod-1.12-py3-none-any.whl.metadata (9.6 kB)
Requirement already satisfied: statsmodels<1,>=0.13.2 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (0.14.5)
Requirement already satisfied: typeguard<5,>=3 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (4.4.4)
Collecting imagehash==4.3.1 (from ydata-profiling)
  Downloading ImageHash-4.3.1-py2.py3-none-any.whl.metadata (8.0 kB)
Requirement already satisfied: wordcloud>=1.9.3 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (1.9.4)
Collecting dacite>=1.8 (from ydata-profiling)
  Downloading dacite-1.9.2-py3-none-any.whl.metadata (17 kB)
Requirement already satisfied: numba<=0.61,>=0.56.0 in /usr/local/lib/python3.12/dist-packages (from ydata-profiling) (0.60.0)
Requirement already satisfied: PyWavelets in /usr/local/lib/python3.12/dist-packages (from imagehash==4.3.1->ydata-profiling) (1.9.0)
Requirement already satisfied: pillow in /usr/local/lib/python3.12/dist-packages (from imagehash==4.3.1->ydata-profiling) (11.3.0)
Requirement already satisfied: MarkupSafe>=2.0 in /usr/local/lib/python3.12/dist-packages (from jinja2<3.2,>=2.11.1->ydata-profiling) (3.0.2)
Requirement already satisfied: contourpy>=1.0.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib<=3.10,>=3.5->ydata-profiling) (1.3.3)
Requirement already satisfied: cycler>=0.10 in /usr/local/lib/python3.12/dist-packages (from matplotlib<=3.10,>=3.5->ydata-profiling) (0.12.1)
Requirement already satisfied: fonttools>=4.22.0 in /usr/local/lib/python3.12/dist-packages (from matplotlib<=3.10,>=3.5->ydata-profiling) (4.59.2)
Requirement already satisfied: kiwisolver>=1.3.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib<=3.10,>=3.5->ydata-profiling) (1.4.9)
R
```

## Célula 4 — Markdown

**Dataset IRIS** ( https://archive.ics.uci.edu/dataset/53/iris )

Um dataset clássico de Fisher, 1936. Um dos primeiros datasets usados para avaliar métodos de classificação.

## Célula 5 — Código

```python
df = pd.read_csv('IRIS.csv')
profile = ProfileReport(df, title="Profiling Report")
profile
```

## Célula 6 — Markdown

**Dataset TIC TAC TOE**( https://archive.ics.uci.edu/dataset/101/tic+tac+toe+endgame )

Um dataset para classificação binária que contém as possíveis configurações do jogo da velha.

**Tarefa:** Execute a análise de dados para este dataset

## Célula 7 — Markdown

**Dataset WINE**( https://archive.ics.uci.edu/dataset/109/wine )

Dataset que usa elementos de análise química para determinar a origem dos vinhos

**Tarefa:** Execute a análise de dados para este dataset
