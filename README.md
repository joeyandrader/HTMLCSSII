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

>