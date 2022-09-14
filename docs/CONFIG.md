
# Configuration File

This contain the full theme config file prefilled with default values
See [REFERENCE.md](./REFERENCE.md) for more detail

```toml
baseurl = "/"
languageCode = "en-us"
theme = "terminal"
paginate = 5

[params]
  # dir name of your main content (default is `content/posts`).
  # the list of set content will show up on your index page (baseurl).
  contentTypeName = "posts"

  # ["orange", "blue", "red", "green", "pink"]
  themeColor = "orange"

  # if you set this to 0, only submenu trigger will be visible
  showMenuItems = 2

  # show selector to switch language
  showLanguageSelector = false

  # set theme to full screen width
  fullWidthTheme = false

  # center theme with default width
  centerTheme = false

  # if your resource directory contains an image called `cover.(jpg|png|webp)`,
  # then the file will be used as a cover automatically.
  # With this option you don't have to put the `cover` param in a front-matter.
  autoCover = true

  # set post to show the last updated
  # If you use git, you can set `enableGitInfo` to `true` and then post will automatically get the last updated
  showLastUpdated = false

  # set a custom favicon (default is a `themeColor` square)
  # favicon = "favicon.ico"

  # Provide a string as a prefix for the last update date. By default, it looks like this: 2020-xx-xx [Updated: 2020-xx-xx] :: Author
  # updatedDatePrefix = "Updated"

  # set all headings to their default size (depending on browser settings)
  # oneHeadingSize = true # default

  # whether to show a page's estimated reading time
  # readingTime = false # default

  # whether to show a table of contents
  # can be overridden in a page's front-matter
  # Toc = false # default

  # set title for the table of contents
  # can be overridden in a page's front-matter
  # TocTitle = "Table of Contents" # default

  #set a theme color for your website
  #metaThemeColor = "#000000"

[params.anchor]
    #hideOnList allows you to disable anchors for list
    hideOnList = false
    #hideOnList allows you to disable anchors for page
    hideOnPage = false

[params.twitter]
  # set Twitter handles for Twitter cards
  # see https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started#card-and-content-attribution
  # do not include @
  creator = ""
  site = ""

#headingAnchor controls if headings links are shown or disabled
[params.headingAnchor]
    #hideOnList allows you to disable anchors for list
    disableOnList = false
    #hideOnList allows you to disable anchors for page
    disableOnPage = false

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

[params.pager]
  #default controls if pager will be shown by default
  default = true
#overwrite allows you to overwrite individual sections by path name
[params.pager.overwrite]
  "path/to/section" = true
  "" = false

[params.listSection]
  #list enables section listing
  list = true
  #post enables adding latest post into section
  latest = true

[languages]
  [languages.en]
    languageName = "English"
    title = "Terminal"
    subtitle = "A simple, retro theme for Hugo"
    owner = ""
    keywords = ""
    copyright = ""
    menuMore = "Show more"
    readMore = "Read more"
    readOtherPosts = "Read other posts"
    newerPosts = "Newer posts"
    olderPosts = "Older posts"
    missingContentMessage = "Page not found..."
    missingBackButtonLabel = "Back to home page"

    [languages.en.params.logo]
      logoText = "Terminal"
      logoHomeLink = "/"

    [languages.en.menu]
      [[languages.en.menu.main]]
        identifier = "about"
        name = "About"
        url = "/about"
      [[languages.en.menu.main]]
        identifier = "showcase"
        name = "Showcase"
        url = "/showcase"
```

to `config.toml` file in your Hugo root directory and change params fields. In case you need, here's [a YAML version](https://gist.github.com/panr/9eeea6f595c257febdadc11763e3a6d1).

**NOTE:** Please keep in mind that currently `main menu` doesn't support nesting.
