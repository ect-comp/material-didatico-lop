# Repetição contada 

Em programação, muitas vezes precisamos executar um conjunto de instruções várias vezes. Para isso, usamos estruturas de repetição, também conhecidas como laços. Existem dois tipos principais de laços: laços condicionais e laços contados. Vamos explorar esses conceitos de maneira didática para entender como e quando utilizá-los.

## Laço Condicional
Um laço condicional repete um bloco de código enquanto uma determinada condição é verdadeira. Não sabemos de antemão quantas vezes o laço irá se repetir, pois isso depende da condição especificada.

Exemplo com `while`:
```javascript
let contador = 0;
while (contador < 5) {
    console.log("Contador é:", contador);
    contador++;
}
```
Neste exemplo, a condição é `contador < 5`. O bloco de código dentro do while será repetido enquanto essa condição for verdadeira. Assim que `contador` se torna 5, a condição não é mais verdadeira e o laço termina.

Características do Laço Condicional:
* A condição de parada é avaliada a cada iteração.
* Não é possível prever o número de repetições.
* Ideal para situações onde a repetição depende de uma condição que pode mudar de forma imprevisível.

 
Laço Contado
Um laço contado repete um bloco de código um número específico de vezes. Aqui, o número de repetições é conhecido e controlado por um contador.

Exemplo com `for`:
```javascript
for (let i = 0; i < 5; i++) {
    console.log("Valor de i:", i);
}
```
Neste exemplo, `i` assume valores de 0 a 4, e o bloco de código é executado 5 vezes. Sabemos exatamente quantas vezes o laço irá se repetir.

Por que o `for` é mais adequado para laços contados?
* Definição clara dos parâmetros: Definimos o valor inicial, o limite e o incremento/decremento. O for calcula automaticamente o número de repetições.
* Foco no que é importante: Dentro do bloco do for, nos preocupamos apenas com as operações a serem repetidas, sem a necessidade de gerenciar manualmente o contador.
* Código mais compacto: O for geralmente resulta em menos linhas de código.
* Legibilidade: O código é mais legível e explícito quanto ao propósito de contar repetições.
* Redução de erros: Evita esquecer de inicializar, incrementar ou decrementar o contador, o que é comum em laços while.

Entender a diferença entre laços condicionais e contados é essencial para escrever códigos eficientes e claros. Use while quando a repetição depende de uma condição variável e for quando você sabe exatamente quantas vezes precisa repetir o bloco de código. Com a prática, a escolha da estrutura adequada se tornará cada vez mais intuitiva.

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


## Encontrando o Maior Elemento de uma Sequência com Repetição

Em programação, encontrar o maior (ou menor) elemento de uma sequência de números é uma tarefa comum que pode ser resolvida de forma simples utilizando estruturas de repetição. Vamos aprender como fazer isso usando um algoritmo intuitivo.

### Entendendo o Algoritmo

O algoritmo para encontrar o maior elemento de um grupo é bastante intuitivo. Vamos ilustrar isso com um exemplo prático.

**Exemplo:**
```
Vou mostrar vários números. Vocês devem me dizer qual é o maior.
Números: 9, -6, 10, 5, 0, -4, -13, 13, -7, 11

Qual o maior número?
Resposta: 13
```

Para encontrar o maior número, seguimos os seguintes passos:

1. **Início com o Trono Vazio**: Imaginamos que temos um trono onde o maior número sentará. No início, o trono está vazio.
2. **Primeiro Elemento**: O primeiro número vê o trono vazio e senta-se nele.
3. **Comparação dos Elementos Restantes**: Para cada número seguinte:
   - Comparamos o número atual com o número sentado no trono.
   - Se o número atual for maior, ele toma o lugar no trono.
4. **Resultado Final**: No final, o número que está no trono é o maior de todos.

### Algoritmo em Pseudocódigo

Vamos agora escrever esse processo em forma de algoritmo:

1. O primeiro elemento encontra o trono vazio e senta-se nele.
2. Para cada elemento restante do grupo:
   - Comparamos com o elemento sentado no trono.
   - Se for maior, este elemento vai para o trono.
3. Ao final, o elemento no trono é o maior.

### Implementação em JavaScript

Vamos implementar este algoritmo em JavaScript para encontrar o maior número de uma sequência.

```javascript
let numeros = [9, -6, 10, 5, 0, -4, -13, 13, -7, 11];

// Inicialmente, consideramos o primeiro elemento como o maior
let maior = numeros[0];

// Usamos uma estrutura de repetição para comparar os demais elementos
for (let i = 1; i < numeros.length; i++) {
    if (numeros[i] > maior) {
        maior = numeros[i]; // O novo maior número assume o "trono"
    }
}

console.log("O maior número é:", maior);
```

**Explicação do Código:**
- **Inicialização**: A variável `maior` é inicializada com o primeiro número da lista.
- **Estrutura de Repetição**: Usamos um laço `for` para percorrer todos os elementos restantes da lista.
- **Comparação e Atualização**: A cada iteração, comparamos o elemento atual com o valor em `maior`. Se o elemento atual for maior, atualizamos `maior` com esse novo valor.
- **Resultado**: Ao final do laço, a variável `maior` contém o maior número da lista.

O processo de encontrar o maior (ou menor) elemento de uma sequência utilizando repetição é direto e intuitivo. Ao seguir um algoritmo simples e implementá-lo em uma linguagem de programação como JavaScript, podemos resolver esse tipo de problema de forma eficiente e clara.






