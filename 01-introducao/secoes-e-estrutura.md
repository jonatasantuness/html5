# Seções e estrutura de um documento HTML5

O **HTML5** possui novos elementos que descrevem a estrutura de uma página web com semânticas padronizadas.

O **HTML4** usa a noção de seções e subseções de um documento para descrever sua estrutura. Uma seção é definida por um Elemento HTML de Divisão ```<div>``` com Elementos HTML de Cabeçalho ```<h1>, <h2> , <h3>, <h4>, <h5> e <h6>``` dentro de si, definindo seu título.

Os elementos ```<div>``` não são obrigatórios para definir uma nova seção. A mera presença de um Elemento de Cabeçalho HTML é suficiente para implicar uma nova seção. Portanto:

```html
<h1>Elefantes da floresta</h1>
<p>Nesta seção, discutiremos os pouco conhecidos elefantes da floresta.
...esta seção continua...
<h2>Habitat</h2>
<p>Os elefantes da floresta não vivem em árvores mas sim entre elas.
...esta subseção continua...
<h2>Dieta</h2>
<h1>Esquilo da mongólia</h1>
```

Semanticamente temos uma estrutura assim:

```html
1. Elefantes da floresta
   1.1 Habitat
   1.2 Dieta
2. Esquilo da mongólia
```

## Problemas resolvidos pelo HTML5

- **Elementos de Seção**: A perspectiva do **HTML4** é muito imprecisa em relação a o que é uma seção e como seu escopo é definido. O **HTML5** elimina a necessidade dos elementos ```<div>``` do algoritmo de estruturação introduzindo um novo elemento, O  ```<section>```, o elemento de Seção do HTML. 

- **Mesclando documentos**: Mesclar diversos documentos é uma tarefa complicada: a inclusão de um subdocumento em um documento principal significa pequenas alterações nos elementos de cabeçalho de modo que a estrutura geral do novo documento continue sólida. Isso é resolvido no HTML5 com a introdução dos elementos de seção ```<article>, <section>, <nav> e <aside>```, que são sempre subseções das seções ancestrais mais próximas, independentemente das seções criadas pelos elementos de cabeçalhos internos de cada subseção.

- **Elemento com informações secundárias**: No **HTML4**, toda seção é parte da estrutura do documento. Mas documentos não lineares são frequentes. Um documento pode ter seções especiais contendo informações que não fazem parte, a não ser que seja relatado, do conteúdo principal, como um bloco de avisos ou uma caixa de explicação. O **HTML5** introduz o elemento ```<aside>```, permitindo assim que tal seção não seja parte da estrutura principal do documento.

- **Informações semânticas sobre o documento**: Novamente, no HTML4 pelo fato de todas as seções semânticas com a tag ```<div>```< fazerem parte da estrutura do documento, não há formas de haver seções que contenham informações relacionadas não ao documento em si, mas ao site no geral, como logos, menus, tabelas de conteúdos, copyright ou avisos legais. Com esse propósito, o HTML5 introduz três novos elementos: ```<nav>```< para coleções de links (tal como uma tabela de conteúdos), ```<footer>``` e ```<header>``` para informações relacionadas ao site. Perceba que ```<footer>``` e ```<header>``` não são conteúdos de seção como o ```<section>```, ao invés disso, eles existem para delimitar semanticamente partes de uma seção.


## Definindo seções em HTML5

Todo conteúdo dentro do elemento ```<body>``` é parte de uma seção. Seções em  HTML5 podem ser encaixadas (aninhadas) com base na seção principal definida pelo elemento ```<body>```, os limites são definidos explicitamente ou implicitamente.

Seções definidas explicitamente são o conteúdo dentro das tags ```<body>,  <section>,  <article>,  <aside>, <footer>,  <header>, e <nav>```.

> Cada seção pode ter a sua própria hierarquia de cabeçalho ```<h1>```

Exemplo: Esse snippet HTML define duas seções de nível superior sendo que a primeira seção possui três subseções:

```html
<section>
  <h1>Forest elephants</h1>

  <section>
    <h1>Introduction</h1>
    <p>In this section, we discuss the lesser known forest elephants.
  </section>

  <section>
    <h1>Habitat</h1>
    <P>Forest elephants do not live in trees but among them.
  </section>

  <aside>
    <p>advertising block
  </aside>
</section>

<footer>
  <p>(c) 2010 The Example company
</footer>
```

