---
hide:
    navigation
---

# Code Blocks

## English version

### Code blocks Google SQL
<div class="grid cards" markdown>




-   !!! info "Code block with title"
    
        ``` sql title="file.sql"
        SELECT * 
        FROM `project_id.dataset_name.table_a`
        ```


-   !!! info "Code block with annotation"
    
        ``` sql
        SELECT * 
        FROM `project_id.dataset_name.table_a` -- (1)
        ```

        1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
            text__, images, ... basically anything that can be written in Markdown.

-   !!! info "Code block with annotation, stripped"
    
        ``` sql
        -- (1)!
        ```

        1.  Look ma, less line noise!

-   !!! info "Code block"
    
        ``` sql
        WITH
        get_data_a AS (
        SELECT * 
        FROM `project_id.dataset_name.table_a`
        ),

        get_data_b AS (
        SELECT * 
        FROM `project_id.dataset_name.table_b`
        ),

        union_all_data AS (
        SELECT * FROM get_data_a UNION ALL 
        SELECT * FROM get_data_b
        )


        SELECT * 
        FROM union_all_data
        ```

-   !!! info "Code block with line numbers"
    
        ``` sql linenums="1"
        WITH
        get_data_a AS (
        SELECT * 
        FROM `project_id.dataset_name.table_a`
        ),

        get_data_b AS (
        SELECT * 
        FROM `project_id.dataset_name.table_b`
        ),

        union_all_data AS (
        SELECT * FROM get_data_a UNION ALL 
        SELECT * FROM get_data_b
        )


        SELECT * 
        FROM union_all_data
        ```

-   !!! info "Highlighting specific lines"
    
        ``` sql hl_lines="13 14"
        WITH
        get_data_a AS (
        SELECT * 
        FROM `project_id.dataset_name.table_a`
        ),

        get_data_b AS (
        SELECT * 
        FROM `project_id.dataset_name.table_b`
        ),

        union_all_data AS (
        SELECT * FROM get_data_a UNION ALL 
        SELECT * FROM get_data_b
        )


        SELECT * 
        FROM union_all_data
        ```

-   !!! info "Highlighting specific lines ranges"
    
        ``` sql hl_lines="7-14"
         WITH
        get_data_a AS (
        SELECT * 
        FROM `project_id.dataset_name.table_a`
        ),

        get_data_b AS (
        SELECT * 
        FROM `project_id.dataset_name.table_b`
        ),

        union_all_data AS (
        SELECT * FROM get_data_a UNION ALL 
        SELECT * FROM get_data_b
        )


        SELECT * 
        FROM union_all_data
        ```


-   !!! info "Highlighting inline code blocks ?"
    
        The ```#!sql FORMAT_DATE(format_string, date_expr)``` Formats the date_expr according to the specified format_string.

</div>


### Code blocks
<div class="grid cards" markdown>

-   !!! info "Code block"
    
        ``` py
        import tensorflow as tf
        ```


-   !!! info "Code block with title"
    
        ``` py title="bubble_sort.py"
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```


-   !!! info "Code block with annotation"
    
        ``` yaml
        theme:
        features:
            - content.code.annotate # (1)
        ```

        1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
            text__, images, ... basically anything that can be written in Markdown.

-   !!! info "Code block with annotation, stripped"
    
        ``` yaml
        # (1)!
        ```

        1.  Look ma, less line noise!

-   !!! info "Code block with line numbers"
    
        ``` py linenums="1"
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```

-   !!! info "Highlighting specific lines"
    
        ``` py hl_lines="2 3"
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```

-   !!! info "Highlighting specific lines ranges"
    
        ``` py hl_lines="2-5"
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```


-   !!! info "Highlighting inline code blocks"
    
        The `#!python range()` function is used to generate a sequence of numbers.

</div>


### Admonitions

<div class="grid cards" markdown>

-   !!! info "with tooltip, inline syntax"
    
        [Hover me](https://decodedataio.github.io/ "I'm a tooltip!")


-   !!! info "Link with tooltip, reference syntax"
    
        [Hover me][Decodedata]
        [Decodedata]: https://decodedataio.github.io/ "I'm a tooltip!"


-   !!! info "Icon with tooltip"
    
        :material-information-outline:{ title="Important information" }

-   !!! info "Text with abbreviations"
    
        - The HTML specification is maintained by the W3C.
        - NACHO
        - JIM

        *[HTML]: Hyper Text Markup Language
        *[W3C]: World Wide Web Consortium

</div>


### Annotations

<div class="grid cards" markdown>

-   !!! info "Text with annotations"
    
        Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
        { .annotate } 

        1.  :man_raising_hand: I'm an annotation! I can contain `code`, __formatted
            text__, images, ... basically anything that can be expressed in Markdown.


-   !!! info "Text with nested annotations"
    
        Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
        { .annotate }

        1.  :man_raising_hand: I'm an annotation! (1)
            { .annotate }

            1.  :woman_raising_hand: I'm an annotation as well!



-   !!! info annotate "Admonition with annotations (1)"
    
        Lorem ipsum dolor sit amet, (2) consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

    1.  :man_raising_hand: I'm an annotation!
    2.  :woman_raising_hand: I'm an annotation as well!

</div>


<div class="annotate" markdown>

> Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.

</div>
1.  :man_raising_hand: I'm an annotation!
