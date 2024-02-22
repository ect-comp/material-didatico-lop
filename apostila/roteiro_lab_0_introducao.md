# Introdução Prática sobre Algoritmos 

## Atividades Introdutórias a Lógica de Programação
Jogos para os programadores de amanhã https://blockly-games.appspot.com/

Jogos do site hora do código:
* https://hourofcode.com/code
* https://code.org/minecraft
* https://hourofcode.com/mchoc
* https://hourofcode.com/silent

## Vídeos Motivacionais 
* Com dedicação, qualquer pessoa pode aprender, vídeo de 2014, https://www.youtube.com/watch?v=ip051U7Rvds
* Vídeo de code.org de 2013, https://youtu.be/nKIu9yen5nc


## Trabalhando com JavaScript e Páginas WEB 

### Primeiro Código em JavaScript 

Abrir o navegador e executar o primeiro código em JavaScript: 
```javascript
	alert("Olá mundo"); 
```

### Primeira Página WEB 

Usando o editor de sua preferência crie o arquivo **index.html** com o conteúdo a seguir: 

```html
<html>
	<head>
	  <meta charset="UTF-8">
	</head>
	<body>
		Minha Primeira Página WEB! 
	</body>
</html>
```
Esta é uma página web muito simples. 

### Inserindo Código JavaScript 

Usando o comando _alert_ na página web para criar a primeira página com JavaScript. 

```html
<html>
	<head>
	  <meta charset="UTF-8">
	  <script> alert("Olá Mundo!") </script>
	</head>
	<body>
		Página WEB!
	</body>
</html>
```
Observe que para usar código java script foi necessário usar as tags `<script>  </script>`: 
```html
<script> alert("Olá Mundo!") </script>
```

### Separando o código JavaScript do HTML 
Crie um novo arquivo chamado **meu_codigo.js** e coloque o seguinte conteúdo: 
```javascript
alert("Olá Mundo!"); 
```

O arquivo **index.html** deve possuir o seguinte conteúdo para "chamar" o script **meu_código.js**: 
```html
<html>
	<head>
	  <meta charset="UTF-8">
	  <script src="meu_codigo.js"></script>
	</head>
	<body>
		Página WEB! 
	</body>
</html>
```

## Referências 

* Exemplo para baixar e começar a resolver os exercícios, https://github.com/LoP-ECT2203/2017.2/blob/master/html/lab0/exemplo_4.zip 
* Exemplos com os códigos vistos acima [https://github.com/LoP-ECT2203/2017.2/html/lab0](https://github.com/LoP-ECT2203/2017.2/tree/master/html/lab0) 
* Código do _ect.js_ [https://github.com/LoP-ECT2203/2017.2](https://github.com/LoP-ECT2203/2017.2/tree/master/html/lab0/exemplo_4/ect.js)
* Tutorial HTML, https://www.w3schools.com/html/default.asp 
