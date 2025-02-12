<!-- {"layout": "title"} -->
# **HTML** parte 2
## Mais _tags_ HTML<br>e Entendendo regras CSS

---
<!-- {"layout": "centered"} -->
# Hoje veremos

- [_Tags_ de listas](#tags-de-listas) de itens
- [Elementos _inline_ _vs._ _block_](#elementos-inline-vs-block)
- [Mais tipos de hiperlinks](#mais-tipos-de-hiperlinks)
- [Entendendo regras CSS](#entendendo-regras-css)



---
<!-- {"layout": "section-header", "hash": "tags-de-listas"} -->
# _Tags_ de listas
## Enumerando coisas

- Lista numerada: `<ol></ol>`
- Lista não-numerada: `<ul></ul>`
- ~~[Lista de termos e definições][dl]~~ (_veja você mesmo_)

[dl]: https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/dl
<!-- {ul:.content} -->

---
## Listas de itens **`<ol></ol>`** e **`<ul></ul>`** 

- Lista **numerada** (também conhecida como _ordenada_):
  - ```html
    <ol>
      <li>Linux</li>
      <li>Windows</li>
    </ol>
    ```
    <!-- {li:style="flex-grow: 1; margin-right: 1em;"} -->
  - ::: result
    <ol>
      <li>Linux</li>
      <li>Windows</li>
    </ol>
    :::
    <!-- {ul:.layout-split-2.no-list-icon.no-padding} -->
    <!-- {li:style="flex-grow: 1;"} -->
    <!-- {ul^1:style="width: 100%;"} -->
- Lista **<u>não</u>-numerada** (ou _não-ordenada_):
  - ```html
    <ul>
      <li>Uva</li>
      <li>Maçã</li>
    </ul>
    ```
    <!-- {li:style="flex-grow: 1; margin-right: 1em;"} -->
  - ::: result
    <ul>
      <li>Uva</li>
      <li>Maçã</li>
    </ul>
    :::
    <!-- {ul:.layout-split-2.no-list-icon.no-padding} -->
    <!-- {li:style="flex-grow: 1;"} -->
    <!-- {ul^1:style="width: 100%;"} -->

---
<!-- {"layout": "section-header", "hash": "elementos-inline-vs-block"} -->
# Elementos _inline_ _vs._ _block_
## Quebrar ou não quebrar linha? :thought_balloon:


![](../../images/philosoraptor.jpg) <!-- {.portrait.centered style="display: block"} -->

Pergunta
~  Por que um **parágrafo** está sempre **abaixo do outro**, mas
  um elemento **`<strong>`** pode ficar **ao lado** de outro texto?

<!-- {dl:.content.width-30} -->

---
## Vamos fazer um *teste*... <!-- {.bullet} -->

1. Colocando dois `<p>` seguidos (lado a lado) no código <!-- {ol:.bulleted} -->
   - ```html
     <p>Primeiro</p> <p>Segundo</p>
     ```
     <!-- {li:style="flex-grow: 1;"} -->
   - ::: result . margin-left: 1em;
     <p>Primeiro</p> <p>Segundo</p>
     :::
     <!-- {ul:.layout-split-2.no-list-icon.no-padding} -->
     <!-- {li:style="flex-grow: 1;"} -->
     <!-- {ol:style="width: 100%;"} -->
1. Colocando dois `<strong>` seguidos
   - ```html
     <strong>Primeiro</strong> <strong>Segundo</strong>
     ```
     <!-- {li:style="flex-grow: 1;"} -->
   - ::: result . margin-left: 1em;
     <strong style="color: inherit;">Primeiro</strong> <strong style="color: inherit;">Segundo</strong>
     :::
     <!-- {ul:.layout-split-2.no-list-icon.no-padding} -->
     <!-- {li:style="flex-grow: 1;"} -->
     <!-- {ol:style="width: 100%;"} -->

Por quê isso acontece? <!-- {.bullet} -->

---
## Elementos **block** e elementos **inline** <!-- {.alternate-color} -->

- Ao desenhar uma página, o navegador precisa decidir **como <u>dispor</u>
  os elementos**
- Alguns elementos são do tipo `block`, outros são `inline`:

  Elementos **`block`** <!-- {dl:.bullet} -->
    ~ são dispotos um <u>abaixo do outro</u>
    ~ ex: parágrafos, títulos e subtítulos, listas <!-- {dd:.bullet} -->

  Elementos **`inline`** <!-- {.alternate-color} -->
    ~ são dispostos um <u>à direita do outro</u>
    ~ ex: links, strong, em, imagens <!-- {dd:.bullet} -->

Vamos ver como o navegador faz... <!-- {.bullet} -->

---
## Elementos **`block`**

![](../../images/flow1.png) <!-- {p:.flex-align-center} -->

---
## Elementos **`inline`** <!-- {.alternate-color} -->

![](../../images/flow2.png) <!-- {p:.flex-align-center} -->

---
<!-- {"layout": "centered-horizontal"} -->
## **`block`** e **`inline`** <!-- {.alternate-color} -->, juntos

![](../../images/flow3.png)

---
<!-- {"layout": "2-column-content"} -->
## De volta ao **`<p>` _vs._ `<strong>`** <!-- {.alternate-color} -->...

- São elementos **`block`**: <!-- {ul:.no-bullets.no-padding} -->
  - **`<p>`**
  - `<h1>, <h2> ... <h6>`
  - `<ul>`, `<ol>`, `<li>`
  - e outros...

1. São elementos **`inline`**: <!-- {.alternate-color} --> <!-- {ol:.no-bullets.no-padding} -->
   - **`<strong>`** <!-- {.alternate-color} -->
   - `<em>`
   - `<del>`, `<ins>`
   - `<mark>`
   - `<em>`
   - `<a>`
   - `<img>`
   - e outros...

---
<!-- {"layout": "section-header", "hash": "mais-tipos-de-hiperlinks"} -->
# Mais tipos de **hiperlinks**
## Ligações internas entre recursos e para emails

- Hiperlinks para:
  - Outras páginas do site
  - Emails
  - Telefones
  - Dentro de uma parte da página
- Atributo _target_

<!-- {ul^1:.content} -->

---
<!-- {"backdrop": "oldtimes"} -->
## *Relembrando* hiperlinks

- [Link externo](http://www.google.com) (para fora da página):
  ```html
  <a href="http://www.google.com">Link externo</a>
  ```
- [Link interno](../../attachments/exemplo.zip) (para algo hospedado no
  próprio computador)
  ```html
  <a href="downloads/exemplo.zip">Link interno</a>
  ```

1. ![](../../images/philosoraptor.jpg) <!-- {.portrait.push-left.bullet} --> <!-- {ol:.flex-align-end.no-bullets.no-padding.bullet} -->
   - Mas como criar um link para **outra página do meu próprio site**? <!-- {ul:.no-bullets.no-padding.bullet} -->

---
## Mais sobre hiperlinks

- [Link para uma **outra página**](/classes/html1/index.html) do próprio site:
  ```html
  <a href="outra-pagina.html">Outra página</a>
  ```
- [Link para **enviar um email**](mailto:coutinho@decom.cefetmg.br) para alguém:
  ```html
  <a href="mailto:fegemo@cefetmg.br">Me envie um email</a>
  ```
  - Ao clicar no link, o navegador abre o email do usuário

1. ![](../../images/philosoraptor.jpg) <!-- {.portrait.push-left.bullet} --> <!-- {ol:.flex-align-end.no-bullets.no-padding.bullet style="margin-top: 1.5em"} -->
   - Como fazer para o link **abrir em outra aba**? <!-- {ul:.no-bullets.no-padding.bullet} -->

---
## O **atributo `target="..."`** dos links

A _tag_ de hiperlink possui um atributo `target="..."` que pode ter
  os seguintes valores:

  `_self` <!-- {dl:.width-10.full-width} -->
    ~ O recurso "linkado" **abre <u>na própria aba</u>** (valor padrão)
    ~ _Exemplo_: `<a href="..." target="_self">Sobre mim</a>`

  `_blank`
    ~ O recurso "linkado" abre em **uma <u>nova</u> aba**
    ~ _Exemplo_: `<a href="..." target="_blank">Salgadinhos</a>`

---
## Link para dentro de uma página

- <video style="float: right; width: 400px; height: 331px; margin-left: 1em" controls autoplay loop="0" src="../../videos/link-interno.mp4"></video>
  Para criar um link para dentro da própria página:
  ```html
  <a href="#id-de-um-elemento">Link interno</a>
  ```
  - Repare o `#id-de-um-elemento`
    ```html
    <h2 id="id-de-um-elemento">Um título</h2>
    ```
    - Ao clicar no link, o navegador vai rolar a barra até que esse `<h2></h2>`
      fique visível e no topo do navegador (**mas o que é esse atributo `id`?**)

---
<!-- {"hash": "id-de-um-elemento-html"} -->
## O **`id`** de um elemento HTML

- É possível **definir um nome** que **identifique um elemento** da página <!-- {ul:.bulleted} -->
- Todo elemento HTML pode ter um atributo `id`. Exemplos:
  ```html
  <img src="..." id="logomarca-da-empresa">
  ```
  ```html
  <h1 id="titulo-principal">Origem da Polícia Intergalática</h1>
  ```
  ```html
  <ul id="melhores-pokemon">...</ul>
  ```
  - O atributo `id` **<u>deve ser único</u> na página**
    - Não pode haver 2+ elementos com um mesmo `id`
  - Podemos **usar o `id` para <u>estilizar elementos</u> em CSS**!

---
<!-- {"layout": "section-header", "hash": "entendendo-regras-css"} -->
# Entendendo **regras CSS**
## Como funcionam as regras

- Formato de uma regra
- Estilizando elementos um a um
- Colocando bordas
- Centralizando imagens
<!-- {ul:.content} -->

---
<!-- {"layout": "centered", "embedSVG": "img[src$='.svg']", "styles": ["../../styles/classes/css-rule-anatomy.min.css"]} -->

::: figure .figure-slides.clean
![Uma regra CSS mostrando](../../images/css-rule-anatomy.svg) <!-- {.css-rule-anatomy} --> <!-- {p:.bullet.figure-step.bullet-no-anim} -->

![Uma regra CSS mostrando](../../images/css-rule-anatomy.svg) <!-- {.css-rule-anatomy.rule} --> <!-- {p:.bullet.figure-step.bullet-no-anim} -->
:::
---
<!-- {"layout": "centered", "embedSVG": "img[src$='.svg']", "state": "show-active-slide-and-previous", "containerStyles": {"--show-2-slides-x-distance": "200px", "--show-2-slides-z-distance": "-150px", "--show-2-slides-rotation": "5deg"}} -->

![Regra CSS](../../images/css-rule-anatomy.svg) <!-- {.css-rule-anatomy.selector.declaration} -->

---
<!-- {"layout": "centered", "embedSVG": "img[src$='.svg']"} -->

![Regra CSS](../../images/css-rule-anatomy.svg) <!-- {.css-rule-anatomy.property.value} -->

---
<!-- {"layout": "tall-figure-left", "embedSVG": "img[src$='.svg']", "hash": "seletores-css", "slideStyles": {"grid-template-columns": ".2fr 1fr"}} -->
## **Seletores** CSS

![Uma regra CSS destacando o seletor](../../images/css-rule-anatomy.svg) <!-- {.css-rule-anatomy.selector style="width: 242px" data-viewbox="50 0 100 65"} -->

- O seletor define a **que(ais) elemento(s)** HTML da página a **regra CSS será aplicada** <!-- {ul:.bulleted-0} -->
- Há [diversos tipos de seletores][outros-seletores]. Veremos 2 hoje:
  1. _tag_
  1. `id`
- Regras podem ter 1+ seletor, separados por vírgula:
  ```css
  /* tanto <p>, qto <h1>, qto <ul> */
  p, h1, ul {
    color: black;
  }
  ```

[outros-seletores]: http://localhost:8080/classes/css2/#outros-seletores

---
<!-- {"hash": "seletor-de-tag"} -->
## Seletor de <u>_tag_</u>

- Se usarmos um seletor que é **o nome de uma _tag_**...
  ```css
  p { /* usamos 'p', que é o nome da tag de parágrafo */
    margin-left: 5%;
  }
  ```
  - ...selecionamos **todos os elementos da página <u>com aquela _tag_</u>**
    (_e.g._, todos os parágrafos)
- Outros exemplos: <!-- {li:.three-column-code} -->
  ```css
  img {
    border-radius: 50%;
  }
  body {
    font-size: 20px;
  }
  strong {
    color: forestgreen;
  }
  ```

---
<!-- {"hash": "seletor-de-id"} -->
## Seletor de <u>`id`</u>

- Se usarmos um seletor **que começa com o símbolo `#`** (_hashtag_)...
  ```css
  #titulo-principal {
    font-family: 'Verdana', sans-serif;
  }
  ```
  - ...selecionamos **<u>apenas o</u> elemento que possua aquele <u>atributo `id`</u>**
    (_e.g._, um `<h1 id="titulo-principal">...</h1>`)

---
<!-- {"layout": "2-column-content"} -->
## Exemplo: estilizando apenas um título `<h2>`

```html
    ...
    <style>
      #ponche-vermelho {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Receitas para Monstros</h1>
    <h2 id="ponche-vermelho">
      Ponche Vermelho</h2>
    <h2>Joelhos de Lagartixa</h2>
    <h2>Orelhas Verdes Fritas</h2>
  </body>
</html>
```

::: result
<h1 style="font: unset; font-size: 125%;">Receitas para Monstros</h1>
<h2 style="color: red; font: unset;">Ponche Vermelho</h2>
<h2 style="color: unset; font: unset;">Joelhos de Lagartixa</h2>
<h2 style="color: unset; font: unset;">Orelhas Verdes Fritas</h2>
:::

---
<!-- {"hash": "colocando-bordas", "embedSVG": "img[src$='.svg']"} -->
## Colocando bordas         

- A **propriedade `border`** é um atalho para `border-width`, `border-style` e
  `border-color`
  - Exemplo (os dois são **equivalentes**):
    ![](../../images/css-rule-anatomy.svg) <!-- {.css-rule-anatomy.property.value.push-right data-viewbox="56 30 90 65" style="width: 250px"} -->
    ```css
    p {
      border-width: 1px;    /* largura de 1 pixel */
      border-style: solid;  /* borda toda colorida */
      border-color: red;    /* cor vermelha */
    }
    ```
    ```css
    p {  /* preferimos esta forma, que é mais sucinta */
      border: 1px solid red;
    }
    ```

---
## Estilos de borda

- Há diversos estilos de borda:
  - `border-style: solid` <!-- {code:style="border: 4px solid red"} -->
  - `border-style: double` <!-- {code:style="border: 4px double red"} -->
  - `border-style: groove` <!-- {code:style="border: 4px groove red"} -->
  - `border-style: outset` <!-- {code:style="border: 4px outset red"} -->
  - `border-style: dotted` <!-- {code:style="border: 4px dotted red"} -->
  - `border-style: dashed` <!-- {code:style="border: 4px dashed red"} -->
  - `border-style: inset` <!-- {code:style="border: 4px inset red"} -->
  - `border-style: ridge` <!-- {code:style="border: 4px ridge red"} --> <!-- {ul:.multi-column-list-2} -->
- Veja a descrição dos [estilos de bordas na MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/border-style)


---
<!-- {"hash": "centralizando-imagens"} -->
## Centralizando imagens

- Para centralizar uma imagem, é necessário definir "margens
  laterais automáticas":
  ```css
  #imagem-principal {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  ```
  - As margens "automáticas" fazem com que o navegador divida o espaçamento
    horizontal igualmente nos dois lados
  - `display: block` é necessário porque `<img>` é `inline`, mas o navegador
    não permite definir margens para elementos `inline`

---
## Problema: **selecionando** elementos

- Como fazemos para selecionar (_e.g._): <!-- {ul:.bulleted} -->
  1. apenas **alguns parágrafos** em vez de todos?
  1. apenas o **primeiro título h2** da página?
  1. apenas **uma imagem em especial**?
- Uma solução possível é usar os atributos universais¹ HTML chamados
  **`class`** e **`id`** para identificar os elementos e estilizá-los
  > ¹**Atributos universais**: aqueles que qualquer elemento pode ter <cite>Coutinho & Hasan, 2021</cite>
  >
- Vamos ver diferentes formas para isso...

---
## Selecionar **por nome de _tag_**

- Até agora, estilizamos elementos HTML de duas formas:
- **Primeira forma:** Selecionando a _tag_:
  ```css
  p {
    color: blue;
  }
  ```
  - Isso faz com que **todos os parágrafos** fiquem com a cor azul

---
## Selecionar **por `id`**

- **Segunda forma:** selecionando 01 elemento em específico
  - Supondo que temos: `<p id="resumo">Este é o resumo da notícia...</p>`:
  ```css
  #resumo {
    color: blue;
  }
  ```
  - Deixando de cor azul apenas o parágrafo cujo `id` é `resumo`.
  - Contudo, <u>não pode haver mais de 1 elemento</u> com o mesmo `id` <!-- {li:.bullet} -->
  - Como fazemos, então, para estilizar não apenas 01, mas **um subconjunto de
    elementos** da forma como queremos? <!-- {li:.bullet} -->
    - Resposta: usando **classes** <!-- {li:.bullet} -->

---
<!-- {"hash": "css-seletor-por-classe"} -->
## Selecionar **por classe**

- Dada a seguinte estrutura de um `<body></body>`:
  ```html
  <p>Primeiro</p>
  <p>Segundo</p>
  <p>Terceiro</p>
  ```
- Para criar uma regra CSS para, digamos, os dois primeiros parágrafos, podemos
  alterar a estrutura HTML para:
  ```html
  <p class="destacado">Primeiro</p>
  <p class="destacado">Segundo</p>
  <p>Terceiro</p> <!-- continua no próximo slide -->
  ```

---
## Selecionar por classe (cont.)

- E, em um arquivo CSS, podemos escrever o nome da _tag_, seguido por um ponto
   "`.`", seguido pelo nome da classe:
  ```css
  p.destacado {
    font-weight: bold; /* negrito */
  }
  ```
- Ou, se quisermos usar a classe `destacado` para outros elementos além de
  `<p></p>`, podemos omitir o nome da _tag_:
  ```css
  .destacado {
    font-weight: bold;
  }
  ```

---
<!-- {"hash": "incluindo-css"} -->
# Incluindo arquivo CSS

- Por enquanto, colocamos o CSS **dentro do arquivo HTML**
   ```html
   <style> /* reaproveitamento de código CSS dentro do arquivo */
     p {
       color: #fff;
     }     /* misturamos código CSS dentro do arquivo HTML */
   </style>
   ```
   - Mas **isto é uma prática ruim**! :scream:

---
## Referenciando o **CSS usando a tag _link_**

- Um arquivo HTML pode referenciar ("incluir") um CSS assim:
  ```html
  <link rel="stylesheet" href="arquivo-de-estilos.css">
  ```
  - Mais de um arquivo HTML pode usar esse CSS
    - **Reaproveitamento** de código CSS
  - **_Caching_** do arquivo CSS: o arquivo é baixado apenas uma vez e
    usado sempre que necessário
    - Útil se o site tem várias páginas
- Quando o navegador lê essa linha, ele baixa esse arquivo CSS e o interpreta

---
<!-- {"layout": "2-column-content"} -->
## Referenciando o CSS : Exemplo de **atalho no Atom**

- Esqueceu toda a sintaxe (forma de escrita)?
- Digite apenas `link` e, logo após, aperte <kbd>Tab ↔️</kbd>:
- O mesmo vale para o VS Code

<video src="../../videos/link-css-atom.mp4" height="340" controls style="margin: 0 auto;"></video>

---
<!-- {"hash": "cores-e-gradientes", "layout": "main-point", "state": "emphatic"} -->
<style>
.color-text { color: #ffff0a; }
.gradient-text {
    background: linear-gradient(to right, #0f9000, #c900d6);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
</style>

# <span class="color-text">Cores</span> e <span class="gradient-text">Gradientes</span>

---
<!-- {"layout": "3-column-content", "slideStyles": {"grid-template-columns": "auto auto auto", "grid-template-rows": "auto auto auto"}, "classes": "compact-code-more", "styles": "../../styles/classes/color-portraits.min.css"} -->
## Notações: Nome, RGB e Hexadecimal

- ### **Nomes** <!-- {ul:.no-bullets.no-padding.no-margin} -->
  <pre class="hljs"><code><span class="color-portrait red"></span> red
  <span class="color-portrait cyan"></span> cyan
  <span class="color-portrait gold"></span> gold
  <span class="color-portrait forestgreen"></span> forestgreen
  <span class="color-portrait cornflowerblue"></span> cornflowerblue
  <span class="color-portrait rebeccapurple"></span> rebeccapurple
  ⋮</code></pre>
1. ### Notação **RGB** <!-- {ol:.no-bullets.no-padding.no-margin} -->
   <pre class="hljs"><code>rgb(<span style="color: #fb4d4d">verme</span>, <span style="color: #18dc18">verde</span>, <span style="color: cornflowerblue;">azul</span>)</code></pre>
   - rgb(...) com número entre 0...255 para <u>verme</u>lho, <u>verde</u>, <u>azul</u> <!-- {li:.smaller-text-80} -->
- ### Notação **Hexadecimal** <!-- {ul:.no-bullets.no-padding.no-margin} -->
  <pre class="hljs"><code>#<span style="color: #fb4d4d">vm</span><span style="color: #18dc18">vd</span><span style="color: cornflowerblue">az</span></code></pre>
  - '#' + 2 caracteres para <u>v</u>er<u>m</u>elho, <u>v</u>e<u>r</u>de, <u>az</u>ul <!-- {li:.smaller-text-80} -->
  - (0...9, A(10)...F(15)) <!-- {li:.smaller-text-80} -->

1. Exemplo: <!-- {ol:.no-bullets.no-padding.no-margin} -->
   ```css
   p {
     color: cyan;
   }
   ```
- Exemplo:<!-- {ul:.no-bullets.no-padding.no-margin} -->
  ```css
  p {
    color: rgb(0, 255, 255);
  }
  ```
1. Exemplo:<!-- {ol:.no-bullets.no-padding.no-margin} -->
   ```css
   p {
     color: #00ffff;
   }
   ```

---
<!-- {"layout": "3-column-content", "slideStyles": {"grid-template-columns": "auto auto auto", "grid-template-rows": "auto auto auto"}, "classes": "compact-code-more", "styles": "../../styles/classes/color-portraits.min.css"} -->
## Cores **com opacidade** <!-- {.underline.upon-activation.delay-1000} --> (transparência)

- ### **Nomes** <!-- {ul:.no-bullets.no-padding.no-margin} --> ❌
  <pre class="hljs"><code><span class="color-portrait red"></span> red
  <span class="color-portrait cyan"></span> cyan
  <span class="color-portrait gold"></span> gold
  <span class="color-portrait forestgreen"></span> forestgreen
  <span class="color-portrait cornflowerblue"></span> cornflowerblue
  <span class="color-portrait rebeccapurple"></span> rebeccapurple
  ⋮</code></pre>
  - Não tem como <!-- {li:.smaller-text-80} -->
1. ### Notação **RGB<u>A</u>** <!-- {ol:.no-bullets.no-padding.no-margin} -->
   <pre class="hljs"><code>rgb<ins>a</ins>(verme, verde, azul, <ins style="color: black; font-weight: bolder">alpha</ins>)</code></pre>
   - `alpha` é a opacidade da cor <!-- {li:.smaller-text-80} -->
     - opacidade = 1 - transparência <!-- {li:.smaller-text-80} -->
   - De 0 (transp.) até 1 (opaco) <!-- {li:.smaller-text-80} -->
- ### Notação **Hexadecimal <u>+AA</u>** <!-- {ul:.no-bullets.no-padding.no-margin} -->
  <pre class="hljs"><code>#vmvdaz<ins style="color: black; font-weight: bolder">aa</ins></code></pre>
  - 2 caracteres para `alpha` <!-- {li:.smaller-text-80} -->
  - De 0 (transp.) até FF (opaco) <!-- {li:.smaller-text-80} -->

1. Exemplo: <!-- {ol:.no-bullets.no-padding.no-margin} -->
   - Não tem!
- Exemplo:<!-- {ul:.no-bullets.no-padding.no-margin} -->
  ```css
  p {
    color: rgba(0, 255, 255, 0.5);
  }
  ```
1. Exemplo:<!-- {ol:.no-bullets.no-padding.no-margin} -->
   ```css
   p {
     color: #00ffff80;
   }
   ```

---
## Mais exemplos de cores

- ```css
  #FF0033 /* maiúsc. ou min. */
  #ff0033
  #f03
  ```
  <!-- {ul:.push-code-right} -->
  Se ambos caracteres de cada componente em hexa são iguais (ex: `#ff0033`), pode escrever só 1 de cada (ex: `#f03`)
- ```css
  rgb(255, 0, 51)
  rgb(100%, 0%, 20%)
  rgba(255, 0, 0, 0.1)         
  ```
  Em vez de 0...255, pode escrever 0%...100% <!-- {li:.clearer} -->
- ```css
  hsl(60, 100%, 50%)
  hsla(240, 100%, 50%, 0.05)   
  ````
  Também existe `hsl(hue, sat, light)`, mas é menos comum <!-- {li:.clearer} -->

---
<!-- {"layout": "centered-horizontal", "hash": "escolhendo-cores"} -->
## Escolhendo cores (<kbd>F12</kbd>)

<video src="../../videos/escolhendo-cores.mp4" height="460" controls style="margin: 0 auto;"></video>

---
<!-- {"hash": "gradientes"} -->
## Gradientes (ou degradês)

- `linear-gradient` é um **valor válido para `background-image`**,
      e não para `background-color` nem para `color`
  - Veja a documentação do que é um [`gradient`](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient)

1. <!-- {ol:.item-code-with-image.full-width.compact-code-more} -->
   ::: result . max-width: calc(100% - 600px);
   0 graus, iniciando com azul e terminando como verde <!-- {style="background-image: linear-gradient( 0deg, blue, #00FF00 ); font-size: 75%; color: white; text-shadow: 1px 1px black;"} -->
   :::
   ```css
   p {
     background-image: linear-gradient( 0deg, blue, #00FF00 );
   }
   ```
1. ::: result . max-width: calc(100% - 650px);
   Começa amarelo e termina azul no canto esquerdo superior  <!-- {style="background-image: linear-gradient( to left top, yellow, blue ); font-size: 75%; color: white; text-shadow: 1px 1px black;"} -->
   :::
   ```css
   p {
     background-image: linear-gradient( to left top, yellow, blue );
   }
   ```
1. ::: result . max-width: calc(100% - 600px);
   Azul, branco e verde <!-- {style="background-image:linear-gradient( 90deg, blue, white 20%,#00FF00); font-size: 75%; color: white; text-shadow: 1px 1px black;"} -->
   :::
   ```css
   p {
     background-image: linear-gradient( 90deg, blue, white 20%, #00FF00 );
   }
   ```

---
<!-- {"layout": "section-header", "hash": "abelhas-e-suas-castas"} -->
# Abelhas :honeybee: e suas castas
## :honey_pot: :honey_pot: :honey_pot: :honey_pot: :honey_pot:

- A atividade das abelhas
- Flutuando coisas
- Pesquisando novas propriedades CSS/elementos HTML
<!-- {ul:.content} -->

---
<!-- {"hash": "flutuando-coisas"} -->
# Flutuando coisas

> ![](../../images/float-magazine.png) <!-- {.push-right style="height: 200px;"} -->
  **Jornais e revistas** costumam colocar **imagens junto ao texto** para
  fazer uma bela diagramação do conteúdo
> <cite>Coutinho, 2017</cite>
> Isso se chama **deixar o elemento** (_e.g._, imagem) **flutuando**
> <cite>Hasan, 2017</cite>

- Na web também queremos fazer isso!

---
<!-- {"layout": "centered-horizontal"} -->
## Como flutuar elementos usando CSS?

![](../../images/pratica-abelhas-operarias.png)

Vamos conhecer um nova propriedade: `float`

---
## Propriedade `float`

- Usado para alterar o fluxo tradicional da página
  - Em CSS:  
    ```css
    img#abelha-operaria {
      float: left; /* left, right, none */
    }              /* none é o valor padrão - sem flutuação */
    ```
  - No HTML:
    ```html
    <img id="abelha-operaria" src="...">
    <p>Texto ...</p>
    ```

---
## Como funciona o `float`

- ![](../../images/float-p1.png) <!-- {.push-right} -->
  Um elemento flutuante é removido do fluxo tradicional e
  - os elementos `block` depois dele fingem que ele não está ali
  - os elementos `inline` depois dele respeitam seu formato
- Vamos fazer com que o parágrafo com `id="amazing"`
  flutue à direita **nos próximos 2 slides**...

---
## Exemplo de `float` (1º passo)

- ![](../../images/float-p2.png)  <!-- {.push-right style="max-height: 440px;"} -->
  Alterando a largura de um parágrafo para 200px
  ```css
  p#amazing {
    width: 200px;
  }
  ```

---
## Exemplo de `float` (2º passo)

- ![](../../images/float-p3.png)  <!-- {.push-right style="max-height: 350px;"} -->
  Flutuando o parágrafo à direita
  ```css
  p#amazing {
    width: 200px;
    float: right;
  }
  ```
  - Repare que:
    - Elementos declarados <u>antes</u> do parágrafo flutuante
      **não são alterados**
    - Elementos declarados <u>depois</u>:
      - Se forem `block`, **ignoram** o elemento flutuante
      - Se forem `inline`, **respeitam** o elemtno flutuante

---
<!-- {"hash": "arredondando-bordas"} -->
# Arredondando bordas

- ![](../../images/borda-arredondada.png) <!-- {.push-right} -->
  Como arredondar bordas?
  - Há muitas propriedades CSS que não teremos tempo de ver no curso
  - Contudo, a Web é uma ótima fonte de informação
  - Pesquise ["como arredondar bordas em CSS" no Google][border-radius-google],
    por exemplo

[border-radius-google]: https://www.google.com.br/search?hl=pt-BR&q=como+arredondar+bordas+em+css&meta=


---
<!-- {"layout": "centered"} -->
# Referências

1. Capítulos 1, 2, 3 do livro "Use a Cabeça -  HTML e CSS"
