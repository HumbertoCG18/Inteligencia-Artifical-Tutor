---
entry_id: "tabuleiro"
title: "src\\dominio\\Tabuleiro.java"
language: "java"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/tabuleiro.java"
---
# src\dominio\Tabuleiro.java

> **Linguagem:** java
> Extraído de: programa-exemplo AG

```java
package dominio;

import operacao.Algoritimo;

//Define um tabuleiro de dimensão n
public class Tabuleiro {

    public boolean[][] tabuleiro;
    public int tamanho;

    public Tabuleiro(int tamanho) {
        this.tamanho = tamanho;
        tabuleiro = new boolean[tamanho][tamanho];
        zeraTabuleiro();
    }

    public void zeraTabuleiro() {
        for (int y = 0; y < tamanho; y++) {
            for (int x = 0; x < tamanho; x++) {
                tabuleiro[x][y] = false;
            }
        }
    }

    public void atualizaTabuleiro(int posicoesY[]) {
        zeraTabuleiro();
        for (int i = 0; i < Algoritimo.getN(); i++) {
            if (posicoesY[i] != -1) {
                tabuleiro[i][posicoesY[i]] = true;
            }
        }
    }

    public boolean[][] getTabuleiro() {
        return tabuleiro;
    }

    public boolean estaLivre(int x, int y) {
        boolean livre = true;
        if (tabuleiro[x][y]) {
            livre = false;
        }
        return livre;
    }

    @Override
    public String toString() {
        String r = "";
        for (int y = 0; y < tamanho; y++) {
            for (int x = 0; x < tamanho; x++) {
                if (tabuleiro[x][y]) {
                    r += " x";
                } else {
                    r += " o";
                }
            }
            r += "\n";
        }
        return r;
    }
}
```
