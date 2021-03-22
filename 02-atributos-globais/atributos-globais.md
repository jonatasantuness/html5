# Atributos Globais

Atributos Globais são atributos comuns a todos elementos HTML;  eles podem ser usados em todos os elementos, embora os atributos não tenham efeito em alguns elementos.

## Estrutura básica do HTML:

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Titulo do Documento</title>
</head>
<body>
    
</body>
</html>
```

Elementos:

- **DOCTYPE**: Tipo do documento.
- **lang**: Linguagem da página.
- **meta charset**: Define o tipo de codificação dos caracteres.
- **meta viewport**: Viewport é área visível do dispositivo do usuário. Quando um layout fixo é acessado por um dispositivo móvel, ele é ajustado e reduzido para caber na tela como se fosse um layout para desktop, esse comportamento obriga o usuário a dar zoom na tela devido a má legibilidade. A meta tag viewport surgiu para que os devs tenham controle sobre o viewport e tenha acesso a media queries, portanto para fazer uma página responsiva é necessário utilizá-la. A configuração nesse exemplo é a mais comum, No nosso exemplo foi determinado que a largura que a largura do viewport é igual à largura do dispositivo e que o layout será exibido na largura inicial sem zoom. O atributo content recebe parâmetros que podem determinar a largura do viewport, a escala inicial para zoom, o valor máximo e mínimo de escala e até impossibilitar o usuário de efetuar zoom.
- **X-UA-Compatible**: É apenas uma correção para compatibilidade (principalmente para o Internet Explorer), para que o HTML5 funcione corretamente, neste caso, quando a página for acessada pelo IE, será utilizado o motor do Edge.
- **title**: Titulo do Documento, é exibido na aba do navegador.