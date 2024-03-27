# Estruturas Condicionais

## Introdução

Uma estrutura condicional é uma construção que permite que um programa tome decisões com base em condições específicas. Ela permite que o programa avalie uma expressão lógica e execute diferentes conjuntos de instruções, dependendo se a condição é verdadeira ou falsa.

A estrutura condicional mais comum é o "if-else", que geralmente segue esta sintaxe:
```javascript
Se (condição) então
    // bloco de código executado se a condição for verdadeira
Senão
    // bloco de código executado se a condição for falsa
Fim Se
```

Funcionamento de uma estrutura condicional em um programa:
1. **Avaliação da Condição**: O programa avalia uma expressão lógica ou uma condição. Por exemplo, a condição pode ser algo como "se o valor de x for maior que 10".
1. **Execução do Bloco de Código**: Se a condição for verdadeira, o programa executa o bloco de código associado ao "então". Isso pode incluir uma ou várias instruções que serão executadas se a condição for atendida.
1. **Execução do Bloco de Código Alternativo**: Se a condição não for verdadeira, o programa pode executar um bloco de código alternativo associado ao "senão", ou pode simplesmente continuar a execução do código após a estrutura condicional.

## Bloco de Código 
Um bloco de código é um conjunto de instruções agrupadas entre chaves `{}`. Esses blocos são usados para agrupar múltiplas instruções em uma única unidade de execução. Os blocos de código são comumente usados em estruturas condicionais (como `if`, `else`, `else if`), loops ( `for`, `while`, `do-while`), funções e em muitos outros contextos onde é necessário agrupar instruções.

Sintaxe para um bloco de código em JavaScript: 
```javascript
{
    // Aqui vão as instruções do bloco de código
}
```
## Exemplo Inicial 

Exemplo de um código em JavaScript para a estrutura condicional `if-else`: 
```javascript
let idade = 20;

if (idade >= 18) {
    // Bloco de código executado se a idade for maior ou igual a 18
    console.log("Você é maior de idade.");
} else {
    // Bloco de código executado se a idade for menor que 18
    console.log("Você é menor de idade.");
}
```
Neste exemplo, se a idade for maior ou igual a 18, o programa imprimirá "Você é maior de idade.". Caso contrário, imprimirá "Você é menor de idade.".

No exemplo anterior, o bloco de código dentro das chaves `{}` após `if (idade >= 18)` e `else` contém as instruções a serem executadas com base na condição da idade.

Os blocos de código ajudam a organizar o código, tornando-o mais legível e facilitando a manutenção. Eles também ajudam a isolar o escopo de variáveis e outras declarações, limitando sua visibilidade a apenas dentro do bloco em que foram definidos. Isso contribui para evitar problemas de poluição do escopo e colisões de nomes de variáveis em programas JavaScript.

As estruturas condicionais são fundamentais para a tomada de decisões em programas de computador. Elas permitem que os programas sejam flexíveis e dinâmicos, respondendo a diferentes situações com comportamentos apropriados. Além do "if-else", existem outras estruturas condicionais, como "switch-case" em algumas linguagens de programação, que oferecem formas mais avançadas de controle de fluxo baseado em condições.

## Estrutura condicional simples
A estrutura condicional simples permite a execução de um grupo de instruções (ou bloco de instruções) quando determinadas condições forem satisfeitas.

Sintaxe: 
* “**if**” em inglês significa “**se**” em português
```javascript
if ( <condição> ) 
{
  <instrução 1>
  <instrução 2>
  <instrução 3>

}
```
## Atividade 1 
Escreva um algoritmo que recebe as 3 notas de um aluno e escreve na tela a palavra “Aprovado” caso sua média seja maior ou igual a 5.0. 
```javascript
nota1 = parseFloat(prompt("Entre com a nota 1:"))
nota2 = parseFloat(prompt("Entre com a nota 2:"))
nota3 = parseFloat(prompt("Entre com a nota 3:"))

media = (nota1 + nota2 + nota3)/3

if (media > 5){
    alert("Aprovado")
}
```

## Operadores relacionais
Operadores relacionais são utilizados em linguagens de programação para comparar valores e expressões, resultando em um valor booleano (**verdadeiro** ou **falso**) que indica se a relação entre os operandos é verdadeira ou falsa. Esses operadores são comumente usados em estruturas condicionais e em expressões que envolvem tomada de decisões.

