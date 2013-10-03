# Scrappply

A ScraperWiki skin for the Appply theme from WooThemes

#### Compiling the .less files

To keep colour operations simple, Scrappply uses [less](http://lesscss.org) to preprocess its css files.

To compile the less files, run `./compile`.

#### Deploying to blog.scraperwiki.com

This theme has no built-in updating. You'll need to `git commit` and `git push` your changes, then SSH into blog.scraperwiki.com and run:

```
cd blog.scraperwiki.com/wp-content/themes/scrappply
./update
```

The `./update` script runs `git pull` and then clears the Varnish cache for each css and png file in the theme folder.

If you're making changes in a branch, make sure to `git checkout` the right branch before running `./update`.

#### Argh! My changes aren't showing up on blog.scraperwiki.com

The ScraperWiki blog is fronted by a Varnish cache. You can clear the cache by clicking the "Purge Varnish Cache" button on the WP Admin Dashboard. Or you can manually clear the cache for individual URLs (eg: `style.css`) by SSHing into blog.scraperwiki.com and running:

```
curl -X PURGE http://blog.scraperwiki.com/wp-content/themes/scrappply/style.css
```
