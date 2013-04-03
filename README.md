Jtme
====

Java Text Mode Emulator - Emulador de Modo Texto para Java

Emula o modo texto em aplicações Java. Criado especialmente para atender o projeto APFJogos (www.apfjogos.com)

Há 3 formas de se usar:
1 - chamando a função diretamente pela classe;
2 - estendendo a classe que será usada;  ou
3 - instanciando a classe Jtme.

Exemplo usando a forma 1:
-------------------------

public class Teste {

  public static void main(String[] args) {
    Jtme.println("Bem vindo ao Jtme");
  }

}


Exemplo usando a forma 2:
-------------------------

public class Teste extends Jtme {

  public static void main(String[] args) {
    println("Bem vindo ao Jtme");
  }

}


INSTRUÇÕES
==========

Impressão:
----------
gotoXY(x,y);                                      // posiciona cursor na coordenada (x,y)
clrScr();                                         // apaga toda a tela
clrEol();                                         // apaga o restante da linha a partir do cursor
print(String s);                                  // imprime uma string na tela
println(String s);                                // imprime uma string na tela e muda de linha


Cursor de Tela:
---------------
cursorOn();                                       // exibe o cursor na tela
cursorOff();                                      // não exibe o cursor na tela
setCursorMode(boolean b);                         // indica o tipo de exibição do cursor
getCursorMode();                                  // pega o estado de exibição do cursor
getCursorX();                                     // pega o valor da coluna do cursor
getCursorY();                                     // pega o valor da linha do cursor


Cores:
------
resetColors();                                    // reseta a cor do texto e de fundo para as cores padrões
setBackGroundColor(Color backgroundColor);        // seta a cor de fundo (muda todas as cores de fundo)
setTextColor(Color textColor);                    // seta a cor do texto (muda todas as cores de texto)


Temporização:
-------------
delay(int x);                                     // espera x milissegundos


Teclado e Digitação:
--------------------
isKeyPressed();                                   // verifica se alguma tecla está sendo pressionada
readKey();                                        // pega a tecla pressionada pelo usuário
typeText();                                       // permite o usuário digitar um texto na tela (retorna a String)
typeTextln();                                     // permite o usuário digitar um texto na tela (retorna a String) e muda de linha
typeText(Object... args);                         // imprime texto e permite o usuário digitar um texto na tela (retorna a String)
typeTextln(Object... args);                       // imprime texto, permite o usuário digitar um texto na tela (retorna a String) e muda de linha



MELHORIAS A SEREM FEITAS:
=========================

 *  1- melhorar a velocidade do piscar do cursor para que fique igual, ou parecido, na maioria das CPUs
 *  2- verificar tamanho da fonte para colocar espaçamento correto
 *  3- melhorar a utilização do teclado, que difere em computadores mais rápidos e em computadores mais lentos)
 *  4- melhorar a constância de velocidade nas interações (ora fica mais lento, ora fica no tempo normal)
 * 
