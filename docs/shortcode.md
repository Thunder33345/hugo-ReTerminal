# Shortcode Document
This page documents all custom shortcodes.

## Page elements
These shortcode are use to create content on pages

### Code
**`code`** (props required: **`language`**; props optional: **`title`**, **`id`**, **`expand`** (default "△"), **`collapse`** (default "▽"), **`isCollapsed`**)
e.g.
```go
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
```
### Details
Details can be use to create a spoiler box(forum style)

```md
{{<details "Lorem _ipsum_ __dolor__">}}
Lorem ipsum _dolor sit amet_, consectetur ~~adipiscing elit~~. Proin luctus, est eget mollis imperdiet, urna purus blandit leo, non tempor.
{{</details>}}
```

### Framed
Framed takes in markdown content and create a box framed text

```md
{{<framed>}}
Lorem ipsum *dolor sit amet*, **consectetur adipiscing elit**. Integer ~~consectetur nec augue~~ tristique venenatis. In viverra risus quam. Suspendisse odio.
{{</framed>}}
```

### Image
**`image`** (props required: **`src`**; props optional: **`alt`**, **`position`** (**left** is default | center | right), **`style`**)
e.g.
```go
{{< image src="/img/hello.png" alt="Hello Friend" position="center" style="border-radius: 8px;" >}}
```

### Link

### Outline
Outline helps you draw a bubble that calls to user's attention

The first arg is heading, and second is subtitle
{{<outline "Warning!!" "Use this __with great care__!">}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque ut luctus ex, eget ullamcorper est. Proin rhoncus massa nec arcu facilisis, id lacinia enim viverra. Curabitur pretium non libero id ullamcorper. Aenean tempor dui ac.
{{</outline>}}


### prismjs

### tfigure

the old terminal's `figure` shortcode
**`tfigure`** (same as `image`, plus few optional props: **`caption`**, **`captionPosition`** (left | **center** is default | right), **`captionStyle`**)
e.g.
```go
{{< figure src="/img/hello.png" alt="Hello Friend" position="center" style="border-radius: 8px;" caption="Hello Friend!" captionPosition="right" captionStyle="color: red;" >}}
```
## Formatting
These shortcode mainly serve as text formatting.

Normally they hold minimal logic and simply emit the given text in wrapped with the relevant html element.

## Mark
Mark highlights given text
```md
{{<mark>}}Text{{</mark>}}
```

## sub
Puts the given text in subscript

## sup
Puts the given text in superscript

## u
Underline given text
