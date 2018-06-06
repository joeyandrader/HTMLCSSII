# HTMLCSSII
Curso HTML5 e CSS3 II: Turbinando as suas páginas : https://cursos.alura.com.br/course/avancando-html-css



<p align="center">
  <img src="https://givingdata.com/wp-content/uploads/2013/07/html-css-js.png">
</p>

# Aula 1: Pixels?

## 1.0 : A medida de % e "em" como funciona.

> A unidade % e "em" funciona da mesma maneira.
> Assim podemos deixar o site responsivo e mais flexivel possivel. podendo usar com varios elementos.

### Como por exemplo:
### Podemos Usar as duas formas
```css
 p {
   font-size: 100%;
   font-family: "arial", sans-serif;
 }
```
```css
 p {
   font-size: 1em;
   font-family: "arial", sans-serif;
 }
```

### Concluimos entao que a fonte da tag:
```html
<p>text</p>
```

> Vai ter um tamanho de 100% com base na fonte padrao do navegador... onde 1em vamos obter o mesmo resultado

## 1.1 : A medida de "rem".

> Podemos aplicar porcentagens em todos os elementos, mais lembrando que algumas vezes podem ta relacionado a largura do elemento pai, assim gerando algumas confusoes.

### Como por exemplo

    1,25 rem = 1,25 x tamanho da fonte

### Se o tamanho da fonte do navegador como por exemplo for 16px, seria:

    16px X 1,25rem = 20px

## 1.2 : A medida de "ch".

>A unidade ch define o tamanho da fonte em relação à largura do caractere "0".

>Supondo que o seu elementos filhos sao baseado na largura do pai, então podemos utilizar uma medida que facilita principalmente na edição de textos dentro de caixas, a medida ch:

>Modificando o tamanho da fonte do navegador, esta medida também modifica-se. Essa medida é boa porque não importa muito a fonte que você está utilizando, ela se adequará muito bem.

>1 ch = largura do caractere "zero" da fonte utilizada

# Aula 2 : Absolute mais a fundo.

## 2.0 Propriedades Positions.

>Aqui vamos entender um pouco mais sobre as proriedades position.

>Para posicionar seus elementos, você precisa inserir uma coordenada. Essas coordenadas são comandadas pelas propriedades: top, left, right ou bottom. Todos os valores de positions só trabalham com essas coordenadas

>Lembrando que se for definir uma propriedade "**left**" não é preciso por "**Right**". O mesmo com top e bottom.

>Um Exemplo:

```html
<style>
    div {
      position: absolute;
      top: 150px;
      left: 150px;
    }
</style>
```
>Nesse caso eu posicionei o elemento a 150 pixels do topo e 150px da esquerda.

## 2.1 Tipos de position

>Existem 3 tipos de valores que usamos na propriedade position: relative, absolute e fixed.

### 2.1.1 Position Fixed
>Essa propriedade faz com que o elemento que voce deseja ficará fixada em um determinado local da pagina web na qual voce definir. E conforme você navega na página o elemento continua onde você o colocou.

>Definindo isso:

```html
<style>
		div#sidebar {
			width: 200px;
			height: 300px;
			background: #75AD45;
			border: 2px solid black;
			position: fixed; /* Fixa o elemento nas coordenadas seguintes */
			top: 30px;
			right: 30px;
			color: white;
			padding: 10px;
    }
</style>
```
>Teremos um Resultado igual a esse. Voce pode ver um exemplo nesse link
> <a href="http://tableless.github.io/exemplos/position-fixed.html">Exemplo de Position Fixed</a>

### 2.1.2 Position Relative

>O position relative posiciona o elemento em relação a si mesmo. Ou seja, o ponto zero será o canto superior esquerdo, e ele começará a contar a partir dali.

>A um exemplo em uma imagem abaixo:

<p align="center">
<img src="https://raw.githubusercontent.com/diegoeis/tableless-static-images/master/2009/05/position-absolute.gif" width="300" height="250">
</p>

