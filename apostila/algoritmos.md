# Algoritmos 

Um algoritmo é uma sequência de instruções bem definidas e organizadas que visam resolver um problema ou realizar uma tarefa específica. Na computação, os algoritmos são a base de todo o processo de resolução de problemas e são essenciais para o desenvolvimento de programas de software.

Um algoritmo é como uma receita culinária: ele descreve passo a passo o que precisa ser feito para alcançar um resultado desejado. Assim como uma receita detalha os ingredientes necessários e as etapas para preparar um prato, um algoritmo descreve os passos necessários para resolver um problema computacional.

**Definição 1:** "É uma sequência lógica de passos que visa atingir um objetivo específico."

## Características dos Algoritmos

1. **Definição precisa**: Cada passo do algoritmo deve ser claramente definido e compreensível.
1. **Entrada e Saída**: Um algoritmo geralmente recebe uma entrada (dados iniciais) e produz uma saída (resultado final) após executar todas as etapas.
1. **Finitude**: O algoritmo deve ter um número finito de passos e deve eventualmente terminar, ou seja, deve chegar a uma conclusão em um tempo finito.
1. **Eficiência**: Um algoritmo eficiente é aquele que resolve o problema de forma rápida e com uso mínimo de recursos.


## Exemplos de Algoritmos

### Algoritmo para Fazer um Sanduíche:
1. Pegue duas fatias de pão.
1. Espalhe manteiga em uma fatia de pão.
1. Coloque queijo e presunto na fatia de pão com manteiga.
1. Cubra com a segunda fatia de pão.
1. Corte o sanduíche ao meio.
1. Se quiser, adicione alface e tomate.

Este é um algoritmo simples que descreve como fazer um sanduíche. Cada passo é claro e direto.

### Como chegar ao parque?

1. Saia de casa em direção ao mercado
1. Depois da farmácia, dobre à direita
1. Conte 3 ruas e dobre à esquerda
1. Ande 500 metros e você chegará ao parque

### Chegar pontualmente à aula de 7:00 horas
1. Acordar às 5h30
1. Tomar banho
1. Tomar o café da manhã
1. Pegar a mochila
1. Sair para a parada de ônibus

### Algoritmo para contar até 10
1. Comece com o número 1.
1. Adicione 1 ao número atual.
1. Se o número for menor ou igual a 10, repita o passo 2.
1. Pare quando chegar a 10.
1. Este algoritmo mostra como contar até 10 usando repetição.

## Exercício 1
O pneu do carro furou, qual o algoritmo que você usaria para substituir o pneu furado?

## Introdução à Lógica 

* O que queremos dizer com “Tem lógica” ou “É lógico” 
* A lógica é o ramo da filosofia que cuida das regras do pensar correto. 
  * Usar corretamente as leis do pensamento
  * Determinar operações válidas ou não 
* A lógica é um meio de garantir que nosso pensamento proceda corretamente a fim de chegar a conhecimentos verdadeiros (válidos)
Colocar ordem no pensamento

### Exemplo 1
* Todo mamífero é um animal
* Todo cavalo é um mamífero
* Logo, todo cavalo é um animal

### Exemplo 2
* Daniela é mais jovem que Adriano
* Carlos é mais velho que Daniela
Logo:
  * Adriano é mais velho que Carlos (Falso)
  * Carlos é mais velho que Adriano (Falso)
  * **Daniela é a mais nova das 3 pessoas (Verdadeiro)**

### Exemplo 3
* “Se o RU servir cuscuz hoje, então eu jantarei no RU”
* “O RU serviu cuscuz”
* Logo, eu jantei no RU

### Exemplo 4 
* Um **pastor** precisa transportar **um carneiro e dois fardos de capim** para o outro lado do rio
* Ele possui um barco pequeno, que transporta **uma coisa de cada vez** (um carneiro ou um fardo de capim)
* Se ele deixar o carneiro junto do capim em alguma das margens do rio, o carneiro come o capim

