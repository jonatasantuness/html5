# Introdução


## O que é HTML?

O HTML (Linguagem de Marcação de Hipertexto) é uma linguagem de marcação utilizada para definir a estrutura do conteúdo de páginas Web.

"Hipertexto" são os links que conectam as páginas da Web entre si. Os Links são um aspecto fundamental da web. Ao carregar conteúdo na Internet e vinculá-lo à páginas criadas por outras pessoas, você se torna um participante ativo na world wide web.

O HTML utiliza tags de "Marcação" para anotar texto, imagem e outros conteúdos que podem ser exibidos em um navegador Web. As marcações podem formatar visualmente a página além de dar a cada elemento algum valor semântico.

A marcação HTML inclui "elementos" especiais como:

```html
<head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, <div>, <span>, <img>, <aside>, <audio>, <canvas>, <datalist>, <details>, <embed>, <nav>, <output>, <progress>, <video>, <ul>, <ol>, <li>
```

## Elementos

O nome de um elemento dentro de uma tag é insensível a maiúsculas e minúsculas. Isto é, pode ser escrito em maiúsculas, minúsculas ou um mistura.

![Estrutura de uma Tag](../img/estrutura-tag.png)

As principais partes de um elemento são:

- **Tag de abertura**: Consiste no nome do elemento (no caso, p), envolvido em parênteses angulares de abertura e fechamento. Isso demonstra onde o elemento começa.
- **Tag de fechamento**: Isso é a mesma coisa que a tag de abertura, exceto que inclui uma barra antes do nome do elemento. Isso demonstra onde o elemento acaba. Esquecer de incluir uma tag de fechamento é um dos erros mais comuns de iniciantes e pode levar a resultados estranhos.
- **Conteúdo**: Esse é o conteúdo do elemento, que nesse caso é apenas texto.
- **Elemento**: A tag de abertura, a de fechamento, e o conteúdo formam o elemento.

Elementos também podem ter atributos, como no exemplo abaixo:

![Atributo de elemento](../img/elemento-atributo.png)

>Nota: Valores de atributos simples que não contém espaço em branco ASCII (ou qualquer um dos caracteres " ' ` = < >) podem permanecer sem aspas, mas é recomendável colocar aspas em todos os valores de atributos, para tornar o código mais consistente e compreensível.

Alguns elementos não possuem conteúdo e são chamados de elementos vazios. Considere o elemento **"img"** que temos na nossa página HTML:

```html
<img src="imagens/firefox-icon.png" alt="imagem de teste">
```

## Anatomia de um documento HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Página de teste</title>
  </head>
  <body>
    <img src="imagens/firefox-icon.png" alt="Imagem de teste">
  </body>
</html>
```

Aqui nós temos:

- ``` <!DOCTYPE html> ``` : Antigamente o doctype era utilizado como link para um conjunto de boas práticas de uma página HTML, o que poderia significar checagem automática de erros e outras coisas úteis. No entanto, atualmente, eles não fazem muito sentido e são basicamente necessários apenas para garantir que o documento se comporte corretamente.
- ``` <html></html> ``` : Esse elemento envolve todo o conteúdo da página e é conhecido como o elemento raiz.
- ``` <head></head> ``` : Fazendo a análogia, esse elemento funciona como o "cérebro" do HTML, nele incluimos links para folhas de estilo, scripts, informações relevantes para motores de busca e outras funcionalidades que não ficam visíveis na página.
- ``` <meta charset="utf-8"> ``` : Metadados são informações que descrevem o conteúdo do seu arquivo, a tag meta deve estar sempre dentro da tag head e pode representar vários tipos de metadados. O atributo charset serve para indicar o formato de codificação de caracteres utilizado no documento.
*ASCII*, *UTF-8*, *ANSI* e *ISO-8859-1* são exemplos de charsets. Cada charset representa um caracter em memória de uma forma diferente. O charset **UTF-8** é o que usamos na web atual e faz parte de um padrão chamado Unicode, sem ele teriamos problemas ao utilizar palavras com acentuação por exemplo.
- ``` <title></title> ``` : Define o título da página, o título que aparece na guia do navegador e também é usado para descrever a página ao adicioná-la aos favoritos.
- ``` <body></body> ``` : Contém todo o conteúdo que você quer mostrar ao público que visita sua página, seja texto, imagens, vídeos, jogos, etc.