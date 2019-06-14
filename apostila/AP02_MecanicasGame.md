>**Mecânicas.**

As leis da Física mandam e desmandam em nosso mundo, e várias vezes nos deparamos com situações em que são necessárias aplicar essas
leis em diferentes tipos de realidade. Aqui, você descobrirá como aplicar física em um jogo feito em JavaScript utilizando a biblioteca
P5.js.
Tópicos a serem explanados: Gravidade, Colisão, Empurrar Objetos.
**“As explicações partem do princípio que o leitor já conhece o mínimo dá biblioteca e sabe executar algumas linhas simples de código,
como criar uma elipse, por exemplo.”**
Durante as explicações, quando houver menção a um ”player”, estarei me referindo a elipse branca.

>**Gravidade**:

Para as exemplificações teremos o seguinte ambiente:

	var g = 0.2;
	var fy = 0;
	var px = 100;
	var py = -100;
	var speed = 4;
	
	function setup() {
	  createCanvas(600, 400);
	}
	
	function draw() {
	  background(0);

  	  if(keyIsDown(LEFT_ARROW)){
  	    px = px - speed;
  	  }
  	  if(keyIsDown(RIGHT_ARROW)){
  	    px = px + speed;
  	  }

	  ellipse(px,py,30,30);
	}

Com isso, você deve obter uma tela preta e uma elipse que não será visível pois ela está na posição -100.

Em um game de plataforma, é importante que exista gravidade, pois o player depende disso para percorrer as plataformas e tudo mais. Por enquanto, ignoraremos toda o material escrito por Isaac Newton e entenderemos a gravidade aqui simplesmente como uma força que fará o objeto cair em direção ao chão.

Primeiro, precisamos definir alguns conceitos, o que é o chão?
No nosso mundo, a força normal atua cancelando as forças atuantes e isso faz com que a gente não atravesse o chão. Mas, como fazemos isso em um jogo? Simples, faremos o chão ser uma posição da qual o player não deve passar.

A gravidade é uma força que atua sobre o player e o faz **acelerar** em direção ao chão. Perceba a presença da palavra “**acelerar**”, isso indica que é um processo de  acréscimo, de soma. 
**Se g = 9.81 m/s, a cada um segundo se é somado 9.81 metros.**

Então: 

	function draw() {
	  background(0);

  	  if(keyIsDown(LEFT_ARROW)){
  	    px = px - speed;
  	  }
  	  if(keyIsDown(RIGHT_ARROW)){
  	    px = px + speed;
  	  }
	  
	  py = py + g;
	  
	  ellipse(px,py,30,30);
	}

Com isso, o player agora deve estar caindo e atravessando a tela. Porém, não é interessante alterar a posição do player diretamente: **py = py + g;**, pois haverão mais forças a serem aplicadas em y, a gravidade não será a única. O correto é calcular as forças resultantes e só depois aplicar na posição. Para calcular as forças em y, utilizaremos a variável **fy**. Logo:
	
	function draw() {
	  backgroun(0);

  	  if(keyIsDown(LEFT_ARROW)){
  	    px = px - speed;
  	  }
  	  if(keyIsDown(RIGHT_ARROW)){
  	    px = px + speed;
  	  }
	  
	  fy = fy + g;
	  py = py + fy;
	  ellipse(px,py,30,30); 
	}

Por enquanto, a existência do **fy** parece desnecessária, mas quando for introduzido mecânicas de pulo ou dash, ela será melhor compreendida.

Agora, o player ainda está passando pela tela, precisamos adicionar um chão.

Como já dito, o chão no jogo será uma posição da qual o player não passará, ou seja, se o player alcançar aquela posição, a força exercida sobre ele deve ser zerada, logo:
	
	function draw() {
	  background(0);

  	  if(keyIsDown(LEFT_ARROW)){
  	    px = px - speed;
  	  }
  	  if(keyIsDown(RIGHT_ARROW)){
  	    px = px + speed;
  	  }
	  
	  fy = fy + g;
	  if(py > 360){
  	    fy = 0;
  	  }
	  py = py + fy;
	  ellipse(px,py,30,30);
	}
