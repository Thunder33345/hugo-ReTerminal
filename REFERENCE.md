# Special variables reference document
## Preface
This is the feature references document, it should document params(site and frontmatter while specifying where they are applicable) and shortcodes.

## Values

Configuration Location:
- Site: This setting can only be set in the main `config.toml`.
- Fallback: This setting can be set in a page's frontmatter, or a site's main config.
- Frontmatter: This setting can only be set in a specific page's frontmatter.

### Meta Indexing control
By default, site will allow indexing when it's built in production, otherwise it uses noindex meta tags.
You can configure this to tell search engine to not index your page by configuring the parameters below.

Below shows the default value for all parameters. Location: Fallback
```toml
#metaRobots allows you to control the meta robots directive
[params.metaRobots]
  #assumeProduction will allow indexing, even when hugo.IsProduction is false
  assumeProduction = false
  #forceNoindex will disable indexing forcefully on all pages
  #all pages will have noindex set and it cannot be overwritten
  forceNoindex = false
  #disableAutoIndex will set pages to noindex by default, instead of allowing index by default
  #can be overwritten by a page's "noindex" parameter
  disableAutoIndex = false
  #indexValue is what to emit, if indexing is allowed
  #empty will stop it from emitting entirely
  #this is only useful if you want a custom directive instead of nothing
  indexValue = ""
  #noindexValue is what to emit, if indexing is not allowed
  noindexValue = "noindex, nofollow"
```
For other valid `indexValue`/`noindexValue` see [Google Developers](https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag)

The frontmatter parameter `noindex`(location: frontmatter) will allow individual page to control if indexing is wanted.

Defaults to unset which will follow site default configuration.

Setting to false will allow index(useful for when `disableAutoIndex` is true), will not overwrite `forceNoindex`.
Setting it true will disallow index of the specific page.

### Heading Anchors
Headings on pages content and listing content are anchored by default, on list and on individual pages. Listing entries's content are intentionally not anchored.

Below shows the default values of each params
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
