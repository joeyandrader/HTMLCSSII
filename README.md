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

**Breve mais conteudo sobre.. porque ate eu nao entendi muito bem so sei que serve para isso ai**