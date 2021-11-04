# Variáveis

Uma variável é um espaço para manter informações durante a execução de um programa. 

## Memória 

A memória é um elemento com capacidade para armazenar qualquer tipo de informação (dados e programas). Ela é dividida em milhares ou milhões de "compartimentos" e cada compartimento tem um número de localização chamado de **endereço de memória**. 


## Variáveis na memória 

Os programas usam a memória para armazenar os dados fornecidos pelo usuário e os resultados parciais das operações sobre estes dados. No passado, para recuperar um dado na memória do computador era necessário saber o seu endereço. Porém, para um programador lembrar de cada número relativo ao endereço de memória utilizado é muito trabalhoso. Logo, as variáveis surgem para resolver esse problema, ao invés de lembrar de um número, basta lembrar do nome da variável para poder acessá-la.    


**Definição:** Uma variável representa um espaço de memória para armazenar um determinado tipo de dado. 

## Declaração de variáveis (Sintaxe) 

JavaScript é uma linguagem permite muita flexibilidade no uso de varíaveis. Os tipos de dados são definidos dinamicamente. Durante a execução do código uma variável pode assumir um tipo no início e durante a execução mudar o seu tipo, por exemplo, a variável pode começar com o tipo `string` (textual) e finalizar com o tipo `number` (numérico). Veja a seguir alguns exemplos de declaração ou criação de variáveis: 

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

## Exercícios

Declare variáveis no console do seu navegador de internet:   
* Use o comando typeof para checar o tipo da variável 
* Declare uma variável x com "var" 
* Atribua um valor inteiro e verifique o tipo
* Atribua um valor textual e verifique o tipo  
* Faça o mesmo para uma variável y criada por uma atribuição 

## Nome de variáveis

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
 
## Usando variáveis
Para atribuir um valor a uma variável use o operador `=`
* O valor que a variável armazenava antes da atribuição é perdido (sobrescrito)
* Lê-se: "<variável> recebe <valor>" 

Exemplos:
```javascript
preco = 8.50
altura = 1.67
genero = 'M'
```


