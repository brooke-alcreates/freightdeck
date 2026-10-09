# FreightDeck — new site (test build)

Static site: no build step. Vercel serves the files as they are.

```
index.html      the whole site (Home, Pricing, About, Resources via #/pricing etc.)
favicon.svg
fonts/          Octosquares (licensed .woff2 files)
img/            hero photo, truck builder screenshot, video poster, loading animation
video/          founder video (H.264 MP4)
vercel.json     marks the test site "noindex" and caches fonts/images/video
```

## Updating the site
Edit or replace a file in GitHub and commit. Vercel redeploys automatically in under a minute.

## Notes
- The test site tells search engines not to index it (in index.html and vercel.json), so it
  won't compete with thefreightdeck.com. Remove both when this becomes the real site.
- The cost estimator calls https://app.thefreightdeck.com/api/try-quote. It prices live only
  when the page is served from a thefreightdeck.com address (e.g. beta.thefreightdeck.com)
  and the API accepts requests from that address.
- Dark mode is switched off. To turn it back on: add class="dark-mode" to the <html> tag and
  delete the <meta name="color-scheme" content="light"> line.
