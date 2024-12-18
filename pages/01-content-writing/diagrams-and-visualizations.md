
GitWiki uses [Mermaid](https://mermaid.js.org/) — a JavaScript-based tool for creating diagrams and visualizations using text and code. It dynamically renders Markdown-inspired text definitions into various types of diagrams and charts.

To create a diagram use the **`{.mermaid}`** tag prefix before the code block

<pre>
{.mermaid}
```
your code goes here
```
</pre>

## Examples

### Flowchart

<pre>
{.mermaid}
```
graph TD
    A-->B
    A-->C
    B-->D
    C-->D
```
</pre>

{.mermaid}
```
graph TD
    A-->B
    A-->C
    B-->D
    C-->D
```

### Pie Chart

<pre>
{.mermaid}
```
pie title NETFLIX
         "Time spent looking for movie" : 90
         "Time spent watching it" : 10
```
</pre>


{.mermaid}
```
pie title NETFLIX
         "Time spent looking for movie" : 90
         "Time spent watching it" : 10
```

### More Examples

Refer to the [Mermaid Documentation](https://mermaid.js.org/syntax.html) for examples.
