# display  (EXIBIÇÃO)

<img src="../imagens/display.gif" width="300px"/>

Configura como o elemento deve ser mostrado
* `block` - bloco (há quebra de linha para cada elemento)
* `inline` - na mesma linha  (não é possível determinar altura e largura, padding/margin vertical não são respeitados)
* `none` - não mostrar
* `inline-block` - na mesma linha, é possível determinar largura e altura, além de ter padding/margin respeitados.

Cada elemento tem um padrão, sendo o mais comum 'block'.

<br/>

## Block Elements

Começam em uma nova linha e ocupam a largura total.

* `<div>`
* `<h1> - <h6>`
* `<p>`
* `<form>`
* `<header>`
* `<footer>`
* `<section>`

É possível determinar uma largura para o elemento, que não ocupara mais a largura total.  
Para `<div>` é interessante determinar a largura maxíma, assim em telas pequenas não aparecerá barra de rolagem. 

## Inline Elements

Começam na mesma linha e ocupam apenas a largura necessária.

* `<span>`
* `<a>`
* `<img>`

## Esconder um Elemento

Há duas possibilidades `display:none` e `visibility:hidden` a primeira desconsidera o elemento totalmente enquanto a segunda apenas esconde o elemento mas o espaço ocupado por ele permanece.

# position (POSICIONAMENTO)

<img src="../imagens/position.gif" />

Determinar a posição (por top, bottom, left, right), só funciona depois que determinar o tipo de posicionamento e funcionará de maneira diferente a depender do tipo de posicionamento.

**Valores possíveis:**
* `static` - por conta browser. (não é possível determinar top, ...)
* `relative` - posição normal, quando determinado top, ... o próximo elemento não ira para próxima linha.
* `fixed` - fixo na tela visível, usar o top, ... para posicionar.
* `absolute` - posicionado (top, ...) em relação ao elemento em que está contido. Se o elemento em que está contido não tem `position` ou tem `position: static;` o elemento será posicionado em relação ao `body`.
* `sticky` - posicionado **relative** até que uma determinada posição de deslocamento seja encontrada na janela de exibição, então, ele passa ser **fixed** (como a posição: fixa).
    ```css
        div {
        position: -webkit-sticky; /* Necessário para o Safari, no Explore não funciona */
        position: sticky;
        top: 0; /*quando elemento aparecer na posição top 0 permanecerá fixo */
    ```

Alguns posicionamento podem implicar em sobreposição, então pe possível ordenar a posição no eixo Oz através da propriedade `z-index: -1;` atributo a cada elemento valores positivos ou negativos. Sem determinar a posição em z a ordem de sobreposição é dado pelo elemento último elemento no html.

# overflow (EXCEDENTE)

Só funciona em elementos com altura definida.

**Valores possíveis:**
* `visible` - Padrão, o conteúdo transborda para fora da caixa do elemento.
* `hidden` - O conteúdo excedente e omitido.
* `scroll` - O conteúdo excedente e omitido, mas é adicionado um barra de rolagem para que haja acesso ao conteúdo.
* `auto` - Similar ao **scroll**, mas a barra só é adicionada se necessária.

`overflow-x` e `overflow-y` determinam como o conteúdo irá transbordar.

# float (TRANSCENDER)

Determina que um elemento deve ser retirado do seu fluxo normal e colocado ao longo do lado direito ou esquerdo do seu containêr, elementos em linhas irão se posicionar ao seu redor.
Exemplo: posicionar uma imagem ao lada de um texto.

**Valores Possíveis:**
* `left` - a esquerda da caixa.
* `right` - a direita da caixa.
* `none` - na posição onde foi inserida, Padrão.
* `inherit` - herdar o valor do elemento superior.

Caso o elemento flutuante seja maior que a caixa do element ao qual ele fluta usar `overflow: auto;` para que ele não ultrapasse a caixa.

# clear (AFINIDADE)

Determinar se pode haver elementos flutuantes ao seu lado.

**Valores possíveis:**
* `none` - pode ter elemento flutuantes, padrão.
* `left` - não pode a esquerda.
* `right`- não pode a direita.
* `both` - não pode em nenhum dos lados.
* `inherit` - herdar valor do elemento superior.