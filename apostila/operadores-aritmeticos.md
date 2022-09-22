# Expressão aritmética

**Definição:** Expressão aritmética é aquela cujos operadores são aritméticos e os operandos são constantes ou variáveis numéricas.

## Operadores 

Símbolo em JavaScript | Função | Exemplo 
----------------------|--------|----------
 `+` | Adição | `2 + 3`, `X + Y`
 `-` | Subtração | `4 - 2`, `N – M`
 `*` | Multiplicação | `3 * 4`, `A * B`
 `/` | Divisão | `10 / 2`, `C / D`, `6 / 5`
 Sem símbolo | Potenciação | `4 * 4 * 4`, `Math.pow(x , y)` , `x**y`
 Sem símbolo | Raiz quadrada | `Math.sqrt(9)`,  `Math.sqrt(x)`
 `%` | Resto da divisão | 7 % 3
 Sem símbolo | Quociente da divisão inteira | `Math.floor( x / y )`

## Precedência de operadores

* Parênteses mais internos
* `*, /, %`
* `+, -`

Exemplos de expressões:
* `A - B * C`
* `(A * (B + C)) % D`

## Exercício
Resolva a expressão: `48 / 2 * (9+3)`

Método 1:
```
48 / 2 * (9 + 3)
48 / 2 * 12
24 * 12
288
```

Método 2: 
```
48 / 2 * (9 + 3)
48 / 2 * 12
48 / 24
2
```

Operadores de mesma precedência são resolvidos da esquerda para direita na expressão. O único resultado da expressão `48 / 2 * (9 + 3)` é 288. 

## Exercícios: 

### Convertendo de horas para dias

Escreva um programa que recebe um número inteiro de horas e imprime o número equivalente em dias. Ex.: 60 horas = 2,5 dias.

Algoritmo: 
1. Entre com o número de horas e guarde em uma variável *horas* 
2. Divida o valor contido em *horas* por 24 
3. Apresente o resultado do passo 2. 

Código: 
```javascript
horas = prompt("Digite as horas: ")
dias = horas / 24 
alert(dias)
``` 

### Cálculo do IMC

Escreva um programa que recebe a altura em metros e a massa em quilos de uma pessoa e calcula seu Índice de Massa Corporal (IMC). A fórmula do IMC é massa dividido por altura ao quadrado. Ver:  

Código: 
```javascript
massa = parseFloat( prompt("Entre com a massa"))
altura = parseFloat( prompt("Entre com a altura"))
imc = massa / ( altura ** 2)
alert("IMC: "+imc)  
```

### Média Ponderada 

Faça um algoritmo que leia as 3 notas de um aluno e calcule a média final deste aluno. Considera que a média é ponderada e que o peso de cada nota é: 2, 3 e 5, respectivamente.

Código: 
```javascript
var nota1 = parseFloat(prompt("Entre com a nota 1: "))
var nota2 = parseFloat(prompt("Entre com a nota 2: "))
var nota3 = parseFloat(prompt("Entre com a nota 3: "))
var media = (nota1*2 + nota2*3 + nota3*5) / (2+3+5)
alert(media)
```

## Referências 

* [_Developer Mozilla_: Operadores aritméticos](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_operators#operadores_aritm%C3%A9ticos)
