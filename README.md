# FreightDeck — new site (test build)

Static site, no build step: Vercel serves these files as they are.

```
index.html        Home, plus Pricing, About and Resources (#/pricing, #/about, #/resources)
permits/ guides/ corridors/   the Resources articles, at the same addresses as the current site
privacy.html  terms.html  start/  llms.txt   carried over unchanged from the current site
assets/site.css   shared styles used by the article pages
fonts/  img/  video/
vercel.json       test-site "noindex", caching, and /pricing -> /#/pricing
```

## Updating
Edit or replace a file on GitHub and commit; Vercel redeploys automatically.
Files in fonts/, img/, video/ and assets/ are cached by browsers for a week, so give a
replacement file a new name and update the reference to it.

## Before launch
- Remove the two "noindex" settings: the robots meta tag in each page and the X-Robots-Tag in vercel.json.
- The cost estimator prices live only when served from a thefreightdeck.com address the API accepts.
- Dark mode is switched off: add class="dark-mode" to <html> and delete the color-scheme meta tag to restore it.
