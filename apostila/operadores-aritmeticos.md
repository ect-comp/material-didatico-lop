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




