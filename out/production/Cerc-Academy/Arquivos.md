Nesta dica mostrarei como podemos usar o método delete() da classe File da linguagem Java para excluir um arquivo no computador local. Se o arquivo for excluído com sucesso, o retorna será true, e false em caso contrário.

Veja o código completo para o exemplo:

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
package arquivodecodigos;

import java.io.*;

public class Estudos{
public static void main(String[] args){
File arquivo = new File("C:\\estudos_java\\osmar.txt");

    if(arquivo.delete()){
      System.out.println("Arquivo excluido com sucesso.");
    }
    else{
      System.out.println("Não foi possivel excluir o arquivo");
    }
}
}

Ao executar este código nós teremos o seguinte resultado:

Arquivo excluido com sucesso.
