**“As explicações partem do princípio que o leitor já conhece o mínimo dá biblioteca e sabe executar algumas linhas simples de código,
como criar uma elipse, por exemplo.”**

**Tópicos a serem explanados: Gravidade, Colisão, Empurrar Objetos.**

**Durante as explicações, quando houver menção a um ”player”, estarei me referindo a elipse branca.**

>**Mecânicas.**

As leis da Física mandam e desmandam em nosso mundo e várias vezes nos deparamos com situações em que são necessárias aplicar essas
leis em diferentes tipos de realidade. Aqui, você descobrirá como aplicar física em um jogo feito em JavaScript utilizando a biblioteca
P5.js.

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

Com isso, o player agora deve estar caindo e atravessando a tela **(DE FORMA BEM LENTA, AGUARDE UM POUCO)**. Porém, não é interessante alterar a posição do player diretamente: **py = py + g;**, pois haverão mais forças a serem aplicadas em y, a gravidade não será a única. O correto é calcular as forças resultantes e só depois aplicar na posição. Para calcular as forças em y, utilizaremos a variável **fy**. Logo:
	
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

No nosso mundo, a força normal atua cancelando a força peso e isso faz com que a gente não atravesse o chão.
Então, no game será necessário algo que faça o player parar, que ele não atravesse determinada posição, aqui não temos as propriedades físicas do nosso mundo, porém, podemos trabalhar o conceito de uma outra forma. Como dito, precisamos fazer com que o player pare e não passe de determinada posição, e se tentarmos algo como: 

	if(posição_y_do_player > determinada_posição){
	  pare_de_cair.
	}

Ou seja, quando o player chegasse a aquela posição ele iria parar de cair, mas, como eu digo pra ele parar de cair?

Simples, pegamos a ideia da normal, a normal atua para cancelar a força exercida em **Y**, logo, basta dizer que a força em **Y** agora é 0.

Como já dito, o chão no jogo será uma posição da qual o player não passará, ou seja, se o player alcançar aquela posição, a força exercida sobre ele (**fy**) deve ser zerada, logo: (**Para demonstração foi escolhido a posição 360 como chão**)
	
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


> **Colisão**:

O código no final deste tópico possui uma exemplificação dos conceitos aplicados abaixo:

**OBSI**: A colisão entre 2 objetos pode ser verificada quando a distância entre eles é igual a soma de seus raios.

**OBSII**: Para isso ser verdade, a posição dos objetos deve ser calculada a partir do centro.

**OBSIII**: Em P5, apenas as elipses possuem essa característica, retângulos e imagens tem sua posição calculada a partir do canto
superior esquerdo. Para usar o centro dos retângulos e nas imagens use dentro do draw os seguintes comandos: **rectMode**(CENTER) e
**imageMode**(CENTER).

Para as exemplificações teremos o seguinte ambiente:

	var x1 = 0, x2 = 400;

	function setup() {
	  createCanvas(400, 400);
	}
	
	function draw() {
	  background(220);
	  ellipse(x1,100,50,50);
	  ellipse(x2,100,30,30);
	  
	  x1 += 1;
	  x2 -= 1;
	}

P5 possui uma função (**dist()**) que calcula a distância entre 2 objetos, ela recebe como parâmetro o X e o Y de dois objetos e retorna a  distância entre eles. Como já dito anteriormente; a colisão entre 2 objetos pode ser verificada quando a distância entre eles é igual a soma de seus raios. Logo, precisamos verificar se a distância entre as 2 elipses é menor que 40, pois, a elipse da direita possui raio = 25 e a elipse da esquerda possui raio = 15.

	function draw() {
	  background(220);
	  ellipse(x1,100,50,50);
	  ellipse(x2,100,30,30);
	  
	  if(dist(x1,100,x2,100) < 40){
	    fill(255,0,0);
	  }else{
	    x1 += 1;
	    x2 -= 1;
	  }
	}
Com isso, as 2 elipses devem estar mudando de cor e parando de se mover ao se tocarem.