### 2.1.2 Position Absolute

>Position Absolute se utiliza do ponto superior esquerdo de outros elementos. Estes elementos são os parentes dele do elemento com position absolute. Mais especificamente o pai.

<p align="center">
<img src="https://raw.githubusercontent.com/diegoeis/tableless-static-images/master/2009/05/flickr-exemplo.jpg" width="300" height="250">
</p>

>No caso, se o DIV pai não tivesse position definido, o div filho iria se referenciar pelo BODY mesmo. Se caso o div pai não tivesse position definido, e se ele também fosse envolvido por outro div com position, o div filho iria se referenciar por este terceiro div.

>Ou seja, ele se baseia no parente mais próximo com position (até chegar ao body caso nada tenha).

# 3.0 Bordas arredondadas e outras novidades do CSS3

## 3.1 Border Radius
>Uma outra propriedade Incrivel presente no css3, é como podemos arredondar bordas.
>Quando usamos uma tag tipo a "**div**" notamos que é uma caixa um quadrado.
>Podemos facilmente mudar isso com novas propriedade "**border-radius**"

>Entao no CSS dizemos que queremos arrendondar a borda da "**div**" com o "**border-radius**".

>Exemplo:
 ```html
<style>
  div {
    border-radius: 10px;
}
  </style>
 ```
 >Então fica assim:

 <p align="center">
<img src="http://i.imgur.com/cAyGxCu.jpg" alt="exemplo de borda arredondada" width="200">
 </p>

 ## 3.2 Como os navegadores se comporta

 >Quando pensamos em criar nosso site e por ate mesmo um estilo legal como o border-radius, pensamos, será que isso vai funcionar em todos os navegadores?.

 >Como será que os navegadores implementaram essas funcionalidades?

 >A gente como desenvolver queremos que nosso site funcione em todos os navegadores.

 >para isso basta apenas usar:

 ```
 Para o google Chrome

 -webkit-border-radius:
 ```

 ```
 Para o FireFox
 
 -moz-border-radius
 ```

 ```
 Para o Explorer
 
 -ms-border-radius
 ```

 ```
 Para o Opera
 
 -o-border-radius
 ```

 ```
 Para o Safari
 
  -webkit-border-radius
 ```
>Muitos navegadores ja estao adaptando para uma so funcionalidade. Os três prefixos principais se resumem em: -webkit-, -ms- e -moz-.

>Usando dessa maneira.

```
-webkit-border-radius: 10px;
-moz-border-radius: 10px;
-ms-border-radius: 10px;
-o-border-radius: 10px;
border-radius: 10px;
```
>Garante Funcionalidade em todos os navegadores,e ate mesmo para alterações futuras. Sem precisar alterar nada no seu codigo.

### Outra pergunta: mesmo assim, ainda se faz necessário deixar o código cheio desses prefixos?
> Na verdade não, tratando-se do border-radius só é preciso:
> ```  
>-webkit-border-radius: 10px;
>-moz-border-radius: 10px;
>border-radius: 10px;
>```

>Outros exemplos mais explicativo:

 <p align="center">
<img src="https://i.stack.imgur.com/FnIqF.png" alt="exemplo de borda Elipticas" width="450" height="150">
 </p>

## 3.3 Propriedade elípticas.

>Como vimos, o border-radius nos permite fazer não apenas bordas redondas como também bordas elípticas.

>Como exemplo abaixo:

 <p align="center">
<img src="http://caelum-online-public.s3.amazonaws.com/avancando-html-css/foto-torta.jpg" alt="exemplo de borda Elipticas" width="200">
 </p>

 > A sintaxe para o border-radius criar bordas elípticas é a seguinte:

 ```
 border-radius: <raios na horizontal> / <raios na vertical>;

 Definido seria assim

 border-radius: 10% 50% / 50% 10%
 ```

 ## 3.4 Propriedade fictícia.

 >Imagine que uma nova especificação do CSS está surgindo para permitir a criação de elementos 3D na página

 >Seria nescessario a propriedade "**depth**" (profundidade)

