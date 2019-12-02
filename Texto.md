# Principais Tags HTML para texto

As tags de texto em HTML devem manter a coerência estrutural e a clareza semântica de cada elemento da página. Toda a parte de estilo (elementos visuais) devem ser feitos via CSS.

## Comentário `<!-- -->`

### Semântica
Um comentário é um elemento intrínseco do código e não texto em si, portanto não tem semântica específica que não seja deixar um comentário para leitores do código fonte.

### Sintaxe
    <!-- comentário no código -->

## Parágrafo `<p>`

### Semântica 
Um parágrafo como bloco no texto. Todo parágrafo deve vir dentro de um elemento `<p>`.

### Atributos
- `align` foi descontinuado no HTML5, em favor do CSS:  
    
            `<p style="text-align:right"> parágrafo </p>`


- `display` (default:block); O atributo CSS block mostra um elemento como um bloco no texto, ou seja, começa numa nova linha e ocupa toda a largura disponível.

### Defaults
        p {
            display: block;
            margin-top: 1em;
            margin-bottom: 1em;
            margin-left: 0;
            margin-right: 0;
            }

---

## Títulos `<h1> -> <h6>`

### Semântica 
Estes são os títulos disponíveis, do mais importante (`<h1>`) até o de destaque pouco maior que o texto (`<h6>`). 
    
### Sintaxe
        <h1> Título </h1>

