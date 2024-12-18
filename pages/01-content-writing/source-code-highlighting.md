GitWiki uses [highlight.js](https://highlightjs.org/) — a JavaScript syntax highlighter library that supports over 192 languages, offers automatic language detection, and has zero dependencies.

To highlight source code use the `{.code}` tag prefix before the code block

<pre>
{: title="Example"}
```
const a = b + c;
```
</pre>

**title** attribute is optional and will be used as the title of the code block

{: title="Example"}
```
const a = b + c;
```

With out title attribute

```
const a = b + c;
```

## Examples

### JavaScript Code

<pre>
{: title="JavaScript Code"}
```
// Using require
const hljs = require('highlight.js');

// Using ES6 import syntax
import hljs from 'highlight.js';
```
</pre>

{: title="JavaScript Code"}
```
// Using require
const hljs = require('highlight.js');

// Using ES6 import syntax
import hljs from 'highlight.js';
```

### Ruby Code

<pre>
{: title="Ruby Code"}
```
# The Greeter class
class Greeter
  def initialize(name)
    @name = name.capitalize
  end

  def salute
    puts "Hello #{@name}!"
  end
end

g = Greeter.new("world")
g.salute
```
</pre>

{: title="Ruby Code"}
```
# The Greeter class
class Greeter
  def initialize(name)
    @name = name.capitalize
  end

  def salute
    puts "Hello #{@name}!"
  end
end

g = Greeter.new("world")
g.salute
```