Símbolo em JavaScript | Descrição | Exemplo que retorna verdadeiro 
----------------------|-----------|----------
Igual (==) | Retorna verdadeiro caso os operandos sejam iguais | 3 == var1, "3" == var1 e 3 == '3' 
Diferente  (!=) | 	Retorna verdadeiro caso os operandos não sejam iguais. | var1 != 4 e var2 != "3"
Estritamente igual (===) | Retorna verdadeiro caso os operandos sejam iguais e do mesmo tipo. |	3 === var1 
Maior que (>) | Retorna verdadeiro caso o operando da esquerda seja maior que o da direita. | var2 > var1 e "12" > 2
Maior que ou igual (>=) | Retorna verdadeiro caso o operando da esquerda seja maior ou igual ao da direita. |  var2 >= var1
Menor que (<) | Retorna verdadeiro caso o operando da esquerda seja menor que o da direita. | var1 < var2
Menor que ou igual (<=) | 	Retorna verdadeiro caso o operando da esquerda seja menor ou igual ao da direita. | var1 <= var2

Exemplos simples com estes operadores: 
```javascript
let a = 5;
let b = 10;

console.log(a == b);  // Falso, porque 5 não é igual a 10
console.log(a != b);  // Verdadeiro, porque 5 é diferente de 10
console.log(a > b);   // Falso, porque 5 não é maior que 10
console.log(a < b);   // Verdadeiro, porque 5 é menor que 10
console.log(a >= b);  // Falso, porque 5 não é maior ou igual a 10
console.log(a <= b);  // Verdadeiro, porque 5 é menor ou igual a 10
```

## Estrutura Condicional Composta 
A estrutura condicional composta permite a seleção entre dois blocos de instruções a partir de uma única condição.

Sintaxe:
```javascript
if ( <condição> ) 
{
  <instrução 1>
  <instrução 2>
  <instrução 3>

} 
else 
{
  <instrução 4>
  <instrução 5>
  <instrução 6>
}
```
## Atividade 2
Escreva um algoritmo que recebe as 3 notas de um aluno e escreve na tela a palavra “Aprovado” caso sua média seja maior ou igual a 5.0, e “Reprovado”, caso contrário.

```javascript
nota1 = parseFloat(prompt("Entre com a nota 1:"))
nota2 = parseFloat(prompt("Entre com a nota 2:"))
nota3 = parseFloat(prompt("Entre com a nota 3:"))

media = (nota1 + nota2 + nota3)/3

if (media > 5){
    alert("Aprovado")
}
else {
    alert("Reprovado")
}
```

## Estrutura Condicional Aninhada 
A estrutura condicional aninhada permite a seleção entre diversos blocos de instruções.

Sintaxe:
```javascript
if ( <condição> ) 
{
  if ( <condição> ) 
  {
    <instrução 1> 
  } 
  else 
  {
    <instrução 2> 
  }
} 
else 
{
  <instrução 3> 
}
```

## Atividade 3
Escreva um algoritmo que recebe as 3 notas de um aluno e escreve na tela a palavra “Aprovado” caso sua média seja maior ou igual a 5.0, “Reprovado” caso sua média seja menor que 3.0, ou “Recuperação” caso sua média esteja entre 3.0 e menor que 5.0.

```javascript
nota1 = parseFloat(prompt("Entre com a nota 1:"))
nota2 = parseFloat(prompt("Entre com a nota 2:"))
nota3 = parseFloat(prompt("Entre com a nota 3:"))

media = (nota1 + nota2 + nota3)/3

if (media > 5){
    alert("Aprovado")
}
else {
    if (media > 3){
        alert("Recuperação")
    }
    else {
        alert("Reprovado")
    }
}
```
## Aplicações

### Teste de Divisibilidade 
Implemente um programa que verifica se um dado número inteiro é **divisível por 6**. 
```javascript
x = parseInt(prompt("Entre com número inteiro:"))
if ( x % 6 == 0) {
   alert("Divisível por 6")
}
```

Implemente um programa que verifica se um dado número inteiro é **divisível por 3, mas não por 5**.
```javascript
x = parseInt(prompt("Entre com número inteiro:"))
if ( x % 3 == 0) {
    if ( x % 5 != 0) {
       alert("Divisível por 3, mas não por 5")
   }
}
```

Implemente um programa que verifica se um dado número inteiro **é ímpar**. Uma possível solução é verificar se o número não é divisível por 2, ou seja, não é par.  
```javascript
x = parseInt(prompt("Entre com número inteiro:"))
if ( x % 2 != 0) {
   alert("É impar")
}
```

Implemente um programa que verifica se um dado número inteiro é **divisível por 4 e por 5**.
```javascript
x = parseInt(prompt("Entre com número inteiro:"))
if ( x % 4 == 0) {
    if ( x % 5 == 0) {
       alert("Divisível por 4 e por 5")
   }
}
```