>Se quisermos testar essa propriedade num site nosso, fazendo um elemento com a classe botao ter uma profundidade de 10px, como deve ser a declaração para conseguirmos testá-la no maior número de usuários possível?
 >```html
 ><style>
  >   .botao {
   >      -webkit-depth: 10px;
   >      -moz-depth: 10px;
   >      depth: 10px;
   >  }
 >  </style>
 >```

 ## 3.5 Prefixos em valores.

 > Com o valor "**calc**" conseguimos fazer calculos no css3.

 >Podemos fazer, por exemplo, com que um elemento tenha metade da largura do item pai menos 10 pixels:

 ```html
 <style>
   div {
    width: calc(50% - 10px);
   }
</style>
 ```
 >E para Suportar bem nos navegadores, apenas atribuir os codigo como exemplo abaixo.

 ```html
 <style>
 div {
    width: -webkit-calc(50% - 10px);
    width: -moz-calc(50% - 10px);
    width: calc(50% - 10px);
}
</style>
 ```
 
 >Mais exemplos:  [Exemplo de calc](https://user-images.githubusercontent.com/24694674/28215628-56c9e7da-68b7-11e7-94d0-a0c44ac5d026.png)

 # Aula 4: Transformações.

 >Vemos que temos podemos transformar algumas coisas no nosso HTML, como um cubo por exemplo.

 > Para isso temos as propriedades ```transform``` e ```perspective```.

 ## 4.1 A propriedade transform.

 >O ```transform```: Faz com que podemos girar, dimensionar, inclinar ou traduzir um determinado elemento, e é uma propriedade poderosa, mas também muito simples de usar. Basta especificar o tipo de transformação que queremos fazer com o objeto:

 >Tem como propriedades como:

 - rotate.
 - scale.
 - skew.
 - translate.

 ```css
 div {
    transform: ...;
}
 ```
 >Exemplos :

 - Com o ```rotate```
- Aqui o objeto está sendo rotacionado em 30 graus:

```css
div {
    transform: rotate(30deg);
}
 ```

 <p align="center">
<img src="http://i.imgur.com/vmAnwrg.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

- Com o ```scale```
- Aqui o objeto aumenta em 1,5 vezes:

```css
div {
    transform: scale(1.5);
}
```

  <p align="center">
<img src="http://i.imgur.com/Gn7nntI.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

 - Com o ```skew```
 - Aqui os ângulos do objeto crescem ou diminuem em 20 graus:

 ```css
div {
    transform: skew(20deg);
}
```

  <p align="center">
<img src="http://i.imgur.com/T3Es5XP.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

 - Com o ```translate```
 - Aqui o objeto foi transladado 10 pixeis para a direita e 50 para baixo:

 ```css
div {
    transform: translate(10px, 50px);
}
```

 <p align="center">
<img src="http://i.imgur.com/yaGxb3m.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

 >Lembrando que como essa propriedade é relativamente nova, talvez seja interessante acrescentar antes dela o prefixo BETA, para versões mais antigas de navegadores:

 ```css
div {
    -webkit-transform: skew(20deg)
        rotate(30deg)
        scale(1.2);
    transform: skew(20deg)
        rotate(30deg)
        scale(1.2);
}
 ```

 ## 4.2 Transformações 3D / propriedade perspective.

 >Com o 3D trabalhamos em 3 eixos para definir o tamanho de nossos objetos: ```x```, ```y``` e ```z```.

  <p align="center">
<img src="http://i.imgur.com/KH7xOki.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

 >Para isso colocamos:
- translateX
- translateY
- translateZ

>Exemplo com codigo:

```css
div {
    transform: translateX(2px);
}
div {
    transform: translateY(4px);
}
div {
    transform: translateZ(6px);
}
```
**Breve mais conteudo sobre.. porque ate eu nao entendi muito bem so sei que serve para isso ai**

# Aula 5 :  Sombras e opacidade.

>Temos formas de sombreamentos e efeitos interessante no nosso CSS, para deixar nosso HTML bem mais interessante. Dois deles são as sombras e a opacidade. Eles destacam os elementos ou dão efeito de iluminação e tridimensionalidade.

## 5.1 Text-Shadow.

>O primeiro que vamos falar é sobre o ```text-shadow```: Que recebe algumas configurações para dar impressão de tridimensionalidade, perspectiva, difusão de luz, além de escolher a cor dessa sombra.

- exemplo como no meu codigo HTML.

```css
h1 {
    text-transform: uppercase;
    font-size: 3em;
    text-shadow: 5px 5px #000;
}
```
- No codigo acima temos o os parametros , ```5px``` ```5px``` e ```#000```.
- o primeiro parametro ```5px``` quer dizer sombra para direita.
- o segundo paramentro ```5px``` quer dizer para baixo.
- o terceiro parametro ```#000``` é a corda sombra.
- se inverter o ```5px``` para ```-5px``` ja da para perceber ne ? esquerda e para cima.

>Terá esse efeito.

<p align="center">
<img src="http://i.imgur.com/Xx8vEXB.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

 >Podemos aplicar esse efeito em qualquer texto do nosso site.

## 5.2 Box-Shadow.

>Outra propriedade que funciona igual o ```text-shadow``` é o ```box-shadow```, que atribui sombreamento aos elementos de caixa.

- Como Exemplo:

```css
.foto-home {
    height: 200px;
    border-radius: 50%;
    box-shadow: 0 0 1em #000;
}
```


>Terá esse efeito:

<p align="center">
<img src="http://i.imgur.com/fl9RNe1.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

>O Mais interessante é poder atribuir esses efeitos em botoes de links.

- Por Exemplo:

```css
.botao-index {
    font-size: 1.25em;
    background-color: #851944;
    color: #FFF;
    padding: .5em;
    border: .2em solid black;
    width: 40ch;
    margin: 2em auto;
    display: block;
    text-align: center;
    box-shadow: 0 0 1em #000, inset 0 0 .5em #FFF;
}
``` 

>Terá esse efeito:

<p align="center">
<img src="http://i.imgur.com/aWQP8yI.jpg" alt="exemplo de borda Elipticas" width="380" height="120">
 </p>

 - Notamos que a uma nova propriedade no ``` box-shadow```  que seria o ```"inset"```  
 
 - ```Inset``` : Faz com que o efeito de sombreamento seja dentro do elemento caixa. Funciona apenas com o ```box-shadow```.

 ## 5.3 Opacidade e cores semitransparentes.

 >Outro elemento interessante de efeito para o nosso HTML é o ```opacity```.

 >A opacidade faz com que podemos deixar o nosso elemento transparente invisivel, semi-transparente ou totalmente visivel.

 - Exemplos:

 ```css
 .rodape-pagina {
    ...
    opacity: .3;
}
 ```

- Ficaria então assim:

<p align="center">
<img src="http://i.imgur.com/J5lvghX.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>
 
 - Definimos o valor de 0.3 de opacidade.

 >Nota que o rodapé mais a fonte estao com opacidade de 0.3.

 - Os valores que podemos passar varia de ```0``` a ```1```. Onde ```0``` totalmente invisivel e ```1``` totalmente visivel.

 >So que temos um problema em relação a isso. quando definimos um valor de ```opacity``` em um elemento cujo esse elemento for pai, ele ira aplicar a transparencia em todos os elemtos ou seja, nos filhos.

 - Para isso temos uma outra propriedade interessante também para aplicar esse efeito de transparencia.

 - exemplo

 ```css
.rodape-pagina {
    background-color: rgba(0, 0, 0, .3);
    ...
}
 ```
<p align="center">
<img src="http://i.imgur.com/ai1Byr7.jpg" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

 - Nota que so o background do rodapé está com opacidade de 0.3.

 >O que usamos é que nem quando definimos uma cor para nosso texto usando o ```RGB```. So que com mais um adicional ```RGBA``` o ```A``` quer dizer o ```ALPHA``` da cor, o que define a transparencia a opacidade da cor.

 <p align="center">
<img src="https://www.techfry.com/images/webmaster/css-rgba.png" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

# Aula 6 : Gradientes.

 > Um efeito super interessante é o Gradient color. Com ele conseguimos criar varios efeitos de cores, Combinar uma cor a outra e etc.

 - No CSS, podemos definir os tipos de cores e combinações que queremos por, com isso usamos o ```linear-gradient()```, que receberá alguns parâmetros:
 
 >Como Exemplos:

 ```css
 .titulo-principal {
     ...
    background-image: linear-gradient(to bottom, #F00, #000);
}
 ```
 - O ```"to bottom"``` indica que o gradiente acontece de cima para baixo. Logo depois escolhemos as cores dos gradientes, neste caso do vermelho ```(#F00)``` ao preto ```(#000)```. Como resultado temos:

  <p align="center">
<img src="http://i.imgur.com/EkbMXxs.jpg" alt="exemplo de borda Elipticas" width="500" height="150">
 </p>

 >Podemos acrescentar também mais de uma cor alem dessas duas que definimos..

 - Exemplo:

 ```css
.titulo-principal {
    ...
    background-image: linear-gradient(to bottom, #F00, #888, #000);
}
 ```
  <p align="center">
<img src="http://i.imgur.com/wUvNYRc.jpg" alt="exemplo de borda Elipticas" width="500" height="150">
 </p>

 >Alem de que podemos definir uma transição de cor entre outra. Quando queremos que a mudança de vermelho para cinza ocorra a uns 80% da altura da imagem, de cima para baixo, deve ficar mais ou menos assim:

  - Exemplo:

 ```css
.titulo-principal {
    background-image: linear-gradient(to bottom, #F00, #888 80%, #000);
}
 ```
  <p align="center">
<img src="http://i.imgur.com/F9jpizs.jpg" alt="exemplo de borda Elipticas" width="500" height="150">
 </p>

 > E assim temos esses efeitos entre as cores.

 ## 6.1 Background size gradient.

 >também podemos redimencionar nosso gradient de cores ou ate mesmo imagens.

 - Usamos a propriedade ```background-size```.
 
 ```css
 .titulo-principal {
     ...
    background-size : 100% 200px;
}
 ```

   <p align="center">
<img src="http://i.imgur.com/zaBRjxT.jpg" alt="exemplo de borda Elipticas" width="500" height="150">
 </p>

 ## 6.2 Background repeat gradient.

 >O gradiente se repete automaticamente. Podemos desligar esse comportamento utilizando a propriedade background-repeat:

  - Usamos a propriedade ```background-repeat```.
 
 ```css
.titulo-principal {
    ...
    background-repeat: no-repeat;
}
 ```

   <p align="center">
<img src="http://i.imgur.com/ledOrSZ.jpg" alt="exemplo de borda Elipticas" width="500" height="150">
 </p>

 ## 6.3 Background attachment gradient.

 >Temos também a propriedade background-attachment, com o valor "fixed". Ela dá aquele efeito de paralaxe na imagem ou na textura do background. É como se elas estivessem fixas à tela do computador.

 ```css
.titulo-principal {
    ...
    background-attachment: fixed;
}
 ```

 ## 6.4 Background position gradient.

 >Outra propriedade interessante é o ```background-position```que podemos definir uma posição para o nosso gradient e com ele criar varios efeitos legais.

 - exemplo:

 ```css
    div {
        min-height: 100%;
        background-color: black;
        background-image: linear-gradient(to right, black, #C00, black);
        background-repeat: no-repeat;
        background-size: 80% 5px;
        background-position: 50% 50%;
    }
 ```

> com esse exemplo temos o resultado de:

   <p align="center">
<img src="http://caelum-online-public.s3.amazonaws.com/avancando-html-css/gradiente-exercicio-bg.png" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

- Note que definimos 50%  e 50% assim centralizando na pagina.

## 6.5 radiais gradient.

>O navegador também é capaz de gerar gradientes radiais, nos quais a cor muda a partir de um ponto em todas as direções.

```css
div {
    ...
    background-image: radial-gradient(yellow, red);
}
```
- Ficaria assim:

<p align="center">
<img src="http://caelum-online-public.s3.amazonaws.com/avancando-html-css/gradiente-radial.png" alt="exemplo de borda Elipticas" width="350" height="250">
 </p>

# Aula 7 Seletores avançados do CSS.

> Alem de seletores como classes e id's. Temos outros seletores que fazem varias coisas interessantes quando queremos selecionar um elemento especificos.

## 7.1 A ~ B:

> Quando queremos selecionar um segundo item em diante . Tipo uma lista.

- Exemplo :

```css
li ~ li {
    margin-top: 1em;
}
```
- Nesta Lista de ```<li>``` a segunda linha em diante vai receber o ```margin-top: 1em;```.

## 7.2 A + B:

>Quando queremos modificar por exemplo um paragrafo depois de um elemento.

- Exemplo :

```html
 <img>
    <p>...</p>
    <p>...</p>
    <p>...</p>
```

- Temos acima o HTML

```css
p {
    text-indent: 4ch;
}

img + p {
    text-ident: 0;
}
```
- No CSS temos todos os paragrafos com ```4ch``` de indentação. Mas Quando inserimos ```img + p``` apenas o primeiro paragrafo não terá a indentação.
- 
## 7.3 A > B:

>Quando queremos editar todos os filhos diretos do primeiro elemento, sem modificar os elementos mais internos.

- Exemplo:

```html
<div>
    <p>...</p>
    <blockquote>
        <p>...</p>
    </blockquote>
    <p>...</p>
</div>
```

- Temos esse HTML acima: com esse CSS.

```css
 div > p {
     color: red;
 }
```

- Apenas os paragrafos dentro da ```<div>```será afetado com a cor vermelha.

```html
<div>
    <p>AFETADO PELO VERMELHO</p>
    <blockquote>
        <p>NAO AFETADO PELO VERMELHO</p>
    </blockquote>
    <p>AFETADO PELO VERMELHO</p>
</div>
```

> Podemos combinar também os seletores:

```css
    .noticia > h1 + p
```
- Aqui estamos pegando todos os títulos "h1" dentro da classe ".noticia" e os parágrafos imediatamente depois desses "h1".

# Aula 8 : Pseudoclasses.

## 8.1 Classes Estruturais:

- :nth-child(odd) **Linhas ímpares**
- :nth-child(even) **Linhas pares**

>Quando criamos uma tabela e queremos atribuir cores a determinado elemento da tabela sem que precisar por classes em cada ```<tr>```, podemos ultilizar os pseudoclasses como mostrado acima.

- Ficaria assim a tabela :

```html
    
    <table>
        <tr>...</tr>
        <tr>...</tr>
        <tr>...</tr>
        <tr>...</tr>
        <tr>...</tr>
    </table>
    
```
- usando os pseudoclasses

```css
    tr:nth-child(odd) {
        Linhas impares  
        ... 
    }  
    tr:nth-child(even) {
        Linhas pares
        ...
    } 
```

> Podemos usar também outra forma de atribuir estilo para um elemento. 

 - Na linguagem que estamos usando, generalizamos essas pseudoclasses com ```":nth-child()"```. Dessa maneira, podemos estilizar não só as linhas pares ou ímpares:

 > Podemos inserir forma dentro do ```":nth-child()"```.

 > como nth-child(2n) que nada mais é do que as linhas pares. 
 
 > Ou nth-child(2n+1), que são as ímpares.


 -  ```:nth-child(xn + c)```

 - **X** é a periodicidade, de quantos em quantos elementos será aplicado o estilo;
 - **C** é o ponto de partida;
 - **N** é a variável, que começa em 0 (zero).

> Mais pseudosclasses
- ```:first-child``` **Primeira Linha**

> Pega o primeiro elemento, (a tabela que é o primeiro filho)

```css
tr:first-child (a tabela é pai e "first-child" é seu primeiro filho)
```
- E o ```:last-child``` que pega a sua **Ultima Linha**.


 > Breve edit**
- ```:nth-of-type```
## 8.2 Classes Dinâmicas:

 >Outa forma interessante de classes é usando esses 4 elementos abaixo:

- :hover
- :focus
- :active
- :checked

 ### 8.2.1 **hover**

> Quando usamos o ```hover``` teremos uma transoformação no nosso estilo ao passar com o mouse no elemento..
- Exemplo:

```html
    <a href="#" >Aqui temos um hover </a>
```

```css
    a {
        color: black;
    }
    a:hover {
        color: red;
    }
```
> A cor do link padrao definido com ```preto```. Ao passar o mouse em cima do link ela mudarar para ```Vermelho```.
> 
### 8.2.2 **focus**

>Quando usamos o ```focus``` teremos uma transformação no nosso estilo, ao clicar no link ele terar um focus conforme definido na folha de estilo...

```html
    <a href="#" >Aqui temos um focus </a>
```

```css
    a {
        color: black;
    }
    a:hover {
        color: red;
        font-size: 20px;
    }
```
> A cor do link padrao definido com ```preto```. Ao passar o mouse em cima do link ela mudarar para ```Vermelho``` e terá um tamanho de ```20px``` enquanto selecionado.

### 8.2.3 **active** 

>Quando usamos o ```active``` ativamos o elemento. Por exemplo, quando clicamos em um link e não soltamos o botão do mouse. Nesse momento, estamos ativando a ação do elemento. Esse estado é ativado também quando navegamos pelos links pelo teclado utilizando o TAB.

```html
    <a href="#" >Aqui temos um focus </a>
```

```css
    a {
        color: black;
    }
    a:active {
        color: red;
        font-size: 20px;
    }
```
> A cor do link padrao definido com ```preto```. Ao passar o mouse em cima do link ela mudarar para ```Vermelho``` e terá um tamanho de ```20px``` enquanto selecionado com o mouse, ao soltar o mouse do link ele volta para o padrao.

### 8.2.4 **checked**

>Quando usamos o ```checked``` teremos uma transformação no nosso estilo, ao clicar em uma tag do tipo ```input``` , ```radio```, teremos uma verificação.

```html
     <div>
        <input type="checkbox" name="my-checkbox" id="opt-in">
        <label for="opt-in">Checked</label>
    </div>
```

```css
div,

input {
  color: black;
}

input:checked + label {
  color: red;
}

input[type="checkbox"]:checked {
  box-shadow: 0 0 0 3px hotpink;
}
```
>Por padrao o ```checkbox``` esta com a cor ```preta```, ao clicar no ```checkbox``` terá uma borda ```rosa```, e uma cor de texto ```vermelho```.

# Aula 9 : Pseudoelementos

> Assim como o ```pseudo-classe```, o ```Pseudo-elementos``` são adicionados aos seletores mas em vez de descrever um estado especial, eles permitem que você aplique estilos em certas partes de um documento.

## 9.1 Tipos de pseudo-elementos

### 9.1.1 **first-letter**

- O ```::first-letter``` permiter pegar a primeira letra do conteudo de um elemento. Podemos usar esse conteudo ate mesmo para destacar uma letra inicial de um texto. Como por exemplo:
- 

```html
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
  tempor incididunt ut labore et dolore magna aliqua.
</p>

```
- NO CSS FICARIA.

```css
    p::first-letter {
        color: red;
        font-size: 32px;
    }

```
- Entao a palavra ```Lorem```, teria o ```"L"``` destacado em vermelho.

### 9.1.2 **before**

- O ```::before``` cria um falso elemento que nos permite adicionar conteúdo antes do conteúdo do elemento selecionado. como exemplo :

```html

    <div>
        Aqui um texto junto com o before antes
    </div>

```
- NO CSS

```css
    div::before {
        content: “pseudo-elemento ::before”;
        color: blue;
    }
```

- Nesse caso a palavra dentro do ```before``` na parte do ```content``` está aparecendo antes do texto e na cor ```azul``` na tag ```<div>```.

### 9.1.3 **after**

- O ```::after``` Também cria um falso elemento que nos permite adicionar conteúdo ao elemento selecionado, so que no final do elemento conteudo. Como por exemplo :

```html
    <div>
        texto que fica antes do conteudo after.
    </div>
```
- NO CSS

```css
    div::after {
        content: "pseudo-elemento ::after";
        color: red;
    }
```
- Com esse exemplo o texto dentro do ```content```aparece depois do texto descrito na tag ```<div>```.

# Aula 10 : Formulários

> Podemos Criar Formularios para nosso Web Site, Seja para inserir contato direto, ou para cadastro de usuarios e etc.

> Para isso Usamos as Tag ```<form>```, ```<label>``` e ```<input>```.

### 10.1 Tipos de Formularios

> Para definir um tipo de input precisamos passar o atributo que queremos

```html
<input type="" >
```

- ```type="text"``` > Refere-se a uma Caixa de texto.
- ```type="radio"``` > Refere-se a um circulo de marcação.
- ```type="email"``` > Refere-se a um campo para email.
- ```type="submit"``` > Refere-se a um Botão de validação.
- ```type="checkbox"``` > Refere-se a uma Caixa de marcação.
- ```type="password"``` > Refere-se a uma Caixa de texto para senhas.

- Entre varios outros, que pode consultar aqui <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/input">Mozzila Firefox Developer Inputs</a>


### 10.2 Input's

> A tag ```<form>``` é a base principal para se iniciar um formulario.

```html
    <form>
        ....
    </form>
```

- Fornece Entrada para o usuario.

> Em seguida podemos atribuir o ```<label>``` e o ```<input>```.
 
```html
    <form>
      <label>
          ...
          <input>
      </label>
    </form>
```

- a Tag ```<label>``` serve para identificar do que se trata aquela tag ```<input>```. Assim atribuindo uma forma especifica que seria o ```(for="")```. So que antes, na tag ```<input>``` é preciso definir um ```(id="")```.

```html
    <form>
      <label for="nome">
          Digite seu nome:
          <input type="text" id="nome">
      </label>
    </form>
```
- Assim o navegador identifica no qual aquele ```<input>``` se refere.

- Alem do ```for```, temos também o atribudo ```name```, no qual é sempre importante ter na maioria dos ```inputs```.

```html
    <label>
        <input type="radio" name="assunto">
        Consultoria
    </label>
```
- O navegador vai saber que aquilo se trata a um rotulo do input. E assim se tiver multiplos assuntos usando a tag ```type="radio"``` o navegador vai selecionar apenas um marcador daquele tema especifico ```"assunto"```.

 - So que precisamos também alem do ```name=""```, informar ao nosso servidor qual tipo de ```"assunto"```estamos se referindo. Por isso usamos mais um atribudo do ```<input>``` que seria o ```value=""```. 
 
```html
    <label>
        <input type="radio" name="assunto" value="consultoria">
        Consultoria
    </label>
```

- Assim o servidor vai receber dados do nosso ```<input>``` corretamente.