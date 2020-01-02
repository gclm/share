# Sample Wrapping Document

  Text block with continuations and hard break spaces[^hard-break-spaces],
            which are two or more trailing spaces  
        at the end of the line.

  Footnote definitions can be arranged within the document[^1].

[^hard-break-spaces]: Hard break spaces are two or more trailing spaces on a line that is part of a paragraph text block

first paragraph before list
* list item 1
list item 1 lazy continuation text  
        with hard break spaces

     Contained child text block of bullet list item

## Ordered **_List_** Formatting
1. Ordered list item 1
list item 
1\. lazy continuation text with hard break spaces  
followed by more text. [Link](http://example.com) 

    Contained child text block of bullet list item ![Image](http://example.com/i.png)

[^1]: Footnote text that will be reformatted as a text block
with continuations and hard break spaces handled  
     according to preferences. Additionally, these elements can be moved within the
 document: top of document, group with first, group with last or bottom of document.

> block quote text with irregular formatting
> that will wrap to margins, respecting hard
> breaks
>>nested block quote
>>nested block quote continuation
>>with hard break spaces  
>>this is a new line

Term 1
: Definition can contain multiple lines with
  lazy continuation and wrapping to margins where necessary.

~ Definition can contain multiple lines with
  lazy continuation and wrapping to margins where necessary.

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

