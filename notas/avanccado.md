# Responsividade

```css
    @media screen and (max-width: 600px) {
        ul.topnav li.right, /*só para menores de 600px*/
        ul.topnav li {float: none;} /*só para menores de 600px*/
    }
```

# Contadores

Variáveis e Funções para criar contagens.

* **counter-reset** - começar uma contagem.
* **counter-increment** - incrementar um unidade a conta.
* **content** - inserir conteúdo de contagem.
* **counter() or counters() function** - adicionar valor da contagem atual.


```css
    body {
        counter-reset: section; /*contagem de seção no body*/
    }

    h1 {
        counter-reset: subsection; /*contagem de subseção no h1*/
    }

    h1::before {
        counter-increment: section; /*adicionar uma unidade no contador de seção*/
        content: "Section " counter(section) ". "; /*inserir conteúdo*/ /*pegar a contagem de seção*/
    }

    h2::before {
        counter-increment: subsection;
        content: counter(section) "." counter(subsection) " ";
    }
```