[Slide da resposta do problema do pastor](https://docs.google.com/presentation/d/1YtX44dXYObqUFsdzCgRvY3sOjjj8UarzH5BIv_754AA/edit?usp=sharing) 

Sugestão de resolução:
1. Levar o carneiro para a margem leste
1. Voltar para a margem oeste
1. Levar um fardo para margem leste
1. Voltar com o carneiro para margem oeste
1. Levar o segundo fardo para margem leste
1. Voltar para margem oeste
1. Levar o carneiro para margem leste

### Outros desafios de lógica 
* [Torre de Hanói](https://www.noas.com.br/ensino-fundamental-1/matematica/torre-de-hanoi/)
* [Na Medida Certa](https://www.sitededicas.com.br/desafios-logicos-na-medida-certa.htm) 


### Por que estudar lógica e algoritmos? 
* Aprender **lógica** é aprender a como **“pensar correto”** para resolver um problema
* Uma sequência de passos é uma forma de explicar/organizar a solução para um problema

**Definição 2:** **Algoritmo** é uma forma de expressar o raciocínio **lógico.**


## Exercício 2

Veja abaixo o teste de QI japonês, conhecido como o problema da travessia do rio. O problema consiste em 8 pessoas que têm que atravessar um rio utilizando uma jangada (Fonte: http://www.japones.net.br/teste-de-qi-japones/).

As oito pessoas são:
* pai;
* mãe;
* dois filhos;
* duas filhas;
* um policial;
* um prisioneiro.

Para efetuar a travessia é necessário seguir algumas regras:
* A jangada só pode carregar duas pessoas por vez;
* Somente o pai, a mãe e o policial sabem manobrar a jangada;
* Os filhos não podem ficar com a mãe na ausência do pai em nenhuma das margens do rio;
* Os filhos não podem ser transportados pela mãe;
* As filhas não podem ficar com o pai na ausência da mãe em nenhuma das margens do rio;
* As filhas não podem ser transportadas pelo pai;
* O prisioneiro não pode ficar com os membros da família na ausência do policial;

# Formas de representação de algoritmos 

## Descrição Narrativa

* Uso da linguagem natural: Português, inglês, espanhol, etc.;
* Considera os passos mais importantes e pode servir de esboço para outras representações. 
* Temos a inconveniência da má interpretação, originando *ambiguidades* e *imprecisões*:
* Para evitar más interpretações, a escrita do algoritmo deve ser mais detalhada: 

### Exemplo 1 
* Chegar pontualmente na aula
  * Acordar às 5h30 
  * Tomar banho 
  * **Tomar o café da manhã** 
  * Pegar a mochila 
  * Sair para a parada de ônibus

### Exemplo 1 - Detalhado 
* Chegar pontualmente na aula
  * Acordar às 5h30 
  * Tomar banho 
  * **Tomar o café da manhã** 
    * Pegar leite na geladeira e servir em um copo 
    * Pegar uma fatia de queijo 
    * Cortar um pão ao meio e colocar o queijo 
    * Comer o sanduíche e tomar o leite 
  * Pegar a mochila 
  * Sair para a parada de ônibus


## Fluxograma 

> ![tabela-fluxograma](https://user-images.githubusercontent.com/19957124/122242073-68e3a680-ce99-11eb-95cc-bd6cf2c2f40a.jpg)
>
> Fonte da imagem: https://www.treinaweb.com.br/blog/conceitos-usados-no-aprendizado-de-programacao 

Exemplo de fluxograma para calcular a média a apartir das notas de três provas:

>  ![Fluxograma_algoritmo01](https://user-images.githubusercontent.com/19957124/122244222-17d4b200-ce9b-11eb-86c6-a8e6708b8d76.png)
>
> Fonte da imagem: [https://saulo.arisa.com.br/](https://saulo.arisa.com.br/wiki/index.php/Introdu%C3%A7%C3%A3o_%C3%A0_L%C3%B3gica_de_Programa%C3%A7%C3%A3o) 



## Pseudocódigo

* Estrutura semelhante às linguagens de programação, porem é uma forma rápida de expressar o algoritmo sem perder tempo com detalhes. 
* Mais didático e fácil compreensão 

### Exemplo - Média de dois números 

```java
inicio
  real n1,n2,r
  ler n1,n2
  r <- (n1 + n2) / 2.0
  escrever "A média é: ", r
fim 
```


## Linguagens de programação

Linguagem padronizada para descrever instruções para um computador. Possui um conjunto de regras sintáticas e semânticas usadas para descrever algoritmos e não possui ambiguidades. 

### Exemplo com a linguagem Javascript

```javascript
x = prompt("Entre com x: ") // leitura de x
y = prompt("Entre com y: ") // leitura de y
media = (parseFloat(x) + parseFloat(y))/2; // cálculo da média
alert("A média é "+media) // escrita do resultado
``` 


Códigos com exemplos na página de LoP no GitHub:
* https://github.com/ect-info/lop/tree/master/codigos 
* https://github.com/ect-info/lop 
* https://github.com/ect-info/codigos-jogo 

## Outros exemplos 
* [Maior que 25](https://whimsical.com/maior-que-25-FYNih4GsfHeXh3tpEz3Min) 
* [Algoritmo representado em forma de um fluxograma](http://www.cristiancechinel.pro.br/my_files/algorithms/bookhtml/node15.html)

## Programação 

Aprender a programar é aprender a resolver problemas usando algoritmos e uma linguagem de programação. Aprender a dividir um problema grande em problemas pequenos resolvendo um problema por vez. Este curso de Lógica de Programação foca em resolver problemas matemáticos. 

## Exercício 1

Você está construindo uma piscina que mede 4,0 metros de largura, 9,0 metros de comprimento e 2,0 metros de profundidade. Para não gastar demais, você precisa calcular exatamente quantos azulejos serão necessários para toda a piscina. Considere que os azulejos medem 60 x 60 cm cada. 
* Qual a sequência de passos (o algoritmo) para resolver esse problema matemático?

Solução 1: 
* Calcular quantos azulejos são necessários para cobrir toda a área da piscina. 

A solução anterior é muito abstrata. Não estão claras as ações necessárias para resolver o problema. É necessário um detalhamento maior. 
Solução 2: 
1. Calcular quantos azulejos são necessários no piso
2. Calcular quantos azulejos são necessários em cada parede
3. Somar o resultado dos passos 1 e 2

Como calcular o passo 1?
* Área total = 4 * 9 = 36m²
* Área do azulejo = 0,6 * 0,6 = 0,36m²
* Quantidade de azulejos = 36 / 0,36 = 100
Essa solução usa azulejos quebrados. 

É possível aprimorar a resolução deste problema da seguinte forma. Para calcular quantos azulejos inteiros serão necessário basta proceder com o seguinte algoritmo: 
a. Calcular quantos azulejos são necessários na largura
b. Calcular quantos azulejos são necessários no comprimento
c. Multiplicar o resultado dos passos a) e b)

## Referências
* [Livros](https://github.com/ect-info/lop/blob/master/bibliografia.md)
* [Cursos online](https://github.com/ect-info/lop/blob/master/cursos_online.md)
* [Outras referências](https://github.com/ect-info/lop/blob/master/referencias.md)

## Cursos Online 
* [Introdução a Programação da Khan Academy](https://pt.khanacademy.org/computing/computer-programming/programming) 
* [Introdução a Computação na Cursera](https://www.coursera.org/learn/ciencia-computacao-python-conceitos) 





