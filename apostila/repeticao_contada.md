# Repetição contada 

## Laço condicional x Laço contado
* Laço condicional: As repetições são controladas por uma condição de parada. Porém, não é possível prever quando vai parar a repetição ou quantas repetições vão ocorrer. A repetição termina quando não satisfaz (não é verdadeira) a condição do comando enquanto (while), ou seja quant alcança aa  chega a condição de parada.
* Laço contado: Repetições controladas por um contador e a quantidade de repetições a seren realizadas são conhecidas e associada ao contador do laço.  

Por que o for é mais adequado para laços contados?
* Definindo o valor inicial, o limite e o incremento/decremento,  já calcula automaticamente quantas vezes o laço irá repetir.
* Dentro do for, entre as chaves do for(bloco), podemos nos preocupar somente com a parte que repete
* Mais compacto (código menor)
* Mais legível ou explícito para o objetivo de contar as repetições
* Ajuda a não esquecer de inicializar e de incrementar/decrementar no código


## Sintaxe 

```javascript
    for ( local para inicialização ; local para condição; local para incremento/decremento )
    {
   	 // Local para as instruções  
    }
``` 
O comando for é lido da seguinte forma: "Para os seguintes valores iniciais, e enquanto a condição for verdadeira, execute as instruções e incremente/decremente."

Descrevendo as 3 cláusulas:
* Cláusula de inicialização
  * Executada uma única vez
  * Executada antes do primeiro teste
  * Permite múltiplas inicializações
  * Opcional
* Cláusula da condição
  * Semelhante à condição do while
  * Obrigatória
* Cláusula do incremento/decremento
  * Executada sempre após as instruções serem executadas
  * Permite múltiplos incrementos/decrementos
  * Opcional


## Exemplo 1 

Implemente um programa que recebe 15 números reais e calcula seus quadrados.
* "Para a quantidade de quadrados calculados, inicialmente zero, e enquanto for menor que 15, receba um número, calcule e imprima seu quadrado e incremente essa quantidade em 1."

```javascript
for ( contador = 0; contador < 15; contador++)
{
   numero = parseFloat(prompt("Entre com um número:"));
   quadrado = numero * numero;
   alert("Quadrado: "+quadrado);
}
```

## Exercícios - Parte 1 
Determine quais números serão impressos em cada for:

1. for  ( i = 0 ; i < 10 ; i++ ) { alert(i); }
1. for  ( i = 0 ; i < 100 ; i+=10 ) { alert(i); }
1. for  ( i = 0 ; i < 100 ; i=i+2 ) { alert(i); }
1. for  ( i = 10 ; i > 0 ; i-- ) { alert(i); }
1. for  ( i = 101 ; i < 150 ; i+=2 ) { alert(i); }
1. for  ( i = 1 ; i <= 1024 ; i=i*2 ) { alert(i); }

Executar estes exemplos no ambiente de programação online e analisar as saídas de cada exercício. 

## Formas variadas de usar o **for**
Outros usos também válidos do for (embora diferentes)
* for  ( ; i < 10 ; ) 
* for  ( i = 0, j = 0 ; i < 10 ; i++, j++ )
* for  ( i = 0, k = 0 ; i < 10 || k > -10 ; )
* for  ( i = 0 ; i != j + k ; i++ )
* for  ( i = Math.sqrt(j) ; i <= Math.pow(j,3) ; i++ )
* for  ( i = 0, j = 10, k = -10 ; i < 10 ; i++, j--, k/=2 )

## Exercícios - Parte 2 

1 - Implemente um programa que escreve os 50 primeiros (rode só com 5):
* Números naturais
* Números naturais pares
* Números quadrados

2 - Implemente um programa que receba a idade de 80 pessoas (rode só com 8) e determina a média da idade das pessoas.

## Algoritmos Tradicionais 
Em programação, embora existam vários tipos de problemas, alguns deles são mais frequentes
* Entender bem e aprender a solução (algoritmo) de cada um deles
* Identificar as pequenas diferenças de cada problema específico

* Contagem 
* Somatório/Produtório 
* Encontrar o melhor valor 

### Contador do for 

