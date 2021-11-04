# Estruturas Condicionais

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

## Operadores relacionais
Utilizado quando for necessário realizar comparações. 
* Os operandos de operadores relacionais são variáveis, constantes ou expressões aritméticas
* Uma operação relacional resulta em **Verdadeiro** ou **Falso**

Símbolo em JavaScript | Descrição | Exemplo que retorna verdadeiro 
----------------------|-----------|----------
Igual (==) | Retorna verdadeiro caso os operandos sejam iguais | 3 == var1, "3" == var1 e 3 == '3' 
Diferente  (!=) | 	Retorna verdadeiro caso os operandos não sejam iguais. | var1 != 4 e var2 != "3"
Estritamente igual (===) | Retorna verdadeiro caso os operandos sejam iguais e do mesmo tipo. |	3 === var1 
Maior que (>) | Retorna verdadeiro caso o operando da esquerda seja maior que o da direita. | var2 > var1 e "12" > 2
Maior que ou igual (>=) | Retorna verdadeiro caso o operando da esquerda seja maior ou igual ao da direita. |  var2 >= var1
Menor que (<) | Retorna verdadeiro caso o operando da esquerda seja menor que o da direita. | var1 < var2
Menor que ou igual (<=) | 	Retorna verdadeiro caso o operando da esquerda seja menor ou igual ao da direita. | var1 <= var2

## Referências
1. [Expressões e operadores em  https://developer.mozilla.org](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_operators) 
