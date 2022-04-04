Pergunta/Tarefa:

Escreva um programa Java que inverte uma palavra, frase ou texto usando recursividade. Seu programa deverá pedir para o usuário informar a string a ser invertida.

Sua saída deverá ser parecida com:

?
1
2
3
4
Informe uma palavra, frase ou texto: Arquivo de Códigos
A string informada foi: Arquivo de Códigos
A string invertida é:
sogidóC ed oviuqrA
Resposta/Solução:

Veja a resolução comentada deste exercício usando Java console:

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
package exercicio;

import java.util.Scanner;

public class Exercicio {
public static void main(String[] args) {
// cria um novo objeto da classe Scanner
Scanner entrada = new Scanner(System.in);

    // vamos pedir para o usuário informar a string
    System.out.print("Informe uma palavra, frase ou texto: ");
    String texto = entrada.nextLine();
     
    // mostra a string informada
    System.out.println("A string informada foi: " + texto);
     
    // agora mostramos a string invetida
    System.out.println("A string invertida é:");
    inverterString(texto);
}

// método recursivo que recebe uma string e a imprime de forma inversa
public static void inverterString(String string) {
// a string está vazia?
if((string == null) || (string.length() <= 1)){
System.out.print(string);
}
// vamos fazer mais uma chamada recursiva
else {
System.out.print(string.charAt(string.length() - 1));
inverterString(string.substring(0, string.length() - 1));
}
}
}


