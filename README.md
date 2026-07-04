# wodenburison.space

Woden Burison's link hub — a single static page in the same "handwritten field
journal" theme as [Woden's Adventures](https://wodensadventures.quest/)
(`themes/journal.css` in that repo). No build step: just `index.html` +
`style.css`.

## Editing links

Open `index.html` and look for the `<!-- LINK CARDS START -->` /
`<!-- LINK CARDS END -->` comments. Each link is one `<a class="link-card">`
block:

```html
<a class="link-card" href="https://example.com" target="_blank" rel="noopener">
  <span class="link-card-pin" aria-hidden="true"></span>
  <span class="link-card-stamp">Category</span>
  <h2 class="link-card-title">Title</h2>
  <p class="link-card-desc">One or two sentence description.</p>
  <span class="link-card-cta">Verb &rarr;</span>
</a>
```

Add, remove, or reorder these freely — nothing else in the page needs to
change. The trailing `.link-card--ghost` div is decorative ("more coming"); it
can remain in place indefinitely.

## Publishing

This repo is served directly by GitHub Pages from the `main` branch root —
there's no `docs/` folder or build step. Just commit and push:

```
git add -A
git commit -m "Update links"
git push
```

Custom domain is `wodenburison.space`, set via the `CNAME` file in this repo's
root plus DNS records at the registrar (A records to GitHub Pages' IPs, or a
CNAME/ALIAS record depending on what the registrar supports for an apex
domain).
