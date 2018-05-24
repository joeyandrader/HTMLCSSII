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
```html
 p {
   font-size: 100%;
   font-family: "arial", sans-serif;
 }
```
```html
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
>Essa propriedade faz com que o elemento que voce deseja ficará fixada em um determinado local da pagina web na qual voce definir...

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