**Exemplificação Geral:**

	var x1 = 0, x2 = 400;
	var x3 = 0, x4 = 400;
	var x5 = 0, x6 = 400;
	
	function setup() {
	  createCanvas(400, 400);
	}
	
	function draw() {
	  background(220);
	  
	  fill(255);
	  text('Colisão entre elipses: ', 0, 15);  
	  if(dist(x1,50,x2,50) < 40){
		fill(255,0,0);
	  }else{
	    x1 += 1;
		x2 -= 1;
	  }
	  ellipse(x1,50,50,50);
	  ellipse(x2,50,30,30);
	  
	  rectMode(CORNER);
	  fill(255);
	  text('Colisão entre retângulos NÃO CENTRADOS: ', 0, 115);  
	  if(dist(x3,150,x4,150) < 40){
		fill(255,0,0);
	  }else{
	    x3 += 1;
		x4 -= 1;
	  }
	  rect(x3,130,50,50);
	  rect(x4,130,30,30);
	  
	  rectMode(CENTER);
	  fill(255);
	  text('Colisão entre retângulos CENTRADOS: ', 0, 215);  
	  if(dist(x5,250,x6,250) < 40){
		fill(255,0,0);
	  }else{
	    x5 += 1;
	    x6 -= 1;
	  }
	  rect(x5,250,50,50);
	  rect(x6,250,30,30);  
	}

> **Empurrar Objetos**:

**OBSI**: Esse parte **NÃO** foi exemplificada em um game de plataforma, porém, **ELE FUNCIONA COM GAMES DE PLATAFORMA TAMBÉM!**

Para as exemplificações teremos o seguinte ambiente:

	var px = 100;
	var py = 100;
	var pr = 30;
	var speed = 5;
	var fx = 0;
	var fy = 0;

	var enemy_X = 0;
	var enemy_Y = 0;
	var enemy_R = 30;

	function setup() {
	  createCanvas(600, 400);
	  enemy_X = random(50,550);
	  enemy_Y = random(50,350);
	}

	function draw() {
	  background(0);

	  fx = 0;
	  fy = 0;
	  if(keyIsDown(LEFT_ARROW)){
	    fx = -speed;
	  }
	  if(keyIsDown(RIGHT_ARROW)){
	    fx = +speed;
	  }
	  if(keyIsDown(UP_ARROW)){
	    fy = -speed;
	  }
	  if(keyIsDown(DOWN_ARROW)){
	    fy = +speed;
	  }
	  px = px + fx;
	  py = py + fy;
	  fill(255);
	  ellipse(px,py,pr,pr);  

	  fill(255,0,0);
	  ellipse(enemy_X,enemy_Y,enemy_R,enemy_R);
	}

**OBSII**: Perceba que, na movimentação no eixo **X** do player, foi utilizado o conceito de força explicado no tópico referente a gravidade. Agora, existe uma força (**fx**) que faz o player se mover no eixo **X**.

Imagine a seguinte situação, há um objeto a sua frente e você deseja move-lo, tira-lo do lugar, o que você faz?

Você o empurra, obviamente.

Mas, o que significa esse "empurrar"? Significa que você aplica uma força sobre o objeto. E em que direção é essa força? Na direção em que eu estiver fazendo força.

Então, para mover um objeto, bastaria eu aplicar sobre ele uma força que tivesse a direção deseja...

Tendo isso em mente, se eu quiser fazer meu player empurrar algo, basta de dizer que, se ele estiver colidindo com objeto, faça força sobre ele, ou seja, que some em seus eixos as forças atuantes sobre o player.

Então:

	function draw() {
	  background(0);

	  fx = 0;
	  fy = 0;
	  if(keyIsDown(LEFT_ARROW)){
	    fx = -speed;
	  }
	  if(keyIsDown(RIGHT_ARROW)){
	    fx = +speed;
	  }
	  if(keyIsDown(UP_ARROW)){
	    fy = -speed;
	  }
	  if(keyIsDown(DOWN_ARROW)){
	    fy = +speed;
	  }
	  px = px + fx;
	  py = py + fy;
	  fill(255);
	  ellipse(px,py,pr,pr);  


	  var soma_raios = (pr+enemy_R)/2; 
	  var distance = dist(px,py,enemy_X,enemy_Y)
	  if(distance < soma_raios){
	    enemy_X = enemy_X + fx;
	    enemy_Y = enemy_Y + fy;
	  }
	  fill(255,0,0);
	  ellipse(enemy_X,enemy_Y,enemy_R,enemy_R);
	}
