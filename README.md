# abe-sitemap

> plugin to generate sitemap.xml

```shell
abe add https://github.com/AdFabConnect/abe-sitemap.git
```

# config

```json
	"sitemap": {
  	"domain": "http://localhost:8000/",
  	"sitemapName": "index_sitemap.xml",
  	"priorities": {
  		"article": "0.5"
  	},
  	"folders": {
  		"regex": "^\/([a-zA-z-]*?)\/",
  		"sitemapName": "directory-sitemap-$1.xml"
  	}
  }
```

Mandatory config:

- domain

Optional config:
- sitemapName (change default sitemap.xml name)
- priorities (key/value = template name/priority number)
- folders (to split sitemap into multiple files)
	- regex (the regex to extract folder)
	- sitemapName (name with "$1" to replace with folder name for example)