Isso leva à seguinte estrutura:
```html
1. Forest elephants
  1.1 Introduction
  1.2 Habitat
  1.3 Section (aside)
```

## Definindo cabeçalho com HTML5

A regra básica é simples: o primeiro elemento de cabeçalho HTML (um de ```<h1>, <h2>, <h3>, <h4>, <h5>, <h6>```) define o cabeçalho da seção atual.

Os elementos de cabeçalho têm uma classificação fornecida pelo número no nome do elemento, onde ```<h1>``` tem a classificação mais alta e ```<h6>```} tem a classificação mais baixa. A classificação relativa é importante apenas dentro de uma seção; a estrutura das seções determina o contorno, não a classificação do cabeçalho das seções. Por exemplo:

```html
<section>
  <h1>Forest elephants</h1>

  <p>In this section, we discuss the lesser known forest elephants.
    ...this section continues...
  <section>
    <h2>Habitat</h2>

    <p>Forest elephants do not live in trees but among them.
    ...this subsection continues...
  </section>
</section>

<section>
  <h3>Mongolian gerbils</h3>

  <p>In this section, we discuss the famous mongolian gerbils.
     ...this section continues...
</section>
```

Isso leva à seguinte estrutura:
```html
1. Elefantes da floresta
  1.1 Habitat
2. Gerbos da Mongólia
```

> Observe que a classificação do elemento de cabeçalho (no exemplo ```<h1>```} para a primeira seção de nível superior, ```<h2>``` para a subseção e ```<h3>``` para a segunda seção de nível superior) não é importante. (Qualquer classificação pode ser usada como cabeçalho de uma seção definida explicitamente, embora essa prática não seja recomendada.)

## Seção implícita

Como os Elementos de Seção HTML5 não são obrigatórios para definir uma seção, para manter a compatibilidade com a Web existente dominada pelo **HTML4**, existe uma maneira de definir seções sem eles. Isso é chamado de corte implícito.

Quando os elementos de cabeçalho (```<h1> a <h6>```) não são o primeiro cabeçalho de suas seções pai, eles definem uma nova seção implícita, exemplo:

```html
<section>
  <h1> Elefantes da floresta </h1>

  <p>Nesta seção, discutiremos os elefantes da floresta menos conhecidos.</p>
    ... esta seção continua ...

  <h3 class="subseção-implícita">Habitat</h3>

  <p>Os elefantes da floresta não vivem em árvores, mas entre elas.</p>
    ... esta subseção continua ...
</section>
```

A estrutura fica assim:

```
1. Elefantes da floresta
  1.1 Habitat (definido implicitamente pelo elemento h3)
```

Se for da mesma classificação que o título do cabeçalho anterior, fecha a seção anterior (que pode ter sido explícita!) e abre uma nova implícita no mesmo nível:

```html
<section>
  <h1>Elefantes da floresta</h1>

  <p>Nesta seção, discutiremos os elefantes da floresta menos conhecidos.</p>
    ... esta seção continua ...

  <h1 class="seção implícita">Gerbos da Mongólia</h1>

  <p>Os gerbos da Mongólia são pequenos mamíferos fofos.</p>
    ... esta seção continua ...
</section>
```

A estrutura fica assim:

```
1. Elefantes da floresta
2. Gerbos da Mongólia (implicitamente definidos pelo elemento h1, que fechou a seção anterior ao mesmo tempo)
```

Se tiver uma classificação mais alta que o título do cabeçalho anterior, fecha a seção anterior e abre uma nova implícita no nível mais alto:

```html
<body>
  <h1> Mamíferos </h1>
  <h2> Baleias </h2>
  <p> Nesta seção, discutimos as baleias nadadoras.
    ... esta seção continua ...</p>
  <section>
    <h3> Elefantes da floresta </h3>
    <p> Nesta seção, discutiremos os elefantes da floresta menos conhecidos.
      ... esta seção continua ...</p>
    <h3> Gerbos da Mongólia </h3>
      <p> Hordas de gerbos se espalharam muito além da Mongólia.
        ... esta subseção continua ...</p>
    <h2> Répteis </h2>
      <p>Répteis são animais com sangue frio.
        ... esta subseção continua ...</p>
  </section>
</body>
```

A estrutura fica assim:

