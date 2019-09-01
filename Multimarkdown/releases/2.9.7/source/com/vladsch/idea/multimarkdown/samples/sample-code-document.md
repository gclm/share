# Sample Markdown Document

[TOC]: #

### Table of Contents
- [Setext heading marker equalization](#setext-heading-marker-equalization)
- [Ordered List Formatting](#ordered-list-formatting)
    - [Block Quote Formatting](#block-quote-formatting)
    - [Code Fence Formatting](#code-fence-formatting)
    - [Verbatim Formatting](#verbatim-formatting)

Heading Formatting
===
Setext heading marker equalization
---
###Heading with *trailing* markers #

  Text block with continuations and hard break spaces[^hard-break-spaces],
            which are two or more trailing spaces  
        at the end of the line.

  Footnote definitions can be arranged within the document[^1].

[^hard-break-spaces]: Hard break spaces are two or more trailing spaces on a line that is part of a paragraph text block

##Unordered **List** Formatting
first paragraph before list
* list item 1
list item 1 lazy continuation text  
        with hard break spaces

     Contained child text block of bullet list item

* list item 2
*
    * sub item
    * [ ] task sub item
        * sub item

      task sub item paragraph with overflow wrapping text
* [ ] task item
    * sub item

      sub item paragraph with Abbr1

* [X] task item
* [x] task item

*[Abbr2]: Abbreviation 2 expanded text

*[Abbr1]: Abbreviation 1 expanded text


## Ordered **_List_** Formatting
1. Ordered list item 1
list item 1 lazy continuation text with hard break spaces  
and Abbr3

    Contained child text block of bullet list item


1. Ordered list item 2
list item 1 lazy continuation text  
        with hard break spaces



   Contained child text block of bullet list item
1. Ordered list item 3
1. Ordered list item 4
1. Ordered list item 5
1. Ordered list item 6
1. Ordered list item 7
1. Ordered list item 8
1. Ordered list item 9
1. Ordered list item 10

*[Abbr3]: Abbreviation 3 expanded text

[1]: http://example.com  "Example"

[^1]: Footnote text that will be reformatted as a text block
with continuations and hard break spaces handled  
     according to preferences. Additionally, these elements can be moved within the
 document: top of document, group with first, group with last or bottom of document.

### `Block Quote` Formatting #

> block quote text with irregular formatting
> that will reflow to margins, respecting hard
> breaks
>>nested block quote
>>nested block quote continuation
>>with hard break spaces  
>>this is a new line

[2]: http://example.com  "Example"
[4]: mailto:me@me.com  "Example"
[3]: ftp://example.com  "Example"

*[Abbr4]: Abbreviation 4 expanded text

Term 1
: Definition can contain multiple lines with   [1]
  lazy continuation and wrapping to margins where necessary.

~ Definition can contain multiple lines with
  lazy continuation and wrapping to margins where necessary. [4]

###Table Formatting

Left Aligned |Left Aligned|Right Aligned|Centered
|-----------|:-----------|----------:|:-----:
Row 1 Cell 1 |Row 1 Cell 2|Row 1 Cell 3 Text|Row 1 Cell 4 Centered
Row 2 Cell 1 |Row 2 Cell 2 Text |Row 2 Cell 3|Row 2 Cell 4 Short
Row 3 Cell 1 |Row 3 Cell 2 |Row 3 Cell 3
[Table Caption]

| マルチバイト |
|:-------|
| Cell |

| Alphabet |
|:---------|
| マルチバイト|

マルチバイ トマルチバイト マルチバイト マルチ バイトマル チバイ トマルチバイト マルチバイ トマル チバイト マルチバイト マルチバイト マルチバイト マルチバイト

| 字段名| 说明| 是否必须 | 备注   |
|---------|:--------|---------|--------|
| status| 状态码    | 是 | String |
| result  | 内容主体  | 否   | Object |
| message | 异常情况的错误信息，供显示给用户 | 否 | String |

异常情 况 的 错误 信息, mixed chars width wrapping mode test 供显 示给用户 异常情况的 错 误信息 供显 示给 用户
异常情 况的错误 信息，供显示给用户 异常情况的错 误信息，供显 示给用户  异常情况 的错误信息，供显示给用户
异常 情况的 错 误 信息，供显 示给 用户

### Code Fence Formatting

```java 
      class Dummy {
          private final int intValue;

          public Dummy(int intValue) {
              this.intValue = intValue;
          }
      }
~~~

- Item

  ~~~java
           class Dummy {
               private final int intValue;

               public Dummy(int intValue) {
                   this.intValue = intValue;
               }
           }
  ```

### Verbatim Formatting

      class Dummy {
          private final int intValue;

          public Dummy(int intValue) {
              this.intValue = intValue;
          }
      }

- Item

          class Dummy {
              private final int intValue;

              public Dummy(int intValue) {
                  this.intValue = intValue;
              }
          }

