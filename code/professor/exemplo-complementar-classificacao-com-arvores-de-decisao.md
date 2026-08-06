---
entry_id: "exemplo-complementar-classificacao-com-arvores-de-decisao"
title: "Exemplo Complementar - Classificação com Árvores de Decisão"
language: "jupyter"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/exemplo-complementar-classificacao-com-arvores-de-decisao.ipynb"
---
# Exemplo Complementar - Classificação com Árvores de Decisão

> **Linguagem:** jupyter

## Célula 1 — Markdown

Inteligencia Artificial - Árvores de Decisão

Profa Silvia Moraes - Set/25

## Célula 2 — Código

```python
from sklearn.datasets import load_iris
from sklearn.datasets import load_breast_cancer
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report, confusion_matrix, accuracy_score
import matplotlib.pyplot as plt
import seaborn as sns
```

## Célula 3 — Código

```python
# Dataset Iris
data = load_iris()
X, y = data.data, data.target
class_names = data.target_names
features_names = data.feature_names

# Dataset Cancer de Mama
#cancer = load_breast_cancer()
#X = cancer.data
#y = cancer.target
#class_names = cancer.target_names
#features_names = cancer.feature_names
```

## Célula 4 — Código

```python
features_names
```

**Saída:**

```text
['sepal length (cm)',
 'sepal width (cm)',
 'petal length (cm)',
 'petal width (cm)']
```

## Célula 5 — Código

```python
# Treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, stratify=y, random_state=42)

print(X_train.shape)
print(X_test.shape)
print(y_train.shape)
print(y_test.shape )
```

**Saída:**

```text
(120, 4)
(30, 4)
(120,)
(30,)
```

## Célula 6 — Código

```python
# Cria a árvore de decisão
modelo = DecisionTreeClassifier(
    max_depth=3,
    random_state=42,
    #criterion="gini",      # ou "entropy"
    criterion="entropy",
)
modelo.fit(X_train, y_train)
```

**Saída:**

```text
DecisionTreeClassifier(criterion='entropy', max_depth=3, random_state=42)
```

## Célula 7 — Código

```python
# Predicao
y_pred = modelo.predict(X_test)
```

## Célula 8 — Código

```python
# Avaliação do modelo
print("\n--- Métricas de Avaliação ---")
print(f"Acurácia: {accuracy_score(y_test, y_pred):.2f}")

conf_matrix = confusion_matrix(y_test, y_pred)
plt.figure(figsize=(10, 6))
sns.heatmap(conf_matrix, annot=True, fmt='d', cmap='Blues',xticklabels=class_names, yticklabels=class_names)
plt.title('Matriz de Confusão - Métricas por Classe\n', fontsize=12)
plt.xlabel('Predito')
plt.ylabel('Verdadeiro')
```

**Saída:**

```text
--- Métricas de Avaliação ---
Acurácia: 0.97

Text(95.72222222222221, 0.5, 'Verdadeiro')

<Figure size 1000x600 with 2 Axes>
```

## Célula 9 — Código

```python
print("\nRelatório de Classificação:")
print(classification_report(y_test, y_pred, target_names=class_names))
```

**Saída:**

```text
Relatório de Classificação:
              precision    recall  f1-score   support

      setosa       1.00      1.00      1.00        10
  versicolor       1.00      0.90      0.95        10
   virginica       0.91      1.00      0.95        10

    accuracy                           0.97        30
   macro avg       0.97      0.97      0.97        30
weighted avg       0.97      0.97      0.97        30
```

## Célula 10 — Código

```python
# Visualização da árvore de decisão
plt.figure(figsize=(12, 8))
plot_tree(
    modelo,
    feature_names=features_names,
    class_names=class_names,
    filled=True,
    rounded=True
)
plt.title("Árvore de Decisão")
plt.show()
```

**Saída:**

```text
<Figure size 1200x800 with 1 Axes>
```
