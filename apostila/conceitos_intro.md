# Introdução  

JavaScript é uma linguagem de programação projetada inicialmente para navegadores web. Uma linguagem de programação é um método de expressar um conjunto de instruções para um computador. 

JavaScript é uma linguagem interpretada, na qual trechos de códigos são traduzidos em instruções de máquinas do computador de forma progressiva. 


## Variáveis

Uma variável em uma linguagem de programação é um local de armazenamento na memória do computador que contém um valor. Esse valor pode ser de diversos tipos, como números, texto, valores lógicos (verdadeiro ou falso) e até mesmo estruturas de dados mais complexas.

As variáveis são essenciais em programação, pois permitem que os programadores armazenem e manipulem dados dinamicamente durante a execução de um programa. Elas também fornecem nomes simbólicos para os dados, facilitando a compreensão e a manutenção do código.

**Definição**: Uma variável é um espaço para manter informações durante a execução de um programa. 

### Memória 

A memória é um elemento com capacidade para armazenar qualquer tipo de informação (dados e programas). Ela é dividida em milhares ou milhões de "compartimentos" e cada compartimento tem um número de localização chamado de **endereço de memória**. 


### Variáveis na memória 

Os programas usam a memória para armazenar os dados fornecidos pelo usuário e os resultados parciais das operações sobre estes dados. No passado, para recuperar um dado na memória do computador era necessário saber o seu endereço. Porém, para um programador lembrar de cada número relativo ao endereço de memória utilizado é muito trabalhoso. Logo, as variáveis surgem para resolver esse problema, ao invés de lembrar de um número, basta lembrar do nome da variável para poder acessá-la.    


**Importante:** Uma variável representa um espaço de memória para armazenar um determinado tipo de dado. 

## Declaração de variáveis (Sintaxe) 
Antes de usar uma variável, é necessário declará-la. Isso envolve especificar o tipo de dados que a variável irá armazenar e fornecer um nome para ela. Por exemplo, em muitas linguagens de programação, a declaração de uma variável do tipo inteiro chamada "idade" pode ser feita da seguinte forma:

JavaScript é uma linguagem permite muita flexibilidade no uso de varíaveis. Os tipos de dados são definidos dinamicamente. Durante a execução do código uma variável pode assumir um tipo no início e durante a execução mudar o seu tipo, por exemplo, a variável pode começar com o tipo `string` (textual) e finalizar com o tipo `number` (numérico). Veja a seguir alguns exemplos de declaração de variáveis: 

Usando a palavra reservada **var**:
* **var** <nome_da_variavel>
* <nome_da_variavel> esse é o espaço para o nome da variável 

Usando inicialização: 
* **var** <nome_da_variavel> [= <valor_inicial>]
* [= <valor_inicial>], usando o operador de atribuição, `=`, para definir uma valor inicial para a variável 

Apenas com atribuição: 
* <nome_da_variavel> = <valor_inicial> 

Exemplos: 
```javascript
var x; 
var y = 0;
z = 1; 
``` 
O código acima possui uma declaração de uma variável x, uma declaração de uma variável y com valor inicial igual a 0 e uma criação de uma variável z com valor 1 considerando que z aparece pela primeira vez no código. 

### Exercícios

Declare variáveis no console do seu navegador de internet:   
* Use o comando typeof para checar o tipo da variável 
* Declare uma variável x com "var" 
* Atribua um valor inteiro e verifique o tipo
* Atribua um valor textual e verifique o tipo  
* Faça o mesmo para uma variável y criada por uma atribuição 

### Nome de variáveis

Regras para nomes de variáveis
* Deve iniciar por uma letra ou por o símbolo '_'
* Pode ser composto por letras, dígitos ou o símbolo '_' 
* Não pode ser uma palavra reservada da linguagem

Exemplos válidos: 
* teste			
* delta_bhaskara		
* TESTE
* soma			
* _1234				
* _tESTe_				
* resultado1
* temp			
* var0				
* raizDelta			

Exemplos não válidos ou não recomendados 
* 10_binario		
* raiz.quadrada		
* teste@				
* resultado-final 		
* divisão

Maiúsculas e minúsculas formam nomes de variáveis diferentes 
* teste, TESTE e tEsTe são variáveis diferentes 

Recomendações para criação de variáveis
* Utilize nomes **representativos**
* Inicie com letra **minúscula**
* Simule o espaço (que não é permitido):
  * Com letra maiúscula: umNomeGrande
  * Com '_': um_nome_grande
 
### Usando variáveis
Uma vez que uma variável tenha sido declarada e atribuída, ela pode ser usada em expressões e operações dentro do programa. 

Para atribuir um valor a uma variável use o operador `=`
* O valor que a variável armazenava antes da atribuição é perdido (sobrescrito)
* Lê-se: "<variável> recebe <valor>" 

Exemplos:
```javascript
preco = 8.50
altura = 1.67
genero = 'M'
```

É importante observar que o valor armazenado em uma variável pode ser alterado ao longo da execução do programa, e as variáveis podem ser utilizadas em diferentes partes do código.

Além disso, as variáveis podem ter escopo, o que significa que elas podem ser acessadas apenas em determinadas partes do código, dependendo de onde foram declaradas. O escopo de uma variável pode ser global (acessível em todo o programa) ou local (acessível apenas em uma parte específica do programa).