### Defaults:
        h1 {
                display: block;
                font-size: 2em;
                margin-top: 0.67em;
                margin-bottom: 0.67em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        h2 {
                display: block;
                font-size: 1.5em;
                margin-top: 0.83em;
                margin-bottom: 0.83em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        h3 {
                display: block;
                font-size: 1.17em;
                margin-top: 1em;
                margin-bottom: 1em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        h4 {
                display: block;
                font-size: 1em;
                margin-top: 1.33em;
                margin-bottom: 1.33em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        h5 {
                display: block;
                font-size: .83em;
                margin-top: 1.67em;
                margin-bottom: 1.67em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        h6 {
                display: block;
                font-size: .67em;
                margin-top: 2.33em;
                margin-bottom: 2.33em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

### Observações: 
- Todo título de seção, subseção, etc, deve vir dentro de algum destes elementos.
- Não importa o nível de título que você escolha usar, desde que a hierarquia entre eles faça sentido (jamais use um `<h2>` como subseção de um `<h3>`)
- Use apenas um `<h1>` por página
- Dos 6 títulos disponíveis, tente usar no máximo 3 por página.

---

##  Container inline `<span>`

### Semântica 
Este elemento é um container genérico que não tem semântica definida, é apenas parte (inline) de um texto que pode ser alterada posteriormente via CSS.

### Observações
- É semelhante ao elemento `<div>` (para criar blocos), porém inline.
- Usado para agrupar elementos sob um único class ou id.
- Usado para compartilhar valores de atributos diversos.
- Segundo a Mozilla, deve ser usado apenas quando nenhum outro elemento semântico for apropriado.

---

## Quebra de página `<br>`
### Semântica
Quebra de linha. Quebra a linha atual e continua o texto numa nova linha dentro do elemento `<p>`, sem a necessidade de se criar um novo parágrafo.
### Sintaxe: 
Não precisa de closing tag.

    A linha acaba aqui <br>

### Observações: 
- Não use esta tag para separar parágrafos.
- Não use para aumentar o espaçamento entre linhas, para isso use CSS (elemento margin ou p)

---

## Ênfase `<em>`

### Semântica
Esta phrase tag dá ênfase a uma palavra, sendo reconhecida por leitores de tela e lida em tom diferente. 

### Observações
Apesar de ser padrão nos browsers estilizar `em` como itálico, você não deve usá-la para colocar um texto em itálico por motivos de assessibilidade e semântica. Para itálico, use CSS.

        em {
        font-style: italic;
        }
---

## Highlight `<mark>`

### Semântica
Phrase tag usada para destacar texto via highlight. 

### Sintaxe
    <mark> highlight em HTML </mark>

### Defaults
    mark {
    background-color: yellow;
    color: black;
    }

----

## `<strong>` Importante

### Semântica
Phrase tag usada para dar importância a uma parte do texto. 

### Sintaxe
    <strong>Strong text</strong>

### Defaults
    strong {
      font-weight: bold;
    }

### Observações
Apesar de ser padrão nos browsers estilizar `strong` como negrito, você não deve usá-la para colocar um texto em negrito por motivos de assessibilidade e semântica. Para negrito, use CSS.

----
## Abreviação `<abbr>` 

### Semântica
Phrase tag usada para indicar abreviação. 

### Sintaxe

    <abbr title = "Rowan Atkinson">Mr. Bean</abbr>

### Defaults
    strong {
      font-weight: bold;
    }

### Atributos
- title: é mostrado quando o mouse passa sobre a abreviação

----

## Definição `<dfn>`

### Semântica
Phrase tag usada para indicar que naquele local fica a definição da palavra.

### Sintaxe

    <dfn>HTML</dfn>

### Defaults
    strong {
      font-weight: bold;
    }

### Atributos
- `title` é o termo a ser definido, da forma como será reconhecido por buscas e leitores


### Observações
- O elemento "parent" mais próximo, seja ele  `<p>`, `<dt>`, `<dd>` ou `<section>`  deve ser a definição do termo em si.
- Por ser a definição, é indicado que esta tag seja usada na primeira vez que a palavra é usada, quando seu significado é dado.

---

##  Citação `<blockquote>`

### Semântica
Phrase tag usada para indicar uma citação extendida de uma outra fonte. 

### Sintaxe

    <blockquote cite="http://www.google.com">
    Texto da citação de outro site.
    </blockquote>

### Atributos
- cite é um atributo cujo valor é uma url, indicando a fonte da citação.

### Observações
- Use a tag `<q>` para citações curtas (inline).
- Além do atributo `cite` da tag `<blockquote>`, existe a tag `<cite>`, que denota o título de um trabalho, erroneamente usada com o nome do autor.
- Para autor, use a tag `<address>`, que é usada para informações de contato (e **somente** é usada para *endereço* caso este seja parte das informações de contato!)
- O elemento `<address>` geralmente é usado dentro de um `<footer>`.


### Defaults
    blockquote {
      display: block;
      margin-top: 1em;
      margin-bottom: 1em;
      margin-left: 40px;
      margin-right: 40px;
    }

    cite {
    font-style: italic;
    }

    address {
    display: block;
    font-style: italic;
    }

---
##  Código `<code>`

### Semântica
Phrase tag usada para indicar que o texto é um código em alguma linguagem de programação ou marcação. 

### Sintaxe
    `<code><?php echo "Hello World!" ?></code>`

### Observações
  - O elemento `<code>` é usado dentro de uma linha de código. Para mais linhas, envolva o `<code>` dentro de um elemento `<pre>`.
  - O elemento `pre` (preformatted text) usa fonte de comprimento fixo (fixed width) e preserva espaços em branco e linhas do texto, portanto é ideal para blocos em que o texto não deve enrolar-se (wrap).
  - Tanto `code` quanto `pre` são usados para código de entrada. Para denotar códido de **saída**, é usado o elemento `<samp>`, como no exemplo abaixo:

   <pre>
      <samp><span class="prompt">mike@interwebz:~$</span> <kbd>md5 -s "Hello world"</kbd> MD5 ("Hello world") = 3e25960a79dbc69b674cd4ec67a72c62
      <span class="prompt">mike@interwebz:~$</span> <span class="cursor">█</span></samp>
   </pre>

### Defaults
    code {
      font-family: monospace;
    }

    pre {
      display: block;
      font-family: monospace;
      white-space: pre;
      margin: 1em 0;
    }

    samp {
      font-family: monospace;
    }


---

##  Teclado `<kbd>`

### Semântica
Phrase tag usada para indicar entrada de texto - seja via teclado, voz ou de qualquer outro tipo.

### Sintaxe
    <kbd>Ctrl</kbd>

### Defaults
    kbd {
    font-family: monospace;
    }

### Observações

    kbd {
    background-color: #eee;
    border-radius: 3px;
    border: 1px solid #b4b4b4;
    box-shadow: 0 1px 1px rgba(0, 0, 0, .2), 0 2px 0 0 rgba(255, 255, 255, .7) inset;
    color: #333;
    display: inline-block;
    font-size: .85em;
    font-weight: 700;
    line-height: 1;
    padding: 2px 4px;
    white-space: nowrap;
    }

---

## Mudança de tema no texto `<hr>`

### Semântica
Este elemento insere uma linha horizontal (horizontal line - hr) entre dois parágrafos, indicando que houve mudança (no tema, no assunto, na cena, etc) dentro da mesma seção.

### Sintaxe
    <hr>

### Defaults
    hr {
        display: block;
        margin-top: 0.5em;
        margin-bottom: 0.5em;
        margin-left: auto;
        margin-right: auto;
        border-style: inset;
        border-width: 1px;
        }

### Obervações
Historicamente, a representação deste elemento é uma linha horizontal, mas agora este elemento é definido em termos semânticos e é possível/recomendável usar CSS para alterá-lo.

### Atributos

- `align` é o alinhamento, que pode assumir os valores `left, center, right`. O default é `left`.
- `color` pode ser o nome da cor ou um valor hexadecimal.
- `noshade` especifica se a linha deve ou não ter sombra
- `height` é a altura em pixels
- `width` é o comprimento em pixels ou porcentagem.


