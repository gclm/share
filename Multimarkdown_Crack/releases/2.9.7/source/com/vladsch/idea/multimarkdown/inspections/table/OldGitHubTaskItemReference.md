This inspection searches for task item marker followed by reference in files with `Old GitHub
Doc` lists parser option enabled.

In **Old GitHub** markdown, before the switch to CommonMark, a task item marker followed by a
link reference was processed as a link reference with explicit text instead of a task list item
marker followed by a reference.

As a work-around a `&nbsp;` needs to be
inserted between the task item marker and the link reference.

