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

## Referências
1. [Expressões e operadores em  https://developer.mozilla.org](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_operators) 
