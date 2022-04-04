Novos elementos podem ser adicionados a um HashSet por meio do método add(), definido originalmente na interface Collection<E> e sobrescrevendo a versão herdada de AbstractCollection<E>. Este método possui a seguinte assinatura:

?
1
public boolean add(E e)
Veja que este método recebe o elemento a ser adicionado e retorna true se o elemento foi inserido com sucesso e false em caso contrário. Note que o elemento será inserido somente se este ainda não estiver contido no conjunto. Veja o seguinte trecho de código:

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
package estudos;

import java.util.HashSet;
import java.util.Iterator;
import java.util.Set;

public class Estudos{
public static void main(String[] args) {
// vamos criar uma instância da classe HashSet
Set<Integer> conjunto = new HashSet<>();

    // vamos tentar inserir três inteiros neste conjunto
    if(conjunto.add(5)){
      System.out.println("Elemento inserido com sucesso.");  
    }
    else{
      System.out.println("O elemento não foi inserido.");
    }
     
    if(conjunto.add(7)){
      System.out.println("Elemento inserido com sucesso.");  
    }
    else{
      System.out.println("O elemento não foi inserido.");
    }
     
    if(conjunto.add(5)){
      System.out.println("Elemento inserido com sucesso.");  
    }
    else{
      System.out.println("O elemento não foi inserido.");
    }
     
    // vamos exibir os elementos inseridos com sucesso
    Iterator iterator = conjunto.iterator();
    while(iterator.hasNext()){
      System.out.println(iterator.next());
    }
}
}

Ao executar este código teremos o seguinte resultado:

?
1
2
3
4
5
Elemento inserido com sucesso.
Elemento inserido com sucesso.
O elemento não foi inserido.
5
7
Veja que o segundo valor 5 não foi inserido, uma vez que o mesmo já estava na coleção. Lembre-se de que objetos da classe HashSet aceitam o elemento null.
