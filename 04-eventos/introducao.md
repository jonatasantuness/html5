# Eventos

## O que são eventos?

Os Eventos Dom (Dom Events) são gatilhos utilizados para notificar ou acionar códigos associados à interação do usuário durante a navegação. Cada evento é representado por um objeto que é baseado na interface [Event](https://developer.mozilla.org/pt-BR/docs/Web/API/Event), e pode ter campos customizados adicionados e/ou funções usadas para obter informações adicionais sobre o evento ocorrido.

Por exemplo, se o usuário clica em um botão numa pagina web, você pode querer responder a esta ação mostrando na tela uma caixa de informações.

No caso da web, eventos são disparados dentro da janela do navegador, e normalmente estão associados à algum item especifico nele — pode ser um único elemento, um conjunto de elementos, o HTML carregado na guia atual, ou toda a janela do navegador. Existem vários tipos diferentes de eventos que podem vir a acontecer, por exemplo:

- O usuário clicando com o mouse sobre um certo elemento ou passando o cursor do mouse sobre um certo elemento.
- O usuário pressionando uma tecla do teclado.
- O usuário redimensionando ou fechando a janela do navegador.
- Uma pagina da web terminando de carregar.
- Um formulário sendo enviado.
- Um video sendo reproduzido, interrompido, ou terminando sua reprodução.
- Um erro ocorrendo.

## Manipuladores de Evento (Event Handler)

Cada evento disponivel possui um **manipulador de eventos (event handler)**, que é um bloco de código (geralmente uma função JavaScript definida pelo usuário) que será executado quando o evento for disparado.

Quando esse bloco de código é definido para rodar em resposta à um evento que foi disparado, nós dizemos que estamos **registrando um manipulador de eventos**.

Note que manipuladores de eventos são, em alguns casos, chamados de **ouvinte de eventos (event listeners)**, Os ouvintes escutam o evento acontecendo, e o manipulador é o codigo que roda em resposta a este acontecimento.

> É importante notar que eventos web não são parte do core da linguagem JavaScript — elas são definidas como parte das APIs JavaScript incorporadas ao navegador.

> Para associar um evento à um elemento HTML podemos utilizar como atributo o prefixo "on" + a palavra chave correspondente ao nome do evento e logo após o nome da função que será o event handler (manipulador do evento), exemplo onclick='showModal(event)'.

## Tipos de Eventos

### Eventos de Janela

---

**afterprint** Disparado depois da página ser impressa.

**beforeprint** Disparado antes da página ser impressa.

**beforeunload** Disparado antes do navegador carregar outra página.

**error** Disparado quando ocorrer um erro.

**hashchange** Disparado quando o hash da url da página é alterado.

**load** Disparado quando toda a página for carregada.

**message** Disparado quando ocorrer uma mensagem.

**offline** Disparado quando o navegador é desconectado da internet.

**online** Disparado quando o navegador é conectado com a internet.

**pagehide** Disparado quando a página é ocultada.

**pageshow** Disparado quando a página é mostrada.

**popstate** Disparado quando a ocorrência no histórico do navegador é alterada.

**resize** Disparado quando a janela é redimensionada.

**storage** Disparado quando o armazenamento do navegador é alterado.

**unload** Disparado quando o usuário atualiza a página ou fecha a janela.

### Eventos de Formulário

---

**blur** Disparado quando o foco do elemento é removido.

**change** Disparado quando termina de altera o valor do elemento.

**contextmenu** Disparado quando o usuário abre o menu de contexto.

**focus** Disparado quando o elemento é focado.

**input** Disparado quando o elemento recebe uma entrada de valor.

**invalid** Disparado quando o valor do elemento é inválido.

**reset** Disparado quando o valor do elemento é redefinido ao estado inicial.

**search** Disparado quando o elemento input do tipo search é enviado.

**select** Disparado quando o valor do elemento é selecionado.

**submit** Disparado quando o formulário é enviado.

### Eventos de Teclado

---

**keydown** Disparado quando a tecla vai para baixo.

**keypress** Disparado quando a tecla é pressionada.

**keyup** Disparado quando a tecla é solta.

### Eventos de Mouse

---

**click** Disparado quando o elemento recebe um clique.

**dblclick** Disparado quando o elemento recebe um clique duplo.

**mousedown** Disparado quando o botão do clique vai para baixo.

**mousemove** Disparado quando o cursor do mouse se move sobre o elemento.

**mouseout** Disparado quando o cursor do mouse não está em cima do elemento.

**mouseover** Disparado quando o cursor do mouse está em cima do elemento.

**mouseup** Disparado quando o botão do clique é solto.

**wheel** Disparado quando a roda do mouse é rodada.

**mouseenter** Disparado quando o cursor do mouse entra em cima do elemento.

**mouseleave** Disparado quando o cursor do mouse sai de cima do elemento.

### Eventos de Drag and Drop

---

**drag** Disparado quando o elemento é arrastado.

**dragend** Disparado quando o elemento para de ser arrastado.

**dragenter** Disparado quando o elemento arrastado entra em um elemento que permite soltar.

**dragleave** Disparado quando o elemento arrastado sai de cima de um elemento que permite soltar.

**dragover** Disparado quando o elemento arrastado passa em um elemento que permite soltar.

**dragstart** Disparado quando o elemento começa a ser arrastado.

**drop** Disparado quando o elemento é solto.

**scroll** Disparado quando o scroll é rolado.

### Eventos de Transferência

---

**copy** Disparado quando o conteúdo do elemento é copiado.

**cut** Disparado quando o conteúdo do elemento é recortado.

**paste** Disparado quando o conteúdo do elemento é colado.

### Eventos de Mídia

---

**abort** Disparado quando o carregamento da mídia é cancelado.

**canplay** Disparado quando a mídia carregou o suficiente para começar.

**canplaythrough** Disparado quando a mídia carregou e pode ser reproduzido até o final.

**cuechange** Disparado quando o texto de uma trilha é alterado.

**durationchange** Disparado quando o tamanho total da mídia é alterado.

**emptied** Disparado quando acontece algum problema e a mídia fica indisponível.

**ended** Disparado quando a mídia foi consumida até o fim.

**error** Disparado quando um erro acontece.

**loadeddata** Disparado quando os dados da mídia são carregados.

**loadedmetadata** Disparado quando os metadados da mídia são carregados.

**loadstart** Disparado quando os dados da mídia começam a ser carregados.

**pause** Disparado quando a mídia é pausada.

**play** Disparado quando a mídia é começada.

**playing** Disparado quando depois que a mídia realmente começou.

**progress** Disparado enquanto o navegador obtém os dados da mídia.

**ratechange** Disparado quando a taxa de reprodução é alterada.

**seeked** Disparado quando a busca de dados da mídia terminou.

**seeking** Disparado quando a busca de dados da mídia está acontecendo.

**stalled** Disparado quando o navegador não pode buscar os dados de mídia por qualquer motivo.

**suspend** Disparado quando a busca de dados da mídia é parado antes de ser completamente carregado.

**timeupdate** Disparado quando a posição da reprodução é alterada.

**volumechange** Disparado quando o volume do áudio da mídia é alterado.

**waiting** Disparado quando a mídia é pausada para armazenar mais dados em buffer.

### Outros Eventos

---

**toggle** Disparado quando o usuário abre ou fecha o elemento details.
