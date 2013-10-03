# Scrappply

A ScraperWiki skin for the Appply theme from WooThemes

#### Compiling the .less files

To compile `scrappply.less` run: `lessc scrappply.less scrappply.css`

#### Deploying to blog.scraperwiki.com

This theme has no built-in updating. You'll need to `git commit` and `git push` your changes, then SSH into blog.scraperwiki.com and run:

```
cd blog.scraperwiki.com/wp-content/themes/scrappply
git pull
```

If you're making changes in a branch, make sure to `git checkout` the right branch before pulling.

#### Argh! My changes aren't showing up on blog.scraperwiki.com

The ScraperWiki blog is fronted by a Varnish cache. You can clear the cache by clicking the "Purge Varnish Cache" button on the WP Admin Dashboard. Or you can manually clear the cache for individual URLs (eg: `style.css`) by SSHing into blog.scraperwiki.com and running:

```
curl -X PURGE http://blog.scraperwiki.com/wp-content/themes/scrappply/style.css
```
