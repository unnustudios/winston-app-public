# winston-app-public

The public pages for **Winston**, an iOS goal tracker: the marketing page, the support page
and the privacy policy that the App Store listing links to.

| Page | File | Purpose |
|---|---|---|
| Marketing | [`index.html`](index.html) | The marketing URL in App Store Connect |
| Support | [`support.html`](support.html) | The support URL in App Store Connect |
| Privacy policy | [`privacy.html`](privacy.html) | The privacy policy URL, which is not waivable |

The app itself is developed in a separate, private repository. This one exists only so those
URLs can be served publicly without the source being public with them.

## Why it is a separate repo

GitHub Pages publishes either the repository root or a `/docs` folder, and only from a public
repository unless you pay for it. Serving these pages from the app's own repo would have meant
either making the source public or publishing a folder that holds internal notes. A repo
containing nothing but the two pages avoids both.

## How it is served

GitHub Pages, from the root of the default branch. Plain HTML and one stylesheet: no Jekyll (hence
`.nojekyll`), no build step, no framework, and nothing fetched from anywhere else, so the pages
load quickly and completely even on a poor connection.

Once Pages is enabled the URLs are:

- `https://unnustudios.github.io/winston-app-public/` — marketing
- `https://unnustudios.github.io/winston-app-public/support.html` — support
- `https://unnustudios.github.io/winston-app-public/privacy.html` — privacy policy

## Changing the policy

The privacy policy describes what the app actually does, and the App Store privacy label describes
the same facts in a different place. **They have to agree**, so the policy is not edited on its own.
It changes when the app's data handling changes, and the date at the top of the page changes with
it.
