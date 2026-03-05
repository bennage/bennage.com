# bennage.com

The official and very serious website of the Bennage family.

A single-page static site hosted on [GitHub Pages](https://pages.github.com/).

## Local Development

No build tools needed. Just open `index.html` in a browser:

```sh
# macOS
open index.html

# Windows
start index.html

# or use any local server
python -m http.server 8000
npx serve .
```

## Adding Photos

1. Drop your photos into the `images/` directory
2. Edit `index.html` — replace the `src="images/placeholder-N.svg"` with your image filenames
3. Update the `alt` text to describe each photo
4. Optionally update the `<figcaption>` with a funny caption

**Tip:** For best results, optimize images before committing (aim for < 500KB each). Tools like [Squoosh](https://squoosh.app/) work great.