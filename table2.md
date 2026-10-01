# Table problem continued

```{list-table} Target table in article 2
:name: target-table
:header-rows: 1

* - A
  - B
* - 3
  - 4
```



```{list-table} Third table in article 1
:header-rows: 1

* - A
  - B
* - 1
  - 2
```
Reference with numref: {numref}`target-table`

Reference with Markdown syntax: [Table {number}](#target-table)

Like figures, the number is hardcoded in the text, rather than taking the number itself
**problem**  
```typst
Reference with numref: #link(<target-table>)[Table~1]

Reference with Markdown syntax: #link(<target-table>)[Table 1]
```

**fix**  
```typst
Reference with numref: #link(<target-table>)[@target-table]

Reference with Markdown syntax: #link(<target-table>)[@target-table]
```