# Special variables reference document
## Preface
This is the feature references document, it should document params(site and frontmatter while specifying where they are applicable) and shortcodes.

## Values

Configuration Location:
- Site: This setting can only be set in the main `config.toml`.
- Fallback: This setting can be set in a page's frontmatter, or a site's main config.
- Frontmatter: This setting can only be set in a specific page's frontmatter.

### Breadcrumb configuration
Breadcrumb will list all the parent sections and home in a nav menu.

You can configure breadcrumbs with the following:
```toml
# sie config
[params.breadcrumb]
  # disable the breadcrumbs entirely
  disable = false
  # hidePages will hide pages from showing up in breadcrumb
  hidePages = false
```

```toml
# in per section's _index.md's frontmatter(fallback)
[breadcrumb]
  # title overwrites the use of default section title
  title = ""
  # hidden hides a specific section from breadcrumb
  hidden = false
```
you can use `breadcrumb.title` to shorten otherwise longer titles in breadcrumb, and `breadcrumb.hidden` to hide certain sections like home

### Taxonomy Configuration
You can configure taxonomy orders on site setting with the following
```toml
[params.taxonomy]
  order = ["series","tags"]
```
In taxonomy's frontmatter, you can configure a term's rendering
for example to change `tags`'s taxonomy, it's `./content/tags/_index.md`
```toml
# title will change what gets display as title
title = "Tags"
# hidden will stop taxonomy's term displays as nothing
taxonomy.displayBlank = true
# changes overwrite how it's displayed
taxonomy.display = ""
```
For example you could set `taxonomy.display` to be `Tagged as:` which would make it show as set

> Tagged as: #foo #bar

Setting to `displayBlank` will hide the taxonomy terms but display the values

### Section Listing
Controls if subsection are listed

TIP: you can add weights into a section's `_index.md` to adjust sorting

Site Config:
```toml
[params.listSection]
  #list enables subsection listing
  list = true
  #post enables adding latest post into subsection
  latest = true
```

Frontmatter config:

You can use this to overwrite site level config for an individual section.

`hideSections` allows you to hide a specified section, you can use the section's folder name(lowercased) to hide a section, if section path is not available for whatever reason, section's title(lowercased) will be fallback.

```toml
showSections = true
showSectionLatest = true
hideSections = []
```

### Pager control
Controls if pager button is visible
Configuration can only be done on site config

```toml
[params.pager]
  #default controls if pager will be shown by default
  default = true
#overwrite allows you to overwrite individual sections by path name
#path name will always be treated as lowercased
#"" can be used for root path
[params.pager.overwrite]
  "path/to/section" = true
  "" = false
```

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
#headingAnchor controls if headings links are shown or disabled
[params.headingAnchor]
    #hideOnList allows you to disable anchors for list
    disableOnList = false
    #hideOnList allows you to disable anchors for page
    disableOnPage = false
```

The frontmatter `showAnchor`(location: frontmatter) key will be able to overwrite it on an per page basis. This will be respected for both Page and List.

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
