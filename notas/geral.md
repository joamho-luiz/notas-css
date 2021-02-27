# SELETORES

## Simples
* `a` elemento.
* `#id` Identificador.  
* `.class` Classe.  
* `*` Selecionar tudo.

## Combinação - relação entre elemento
* `div  p` - Todos os `p` dentro de `div`.
* `div > p` - Todos os `p` filhos diretos de `div`.
* `div + p` - Todos os `p` seguidos de `div`, importante que `p` e `div` tenham o mesma acedência.
* `div ~ p` - Todos os `p` aparecem depois de uma `div`, não importando sua origem.

## Pseudo classe - certo estado
* `a:link` - não visitado.
* `a:visited` - visitado.
* `a:hover` - cursor do mouse em cima.
* `a:active` - momento do click.
* `i:first-child` - primeiro elemento `i` filho de qualquer elemento.
* `a:not(.ativa)` - todos os `a` exceto a classe `ativa`.
* `input:checked` - todos os `input` que estão selecionados.
* `input:default` - todos os `input` com valor padrão.
* `input:disabled` -  todos os `input` que estão desabilitados. 
* `	p:empty` - todos os `p` que não possuem filhos.

Confira mais [aqui](https://www.w3schools.com/css/css_pseudo_classes.asp "W3C").

## Pseudo elemento - Parte de um elemento
* `p::first-line` - Primeira linha de parágrafos.
* `p::first-letter` - primeira letra de parágrafos.
* `h1::before` - inserir conteúdo antes de um elemento.
    ```css
        h1::before {
            content: url(smiley.gif);
        }
    ```
* `h1::after` - inserir conteúdo antes de um elemento. 
* `::marker` - selecionar o marcadores de listas (ordenadas ou não).
    ```css
        ::marker {
            color: red;
            font-size: 23px;
        }
    ```
* `::selection` - Quando um texto for selecionado.
    ```css
        ::selection {
            color: red;
            background: yellow;
        }
    ```
* Confira mais [aqui](https://www.w3schools.com/css/css_pseudo_elements.asp "W3C").

## Atributo - atributo ou valor
* `a[target]` - Atributo
* `a[target = "_blank"]` - Valor  
* `[class~="flower"]` -  `class` que tenham `flower`, precisa está isolado.
* `[class|="top"]` - `class` que comecem com `top` ou `top-`, precisa está isolado.
* `[class^="top"]` - `class` que comecem com `top`, não precisa estar isolado. 
* `[class$="test"]` - `class` que terminam com `test`, não precisa estar isolado.
* `[class*="te"]` - `class` que possuam `te` em seu valor, não precisa estar isolado.

## Mais Seleções
* `a,i,p` Mais de um seletor

## Especificidades
Determina qual declaração tem mais prioridade. Se tiverem mesma prioridade o última declaração a ser lida será aplicado.

* Pelo local da declaração
    `Browser` << `Arquivo externo` < `Head` << `atributo da tag`

* Pelo tipo de seletor
    Prioridade| Seletores
    -- | --
    1.000 | Inline styles - atributo style na tag html
    100 | IDs
    10 | Classes, attributes and pseudo-classes
    1 | Elements and pseudo-elements
    0 | *, body *, inherited 

* Força que estilo seja aplicado
    `background-color: red `**`!important;`** - está declaração ganha um nível superior de prioridade.
<br><br><br>

# UNIDADES DE MEDIDAS

* O '0' não precisa de unidade de medida
* Algumas propriedades aceitam valores negativo.

## Unidades Absolutas
Simbolo | Nome | Conversão
-- | -- | --
cm	| centímetros
mm	| milímetros
in	| polegadas | 1in = 96px = 2.54cm
px | pixels | 1px = 1/96th of 1in (varia)
pt	| pontos | 1pt = 1/72 of 1in
pc	| paicas | 1pc = 12 pt 

<br><br>

## Unidades Relativas
Simbolo | Descrição
-- | -- 
em | Relativo ao tamanho da fonte do elemento (2em significa 2 vezes o tamanho da fonte atual)	
rem | Relativo a font-size do elemento raiz
% | Relativo ao tamanho do elemento pai	
vw | Relativo a 1% da largura da janela
vh | Relativo a 1% da altura da janela
vmin | Relativo a 1% da menor dimensão da janela
vmax | Relativo a 1% da maior dimensão da janela
. | .
_ex_ | _Relative to the x-height of the current font (rarely used)_
_ch_ | _Relative to width of the "0" (zero)_	

<br><br><br>

# Cores
* hexadecimal `#123456`  
* RGB `rgb(0,0,0)`
* RGBA `rgba(0,0,0,0)`
* HSL(A) `(165, 81%, 93%, (.6))` &nbsp; &nbsp; (Hue: °, Saturation: %, Brightness: %)  
A = transparência.  
Hue = matiz.
<br><br><br>

# Aplicações Passadas

Vale para: _padding_, _border_, _margin_.

  Valor | Aplicação
  -|-
  Um | (⮃⮂)
  Dois | ⮃ ⮃
  Três | 🡡 ⮂ 🡣
  Quatro | 🡡 🡢 🡣 🡠

<br><br><br>

# Deslocados
* `resize: none;` - Para evitar que o usuário redimensione a área de texto.
* `cursor: pointer;` - Mudar o cursor para mão indicando.
* `opacity`
    * Aceita o  valor entre 0.0 e 1.0 (Aplica transparência em tudo que está contido no elemento).
    * Para aplicar transparência em apenas algo colorido usar RGBA.