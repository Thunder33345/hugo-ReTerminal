# Special variables reference document
## Preface
This is the feature references document, it should document params(site and frontmatter while specifying where they are applicable) and shortcodes.

## Values

### Heading Anchors
Headings on pages content and listing content are anchored by default, on list and on individual pages. Listing entries's content are intentionally not anchored.

Bellow shows the default values of each params
```toml
[params.anchor]
    #hideOnList allows you to disable anchors for list
    hideOnList = false
    #hideOnList allows you to disable anchors for page
    hideOnPage = false
```

The frontmatter `showAnchor` key will be able to overwrite it on an per page basis. This will be respected for both Page and List.

## Shortcode

## Vanilla

### Frame
List and Home pages can optionally have a frame around the post to stand out. You can do this by setting the `framed` key to true in front matter.

This is only for List and Home, individual pages are not supported.
```yaml
framed: false
```

TODO: document vanilla terminal features for future references
List of default frontmatter keys:
author
authorTwitter
cover
keywords
showFullContent
readingTime
hideComments
Toc
TocTitle

## Builtin
Commons: title, date, lastmod, tags, description
[See More](https://gohugo.io/content-management/front-matter/#front-matter-cascade)