Em problemas de laço contado, usamos uma variável numérica para controlar as repetições: 
* Dizemos que essa variável é o contador do for
* O número de repetições depende do seu valor inicial, do seu valor limite e do incremento/decremento
* Seu significado ou uso depende da lógica adotada para cada problema, e de como podemos aproveitar esta variável diretamente no código para obter as saídas

O contador pode ser aplicado com diferentes lógicas de uso: 

Exemplo: “Implemente um programa que recebe peso e altura de 100 pessoas, calcula e imprime o IMC de cada uma.”

Qual a lógica do uso do contador em cada for para o problema acima?
* for ( cont = 0 ; cont < 100 ; cont++ )
  * “quantidade de pessoas cujo IMC já foi calculado”
* for ( cont = 1 ; cont <= 100 ; cont++ )
  * “número ou ordem da pessoa cujo IMC está sendo calculado”
  * 1ª pessoa, 2ª pessoa, …, 100ª pessoa
* for ( cont = 100 ; cont > 0 ; cont-- )
  * “quantidade de pessoas cujo IMC falta calcular”


“Implemente um programa que escreve na tela todos os números entre 300 e 400 (inclusive) que são múltiplos de 8.”


## Exemplo 2 

“Implemente um programa que escreve na tela todos os números entre 300 e 400 (inclusive) que são múltiplos de 8.”
* O que vai ser repetido?
* Quantas repetições serão realizadas?

É possível utilizar uma mesma variável para dois papéis  diferentes
* A variável cont se usa, ao mesmo tempo, para controlar a quantidade de repetições e para ser o número testado

```javascript
resultado = "R: "    //uma variável string pode ser usada para
                     //mostrar a saída
for ( cont = 300; cont <= 400; cont++){
  if ( cont % 8 == 0) {
    resultado = resultado + cont + " "
  }
}
alert(resultado)
```


## Exemplo 3 

“Implemente um programa que escreva os  termos da sequência a seguir, iniciando do 10º até o 20º (inclusive).”
* S = (1/1, 1/3, 1/5, 1/7, 1/9, ...  )

```javascript
S=""; //usando string (mas não é obrigatório)
for ( i = 10; i<= 20; i++){
        termo_i=" 1 /"+(2*i-1)+", "
        S =S+ termo_i;
}
alert(S);
``` 

## Somatório 

O que entendemos por acumular valores (soma parcial)?

“Implemente um programa que recebe 2 números inteiros A e B. O programa deve acumular/somar o valor de B ao valor de A e imprimir o resultado.”

Acumulador: Adicionar/somar um novo valor a algum valor já existente.

O acúmulo dos valores é a soma parcial dos valores, armazenado em uma mesma variável que já existia, mudando o valor que tinha.

```javascript
A=A+B;
alert(A);
```

## Exemplo 4 

“Implemente um programa que calcula o somatório de todos os números entre 300 e 400 (inclusive).”

Para resolver problemas de somatório, devemos:
*  Inicializar uma variável somatório em zero (termo neutro)  
* Calcular cada termo do somatório
  * Obs.: Os números de 300 a 400 formam uma sequência
* Acumular cada termo do somatório
  * Inicializado com o termo neutro
* Escrever o resultado
  * Depois de acumular todos os valores

```javascript
Soma=0;
for ( i = 300; i<= 400; i++){
  Soma =Soma+i;
}
alert(Soma);
```

## Exemplo 5
Implemente um programa que calcula a soma dos 10 primeiros termos da sequência abaixo:
* S = (1/1, 1/3, 1/5, 1/7, 1/9, ...  )

Série é a soma dos termos de uma sequência. Podemos reescrever o enunciado do exemplo assim:
* S=1 + 1/3 + 1/5 + 1/7 + 1/9 + ...

```javascript
Soma=0;
for ( i = 1; i<= 10; i++){
  termo_i=1/(2*i-1)
  Soma =Soma+termo_i;
}
alert(Soma);
```

## Produtório 

“Implemente um programa que recebe um número natural N e calcula N!”

Fatorial
* O fatorial de N, ou N!, nada mais é que o produtório de N; 

Fatorial = 1 * 2 * 3 * ... * N 









