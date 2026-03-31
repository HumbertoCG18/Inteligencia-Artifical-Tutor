---
entry_id: "knn"
title: "ExemploKnn\\arquivosIris\\Knn.java"
language: "java"
category: "codigo-professor"
unit: ""
source: "raw/code/professor/knn.java"
---
# ExemploKnn\arquivosIris\Knn.java

> **Linguagem:** java
> Extraído de: Exemploknn

```java
/**
 * Escreva a descrição da classe KMeans aqui.
 * 
 * @author (seu nome) 
 * @version (número de versão ou data)
 */
import java.util.*;
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class Knn
{
    private static double[][] dadosTreino;
    private static double[][] dadosTeste;
    private static double [][]distancia;
    private static int k;
    
    
    public static void main(String args[]){
        //busca os dados do arquivo iris.data
        System.out.println("\nDados para Treino");
        dadosTreino = new double[120][5];
        carga("iris_treino.txt",dadosTreino);
        escreveDados(dadosTreino);
        
        System.out.println("\nDados para Teste");
        dadosTeste = new double[30][5];
        carga("iris_teste.txt",dadosTeste);
        escreveDados(dadosTeste);
        
        //define o número de vizinhos
        k=9;
        
        executaKnn();
    }
    
    /**
     * Carrega dos dados do arquivo iris.data para a matriz dados. A classe da planta, o 5o atributo, não é considerado.
     */
    public static void carga(String nome, double[][]dados){
        Scanner ler = new Scanner(System.in);
         
        //System.out.printf("\nConteúdo do arquivo texto:\n");
        try {
            FileReader arq = new FileReader(nome);
            BufferedReader lerArq = new BufferedReader(arq);
 
            String linha = lerArq.readLine(); 
            int i = 0;
            while (linha != null) {
               // System.out.printf("%s\n", linha);

                String[] valor = linha.split(",");       
                linha = lerArq.readLine(); 
                if(valor.length == 5) {
                    for(int j = 0; j < 4; j++)  dados[i][j] = Double.parseDouble(valor[j]);
                    if(valor[4].equals("Iris-virginica")) dados[i][4]=1;
                    else if(valor[4].equals("Iris-versicolor")) dados[i][4]=2;
                         else dados[i][4]=3;
                    i++;
                }
   
            }
            arq.close();
        } 
        catch (IOException e) {
                System.err.printf("Erro na abertura do arquivo: %s.\n",
                e.getMessage());
        }
    }
    
    /**
     * Escreve os dados 
     */
    public static void escreveDados(double [][] dados){
        //System.out.println("\n\n--------- D A D O S ---------");
        System.out.println("     x1  x2  x3  x4  classe");
        for(int i = 0; i < dados.length; i++) {
                System.out.print((i+1)+ " : ");
                for(int j = 0; j < dados[i].length; j++) {
                    System.out.print(dados[i][j] + " ");
                }
                System.out.println();
        }
    }
    
    
    /**
     * Calcula a distância eucliadiana entre um dado corrente (atual) e uma amostra
     */
    public static double euclidiana(double[] atual, double[] amostra) {
      double soma = 0;
      for(int i = 0; i < atual.length-1; i++) {
          soma += Math.pow(atual[i] - amostra[i], 2);
      }
      return Math.sqrt(soma);
    }
    
    
    public static void executaKnn(){
        int acertos = 0;
    	for(int i=0; i<dadosTeste.length; i++){
		distancia = new double[dadosTreino.length][2];
		for(int j=0; j<dadosTreino.length;j++){
			distancia[j][0] = euclidiana(dadosTeste[i],dadosTreino[j]);
			distancia[j][1] = dadosTreino[j][4];
    		}
    		//System.out.println("Antes");
    		//exibeDistancias(distancia);
    		ordena(distancia);
    		//System.out.println("Depois");
    		//exibeDistancias(distancia);
    		System.out.println("Classe Predita:" + moda(distancia));
    		//break;
    		
    	}
    }
  
   public static void ordena(double [][]distancia){
   	double []aux;
   	for(int i=0; i<distancia.length-1; i++){
   		for(int j=0; j<distancia.length-1-i; j++){
   			if(distancia[j][0]>distancia[j+1][0]){
   				troca(distancia[j],distancia[j+1]);
   			}
   		}
        }
   }
   
  public static void troca(double linha1[], double linha2[]){
  	double aux;
  	for(int i=0; i<linha1.length; i++){
  		aux = linha1[i];
  		linha1[i] = linha2[i];
  		linha2[i] = aux;
  	}
  }
  
  public static void exibeDistancias(double [][] distancia){
  	for(int i=0; i<distancia.length; i++){
  		System.out.println("Distancia: " + distancia[i][0] + " Classe do vizinho: " + distancia[i][1]);
  	}
  }
  
  public static int moda(double [][]distancia){
  	int rotulo, cont, classe=-1, quant=0;
  	for(int c=1; c<=3; c++){
  		cont = 0;
  		for(int i=0; i<k; i++){
  			if(distancia[i][1]==c) cont++;
  		}
  		if(cont>quant){
  			quant = cont;
  			classe = c;
  		}
  	}
  	return classe;
  }
    
}

```
