Ex: 1 - Suponhamos que um produto que custe R$ 178,00 sofra um acréscimo de 15%. Qual o valor final do produto? Veja o código em Java:

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
public class Estudos{
public static void main(String args[]){
double valor = 178.00; // valor original
double percentual = 15.0 / 100.0; // 15%
double valor_final = valor + (percentual * valor);

    System.out.println("O valor final do produto é: " +
      valor_final);   
 
    // O resultado será 204,70
 
    System.exit(0);
}
}

Ex: 2 - Um produto, cujo valor original era de R$ 250,00, teve um desconto de 8%. Qual foi seu valor final? Veja o código em Java:

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
public class Estudos{
public static void main(String args[]){
double valor = 250.00; // valor original
double percentual = 8.0 / 100.0; // 8%
double valor_final = valor - (percentual * valor);

    System.out.println("O valor final do produto é: " +
      valor_final);   
 
    // O resultado será 230,00
 
    System.exit(0);
}
}

Ex: 3 - Em um concurso de perguntas e respostas, um jovem acertou 72 das 90 perguntas apresentadas. Qual foi a porcentagem de acertos? E a porcentagem de erros? Veja o código em Java:

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
public class Estudos{
public static void main(String args[]){
double perguntas = 90.0;
double acertos = 72.0;

    System.out.println("Porcentagem de acertos: " +
      ((acertos / perguntas) * 100) + "%");
 
    System.out.println("Porcentagem de erros: " +
      (((perguntas - acertos) / perguntas) * 100) + "%");   
 
    // Os resultados serão 80% e 20%
 
    System.exit(0);
}
}

Ex: 4 - Um aparelho de CD foi adquirido por R$ 300,00 e revendido por R$ 240,00. Qual foi a porcentagem de lucro na transação? Veja o código em Java:

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
public class Estudos{
public static void main(String args[]){
double v_ant = 300.0; // valor anterior
double v_nov = 340.0; // valor novo
double p_lucro = 0.0; // porcentagem de lucro

    while(v_ant + ((p_lucro / 100.0) * v_ant) < v_nov){
      p_lucro = p_lucro + 0.1;
    } 
 
    System.out.println("A porcentagem de lucro foi de: " +
      p_lucro + "%");   
 
    // O resultado será 13,39
 
    System.exit(0);
}
}

Ex: 5 - Uma loja repassa 5% do lucro a seus vendedores. Se um produto custa R$ 70,00, qual o valor em reais repassado a um determinado vendedor? Veja o código em Java:

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
public class Estudos{
public static void main(String args[]){
double valor = 70.0; // valor do produto
double porcent = 5.0 / 100.0; // 5%

    double comissao = porcent * valor;
 
    System.out.println("O valor repassado ao vendedor e: " +
      comissao); 
 
    // O resultado será 3,5
 
    System.exit(0);
}
}
