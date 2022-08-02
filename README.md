# Metodos-em-Java-


Ir para o conteúdo principal
Damares Costa de Souza 
Moodle - IFRS

Programação Básica com Java III - Turma 2022B
Painel Meus cursos  PBJIII2022B 4. Procedimentos, Funções e Métodos  4.7. Construindo Métodos em Java
4.7. Construindo Métodos em Java
Nas seções anteriores estudamos como dividir algoritmos em partes menores chamadas sub-algoritmos. Agora passaremos a estudar como implementar procedimentos e funções em nossos programas em Java, através do uso de um recurso chamado método. Já falamos sobre o uso de métodos anteriormente, mas agora aprenderemos a construir nossos próprios para os mais diferentes fins.

Um método em Java é um conjunto de instruções que, assim como os procedimentos e funções, pode receber dados externos (os parâmetros) e devolver resultados (como as funções). Trabalharemos neste capítulo com um tipo especial de métodos em Java, chamado de métodos estáticos. Estes métodos são utilizados diretamente a partir das classes em que foram definidos e não necessitam de instâncias para serem executados. Existe outro tipo de métodos que você deve estudar futuramente, ao conhecer a programação orientada a objetos. Infelizmente este assunto está fora do escopo deste curso.

Todos os programas que escrevemos até agora utilizavam uma abordagem chamada monolítica. Nesta abordagem, todo o código do programa é escrito em um único conjunto de instruções.

A partir de agora, escreveremos programas que utilizam a abordagem modular. Iremos escrever programas que dividem seu código em diversos procedimentos e funções, utilizando o conceito de métodos.

Assim como nos algoritmos, para criarmos um método em Java precisamos defini-lo dentro de uma classe. Como todos os programas em Java são classes, podemos definir métodos dentro das classes de nossos programas. O formato geral de uma definição de método estático em Java que utilizaremos neste capítulo é mostrado abaixo.



static tipo de retorno nome do método ( parâmetros )

{

instruções

}



A palavra static é usada para especificar que o método definido é estático. Por enquanto, em todos os métodos que escrevermos, utilizaremos essa palavra. O restante da definição do método é semelhante à definição de uma função na forma:

                 função nome do método ( parâmetros ) : tipo de retorno
                 início
                        instruções
                 fim

Como todas as definições de métodos exigem um valor de retorno, todos os métodos em Java se comportam como funções. Mas sendo assim, como implementar procedimentos em Java? Para contornar esse problema, existe um tipo especial em Java chamado void. O tipo void, quando usado como tipo de retorno de um método, especifica que o método não irá retornar valores. Logo, se desejamos implementar um procedimento em Java, basta criarmos um método cujo tipo de retorno é void.

A lista de parâmetros na definição de métodos em Java é uma lista separada por vírgulas, na qual o método declara o nome e o tipo de cada parâmetro. Diferentemente dos algoritmos, para cada parâmetro deve ser especificado seu tipo, mesmo que existam vários parâmetros consecutivos com o mesmo tipo. Por exemplo, um método chamado media que calcula a média de dois números reais, poderia ser definido da seguinte forma:


         static double media ( double a, double b )
         {
            ...
         }

onde a e b são os nomes dos parâmetros. A declaração

         static double media ( double a, b )
         {
            ...
         }


produziria um erro de sintaxe no programa, pois para cada parâmetro deve ser especificado um tipo. Assim como nos algoritmos, cada parâmetro real passado a um método deve ser compatível com o tipo do parâmetro correspondente na definição do método. Por exemplo, um parâmetro do tipo double pode receber valores 7.35, 22 ou -0.03546, mas não “teste” (porque um valor do tipo String não pode ser atribuído a uma variável double). Se um método não recebe nenhum valor, a lista de parâmetros será vazia (isto é, após o nome do método há um conjunto vazio de parênteses).

O código abaixo mostra uma implementação para o algoritmo mostrado no tópico sobre funções (4.4).


1      public class Quadrado2 {

2

3            static double quad( double num ) {

4                   double resultado;

5                   resultado = num * num;

6                   return resultado;

7            } // fim do metodo quad

8

9            public static void main(String[] args) {

10                  double N;

11

12                  System.out.print(“Numero: “);

13                  N = Double.parseDouble(System.console().readLine());

14

15                  System.out.printf(“O quadrado do número é %f\n”,

16                                                    quad(N));

17

18           } // fim do metodo main

19

20     } // fim da classe Quadrado2



Neste exemplo, é definido um método chamado quad, que recebe um parâmetro do tipo double e retorna o quadrado dele. Veja que o comando equivalente a retorne em Java é return. O funcionamento do comando return é idêntico ao de retorne. Na linha 4 é declarada uma variável local ao método quad, chamada resultado. Assim como no programa, dentro de métodos podemos definir variáveis locais em qualquer lugar dentro do conjunto de instruções do método. Assim como em pseudocódigo, as variáveis locais são visíveis apenas no método onde foram declaradas.


Olhando para a definição de main, podemos perceber que ele também é um método estático que recebe um parâmetro e não retorna valor (pois o tipo de retorno é void). Vínhamos definindo métodos desde o início e não sabíamos! Todo programa Java é uma classe que define um método chamado main. Podemos definir classes sem main, mas essas classes não podem ser executadas como programas.

Como main é um método, toda variável declarada dentro dele é uma variável local ao método. Ou seja, não podemos utilizar variáveis declaradas dentro de main em outros métodos da classe. Por exemplo, utilizar a variável N declarada no método main da figura anterior seria um erro, pois ela é visível somente dentro do método main. Em outras palavras, variáveis declaradas dentro do método main não são globais.
Note que na linha 16 não escrevemos o nome da classe antes do nome do método, quando o invocamos. Quando um método é chamado dentro da própria classe em que é definido, isso não é necessário.

Última atualização: domingo, 1 nov 2020, 20:37
Seguir para...
Academi
Dúvidas? 
Perguntas frequentes

Fale conosco | Suporte | Contato

Informação
Termos e Condições de Uso
Aviso de Privacidade e Proteção de Dados Pessoais
Contato
Rua Gen. Osório, 348, Bento Gonçalves/RS
Siga-nos
Copyright © 2017 - Desenvolvido por LMSACE.com. Distribuído por Moodle
