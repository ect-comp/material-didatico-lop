# Entrada e Saída de Dados

Dispositivos de entrada
* Teclado, mouse, tela sensível ao toque, sensor de temperatura, etc.

Dispositivos de saída
* Tela, caixas de som, impressora, leds, etc. 

Nos nossos programas
* **Entrada:** teclado
* **Saída:** tela (janela, terminal ou prompt)


## Saída de dados

Imprime ou apresenta textos e variáveis para o usuário do programa.  

Saída de dados em algoritmo (explicado) 
* Escreva um valor na tela 

Saída de dados em JavaScript 
* Comando: `alert(valor)`

Exemplo de código para mostrar um texto na tela:
```javascript
alert("Olá Mundo!");
```

## Entrada de dados

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
