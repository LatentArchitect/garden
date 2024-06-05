# Commonmark
[[Using Markdown]]

## Core Syntax

```
# Header 1 #
## Header 2 ##
### Header 3 ###             (Hashes on right are optional)
#### Header 4 ####
##### Header 5 #####

## Markdown plus h2 with a custom ID ##         {#id-goes-here}
[Link back to H2](#id-goes-here)

This is a paragraph, which is text surrounded by whitespace. Paragraphs can be on one 
line (or many), and can drone on for hours.  

Here is a Markdown link to [Warped](http://warpedvisions.org), and a literal . 
Now some SimpleLinks, like one to [google] (automagically links to are-you-
feeling-lucky), a [wiki: test] link to a Wikipedia page, and a link to 
[foldoc: CPU]s at foldoc.  

Now some inline markup like _italics_,  **bold**, and `code()`. Note that underscores in 
words are ignored in Markdown Extra.

![picture alt](/images/photo.jpeg "Title is optional")     

> Blockquotes are like quoted text in email replies
>> And, they can be nested

* Bullet lists are easy too
- Another one
+ Another one

1. A numbered list
2. Which is numbered
3. With periods and a space

And now some code:

    // Code is just text indented a bit
    which(is_easy) to_remember();

~~~

// Markdown extra adds un-indented code blocks too

if (this_is_more_code == true && !indented) {
    // tild wrapped code blocks, also not indented
}

~~~

Text with  
two trailing spaces  
(on the right)  
can be used  
for things like poems  

### Horizontal rules

* * * *
****
--------------------------


<div class="custom-class" markdown="1">
This is a div wrapping some Markdown plus.  Without the DIV attribute, it ignores the 
block. 
</div>

## Markdown plus tables ##

| Header | Header | Right  |
| ------ | ------ | -----: |
|  Cell  |  Cell  |   $10  |
|  Cell  |  Cell  |   $20  |

* Outer pipes on tables are optional
* Colon used for alignment (right versus left)

## Markdown plus definition lists ##

Bottled water
: $ 1.25
: $ 1.55 (Large)

Milk
Pop
: $ 1.75

* Multiple definitions and terms are possible
* Definitions can include multiple paragraphs too

*[ABBR]: Markdown plus abbreviations (produces an <abbr> tag)
```
---
## Extended Syntax

##### *Abbr*
*[Abbr]: Abbreviation / Definition

!!! info
    Word that should be defined
    *[Word]: Definition for that word
    Defining that Word going forward within that document will be persistent.

##### Custom ID for Headings {#custom-heading-id}

##### Container Divs:
Extended Markdown allows the use of container divs for custom styling:

::: warning
This is a warning
:::

##### Admonitions:
Admonitions can be used for side notes, warnings, tips, etc. (Common in some Markdown extensions like Python-Markdown-Myst):

!!! note
    This is a note

### Special Attributes
With Markdown Extra, you can set the id and class attribute on certain elements using an attribute block. For instance, put the desired id prefixed by a hash inside curly brackets after the header at the end of the line, like this:

```
Header 1            {#header1}
========

## Header 2 ##      {#header2}
Then you can create links to different parts of the same document like this:

[Link back to header 1](#header1)
To add a class name, which can be used as a hook for a style sheet, use a dot like this:

## The Site ##    {.main}
You can also add custom attributes having simple values by specifying the attribute name, followed by an equal sign, followed by the value (which cannot contain spaces at this time):

## Le Site ##    {lang=fr}
The id, multiple class names, and other custom attributes can be combined by putting them all into the same special attribute block:

## Le Site ##    {.main .shine #the-site lang=fr}
At this time, special attribute blocks can be used with

headers,
fenced code blocks,
links, and
images.
For image and links, put the special attribute block immediately after the parenthesis containing the address:

[link](url){#id .class}  
![img](url){#id .class}
Or if using reference-style links and images, put it at the end of the definition line like this:

[link][linkref] or [linkref]  
![img][linkref]

[linkref]: url "optional title" {#id .class}

```