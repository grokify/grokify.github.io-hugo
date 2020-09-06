# Grokify Web Site

## Deployment Guide

### Initialize Hugo

```
$ brew install hugo
$ hugo new site <sitename>
```

```
Congratulations! Your new Hugo site is created in /path/to/grokify.

Just a few more steps and you're ready to go:

1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/ or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

Visit https://gohugo.io/ for quickstart guide and full documentation
```

### Add Theme

```
$ git init
$ git submodule add https://github.com/chipzoller/hugo-clarity themes/hugo-clarity
$ cp -a themes/hugo-clarity/exampleSite/* .
```

### Add Disqus

`config.toml`

```
publishdir = "docs"
disqusShortname = "grokify"
```

`themes/hugo-clarity/layouts/_default/single.html`

```
    {{ template "_internal/disqus.html" . }}
```

### Add Menu

`data/menu.yaml`