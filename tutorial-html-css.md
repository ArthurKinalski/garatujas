# 💻 ia26-webdesign (versão simplificada)

Este repositório contém um guia introdutório de **Web Design**, focado em ensinar os conceitos básicos para criação de páginas web.

---

## Antes do início

É desejável que os alunos tenham um ambiente de desenvolvimento configurado em suas máquinas, incluindo um editor de código e um navegador web atualizado. Nesta disciplina, utilizaremos o Visual Studio Code como editor de código (por ser gratuito e o mais utilizado no mercado) e o Google Chrome como navegador web (pelos mesmos motivos).

## HTML - HyperText Markup Language (Linguagem de Marcação de Hipertexto)

HTML é uma linguagem de marcação usada para organizar o conteúdo de páginas web de forma acessível e estruturada. Ele utiliza tags (como `<h1>`, `<p>`, `<a>`) para definir cada tipo de conteúdo, podendo incluir atributos (class, id, src) para adicionar mais informações.

Funciona de forma parecida com o Word: você “marca” partes do texto. Essas marcações são feitas com tags de abertura e fechamento, como `<p>texto</p>`, onde o conteúdo fica entre elas.

![Animação de seleção](docs/select.gif)

Na animação acima, o usuário escreve em um editor a frase `lorem ipsum dolor sit amet potentia` e, então, executa algumas seleções de definição de formatação. A seguir, veremos, passo a passo, o equivalente em HTML para cada uma dessas seleções/formatações.

1. O usuário seleciona `lorem ipsum` e aplica a formatação de negrito.
  - Em HTML, o código correspondente seria `<strong>lorem ipsum</strong> dolor sit amet potentia`, onde a tag `<strong>` é usada para indicar que o texto deve ser exibido em negrito. No exemplo, a marcação começa com a tag `<strong>` e termina com a tag de fechamento `</strong>`, indicando que o texto entre essas tags deve ser exibido em negrito.
2. O usuário seleciona `sit amet` e aplica a formatação de itálico.
  - Em HTML, o código correspondente seria `<strong>lorem ipsum</strong> dolor <em>sit amet</em> potentia`, onde a tag `<em>` é usada para indicar que o texto deve ser exibido em itálico. No exemplo, a marcação começa com a tag `<em>` e termina com a tag de fechamento `</em>`, indicando que o texto entre essas tags deve ser exibido em itálico.
3. O usuário seleciona `ipsum dolor sit` e aplica a cor vermelha.
  - Em HTML, o código correspondente seria `<strong>lorem <span style="color: red;">ipsum dolor sit</span></strong> amet <em>sit amet</em> potentia`, onde a tag `<span>` é usada para aplicar estilos específicos a um trecho de texto, e o atributo `style` é usado para definir a cor do texto como vermelha. No exemplo, a marcação com a tag `<span>` começa antes de `ipsum` e termina após `sit`, indicando que o texto entre essas tags deve ser exibido em vermelho.

> **⚠️ Nota:**
>
> O HTML é uma linguagem de marcação, e seu principal objetivo é estruturar o conteúdo de uma página web. Caso pesquise na internet, notará que existem outras tags para aplicar formatações como negrito e itálico, como `<b>` e `<i>`, respectivamente. No entanto, as tags `<strong>` e `<em>` são consideradas mais semânticas, pois indicam a importância do texto, enquanto as tags `<b>` e `<i>` são puramente de formatação visual. Portanto, é recomendado usar as tags semânticas para melhorar a acessibilidade e a compreensão do conteúdo.
>
> `<strong>` e `<em>` fazem sentido tanto para leitores sem deficiência quanto para leitores com deficiência, pois indicam a importância do texto, enquanto `<b>` e `<i>` são puramente de formatação visual e podem não ser interpretados corretamente por leitores de tela ou outros dispositivos assistivos.

### Estrutura básica de um documento HTML

Todo documento HTML começa com `<!DOCTYPE html>`, que indica ao navegador que é um arquivo HTML5.

Ele é dividido em duas partes principais:

`<head>` → contém informações da página (título, links, scripts), mas não aparece para o usuário
`<body>` → contém todo o conteúdo visível (textos, imagens, links, etc.)

Ou seja, o `<head>` configura a página e o `<body>` mostra o conteúdo.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
   <meta charset="UTF-8">
   <title>Título da Página</title>
   <!-- Links para arquivos CSS e scripts JavaScript podem ser adicionados aqui -->
</head>
<body>
   <!-- Conteúdo visível da página é adicionado aqui -->
</body>
</html>
```
> **⚠️ Nota:**
>
> Todo o código HTML deve ser escrito dentro da tag `<html>`, que é a raiz do documento. O atributo `lang="pt-BR"` indica que o idioma principal do conteúdo da página é o português do Brasil, o que é importante para a acessibilidade e para os mecanismos de busca entenderem o idioma da página. O elemento `<meta charset="UTF-8">` define a codificação de caracteres do documento como UTF-8, garantindo que caracteres acentuados e outros símbolos sejam exibidos corretamente. O elemento `<title>` define o título da página, que é exibido na aba do navegador e nos resultados de busca.

### Atributos HTML

Atributos HTML são usados para adicionar informações extras aos elementos. Eles ficam na tag de abertura e são escritos como nome="valor".

Servem para definir coisas como comportamento e aparência, por exemplo:

href → define o link.

src → define a imagem.

Eles são importantes para personalizar e controlar os elementos da página.

Imagine que temos a necessidade de criar um link para o site do Google em uma página web. Para isso, podemos usar a tag `<a>` (âncora) e o atributo `href` para especificar o URL do Google. O código HTML correspondente seria:

```html
<a href="https://www.google.com">Visite o Google</a>
```
O que resultaria em um link clicável com o texto "Visite o Google". Quando o usuário clicar nesse link, ele será redirecionado para a página do Google. O atributo `href` é fundamental para criar links em HTML, e seu valor deve ser um URL válido para garantir que o link funcione corretamente, como é possível ver no resultado abaixo:

[Visite o Google](https://www.google.com)

### Lista de todas as tags HTML

Nestes links, você pode encontrar uma lista completa de todas as tags HTML, juntamente com suas descrições e exemplos de uso: [MDN Web Docs - Elementos HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element) ou [W3Schools - HTML Tags](https://www.w3schools.com/TAGS/default.asp).

## CSS - Cascading Style Sheets (Folhas de Estilo em Cascata)

O CSS é uma linguagem de estilo que controla a aparência e o layout de uma página web.

Ele separa o visual (CSS) da estrutura do conteúdo (HTML), deixando o código mais organizado.

O CSS usa seletores para escolher elementos HTML e declarações para definir propriedades como cores, fontes e espaçamento.