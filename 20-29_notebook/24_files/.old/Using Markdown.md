# Using Markdown

1. [Using Markdown](#using-markdown)
   1. [Basics](#basics)
   2. [Standard Markdown](#standard-markdown)
      1. [Syntax](#syntax)
      2. [Extended Syntax](#extended-syntax)
   3. [Commonmark](#commonmark)
      1. [Syntax](#syntax-1)
      2. [Extended Syntax](#extended-syntax-1)
   4. [GFM](#gfm)
      1. [Syntax](#syntax-2)
      2. [Extended Syntax](#extended-syntax-2)
   5. [Other Markdown Syntax](#other-markdown-syntax)
2. [Latent Architect Markdown Setup](#latent-architect-markdown-setup)
   1. [Extended Components and Syntax](#extended-components-and-syntax)
      1. [Containers](#containers)
      2. [Comments](#comments)
   2. [Pandoc](#pandoc)
   3. [HTML in Markdown](#html-in-markdown)
   4. [VSCode](#vscode)
      1. [Variables](#variables)


[[Markdown VSCode Extensions]]

!!! Docs & Reference
    [DeveloperHub](https://docs.developerhub.io/support-center/using-markdown)
    [markdown-it](https://github.com/markdown-it/markdown-it)
    [markdown-it-style](https://github.com/zzzze/markdown-it-style)
    [VSCode Markdown](https://code.visualstudio.com/docs/languages/markdown)
    [markdown-it-attrs](https://github.com/arve0/markdown-it-attrs)
    [mkDocs ref - content-tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/)
    [vite markdown custom containers](https://vitepress.dev/guide/markdown#custom-containers)
    [Razor Press - Custom Markdown Containers](https://docs.servicestack.net/razor-press/containers)
    [Multimarkdown criticMarkup](https://fletcher.github.io/MultiMarkdown-6/syntax/critic.html)


## Basics

There are two three common markdown specs that are widely used:

| [Standard Markdown](#standard-markdown) | [Commonmark](#commonmark) | [Github Flavored Markdown](#GFM) |
| - | - | - |

<!-- ![[Commonmark]] -->

## Standard Markdown
::: headerCaption
[^1] Standard Markdown Spec
:::

### Syntax

***Linking syntax:*** [^4] #ExternalSource
::: externalSourceQuote
*Below are a few ways to write Reference-Links:*

    [I'm an inline-style link](https://www.somewebsite.com)
    [I'm an inline-style link with title](https://www.somewebsite.com "somewebsite's Homepage")
    [I'm a reference-style link][Arbitrary case-insensitive reference text]
    [I'm a relative reference to a repository file](../blob/master/LICENSE)
    [You can use numbers for reference-style link definitions][1]
    Or leave it empty and use the [link text itself]
    Some text to show that the reference links can follow later.
    [arbitrary case-insensitive reference text]: https://www.somewebsite.org
    [1]: http://somewebsite.org
    [link text itself]: http://www.somewebsite.com
:::

***Example for link titling:*** [^5] #ExternalSource
::: externalSourceQuote
*The link URL may, optionally, be surrounded by angle brackets:*

    [id]: <http://example.com/>  "Optional Title Here"
    You can put the title attribute on the next line and use extra spaces or tabs for padding, which tends to look better with longer URLs:
    [id]: http://example.com/longish/path/to/resource/here
    "Optional Title Here"
:::

***Example for footnotes:*** [^6] #ExternalSource
::: externalSourceQuote
*How to add simple footnotes:*
    
    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].
    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"
:::

### Extended Syntax

## Commonmark 
::: headerCaption
[^2] Commonmark Spec
:::

### Syntax

### Extended Syntax

## GFM
::: headerCaption
[^3] GFM Spec
:::

### Syntax

### Extended Syntax

## Other Markdown Syntax

- [PHP Markdown & PHP Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#html)
- [MultiMarkdown](https://michelf.ca/projects/php-markdown/extra/#html)
  - [MultiMarkdown Syntax Cheat Sheet](https://rawgit.com/fletcher/MultiMarkdown-6-Syntax-Guide/master/index.html)
- 

# Latent Architect Markdown Setup

VSCode, with my current configuration uses [[markdown-it]] for rendering/parsing the markdown. See linked note for markdown-it documentation.

## Extended Components and Syntax

### [Containers](https://docs.servicestack.net/razor-press/containers#built-in-containers:~:text=your%20Markdown%20documents.-,Built%2Din%20Containers,-Most%20of%20VitePress)

::: info
this is an example
:::

!!! NOTE #NOTE
    The Containers above do not work within Foam or VSCode with current config

### Comments

Standard:
```html
<!-- this is a comment -->
<!-- 
you can comment out lines contained
within these braces
 -->

```

Other:
```markdown
[//]: # (this is a comment)
[//]: <this is also a comment apparently>
[//]: # "this is a comment"
[comment]: # (could possibly use this to link ALL comments)
```

External notes found about comments:

    Both conditions are important:

    Using # (and not <>)
    With an empty line before the comment. Empty line after the comment has no impact on the result.
    The strict Markdown specification CommonMark only works as intended with this syntax (and not with <> and/or an empty line)

    To prove this we shall use the Babelmark I, by Alexandre Mutel. This tool checks the rendering of particular source code on a large number of Markdown implementations.

    (+ — passed the test, - — didn't pass, ? — leaves some garbage which is not shown in rendered HTML).

    No empty lines, using <> 13+, 15-
    Empty line before the comment, using <> 20+, 8-
    Empty lines around the comment, using <> 20+, 8-
    No empty lines, using # 13+ 1? 14-
    Empty line before the comment, using # 23+ 1? 4-
    Empty lines around the comment, using # 23+ 1? 4-
    HTML comment with 3 hyphens 1+ 2? 25- from the chl's answer (note that this is different syntax)
    This proves the statements above.

    These implementations fail all 7 tests. There's no chance to use excluded-on-render comments with them.

    cebe/markdown 1.1.0
    cebe/markdown MarkdownExtra 1.1.0
    cebe/markdown GFM 1.1.0
    s9e\TextFormatter (Fatdown/PHP)


## Pandoc 
::: headerCaption
[^7] Pandoc Spec
:::

## HTML in Markdown
#HTML #Markdown #CSS

You can put the styles at the bottom of the document. Refer to [[Snippets]] for example. Also see this [reference](https://www.freecodecamp.org/news/inline-css-guide-how-to-style-an-html-tag-directly/) for in-depth explanation of inline styles for #CSS

## VSCode

[Markdown editing with Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown)

### Variables

Taken from: [Markdown editing with Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown#:~:text=By%20default%20VS%20Code,r/image.png.)

By default VS Code automatically copies dropped or pasted images outside of the workspace into your workspace. The markdown.copyFiles.destination setting controls where the new image file should be created. This setting maps globs that match on the current Markdown document to image destinations. The image destinations can also use some simple variables. See the markdown.copyFiles.destination setting description for information about the available variables.

For example, if we want every Markdown file under /docs in our workspace to put new media files into an images directory specific to the current file, we can write:

```
"markdown.copyFiles.destination": {
  "/docs/**/*": "images/${documentBaseName}/"
}
```

Now when a new file is pasted in /docs/api/readme.md, the image file is created at /docs/api/images/readme/image.png.

You can even use simple regular expressions to transform variables in a similar way to snippets. For example, this transform uses only the first letter of the document file name when creating the media file:

```
"markdown.copyFiles.destination": {
  "/docs/**/*": "images/${documentBaseName/(.).*/$1/}/"
}
```

When a new file is pasted into /docs/api/readme.md, the image is now created under /docs/api/images/r/image.png.

<!-- # Footer -->

<!-- ## Definitions -->

*[GFM]: - Github Flavored Markdown

<!-- ## Links & Refs -->

[^1]: [Markdown Spec](https://daringfireball.net/projects/markdown/syntax) 
[^2]: [Commonmark Spec](https://spec.commonmark.org/0.30/)
[^3]: [GFM Spec](https://github.github.com/gfm/)
[^4]: [Source for linking options in md syntax](https://stackoverflow.com/questions/24580042/github-markdown-are-macros-and-variables-possible#:~:text=Below%20are%20a%20few%20ways%20to%20write%20Reference%2DLinks)
[^5]: [Source for link titling in md syntax](https://daringfireball.net/projects/markdown/syntax#hr:~:text=SPAN%20ELEMENTS-,LINKS,-Markdown%20supports%20two)
[^6]: [Source for footnotes in md syntax](https://daringfireball.net/projects/markdown/syntax#hr:~:text=Here%E2%80%99s%20an%20example%20of%20reference%20links%20in%20action%3A)
[^7]: [Pandoc](https://pandoc.org/)