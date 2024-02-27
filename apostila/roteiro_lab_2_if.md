# Laboratório 2
Prática com: 
* Estruturas condicionais 
* Operadores lógicos

## Dia 1: Atividades de treinamento e demonstrações 
* [Atividades Práticas na Plataforma LoP](https://lop.natalnet.br) (listas de exercícios):
  * Estrutura Condicional - Lista Ressolvida (LOP)

### Vídeos da Lista Resolvida  
* [Altura acima de média](https://youtu.be/r5EQIPde8T0)
* [Altura abaixo da média](https://youtu.be/pe40iJmUrMc)
* [Compara com 10](https://youtu.be/o4ZO5dMkxG0)  
* [Compara com 20](https://youtu.be/n7xOLgd71Io)  
* [O quadrado ou raiz](https://youtu.be/MdZsgg5juTw) 
* [Compara com 20 parte 2](https://youtu.be/Cwn25LIXrvc) 
* [Menor de 3 números](https://youtu.be/2-RVn_UqiPE)
 
### Códigos dos Exercícios Resolvidos 
#### Altura acima de média
```javascript
altura = parseFloat(prompt("Entre com a altura:"))
if ( altura > 1.73 ) {
    alert("Acima da media")
}
```

#### Altura abaixo da média
```javascript
altura = parseFloat(prompt("Entre com uma altura:"))
if (altura < 1.73 ) {
    alert("Abaixo da media")
}
```

#### Compara com 10
```javascript
var x; 
x = prompt("Entre com um número"); 
if ( x == 10 ){
    console.log("igual"); 
}
```

#### Compara com 20
```javascript
x = parseFloat(prompt("Entre com um número:"))
if ( x >= 20 ){
    alert("maior ou igual")
}
if ( x < 20 ){
    alert("menor")
}
```

#### O quadrado ou raiz
```javascript
x = parseFloat(prompt("Entre com um número"))
if ( x < 0 ) {
    alert( Math.pow(x, 2) )
} 
else {
    alert( Math.sqrt(x))
}
```

#### Compara com 20 parte 2
```javascript
x = parseFloat(prompt("Entre com um número:"))
if ( x > 20 ){
    alert("maior")
}
else {
    if ( x < 20 ){
        alert("menor")
    }
    else {
        alert("igual")
    }
}
```

#### Menor de 3 números
```javascript
x = parseFloat(prompt("Entre com x"))
y = parseFloat(prompt("Entre com y"))
z = parseFloat(prompt("Entre com z"))

var menor;  
// verifico se x é o menor de todos 
if ( x <= y ){ 
    if ( x <= z ){
        menor = x; 
    }
}
// verifico se y é o menor de todos 
if ( y <= x) {
    if ( y <= z ){
        menor = y; 
    }
}
// verifico se z é o menor de todos 
if (z <= x){
    if ( z <= y) {
        menor = z; 
    }
}
alert(menor)
```
 

### Exercícios Extras
## Dia 2: Prática  
Resolver os exercícios da lista "Estrutura Condicional - Lista Prática" da [Plataforma LoP](https://lop.natalnet.br). 

Ordem das questões:
* Calcular Índice de Massa Corporal (IMC) - parte 1
* Índice de Massa Corporal (IMC) - parte 2
* IMC simples com 2 decisões
* IMC novamente com 2 decisões
* Encontrando números pares
* Par ou impar
* Média com 3 situações de decisão
* Média com 3 situações de decisão - parte 2
* Idades e permissões
* Divisível por 3 e por 4 ao mesmo tempo
* Categorias de natação
* Divisível por 3 e por 4 - versão mais complexa
* Divisível por 3 e por 4 - versão ainda mais complexa
