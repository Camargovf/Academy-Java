
Java ::: Coleções (Collections) ::: Set (Conjunto)

Java Collections - Como usar a interface Set em seus códigos Java
Quantidade de visualizações: 3445 vezes
A interface Set estende a interface Collection mas não adiciona novos métodos ou constantes. Em vez disso, esta interface define que uma instância de Set não contenha elementos duplicados. Esta responsabilidade é transferida para as classes que implementam a interface.

A classe abstrata AbstractSet é uma classe de conveniência que herda da classe também abstrata AbstractCollection e implementa a interface Set. A classe AbstractSet fornece implementações concretas para os métodos equals() e hashCode(). Estes métodos permitem a funcionalidade da não permissão de elementos duplicados nos conjuntos.

As classes concretas mais conhecidas da interface Set são:

HashSet - Esta classe é implementada em cima de uma tabela hash, ou seja, um array (matriz) na qual os elementos são armazenados em posições calculadas de acordo com o seu conteúdo. Uma característica interessante de HashSet é que os elementos raramente são retornados na mesma ordem na qual foram inseridos.

LinkedHashSet - Esta classe estende a classe HashSet com uma implementação de lista ligada (linked list) que permite a ordenação dos elementos no conjunto.

TreeSet - Esta classe é uma classe concreta que implementa a interface SortedSet. A interface SortedSet é uma sub-interface de Set que garante que os elementos no conjunto estejam ordenados. Além disso, esta interface fornece os métodos first() e last() para acessar o primeiro e o último elemento do conjunto. Há ainda os métodos headSet(toElement) e tailSet(fromElement) para retornar uma faixa do conjunto cujos elementos sejam "menores" que toElement e "maiores" que fromElement.

Seja qual for a implementação de Set que você queira usar, é sempre uma boa idéia codificar em cima da interface. Isso facilita a troca de HashSet por TreeSet ou vice-versa sem grandes modificações no seu código.

Veja um exemplo no qual usamos a classe concreta HashSet para representar um conjunto de cinco strings únicas:

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
package estudos;

import java.util.HashSet;
import java.util.Iterator;
import java.util.Set;

public class Estudos{
public static void main(String[] args) {
// vamos criar uma instância da classe HashSet
Set<String> conjunto = new HashSet<>();

    // vamos inserir cinco elementos no Set
    conjunto.add("Açucar");
    conjunto.add("Macarrão");
    conjunto.add("Feijão");
    conjunto.add("Carne");
    conjunto.add("Maionese");
     
    // vamos exibir os elementos inseridos
    Iterator iterator = conjunto.iterator();
    while(iterator.hasNext()){
      System.out.println(iterator.next());
    }
}
}


Ao executar este trecho de código teremos um resultado parecido com:

?
1
2
3
4
5
Macarrão
Feijão
Carne
Açucar
Maionese

Note que raramente os elementos serão exibidos na ordem na qual eles foram inseridos. Experimente agora trocar a linha:

Set<String> conjunto = new HashSet<>();

por

Set<String> conjunto = new LinkedHashSet<>();

Execute o código novamente e verá que agora os elementos são exibidos na mesma ordem que foram inseridos.