Em resumo, uma variável em uma linguagem de programação é um contêiner de dados que pode armazenar e manipular valores durante a execução de um programa. Elas são elementos fundamentais para a criação de programas dinâmicos e flexíveis.



## Entrada e Saída de Dados

A entrada de dados refere-se ao processo de fornecer informações ou comandos para um sistema computacional. Esses dados podem ser de diferentes tipos, como texto, números, comandos de controle, entre outros, e são inseridos no sistema por meio de dispositivos de entrada.

Exemplos de dispositivos de entrada:
* Teclado,
* Mouse,
* Tela sensível ao toque,
* Sensor de temperatura,
* Microfone. 


Os dispositivos de saída em computação são periféricos ou componentes do sistema que apresentam informações, resultados ou dados processados ​​para os usuários de uma forma compreensível. Eles são responsáveis por comunicar os resultados das operações realizadas pelo computador ou pelos dispositivos conectados ao sistema.

Exemplos de dispositivos de saída: 
* Monitor ou tela,
* Caixas de som,
* Impressora,
* LEDs. 

Nos nossos programas
* **Entrada:** teclado
* **Saída:** tela (janela, terminal ou prompt)


### Saída de dados

Imprime ou apresenta textos e variáveis para o usuário do programa.  

Saída de dados em algoritmo (explicado) 
* Escreva um valor na tela 

Saída de dados em JavaScript 
* Comando: `alert(valor)`

Exemplo de código para mostrar um texto na tela:
```javascript
alert("Olá Mundo!");
```

### Entrada de dados

Lê o valor digitado e armazena em uma variável. A valor de entrada deve ser compatível com o tipo de dado da variável. Quando o camando de leitura de dados é executado, o programa fica esperando indefinidamente até que a entrada de dados seja concluída ou fornecida. 

Entrada de dados em algoritmo (explicado)
* Leia um valor 

### Entrada em JavaScript

Para ler um texto: 
```javascript
valor = prompt("Mensagem");
```

Para ler um número real:
```javascript
valor = parseFloat(prompt("Mensagem")); 
```

Para ler um número inteiro: 
```javascript
valor = parseInt(prompt("Mensagem"));
```


## Expressão Aritmética

Uma expressão aritmética em uma linguagem de programação é uma combinação de números, operadores matemáticos e variáveis que, quando avaliada, produz um valor numérico. Ela é como uma fórmula matemática que pode ser calculada pelo computador para obter um resultado.

**Definição:** Expressão aritmética é aquela cujos operadores são aritméticos e os operandos são constantes ou variáveis numéricas.

Principais componentes de uma expressão aritmética: 

1. **Números**: São os valores numéricos que compõem a expressão, como 2, 5, 10, etc.
1. **Operadores Matemáticos**: São os símbolos que indicam operações a serem executadas. Os operadores mais comuns são:
    1. Adição (+)
    1. Subtração (-)
    1. Multiplicação (*)
    1. Divisão (/)
    1. Exponenciação (**) - em JavaScript 
    1. Módulo (%) - retorna o resto da divisão entre dois números
1. **Variáveis**: São símbolos que representam valores que podem variar durante a execução do programa. Por exemplo, se tivermos a variável "idade", ela pode ser usada em uma expressão aritmética para representar a idade de uma pessoa.

Exemplo de uma expressão aritmética: 
```javascript
2 + 3 * (idade - 5)
```
Nesta expressão, contêm números (2, 3, 5), operadores (+, *, -), e uma variável (idade). Quando esta expressão é avaliada, ela primeiro resolve a operação dentro dos parênteses, subtrai 5 da variável "idade", multiplica o resultado por 3, e depois adiciona 2 ao resultado final.

Em linguagens de programação, expressões aritméticas são frequentemente usadas em diversas situações, como calcular valores, atualizar variáveis, tomar decisões com base em resultados numéricos, entre outras. Elas formam a base para cálculos matemáticos e são uma parte fundamental da programação.


### Tabela com alguns operadores 

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

### Precedência de operadores

* Parênteses mais internos
* `*, /, %`
* `+, -`

Exemplos de expressões:
* `A - B * C`
* `(A * (B + C)) % D`

#### Reflexão
Resolvendo a expressão: `48 / 2 * (9+3)`

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

Os operadores de mesma precedência são resolvidos da esquerda para direita na expressão. O único resultado da expressão `48 / 2 * (9 + 3)` é 288. 

### Exercícios: 

#### Convertendo de horas para dias

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

#### Cálculo do IMC

Escreva um programa que recebe a altura em metros e a massa em quilos de uma pessoa e calcula seu Índice de Massa Corporal (IMC). A fórmula do IMC é massa dividido por altura ao quadrado. Ver:  

Código: 
```javascript
massa = parseFloat( prompt("Entre com a massa"))
altura = parseFloat( prompt("Entre com a altura"))
imc = massa / ( altura ** 2)
alert("IMC: "+imc)  
```

#### Média Ponderada 

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
* [Developer Mozilla: Operadores aritméticos](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_operators#operadores_aritm%C3%A9ticos)
* Slides de aulas da disciplina de Lógica de Porgramação da ECT-UFRN, consultados em 10/03/2022.
* ChatGPT 3.5, https://chat.openai.com/, consultado em 22/02/2024.

 

