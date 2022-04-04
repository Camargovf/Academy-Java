A Matriz quadrada é um tipo especial de matriz que possui o mesmo número de linhas e o mesmo número de colunas, ou seja, dada uma matriz Anxm, ela será uma matriz quadrada se, e somente se, n = m, onde n é o número de linhas e m é o número de colunas.

Em geral as matrizes quadradas são chamadas de Matrizes de Ordem n, onde n é o número de linhas e colunas. Dessa forma, uma matriz de ordem 4 é uma matriz que possui 4 linhas e quatro colunas.

Toda matriz quadrada possui duas diagonais, e elas são muito exploradas tanto na matemática quanto na construção de algorítmos. Essas duas diagonais são chamadas de Diagonal Principal e Diagonal Secundária.

A diagonal principal de uma matriz quadrada une o seu canto superior esquerdo ao canto inferior direito. 

Nesta dica veremos como calcular a soma dos valores dos elementos da diagonal principal de uma matriz usando Java. Para isso, só precisamos manter em mente que a diagonal principal de uma matriz A é a coleção das entradas Aij em que i é igual a j. Assim, tudo que temos a fazer é converter essa regra para código Java.

Veja um trecho de código Java completo no qual pedimos para o usuário informar os elementos da matriz e em seguida mostramos a soma dos elementos da diagonal superior:

?
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
package arquivodecodigos;

import java.util.Scanner;

public class Estudos{
public static void main(String[] args) {
// vamos fazer a leitura usando a classe Scanner
Scanner entrada = new Scanner(System.in);

    // vamos declarar e construir uma matriz de três linhas e três colunas
    int matriz[][] = new int[3][3];
    int soma_diagonal = 0; // guarda a soma dos elementos na diagonal principal
      
    // vamos ler os valores para os elementos da matriz
    for(int i = 0; i < matriz.length; i++){ // linhas
      for(int j = 0; j < matriz[0].length; j++){ // colunas
        System.out.print("Informe o valor para a linha " + i + " e coluna " 
          + j + ": ");
        matriz[i][j] = Integer.parseInt(entrada.nextLine());       
      }       
    }
      
    // vamos mostrar a matriz da forma que ela
    // foi informada
    System.out.println();
    // percorre as linhas
    for(int i = 0; i < matriz.length; i++){ 
      // percorre as colunas
      for(int j = 0; j < matriz[0].length; j++){ 
        System.out.printf("%5d ", matriz[i][j]);
      }
      // passa para a próxima linha da matriz
      System.out.println();
    }
      
    // vamos calcular a soma dos elementos da diagonal   
    // principal
    for(int i = 0; i < matriz.length; i++){
      for(int j = 0; j < matriz[0].length; j++){
        if(i == j){
          soma_diagonal = soma_diagonal + matriz[i][j];
        }
      }
    }
      
    // finalmente mostramos a soma da diagonal principal
    System.out.println("\nA soma dos elementos da diagonal principal é: " 
      + soma_diagonal);
}
}

Ao executar este código Java nós teremos o seguinte resultado:

?
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
Informe o valor para a linha 0 e coluna 0: 3
Informe o valor para a linha 0 e coluna 1: 7
Informe o valor para a linha 0 e coluna 2: 9
Informe o valor para a linha 1 e coluna 0: 2
Informe o valor para a linha 1 e coluna 1: 4
Informe o valor para a linha 1 e coluna 2: 1
Informe o valor para a linha 2 e coluna 0: 5
Informe o valor para a linha 2 e coluna 1: 6
Informe o valor para a linha 2 e coluna 2: 8

    3     7     9 
    2     4     1 
    5     6     8 

A soma dos elementos da diagonal principal é: 15