### Teste de Intervalo 
Implemente um programa que verifica se um dado número é **maior do que 5**, ou seja, está no intervalo aberto de 5 a +infinito. 
```javascript
x = parseFloat(prompt("Entre com número:"))
if ( x > 5 ) {
   alert("Maior do que 5")
}
```

Implemente um programa que verifica se um dado número está no **intervalo fechado de -3.2 a 9.23**.
```javascript
x = parseFloat(prompt("Entre com número:"))
if ( x >= 3.2 ) {
    if ( x =< 9.23 ) {
        alert("Maior do que 5")
    }
}
```

Implemente um programa que verifica se um dado número **não está no intervalo fechado de -5 a 30**. Faça uma análise visual deste intervalo. 
```javascript
x = parseFloat(prompt("Entre com número:"))
if ( x <= -5 ) {
    alert("Não está no intervalo fechado de -5 a 30")
}
if ( x >= 30 ) {
    alert("Não está no intervalo fechado de -5 a 30")
}
```
## Exercício 1
Implemente um programa que mostra a situação do aluno como  “Aprovado” ou “Reprovado” de acordo com sua média final e a quantidade de faltas. O programa deve receber como entradas as faltas e duas notas do aluno. 

* O aluno será reprovado por falta se faltar mais que ¼ das aulas (o número total de aulas é 90);
* Se o aluno ficar com média no intervalo [3, 5[, ele está em “Recuperação” e deverá fazer prova de reposição; 
  * Caso o aluno faça prova de reposição, o programa deve pedir para o usuário informar a nota da prova de reposição e substituir na menor nota. 
* O aluno será aprovado se obtiver média 5 ou maior, senão será reprovado

## Expressões lógicas

Uma expressão lógica em linguagem de programação é uma construção que resulta em um valor booleano, ou seja, verdadeiro ou falso. Ela combina operandos (valores, variáveis ou outras expressões) com operadores lógicos para formar uma afirmação que pode ser avaliada como verdadeira ou falsa.

As expressões lógicas são frequentemente usadas em estruturas de controle, como condicionais e loops, para tomar decisões com base em condições específicas. Elas também são usadas em validações, algoritmos de busca e outras áreas da programação onde a lógica booleana é necessária.

Principais componentes das expressões lógicas:
* A condição de uma estrutura condicional é sempre uma expressão lógica.
* **Expressão lógica** é aquela cujos **operadores** são **lógicos** ou **relacionais** e que o resultado da expressão é um valor verdadeiro ou falso.

### Operadores lógicos

Expressões lógicas desempenham um papel fundamental na programação, permitindo aos desenvolvedores criar condições complexas a partir de condições simples. Por meio dos operadores lógicos, como AND (E), OR (OU) e NOT (NÃO), é possível combinar várias condições para formar expressões mais elaboradas.

Os operadores lógicos facilitam o raciocínio ao permitir que os programadores expressem de forma clara e concisa as condições que desejam avaliar em seus programas. Ao utilizar expressões lógicas, é possível criar instruções que respondam a uma ampla gama de situações e cenários, tornando o código mais adaptável e flexível.

Além disso, as expressões lógicas tornam o código mais breve, pois permitem que várias condições sejam avaliadas em uma única linha de código. Isso resulta em um código mais limpo e legível, facilitando a compreensão e manutenção do programa.

Em uma expressão lógica, os operandos dos operadores lógicos são chamados proposições. Essas proposições são declarações ou expressões que podem ser avaliadas como verdadeiras ou falsas. Elas são a base sobre a qual os operadores lógicos operam, e cada proposição possui um de dois valores possíveis: verdadeiro ou falso.

Por exemplo, considere as proposições "3 é maior que 2" e "7 é menor que 5". Ambas são expressões que podem ser avaliadas como verdadeiras ou falsas. No primeiro caso, a proposição é verdadeira, enquanto no segundo caso, é falsa.

Quando essas proposições são combinadas com operadores lógicos, uma operação lógica é realizada. Essa operação resulta em outra proposição que também pode ser avaliada como verdadeira ou falsa, dependendo dos valores das proposições originais e do tipo de operador lógico utilizado. É importante ressaltar que uma proposição é uma afirmação individual que pode ser verdadeira ou falsa, uma expressão lógica é uma combinação de proposições e operadores lógicos que produz um valor booleano quando avaliada. Logo, as expressões lógicas são construídas a partir de proposições, mas não são idênticas a elas.
 
Portanto, as expressões lógicas são uma ferramenta poderosa na programação, fornecendo aos desenvolvedores uma maneira eficiente de criar condições e tomadas de decisão em seus programas, facilitando o desenvolvimento de software robusto e eficaz. Dominar a estrutura condicional e os operadores lógicos é, certamente, a base para se aprender lógica de programação. 

Operadores lógicos em JavaScript:

| Símbolo  | Função |
| :---: | :---: |
|   &&   |  E (Conjunção)   |
|  \|\|  |  OU (Disjunção)  |
| !  |  Não (Negação)  |


### Atividades 
1. Implemente um programa, utilzando operadores lógicos, que verifica se um dado número inteiro é divisível por 3, mas não por 5.
2. Implemente um programa que verifica se um dado número está no intervalo fechado de -3.2 a 9.23, use operadores lógicos. 

### Tabela Verdade   
Uma tabela verdade é uma tabela que mostra todas as possíveis combinações de valores de verdade para uma expressão lógica. Essas tabelas são usadas para determinar o resultado de uma expressão lógica em todas as suas diferentes condições.

As tabelas verdade são construídas listando todas as combinações possíveis de valores verdadeiros (V) e falsos (F) para as proposições envolvidas na expressão lógica. Em seguida, o valor verdadeiro ou falso resultante da expressão é determinado para cada combinação.

As tabelas verdade são úteis para entender o comportamento de expressões lógicas complexas, especialmente quando envolvem múltiplas proposições e operadores lógicos. Elas ajudam os programadores a visualizar todas as possíveis situações e a determinar como uma expressão lógica se comportará em cada uma delas.


#### Operador Lógico E 

O operador lógico E, representado por "&&", retorna verdadeiro apenas se ambas as proposições envolvidas forem verdadeiras. Se pelo menos uma das proposições for falsa, o resultado será falso.

Exemplos de afirmações usando o operador lógico E, expressas de linguagem natural:
* "Eu vou comprar sorvete se estiver calor e eu tiver dinheiro no bolso."
  * Esta afirmação implica que duas condições devem ser verdadeiras para que a ação de comprar sorvete ocorra: o clima precisa estar quente e ensolarado (calor), e a pessoa precisa ter dinheiro disponível no bolso.
* "Vou assistir ao filme se estiver em cartaz no cinema e meus amigos quiserem ir também."
  * Esta afirmação indica que duas condições precisam ser atendidas para que a pessoa assista ao filme: o filme deve estar sendo exibido no cinema (estar em cartaz) e os amigos também devem querer ir.
* "Eu vou à festa se for sexta-feira e eu não tiver nenhum compromisso importante no dia seguinte."
  * Esta afirmação sugere que a pessoa comparecerá à festa apenas se duas condições forem verdadeiras: é sexta-feira (e não outro dia da semana) e não há nenhum compromisso importante agendado para o dia seguinte.

Esses exemplos ilustram como o operador lógico E é usado para combinar duas condições distintas em uma única afirmação, onde ambas as condições precisam ser verdadeiras para que a ação especificada ocorra.

A tabela verdade do operador lógico E é apresentada a seguir: 

| A | B | A && B |
|---|---|--------|
| V | V |   V    |
| V | F |   F    |
| F | V |   F    |
| F | F |   F    |

Na tabela verdade:
* Quando A e B são ambas verdadeiras (V && V), o resultado é verdadeiro (V).
* Quando A é verdadeira e B é falsa (V && F), o resultado é falso (F).
* Quando A é falsa e B é verdadeira (F && V), o resultado é falso (F).
* Somente quando ambas A e B são falsas (F && F), o resultado é falso (F).

O operador lógico E é útil quando queremos que todas as condições sejam atendidas para que uma determinada ação ocorra. Se qualquer uma das condições não for atendida, o resultado será falso. Isso é especialmente útil em situações onde múltiplas condições devem ser verdadeiras para que um determinado bloco de código seja executado.

#### Operador Lógico OU 
O operador lógico OU, representado por "||", retorna verdadeiro se pelo menos uma das proposições envolvidas for verdadeira. Isso significa que ele retorna falso apenas se ambas as proposições forem falsas.

Exemplos de afirmações usando o operador lógico E, expressas de linguagem natural:
* "Vou comprar o laptop se ele estiver em promoção ou vier com brindes grátis."
  * Nesta afirmação, a pessoa considerará comprar o laptop se uma das duas condições for verdadeira: o laptop está em promoção (com desconto) ou vem com brindes grátis.
* "Vou fazer a viagem se o clima estiver ensolarado ou se o destino for uma praia paradisíaca."
  * Nesta afirmação, a pessoa optará por fazer a viagem se pelo menos uma das condições for atendida: o clima estiver ensolarado ou o destino da viagem for uma praia paradisíaca.
* "Eu comprarei o apartamento se ele tiver uma boa localização ou se tiver uma vista panorâmica."
  * Neste caso, a pessoa considerará comprar o apartamento se uma das duas condições for verdadeira: o apartamento estiver bem localizado (em uma área conveniente) ou oferecer uma vista panorâmica desejável.

Esses exemplos ilustram como o operador lógico OU é usado para combinar duas condições distintas em uma única afirmação, onde apenas uma das condições precisa ser verdadeira para que a ação especificada ocorra.

A tabela verdade do operador lógico OU é apresentada a seguir: 

| A | B | A \|\| B |
|---|---|--------|
| V | V |   V    |
| V | F |   V    |
| F | V |   V    |
| F | F |   F    |

Nesta tabela verdade:

* Quando A e B são ambas verdadeiras (V || V), o resultado é verdadeiro (V).
* Quando A é verdadeira e B é falsa (V || F), o resultado é verdadeiro (V).
* Quando A é falsa e B é verdadeira (F || V), o resultado é verdadeiro (V).
* Somente quando ambas A e B são falsas (F || F), o resultado é falso (F).

Essencialmente, o operador lógico OU verifica se pelo menos uma das proposições é verdadeira. Se pelo menos uma delas for verdadeira, o resultado será verdadeiro. Isso é útil quando queremos executar um bloco de código se qualquer uma das condições for atendida, sem a necessidade de ambas serem verdadeiras.

#### Operador de Negação
O operador de negação, representado por "!", inverte o valor de uma proposição. Em outras palavras, se a proposição for verdadeira, a negação será falsa, e se a proposição for falsa, a negação será verdadeira.

A tabela verdade do operador lógico Negação é apresentada a seguir:

| A | !A |
|---|----|
| V |  F |
| F |  V |

Na tabela verdade:

* Quando A é verdadeira, sua negação (!A) é falsa.
* Quando A é falsa, sua negação (!A) é verdadeira.

O operador lógico Negação é frequentemente usado para inverter o resultado de uma condição. Por exemplo, se queremos verificar se uma variável é diferente de zero, podemos usar a negação da condição "a variável é igual a zero" para obter o resultado desejado: 
```javascript
x = 5;
if (!(x == 0)) {
    // Executa se x for diferente de zero
}
```

No exemplo acima, a negação da condição "x é igual a zero" garante que o bloco de código seja executado apenas se x for diferente de zero. Isso demonstra como o operador de negação pode ser útil para controlar o fluxo do programa com base em condições específicas.

### Precedência entre operações

1. NÃO (!)
1. Operadores aritméticos
1. Operadores relacionais
1. E (&&)
1. OU (||)

Exemplos:
```javascript
2 < 5 && 15/3 == 5
```

```javascript
5*4 >= 20 && 17/4 < 3 || 2+3 == 5
```

### Exercícios 

1 - Determine os resultados obtidos na avaliação das expressões lógicas seguintes, sabendo que A = 2, B = 7 e C = 3:

1. A > B-1 || A > B - 2   
1. C > A || B < C && A + 5 > B  
1. A == C-1 && B * 2 > A*C && (A+B+C)/2 < B 
1. C - A > B / 3 || !(5 + C – A <= 12)             
1. C*3 >= B && 5+A <= B && B-C >= A*2 && B*3 > (B+C)*2


2 - Implemente um programa que verifica se um dado número inteiro é divisível por 3, 4 e 5 ao mesmo tempo.
```javascript
//… divisível por 3 e divisível por 4 e divisível por 5...
```

3 - Implemente um programa que verifica se um dado número está no intervalo fechado de 0 a 10 ou no intervalo aberto de 30 a 40.
```javascript
//… dado número é maior ou igual a 0 e menor ou igual a 10 ou maior que 30 e menor que 40.
```

4 - Implemente um programa que verifica se um dado número não está no intervalo fechado de -5 a 30
```javascript
… dado número não é maior ou igual a -5 e menor ou igual a 30
```



## Referências
1. [Expressões e operadores em  https://developer.mozilla.org](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_operators)
2. Slides de aulas da disciplina de Lógica de Porgramação da ECT-UFRN, consultados em 10/03/2022.
3. ChatGPT 3.5, https://chat.openai.com/, consultado em 26/02/2024.
