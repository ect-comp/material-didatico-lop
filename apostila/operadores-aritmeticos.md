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

