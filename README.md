
# Hugo Atom Feed

This is a fork of [Kausal Modi's `hugo-atom-feed` theme](https://github.com/kaushalmodi/hugo-atom-feed) which makes a few changes to work better for my uses. In nearly all cases, you should use the original theme and not this fork. **This is not a standalone Hugo theme, this is a Hugo theme component which works alongside another theme.**


## What's changed in this fork

  1. The ATOM feed pathname has changed from `<DIR>/atom.xml` to `<DIR>/feed.xml`. This is part personal preference, and part to match the path for my previous Jekyll blog

  2. The ATOM feed title has changed from `<PAGE-TITLE> on <SITE-TITLE>` to `<PAGE-TITLE> | <SITE-TITLE>`. The "on" just doesn't work for my site name

  3. All regular pages are included in feeds, not just those from sections in `.Site.Params.mainpages`

  4. The `utm_source` query parameter is not added to permalinks

  5. A `<blockquote>` element with the page description is not added before the content in the feed


## Usage

To enable ATOM feeds for your site:

  1. Add this theme as a submodule to your Hugo site repo:

     ```bash
     git submodule add https://github.com/rowanmanning/hugo-atom-feed.git themes/atom-feed
     ```

  2. Add the theme to your site's config file (examples in TOML/YAML):

     ```toml
     theme = ["atom-feed", "YOUR-THEME"]
     ```

     ```yaml
     theme: ["atom-feed", "YOUR-THEME"]
     ```

  3. Add "ATOM" to all of the page kinds in your site's config file (examples in TOML/YAML):

     ```toml
     [outputs]
       home = ["HTML", "ATOM"]      # Default is ["HTML", "RSS"]
       section = ["HTML", "ATOM"]   # Default is ["HTML", "RSS"]
       taxonomy = ["HTML", "ATOM"]  # Default is ["HTML", "RSS"]
     ```

     ```yaml
     outputs:
       home: ["HTML", "ATOM"]      # Default is ["HTML", "RSS"]
       section: ["HTML", "ATOM"]   # Default is ["HTML", "RSS"]
       taxonomy: ["HTML", "ATOM"]  # Default is ["HTML", "RSS"]
     ```

[See the original README for more usage instructions](https://github.com/kaushalmodi/hugo-atom-feed#readme).
