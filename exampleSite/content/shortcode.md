+++
title = "Shortcode Showcase"
date = "2019-07-18"
author = "Thunder"
toc = true
+++

foo bar

## Built in
figure
{{< figure src="/img/hello.jpg" link="/" alt="A toy character standing on a wooden surface." title="title" caption="caption" width="500" attr="terminal theme">}}

gist
{{< gist spf13 7896402 >}}

highlight
{{< highlight html "linenos=table,hl_lines=1 4-7,linenostart=199" >}}
<section id="main">
  <div>
   <h1 id="title">{{ .Title }}</h1>
    {{ range .Pages }}
        {{ .Render "summary"}}
    {{ end }}
  </div>
</section>
{{< /highlight >}}
codeblock
```html
<section id="main">
  <div>
   <h1 id="title">{{ .Title }}</h1>
    {{ range .Pages }}
        {{ .Render "summary"}}
    {{ end }}
  </div>
</section>
```
------
## Reterminal

details
{{<details "Lorem _ipsum_ __dolor__">}}
Lorem ipsum _dolor sit amet_, consectetur ~~adipiscing elit~~. Proin luctus, est eget mollis imperdiet, urna purus blandit leo, non tempor.
{{</details>}}

framed

{{<framed>}}
Lorem ipsum *dolor sit amet*, **consectetur adipiscing elit**. Integer ~~consectetur nec augue~~ tristique venenatis. In viverra risus quam. Suspendisse odio.
{{</framed>}}

link {{<link href="https://example.com">}}foobar{{</link>}}

noop

{{<noop>}}
noop, this wont be shown!
{{</noop>}}

outline

{{<outline>}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque ut luctus ex, eget ullamcorper est. Proin rhoncus massa nec arcu facilisis, id lacinia enim viverra. Curabitur pretium non libero id ullamcorper. Aenean tempor dui ac.
{{</outline>}}

outline with heading

{{<outline "Warning!!" "Use this __with great care__!">}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque ut luctus ex, eget ullamcorper est. Proin rhoncus massa nec arcu facilisis, id lacinia enim viverra. Curabitur pretium non libero id ullamcorper. Aenean tempor dui ac.
{{</outline>}}

some filler text

Sub and Sup script

Foo{{<sub>}}ba{{</sub>}}{{<sup>}}r{{</sup>}}

Underline(u) & Highlight(Mark)

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. {{<u>}}Proin ut bibendum ante{{</u>}}. Maecenas imperdiet diam ut nisl egestas pharetra et nec nulla. Nam nec sagittis odio, id bibendum justo. {{<mark>}}Vivamus lacinia ligula id ante egestas lobortis{{</mark>}}. Vivamus iaculis, enim non.



------
## Terminal
foo

image:
{{< image src="/img/hello.jpg" alt="Hello Friend" position="center" style="border-radius: 8px;" >}}
bar
{{< tfigure src="/img/hello.jpg" alt="Hello Friend" position="left" style="border-radius: 8px;" caption="Hello Friend!" captionPosition="center" captionStyle="color: red;" >}}
baz
{{< code language="css" title="Really cool snippet" id="1" expand="Show" collapse="Hide" isCollapsed="true" >}}
pre {
  background: #1a1a1d;
  padding: 20px;
  border-radius: 8px;
  font-size: 1rem;
  overflow: auto;

  @media (--phone) {
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  code {
    background: none !important;
    color: #ccc;
    padding: 0;
    font-size: inherit;
  }
}
{{< /code >}}

