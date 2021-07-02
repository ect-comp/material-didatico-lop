# Repetição Condicional


As estruturas de repetição são usadas quando precisamos executar diversas vezes uma mesma sequência de instruções.
Em JavaScript:
* **while** (enquanto)
* **do-while** (faça enquanto)
* **for** (para)
As diferentes estruturas de repetição são semanticamente equivalentes. 

Sintaxe:
```javascript
while ( condição ) {
   // instruções 
}
```
"Enquanto a condição for verdadeira, execute as instruções."

Sintaxe:
```javascript
do {
   // instruções 
} while ( condição );
```
" Faça as instruções, Enquanto a condição for verdadeira."

## Exercícios 

Execute passo a passo os códigos a seguir: 

Repetição simples: 
```javascript
var x = 10
var y = 40 
while ( x > 3 ) {
   x = y / 3 
   y = x + 2 
}
```

Repetição com *loop* infinito: 
```javascript
var x = 9
var y = 12 
while ( x > 3 ) {
   x = y - 8 
   y = x * 3 
}
```
