# `site`

The pages that have to be reachable from the public web: a short page about
the app and the privacy policy Google Play requires on the listing.

| File | What |
|---|---|
| `index.html` | What Wibblewall is, in a few lines, with links to the policy. |
| `privacy/index.html` | The privacy policy, English and Russian on one page. **The policy's source of truth.** |
| `wobblo.png` | The icon, 256 px, from `tool/art/build_art.py` — redrawn with the rest of the art. |

**Published from its own public repository**, `jqdevAM/wobblo-site`, as
pin16 and tintora do with theirs: GitHub Pages serves everything in the
repository it is turned on for, and this one holds the code and its docs.

To publish or update:

1. Copy everything in `site/` into the root of `wobblo-site`.
2. There: Settings → Pages → Deploy from a branch → `main`, folder `/` (root).
3. The pages are then at
   - https://jqdevam.github.io/wobblo-site/ and
   - https://jqdevam.github.io/wobblo-site/privacy/ — the URL Play Console
     asks for.

The developer page at https://jqdevam.github.io/ (repository
`jqdevAM.github.io`) has a card for Wibblewall linking to both.

**Keep the policy in step with the app.** Every sentence in it is a claim
about behaviour: what is stored, what leaves the phone, what the app asks the
phone for. Today the claims are that the app stores only the choices listed,
that its own code sends nothing anywhere, and that the one thing online is
the Yandex ad banner at the bottom of the list of wallpapers — asked about
first, personalised only if allowed — with the permissions it brings
(internet, network state, advertising ID, install referrer; the release
script refuses any other). Adding a permission, an SDK, or anything else that
goes online means changing the policy first. When it changes, change the
date at the top of both languages.
