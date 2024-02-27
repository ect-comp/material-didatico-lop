# Laboratório 1
Prática com: 
* Entrada e saída de dados;
* Operadores aritméticos.

## Dia 1: Atividades de treinamento e demonstrações 

* [Atividades Práticas na Plataforma LoP](https://lop.natalnet.br) (listas de exercícios):
  * Expressões Aritméticas - Lista Ressolvida (LOP)
  
### Vídeos da Lista Resolvida  

* [É preciso praticar muito!](https://youtu.be/SGVvmI232m8)
* [Introdução a Soma](https://youtu.be/0bEVryfsQtA)
* [Programa Bom Dia!](https://youtu.be/Jl0Rb4Db7eI)
* [Calculando expressões - parte 1](https://youtu.be/Xv47XGJW0ww)
* [Média Ponderada](https://youtu.be/OlkqDmkUrBQ)

### Extra: 
* [Outros vídeos](https://www.youtube.com/playlist?list=PLfGOgFSaHKF7xHNtja3bDdmf_Sv6GEP2D) 
* [Funções Aritméticas](https://docs.google.com/presentation/d/18CEr3y0nxRW6m7agx3viJGWOfMU167grxfrmvotMAUk/edit?usp=sharing)

 
### Códigos dos Exercícios Resolvidos 
#### É preciso praticar muito! 
```javascript
alert("Eh preciso praticar muito para aprender a programar!")
```

#### Introdução a Soma
```javascript
alert( (10 + 13) + " " + (125 + 373) + " "+ (4235 + 8962))
```

#### Programa Bom Dia!
```javascript
nome = prompt("Entre com um nome: ");
alert("Bom Dia " + nome} + "!" );
```

#### Calculando expressões - parte 1
```javascript
a = 1.5 
c = 2
d = 3
r = a * (c + d)
alert(r)
```

#### Média Ponderada
```javascript
nota1 = parseFloat(prompt("Nota 1:"))
nota2 = parseFloat(prompt("Nota 2:"))
nota3 = parseFloat(prompt("Nota 3:"))

media = (nota1*2 + nota2*3 + nota3*5) / 10

alert(media) 
```

### Exercícios Extras

Escreva um programa que recebe um número inteiro de horas e imprime o número equivalente em dias. Ex.: 60 horas = 2,5 dias.
```javascript
horas = parseInt(prompt("Entre o número de horas: "))
dias = horas/24
alert(dias)
```

Escreva um programa que recebe a altura em metros e a massa em quilos de uma pessoa e calcula seu Índice de Massa Corporal (IMC). 
> $`IMC = \frac{massa}{altura^2}`$
```javascript
altura = parseFloat(prompt("Entre a altura: "))
massa = parseFloat(prompt("Entre a massa: "))
imc = massa / ( altura**2)
alert(imc)
```

## Dia 2: Prática  
Resolver os exercícios da lista "Expressões Aritméticas - Lista Prática" da [Plataforma LoP](https://lop.natalnet.br). 

Ordem das questões:
* Calculando expressões - parte 2
* Calculando expressões - parte 3
* Calculando expressões - parte 4
* Imprimindo uma mensagem com um valor
* Convertendo de horas para dias
* Convertendo de metros para polegadas
* Convertendo pés, jardas e milhas
* Cálculo do IMC
* Calculo de expressão com expoente
* Calculando expressões com raiz
  

