<!-- {"layout": "title"} -->
# **Extra**
## Tabelas, Video, Áudio, Web fonts, Tesouros :crown: e Piratas



---
<!-- {"layout": "centered"} -->
# Hoje veremos

1. [Tabelas simples](#tabelas-simples)
1. [Tabelas completas](#tabelas-completas)
1. [Estilizando tabelas](#estilizando-tabelas)
1. [Vídeo e Áudio](#video-e-audio)
1. [Web fonts](#web-fonts)
1. [Piratas e seus tesouros - o que precisamos para](#piratas-e-seus-tesouros) 👑

---
<!-- {"hash": "tabelas"} -->
# Tabelas

<iframe width="470" height="270" src="https://jsfiddle.net/danielhasan/nmrbhqkb/7/embedded/result/" allowfullscreen="allowfullscreen" frameborder="0" class="flex-align-center"></iframe>

- Nesta aula iremos:
  - fazer a estrutura desta tabela via **HTML**
  - estilizar esta tabela via **CSS**

---
<!-- {"layout": "2-column-content"} -->
## O que uma tabela possui?

<iframe width="470" height="270" src="https://jsfiddle.net/danielhasan/nmrbhqkb/7/embedded/result/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

- Que partes compõem uma tabela? <!-- {ul:.bulleted} -->
  - Linhas e colunas, sendo:
    - uma linha com o **cabeçalho**
    - última linha com o **rodapé**
  - Legenda
- Em HTML, utilizamos _tags_ para indicar os elementos de uma tabela


---
<!-- {"layout": "section-header", "hash": "tabelas-simples"} -->
# Tabelas simples
## Linhas e células

- Elementos:
  - `<table></table>`
  - `<tr></tr>`
  - `<td></td>` e `<th></th>`

<!-- {ul^1:.content} -->

---
<!-- {"hash": "tags-basicas-de-tabela"} -->
## **_Tags_ básicas** de uma Tabela

- ![Exemplo de Tabela Exibindo suas Tags](../../images/table-tags.svg) <!-- {.push-right.invert-colors-dark-mode width="500" height="218"} -->
  Tabelas são criadas com as tags:
  - **`<table>...</table>`**
  - **`<tr>...</tr>`**, linha da tabela
  - **`<td></td>`**, célula de dados
  - **`<th></th>`**, célula do cabeçalho
- A **tabela** inicia-se com `<table>` e finaliza com `</table>`
- Cada **linha** possui a _tag_ `<tr>` correspondente, finalizada com `</tr>`
- A _tag_ `<td>...</td>` armazena os dados de uma **célula** da tabela
  - Para o **cabeçalho**, ao invés de `<td>`, utiliza-se a _tag_ `<th>`
- As _tags_ `<td>` e `<th>` **devem** estar dentro de uma linha (`<tr>`) <!-- {ul:.full-width} -->

---
<!-- {"layout": "centered-horizontal", "playMediaOnActivation": {"selector": "#simple-table" }} -->
<video src="https://fegemo.github.io/cefet-front-end-large-assets/videos/coding-simple-table.mp4" id="simple-table" width="742" height="458" controls></video>

Repare que, por padrão, as células `<th>` ficam em <span style="font-weight: bold;">negrito</span>

---
<!-- {"hash": "meclando-celulas-horizontais-e-verticais", "layout": "2-column-content"} -->
## Mesclando células **horizontais** e **verticais**

```html
<table>
  <tr>
    <th colspan="2">Pessoas</th>
  </tr>
  <tr>
    <td>2005046102</td>
    <td>Epaminondas</td>
  </tr>
</table>
```

- ![](../../images/table-colspan.png) <!-- {.push-right.invert-colors-dark-mode} -->
  **`colspan="X"`** faz com que aquela **célula ocupe `X` colunas**
  - Para mesclar células "para baixo", usamos **`rowspan="Y"`**, onde `Y` é o
    **número de linhas** que a célula vai ocupar
- Exemplos: de [`colspan`](https://jsfiddle.net/fegemo/o6gsb0t9/) e
  de [`rowspan`](https://jsfiddle.net/fegemo/65rvt05m/) (clique para ver)

---
## A tabela do nosso exemplo

<iframe width="65%" height="375" src="//jsfiddle.net/danielhasan/nmrbhqkb/17/embedded/result,html/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0" class="flex-align-center"></iframe>

OBS: Como ainda não alteramos o **estilo**, ainda não há **borda**

---
<!-- {"layout": "section-header", "hash": "tabelas-completas"} -->
# Tabelas completas
## Cabeçalho, Corpo e Rodapé

- Elementos:
  - `<caption>...</caption>`
  - `<thead>...</thead>`
  - `<tbody>...</tbody>`
  - `<tfoot>...</tfoot>`

<!-- {ul^1:.content} -->

---
<!-- {"hash": "caption"} -->
## _Tag_ `caption` para colocar **legenda**

- Coloca uma legenda na tabela:
  ```html
  <table>
    <caption>Quadro 01: Alunos Matriculados</caption> <!-- aqui -->
    <tr>
      <th>Matrícula</th><th>Nome</th>
    </tr>
    <tr>
      <td>201792829293</td><td>Alice Fernandez</td>
    </tr>
  </table>
  ```
  - Exemplo: https://jsfiddle.net/danielhasan/8tr4z959/

---
## Tabela do nosso exemplo (<ins>com caption</ins>)

<iframe width="65%" height="375px" src="https://jsfiddle.net/danielhasan/nmrbhqkb/19/embedded/result,html/" allowfullscreen="allowfullscreen" frameborder="0" class="flex-align-center"></iframe>

OBS: Como ainda não alteramos o **estilo**, ainda não há **borda**

---
<!-- {"hash": "tag-de-cabecalho-e-rodape", "layout": "2-column-content", "embeddedStyles": "pre.hljs { max-height: 100%; }"} -->
## _Tags_ de **cabeçalho**, **corpo** e **rodapé** da tabela

<!-- {h2:.compact-code-more} -->

```html
<table>
  <caption>Gastos em janeiro</caption>
  <thead> <!-- cabeçalho -->
    <tr>
      <th>Descrição</th><th>Valor</th>
    </tr>
  </thead>
  <tbody> <!-- corpo -->
    <tr>
      <td>Alimentação</td><td>300,00</td>
    </tr>
    <tr>
      <td>Transporte</td><td>100,00</td>
    </tr>
  </tbody>
  <tfoot> <!-- rodapé -->
      <tr>
        <td>Total</td><td>400,00</td>
      </tr>
  </tfoot>
</table>
```

- [Exemplo no jsfiddle](https://jsfiddle.net/danielhasan/z62vg9xq/5/)
- `<thead>`, `<tbody>` e `<tfoot>` devem **marcar _as linhas_** que compõem o
  corpo, o cabeçalho e o rodapé
  - Útil para:
    - aplicarmos **estilos** diferentes no **corpo**, **cabeçalho** e
      **rodapé**
    - impressão: se a tabela for maior que a página, o cabeçalho
      aparecerá em todas as páginas

---
## Tabela do nosso exemplo (<ins>completa</ins>)

<iframe width="65%" height="375px" src="https://jsfiddle.net/danielhasan/nmrbhqkb/10/embedded/result,html/" allowfullscreen="allowfullscreen" frameborder="0" class="flex-align-center"></iframe>

~~OBS:~~ chegou a hora de estilizar!

---
<!-- {"layout": "section-header", "hash": "estilizando-tabelas"} -->
# Estilizando tabelas
## Deixando-as mais atrativas

- Colocando bordas
- Propriedade de largura: `width`
- Margem e _padding_
- A propriedade `border-collapse` em tabelas
- Fontes: `font-size`, `font-style`, `font-weight` e `text-decoration`
<!-- {ul:.content} -->

---
<!-- {"backdrop": "oldtimes"} -->
## Colocando bordas         

- A **propriedade `border`** é um atalho: `border-width`, `border-style` e
  `border-color`
  - Exemplo (os dois são **equivalentes**):
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
<!-- {"hash": "bordas"} -->
## Bordas

- De forma similar, podemos exibir apenas a borda do
  **topo**, **direita**, **abaixo** ou **esquerda**
- Para isso, usamos:  `border-top`, `border-right`, `border-bottom` e
  `border-left`
  - ```css
    p {
      border-top: 1px solid red;
      border-bottom: 2px dotted blue;
    }
    ```
    <!-- {li:style="flex-grow: 1;"} -->
  - ::: result
    <p style="border-top: 1px solid red; border-bottom: 2px dotted blue;">Sou o mestre das bordas!</p>
    :::
    <!-- {ul^0:.layout-split-2.no-list-icon.no-padding} -->
    <!-- {li:style="flex-grow: 1;"} -->
- Também podemos usar a forma mais extensa. Por exemplo, `border-top-width`,
  `border-top-style` e `border-top-color` definem, respectivamente, a largura,
  o estilo e a cor da borda do topo

---
<!-- {"hash": "propriedade-border-collapse"} -->
## Colocando **bordas na tabela**

- <iframe width="39%" height="165" src="https://jsfiddle.net/danielhasan/nmrbhqkb/23/embedded/result,css,html/" allowfullscreen="allowfullscreen" frameborder="0" class="push-right" style="margin-top: -1em"></iframe>
  Ao adicionar a borda nas células de uma tabela o resultado ficaria assim ➡️:
  <pre class="hljs hljs-html compact-code-more"><code>td {
    border: 1px solid black;
  }</code></pre>
- <iframe width="39%" height="200px" src="https://jsfiddle.net/danielhasan/nmrbhqkb/24/embedded/result,css,html/" allowfullscreen="allowfullscreen" frameborder="0" class="push-right" style="clear: right; margin-top: 2em"></iframe>
  
  Para mudarmos isso, adicionamos `border-collapse: collapse` à regra CSS
  da tabela: <!-- {li:.two-column-code} --> <!-- {ul:.bulleted-0} -->
  <pre class="hljs hljs-html compact-code-more two-column-code"><code>td {
    border: 1px solid black;
  }
  table {
    border-collapse: collapse;
  }</code></pre>
  
  - Este é o **comportamento desejado** praticamente **sempre** para as bordas
  
---
<!-- {"hash": "margin-e-padding"} -->
## Margem e _Padding_

![Desenho de máscara de festa a fantasia](../../images/margin-and-padding.svg) <!-- {p:.flex-align-center.medium-width.invert-colors-dark-mode} --> <!-- {.full-width} -->

**`padding`** 
~ Espaçamento interno, da borda para dentro

**`border`**
~ Tamanho da borda

**`margin`**
~ Espaçamento externo, da borda para fora

---
<!-- {"layout": "2-column-content"} -->
## Margem e _Padding_ - Exemplo

<iframe width="100%" height="450" src="https://jsfiddle.net/fegemo/ovt08qcb/embedded/result,css,html/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

- Todo elemento pode ter: <!-- {ul:.bulleted-0} -->
  1. `padding` (esp. interno)
  1. uma borda
  1. `margin` (esp. externo)
- Versão sem atalho ou com: <!-- {li:.two-column-code.compact-code-more} -->
  ```css
  margin-top: 12px;
  margin-right: 3px;
  margin-bottom: 6px;
  margin-left: 9px;

  margin: 12px 3px 6px 9px;
  /*
   ordem: ⬆️  ➡️  ⬇️  ⬅️
   (tipo um relojinho)
  */
  ```
  - Mesmo vale para `padding`
- Na vertical, as margens colapsam:
  - Margem: max(cima, baixo)

---
<!-- {"hash": "largura-de-elementos"} -->
## **Largura** dos elementos

- Podemos especificar a largura dos elementos _**block**_ por meio da
  propriedade **width**
  - ```css
    p {
      width: 260px;
    }
    ```
    <!-- {li:style="flex-grow: 1;"} -->
  - <iframe width="100%" height="206" src="https://jsfiddle.net/fegemo/4z6d68gw/embedded/result,css/" allowfullscreen="allowfullscreen" frameborder="0" style="margin-top: -1.7em"></iframe>

    <!-- {ul^0:.layout-split-2.no-list-icon.no-padding} -->
    <!-- {li:style="flex-grow: 1;"} -->

**Observação**: não é possível definir largura de elementos **inline**.
Esses elementos possuem exatamente a largura necessária para apresentar seu conteúdo <!-- {p:.note.alert} -->

---
<!-- {"hash": "outras-propriedades-do-texto"} -->
## Outras propriedades CSS para texto

**`font-size`** <!-- {dl:.full-width.width-20} -->
  ~ <iframe width="280px" height="400px"  src="https://jsfiddle.net/fegemo/x2m8fnL6/3/embedded/result,css/" allowfullscreen="allowfullscreen" frameborder="0" class="push-right"></iframe>
    Define o tamanho da fonte, ex: <code>18px</code>

**`font-weight`**
  ~ Define a espessura da fonte
  ~ Valores: `normal` <!-- {code:style="font-weight: normal"} -->,
    `lighter` <!-- {code:style="font-weight: lighter"} -->,
    `bold` <!-- {code:style="font-weight: bold"} -->,
    `bolder` <!-- {code:style="font-weight: bolder"} --> ou um número
    representando sua espessura

**`font-style`**
  ~ Define o estilo da fonte
  ~ Valores: `normal` <!-- {code:style="font-style: normal"} --> e
    `italic` <!-- {code:style="font-style: italic"} -->

**`text-decoration`**
  ~ Sublinha, risca ou coloca um risco acima do texto:
  ~ Valores: `none` <!-- {code:style="text-decoration: none"} --> (nenhum),
    `underline` <!-- {code:style="text-decoration: underline"} --> (sublinhado),
    `overline` <!-- {code:style="text-decoration: overline"} --> (acima do texto),
    `line-through` <!-- {code:style="text-decoration: line-through"} --> (riscado)

---
<!-- {"layout": "2-column-content"} -->
## Estilizando a tabela do nosso exemplo

<iframe width="98%" height="400" src="https://jsfiddle.net/fegemo/yezb7ebo/embedded/result/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

<iframe width="98%" height="400" src="https://jsfiddle.net/fegemo/yezb7ebo/embedded/css,html/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>



---
<!-- {"layout": "section-header", "hash": "formatos-de-imagens"} -->
# Formatos de imagens
## Usando diferentes formatos

- JPEG
- GIF
- PNG
- SVG
<!-- {ul:.content} -->

---
## Imagens

- Usamos a tag `<img src="...">`, que é um **elemento _void_**
  - Ou seja, não tem conteúdo nem tag de fechamento
- Formato geral
  ```html
  <img src="imagens/nome-do-arquivo.jpg" alt="Descrição bacana">
  ```
  - [Referência na Mozilla Developer Network][mdn-img]
- Mas que **formatos** <!-- {.underline.upon-activation} --> de imagens existem?

[mdn-img]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img

---
## Imagens: **formato**

- Existem vários formatos de imagens suportados por navegadores: <!-- {.bullet} -->

**JPEG** (ou JPG) <!-- {strong:.alternate-color} -->  <!-- {dl:.bulleted} -->
~ bom para **fotos** tiradas do mundo real, que possuem muita variação de cor. Não possui
  transparência

**GIF** <!-- {strong:.alternate-color} -->
~ **transparência** de 1 bit e suporta **animações** de quadros
~ apenas 256 cores na imagem (muito pouco!!)

**PNG** <!-- {strong:.alternate-color} -->
~ **transparência** de 8 bits e suporta **mais cores** que GIF
~ bom formato para imagens com pouca variação de cor

**SVG** <!-- {strong:.alternate-color} -->
~ imagens **vetoriais** que não perdem qualidade se **ampliadas**

*[JPEG]: Joint Photographic Experts Group*
*[GIF]: Graphics Interchange Format*
*[PNG]: Portable Network Graphics*
*[SVG]: Scalable Vector Graphics*

---
<!-- {"layout": "2-column-content-zigzag"} -->
## Transparências: PNG _vs_ GIF

**GIF**: Um pixel é totalmente transparente ou totalmente opaco

::: figure .no-margin
![Exemplo de transparência usando GIF](../../images/gif-transparency-2.gif) <!-- {p:.center-aligned} -->
![Exemplo de transparência usando GIF](../../images/gif-transparency.gif)
:::

**PNG**: Opacidade pode variar entre 0 (transparente) e 255 (opaco), ou
0% e 100%

::: figure .no-margin
![Exemplo de transparência usando PNG](../../images/png-transparency-2.png) <!-- {p:.center-aligned} -->
![Exemplo de transparência usando PNG](../../images/png-transparency.png)
:::

---
<!-- {"layout": "2-column-content-zigzag"} -->
## Imagens **vetoriais** (_e.g._, SVG)

Imagem _bitmap_ (JPG, GIF, PNG) original (pequena) e aumentada
(fica "**estourada**")

::: figure .no-margin
![Exemplo de transparencia usando PNG](../../images/imagem-bitmap.png) <!-- {p:.center-aligned} -->
![Exemplo de transparencia usando PNG](../../images/imagem-bitmap.png)<!-- {style="width: 100px"} -->
:::

Imagem vetorial (SVG) original (pequena) e aumentada (mantém a qualidade)

::: figure .no-margin
![Exemplo de transparencia usando PNG](../../images/imagem-vetorial.svg) <!-- {p:.center-aligned} -->
![Exemplo de transparencia usando PNG](../../images/imagem-vetorial.svg)<!-- { style="width: 100px"} -->
:::

---
<!-- {"layout": "section-header", "hash": "video-e-audio"} -->
# Vídeo e Áudio
## Usando elementos multimídia

- Vídeo
- Áudio
<!-- {ul:.content} -->

---
# Formatos de Vídeo

- Existem diversos **formatos de arquivo**:
  - AVI (.avi)
  - WebM (.webm)
  - MP4 (.mp4, .m4v)
  - Ogg (.ogg)
  - Flash Video (.flv)
  - ASF (.asf) <!-- {ul:.multi-column-list-2} -->
- Nem todo navegador consegue exibir todos os formatos!
  - Às vezes, devemos disponibilizar mais de um formato do vídeo

---
## O elemento **video**

- Para exibir um vídeo, existe um elemento similar ao de imagem:
  ```html
  <video src="videos/fendadobiquini.mp4"></video>
  ```
- Resultado:

  <video src="../../videos/fendadobiquini.mp4" width="320" height="240" class="push-left" style="margin-right: 2em;"></video>
  - O `<video>` abre e fecha (_i.e._, `</video>`)
  - O elemento `<vídeo>` surgiu no HTML5
  - O que estiver dentro da _tag_ `<video>...</video>` é exibido caso
    o navegador não consiga exibi-lo
  - Por padrão, não há controles para o vídeo

---
## Querida, onde está o controle?

- O atributo `controls` associa um conjunto de controles ao `<video>`
  ```html
  <video src="videos/fendadobiquini.mp4" controls></video>
  ```
- Resultado:

  <video src="../../videos/fendadobiquini.mp4" width="320" height="240" controls class="push-left" style="margin-right: 2em;"></video>
  - Repare que `controls` é um atributo que não requer um valor
    - Isso se chama **atributo booleano**

---
## Opções (atributos) de **video**

`controls`
  ~ mostra um conjunto de controles

`autoplay`
  ~ começa a executar o vídeo assim que a página carregar

`muted`
  ~ tira o som

`preload="..."`
  ~ começa a baixar o vídeo assim que a página carrega
  ~ `preload="none"`: não pré-carrega
  ~ `preload="metadata"`: pré-carrega apenas metadados
  ~ `preload="auto"`: pré-carrega todo o vídeo

`loop="x"`
  ~ quantas vezes o vídeo deve ser executado (0 = infinitas)

`poster="http://..."`
  ~ URL de uma imagem mostrada antes do vídeo ser executado

- Também há os atributos `width="x"` e `height="y"`

---
## Suporte dos navegadores por formato

- Nem todos navegadores suportam **os mesmos formatos de vídeo**
- Assim, usamos uma outra forma do elemento `<video>`:
  ```html
  <video width="320" height="240" controls>
    <source src="bob-esponja.mp4" type="video/mp4; codecs=avc1.42E01E,mp4a.40.2">
    <source src="bob-esponja.webm" type="video/webm; codecs=vp8,vorbis">
    <source src="bob-esponja.ogv" type="video/ogg; codecs=theora,vorbis">
    Seu navegador não suporta o elemento video.
  </video>
  ```
- O navegador tentará abrir o vídeo `bob-esponja.mp4` (_i.e._, o primeiro)
  - se não conseguir, tentará o arquivo `bob-esponja.webm` (2º)
  - caso ainda não consiga, tentará o `bob-esponja.ogv` (3º)
  - se, mesmo assim, não conseguir, será exibido o texto

---
<!-- {"layout": "3-column-content", "scripts": ["../../scripts/classes/caniuse.min.js"]} -->
## Suporte **hoje** (formatos de vídeo)

<div class="caniuse" data-feature="webm"></div>

<div class="caniuse" data-feature="mpeg4"></div>

<div class="caniuse" data-feature="ogv"></div>

---
## Audio

- `<audio>` funciona **exatamente** da mesma forma que `<video>` <!-- {ul:.full-width.compact-code} -->
  - [Referência na MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio)
- Formatos mais comuns: **MP3** <!-- {strong:.alternate-color} --> e
  **OGG**  <!-- {strong:.alternate-color} -->
- Exemplo:
  <audio src="../../audios/banjo-kazooie-short.mp3" controls loop="0" class="push-right" style="margin-left: 0.5em; margin-top: 1.25em"></audio>
  ```html
  <audio src="banjo-kazooie.mp3" controls loop="0"></audio>
  ```

1. <!-- {ol:.no-bullets.no-padding.layout-split-2} -->
   <div class="caniuse" data-feature="mp3"></div>
1. <div class="caniuse" data-feature="ogg-vorbis" style="margin-left: 1em"></div>

*[MP3]: MPEG-1/2 Audio Layer 3*

---
<!-- {"layout": "section-header", "hash": "web-fonts"} -->
# _Web Fonts_
## Usando fontes não-instaladas

- Formatos de fontes
- A regra `@font-face`
- Google Fonts
<!-- {ul:.content} -->

---
# Web Fonts

- Motivação:
  - Utilizar **fontes que não estão instaladas** no computador
- Passos:
  1. Escolher a fonte
  1. Gerar **todos os formatos** para que funcione em todos os principais
     navegadores
     - `.ttf`
     - `.otf`
     - `.eot`
     - `.woff`
     - `.woff2` <!-- {ul:.multi-column-list-5} -->
  1. Publicar a fonte na Internet (ou no seu próprio site)

---
## Web Fonts (cont.)

1. Descrever a fonte no arquivo CSS usando `@font-face {...}`: <!-- {ol:.compact-code} -->
   ```css
   @font-face {
     font-family: "Emblema One";    /* dando um nome à fonte */
     src: url("fonts/EmblemaOne-Regular.woff2") format('woff2'), /* 1º formato */
          url("fonts/EmblemaOne-Regular.woff")  format('woff'),  /* 2º formato */
          url("fonts/EmblemaOne-Regular.ttf")   format('ttf');   /* 3º formato */
   }
   ```
2. Usar a fonte:
   ```css
   h1 {
     font-family: "Emblema One", sans-serif;
   }
   ```
   - Sempre coloque uma segunda opção (_e.g._, `sans-serif`)


---
<!-- {"layout": "2-column-content", "scripts": ["../../scripts/classes/caniuse.min.js"]} -->
## **Formatos de fonte** e os navegadores

<div class="caniuse" data-feature="woff2" style="width: 75%"></div>
<div class="caniuse" data-feature="woff" style="width: 75%"></div>

- **WOFF2** é até 50% menor que **WOFF** <!-- {ul:.span-columns} -->
- **TTF** é suportado em todos navegadores

---
## Usando fontes "mais facinho"

- ![](../../images/google-fonts.png) <!-- {.push-right.small-width} -->
  Gerar os formatos de fonte necessários pode dar trabalho
- Outra alternativa é usar **sites que provêem diversas fontes** para
  serem usadas
  - Exemplos:
    1. [**Google Fonts**][google-fonts] <!-- {strong:.alternate-color} -->
    1. [Dafont][dafont]
    1. [FontSpace][font-space]
  - Além de ter vários formatos das fontes, eles fornecem o código CSS

[google-fonts]: https://fonts.google.com/
[dafont]: http://www.dafont.com/pt/
[font-space]: http://www.fontspace.com/





---
<!-- {"layout": "section-header", "hash": "piratas-e-seus-tesouros"} -->
# Piratas e seus Tesouros 👑
## Ajude Barba-Ruiva!

- Definindo uma imagem de fundo da página
- Ocupando toda a altura do navegador
- Textos sombreados
- Cores semitransparentes

<!-- {ul:.content} -->

---
<!-- {"backdrop": "piratas"} -->

---
<!-- {"hash": "imagem-de-fundo"} -->
# Imagem de fundo

```css
body {
  background-image: url(caminho-para-a-imagem);
  background-repeat: no-repeat;
  background-position: left bottom;
  background-size: cover;
}
```

- `background-image` para escolher que imagem será usada
- `background-repeat: no-repeat` para que a imagem apareça só 1x
- `background-position: left bottom` para fixar que o canto **inferior
  esquerdo** da imagem fique sempre visível
- `background-size: cover` para que a imagem **cubra todo o espaço** da tela

---
## **Ancorando** a imagem **em um canto da tela**

![](../../images/background-position-left-bottom.png)
![](../../images/background-position-right-bottom.png)

<!-- {p:style="margin-bottom: 0;"} -->

- Deixando um canto da imagem sempre visível com `background-position`
- Outros valores possíveis: `left top`, `center center`, `center bottom` etc.


---
## Ajustando o **tamanho da imagem**

![](../../images/background-size-cover.png)
![](../../images/background-size-contain.png)

<!-- {p:style="margin-bottom: 0;"} -->

- `background-size: cover`: imagem redimensionada para cobrir todo o espaço
- `background-size: contain`: imagem redimensionada para aparecer completamente

---
<!-- {"hash": "ocupando-toda-altura-navegador"} -->
## Ocupando toda a altura do navegador

![](../../images/ocupando-toda-altura-disponivel.png)

---
## Ocupando toda a altura do navegador (cont.)

- **1ª tentativa**: definir a altura do elemento `body` como `100%`:
  ![](../../images/ocupando-toda-altura-disponivel-body.png) <!-- {.push-right style="height: 134px; margin-top: 1em;"} -->
  ```css
  body {
    height: 100%;
  }
  ```
- **Jeito certo**: definir a altura **do elemento `body` <ins>e do
  `html`</ins>** como `100%`:
  ![](../../images/ocupando-toda-altura-disponivel-body-html.png) <!-- {.push-right style="height: 134px; margin-top: 1em;"} -->
  ```css
  html, body {
    min-height: 100%;
  }
  ```

---
<!-- {"hash": "textos-sombreados"} -->
## Textos <span style="text-shadow: 2px 2px purple; color: hotpink;">sombreados</span>

![](../../images/text-shadow-none.png)
![](../../images/text-shadow-black.png)

<!-- {p:style="margin-bottom: 0;"} -->

- Colocar sombras em textos facilita sua leitura quando o texto está sobre uma
  imagem que pode ter muitas cores
  ```css
  h1 {
    text-shadow: 2px 2px black;
  }
  ```

---
<!-- {"hash": "cores-transparentes"} -->
## Cores semitransparentes

- É possível usar cores com transparência, que deixam
  "o que está atrás" aparecer. Por exemplo:
  - ```css
    color: rgba(255, 255, 255, 0.20); /* ou #fff3: branco 20% opaco */
    color: rgba(255, 255, 255, 0.67); /* ou #fffa: branco 67% opaco */
    color: rgba(255, 255, 255, 1);    /* mesmo que white */
    color: rgba(0, 0, 0, 0.53);       /* ou #0008: preto 53% opaco */
    color: rgba(0, 0, 255, 0.53);     /* ou #00f8: azul 53% opaco */
    ```
    <!-- {li:style="flex-grow: 1;"} -->
  - ::: result
    - branco <!-- {li:style="color: rgba(255, 255, 255, 0.3)"} -->
    - branco <!-- {li:style="color: rgba(255, 255, 255, 0.7)"} -->
    - branco  <!-- {li:style="color: rgba(255, 255, 255, 1)"} -->
    - preto  <!-- {li:style="color: rgba(0, 0, 0, 0.5)"} -->
    - _azul_ <!-- {em:style="color: rgba(0, 0, 255, 0.6); font-style: normal;"} -->
    :::
    <!-- {ul^1:.layout-split-2.no-list-icon.no-padding} -->
    <!-- {li:style="flex-grow: 1;"} -->
    <!-- {ul^2:style="width: 100%;"} -->
- Podemos usar a notação RGBA(...) ou hexadecimal


---
## Cores semitransparentes

- Também podemos fazer isso com `background-color`:
  - ```css
    p {
      /* preto 50% opaco */
      background-color: rgba(0, 0, 0, 0.5);
      color: white;
    }
    ```
    ```html
    <p>Yarrr Harrr, marujo!!</p>
    ```
    <!-- {li:style="flex-grow: 1;"} -->
  - ::: result
    <p style="background-color: rgba(0, 0, 0, 0.5); color: white;">Yarrr Harrr, marujo!!</p>
    :::
    <!-- {ul^0:.layout-split-2.no-list-icon.no-padding} -->
    <!-- {li:style="flex-grow: 1;"} -->
    <!-- {ul^1:style="width: 100%;"} -->
    - Repare que o fundo do parágrafo ficou azulado
      - ...porque o fundo da página era azul


---
<!-- {"layout": "centered"} -->
# Referências

1. Capítulos 13 do livro Use a Cabeça HTML e CSS, 2ª edição
