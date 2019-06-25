>Vetor? Que Trem é Esse? 

Você tem dificuldade em entender como trabalhar com vetores em programação? Esta analogia talvez possa te colocar de volta nos “trilhos” da matéria... 

Se você já estudou estruturas de repetição, muito provavelmente conhece a estrutura “**for**”. Utilizamos ela como uma espécie de contador, que é executado uma certa quantidade de vezes. Quando o utilizamos, sabemos em que valor iremos começar e até onde temos que ir, por exemplo: **for( i = 0; i < 5; i++);**  Nesse caso, o **for** começará seu **i** em **0** e irá até um valor menor que **5**, sendo incrementado de **1** em **1** **( i++ ou i+1 )**. Nesse caso, os valores percorridos seriam: **0 , 1 , 2 , 3, 4**; (Perceba que, ele vai de zero até um valor menor que 5: **( i = 0; i < 5 )**. 

Após essa mini revisão, vamos unir o for aos vetores, que a partir de agora deixarão de ser vetores e passarão a ser trens. 

No for usamos uma variável para ir “contando” os valores, no exemplo acima, a variável utilizada foi o i. Que a partir de agora começaremos a trata-la como sendo o maquinista de um trem. 
 
Imagine a seguinte situação, você está trabalhando para uma companhia de trens e sua função é contar quantas pessoas vem nesse trem, para isso, você precisa fazer a somatória de pessoas em cada vagão. Você conta com o maquinista do trem para que ele pegue o número de pessoas que está dentro de cada vagão. Digamos que acabou de chegar um trem com 5 vagões: 

Perceba que a numeração dos vagões começa em 0. Devemos agora, fazer nosso trabalho, precisamos da quantidade total de pessoas desse trem. Então, dizemos para o maquinista, vá do vagão 0 até o vagão 4, de um em 1, e me informe a quantidade de pessoas que tem em cada vagão. Então o maquinista começa;

(Os vagões serão representados por colchetes [ ])

O maquinista começa em 0 e vai até o 4º vagão, de um em um, logo:

**for(i = 0; i < 5; i++)**

Quando **i** = **0**: No [ i ] do trem: 15 pessoas; 

Quando **i** = **1**: No [ i ] do trem: 9 pessoas;

Quando **i** = **2**: No [ i ] do trem: 7 pessoas;

Quando **i** = **3**: No [ i ] do trem: 2 pessoas;

Quando **i** = **4**: No [ i ] do trem: 8 pessoas.


Agora, trabalharemos a mesma situação utilizando programação, com o mesmo exemplo, temos um trem e queremos a somatória de pessoas que estão nele.

De acordo com o que combinamos mais a cima, a partir de agora vetores são trens, e a nossa variável do for será o maquinista, tendo isso em mente, vamos ao código.

Primeiro em JavaScript e depois em C++.

(Código JavaScript) 

	var Trem = [15, 9, 7, 2, 8];	// Aqui temos nosso trem, de 5 vagões.
	var somatoria = 0;	// Criamos uma variável para armazenar a somatória.
	
	// Como o trem tem 5 vagões, precisamos dizer para o maquinista ( i ), que ele deve começar no vagão 0, 
	e ir até o vagão 4, logo:
	for( var i = 0; i < 5; i++) ou também é correto: for( var i = 0; i <= 4; i++)
	
	for( var i = 0; i < 5; i++){
		somatoria = somatoria + Trem[  ]  ← Leia a OBS1
	}
	
	OBS1: Entre os colchetes, precisamos informar qual é o vagão que queremos acessar, agora, quem ficou responsável de percorrer 
	todos os vagões? Quem ficou responsável por ir do 0 ao 4º vagão? Exatamente, o maquinistas, o nosso ( i ). Logo:

	for( var i = 0; i < 5; i++){
		somatoria = somatoria + Trem[i] ;
	}

	cout << somatoria;	// A resposta esperado é 41;

(Código C++)

	int Trem[5] = {15, 9, 7, 2, 8};	// Aqui temos nosso trem, de 5 vagões.
	int somatoria = 0;	// Criamos uma variável para armazenar a somatória.
	
	// Como o trem tem 5 vagões, precisamos dizer para o maquinista ( i ), que ele deve começar no vagão 0, e ir até o vagão 4, 
	logo:
	for( int i = 0; i < 5; i++) ou também é correto: for( int i = 0; i <= 4; i++)
	
	for( int i = 0; i < 5; i++){
		somatoria = somatoria + Trem[  ]  ← Leia a OBS1
	}
	
	OBS1: Entre os colchetes, precisamos informar qual é o vagão que queremos acessar, agora, quem ficou responsável de percorrer 
	todos os vagões? Quem ficou responsável por ir do 0 ao 4º vagão? Exatamente, o maquinistas, o nosso ( i ). Logo:

	for( int i = 0; i < 5; i++){
		somatoria = somatoria + Trem[i] ;
	}

	cout << somatoria;	// A resposta esperado é 41;