```
1. Mamíferos
  1.1 Baleias (definidos implicitamente pelo elemento h2)
  1.2 Elefantes da floresta (definidos explicitamente pelo elemento de seção)
  1.3 Gerbos da Mongólia (implicitamente definidos pelo elemento h3, que fecha a seção anterior ao mesmo tempo)
  1.4 Répteis (definidos implicitamente pelo elemento h2, que fecha a seção anterior ao mesmo tempo)
```

> Para tornar sua marcação compreensível por humanos, é uma boa prática usar tags explícitas para abrir e fechar seções e corresponder a classificação do cabeçalho ao nível de aninhamento de seção pretendido.

## Sobrepondo seções implícitas

Às vezes, uma seção precisa ter vários títulos, por exemplo, uma seção sobre um livro ou filme que possui um título secundário:

```html
<section>
  <h1>Justine</h1>
  <h2>Os Infortúnios da Virtude</h2>
</section>
```

leva ao seguinte esboço:

```
1. Justine
  1.1 Os Infortúnios da Virtude
```

O Elemento de Grupo de Cabeçalhos ```<hgroup>``` (introduzido no **HTML5**).oculta todos os títulos de cabeçalhos do esboço, exceto o primeiro, permitindo uma substituição do corte implícito. Com esse elemento, o exemplo do livro secundário:

```html
<section>
  <hgroup>
    <h1>Justine</h1>
    <h2>Les Malheurs de la vertu</h2>
  </hgroup>
</section>
```

leva ao seguinte esboço:

```
1. Justine
```

## Caminhos de Seção

Uma **raiz de seção** é um elemento HTML que pode ter seu próprio esboço, porém as seções e os títulos de cabeçalho dentro deles não contribuem para o esboço de seus ancestrais.

Ao lado de ```<body>```, que é a raiz de seção lógica de um documento, geralmente são elementos que introduzem conteúdo externo na página: ```<blockquote>```, detalhes , fieldset , figura e td .

Exemplo:

```html
<section>
  <h1>Elefantes da floresta</h1>

  <section>
    <h2> Introdução </h2>
    <p> Nesta seção, discutiremos os elefantes da floresta menos conhecidos</p>
  </section>

  <section>
    <h2> Habitat </h2>

    <p>Os elefantes da floresta não vivem em árvores, mas entre eles. Vamos veja o que os cientistas estão dizendo em "<cite> O elefante da floresta em Bornéu </cite>":
    <blockquote>
      <h1>Bornéu</h1>
      <p>O elemento florestal vive em Bornéu</p>
    </blockquote>
  </section>
</section>
```

Isso resulta no seguinte esboço:

```
1. Elefantes da floresta
  1.1 Introdução
  1.2 Habitat
```

Este esboço não leva em consideração o ```<h1>```d entro do ```<blockquote>``` que, sendo uma citação externa, é uma raiz de seção e isola seu esboço interno.


## Seções de fora da estrutura

O **HTML5** apresenta quatro novos elementos que permitem definir seções que não pertencem ao esquema principal de um documento da web:

### aside

O elemento ```<aside>``` define uma seção que, embora relacionada ao elemento principal, não pertence ao fluxo principal, como uma caixa de explicação ou um anúncio. Ele tem seu próprio esboço, mas não pertence ao principal.

### nav

O elemento ```<nav>``` define uma seção que contém links de navegação.

### header

O elemento ```<header>``` define um cabeçalho da página, geralmente contendo o logotipo e o nome do site e em geral contém um menu. Apesar do nome, ele não está necessariamente posicionado no início da página.

### footer

O elemento HTML da seção do rodapé ```<rodapé>``` define um rodapé da página, normalmente contendo os direitos autorais e legais observados e algumas vezes alguns links. Apesar do nome, ele não está necessariamente posicionado na parte inferior da página.

## Endereços e horário de publicação

O autor de um página geralmente deseja publicar algumas informações de contato, como o nome e o endereço do autor. O **HTML4** permitiu isso por meio do elemento ```<address>```, que foi estendido no HTML5.

O elemento ```<address>``` agora está vinculado ao seu ancestral mais próximo ```<body>``` ou ```<article>```.

> Um documento pode ser feito de seções diferentes de diferentes autores. Uma seção de outro autor que não a da página principal é definida usando o elemento ```<article>```.

> Da mesma forma, o novo elemento HTML5 ```<time>```, com seu conjunto de atributos booleanos pubdate, representa a data de publicação associada ao documento inteiro, respectivamente ao artigo, relacionado ao ancestral mais próximo ```<body>``` ou ```<article>```.