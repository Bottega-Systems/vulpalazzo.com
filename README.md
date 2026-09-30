# vulpalazzo.com

The landing page for **Vulpalazzo**, a game by Bottega Systems. One static page,
served by GitHub Pages. No build step, no framework, no cookies, no tracking.

**Treat this repository as public, whatever its setting says** — everything in it
is served to the whole internet the moment it is deployed. It holds only what the
page shows: approved copy, the fox mark, and screenshots the Marquee has signed
off. **Nothing from the game's private repository goes here** — above all nothing
from `assets/imagine_raw/`.

## The rules that keep it one page

It was approved on 2026-09-22 as a one-off, with bounds. They are the scope:

- **One static page.** No CMS, blog, accounts, e-commerce or tracking.
- **Live on this page means approved** *(the Owner, 2026-09-30; this replaced "the copy
  is the store page's, word for word")*. The page is the company's source of what its
  customers should know. **The Barker drafts posts from what's live here**, so every post
  starts from signed-off copy, and months later the same material comes back with new
  screenshots and new wording. It never gives away story secrets. The Steam page's copy
  (`docs/STEAM_PAGE.md` in the game's repository) is kept consistent with it.
- **Every change is previewed privately first.** Before a pull request, the page is
  published as a private Claude page (the preview:
  https://claude.ai/artifact/GKGumjEkmu6a2vjXXTtdhA). The Owner looks at it on his phone
  and shares it with friends by link. Only what he likes becomes a pull request, and
  **merging it publishes it.** Nothing public is ever used as a scratchpad.
- **No email signup form** until the company has a marketing email service, a PO
  box address for the footer, and unsubscribe handling. The form is the front
  door of that plan, so it arrives with it.
- **No trailer** until one exists.
- **Safe for work.** The rating (Mature: suggestive, never explicit) is stated in words, never shown. *(Was "adults only" until 2026-09-25, when the copy caught up with the 2026-09-14 Mature decision.)*
- The game's accessibility rules apply: colour is never the only signal, every
  image has alt text, text stays readable.

**If it ever needs to grow past one page, that is the day it gets its own seat.**

## Three things on the page that can go stale

- **`96.46%`**: Classic's return to player at the default bet, `documented_rtp` in the
  game repo's `data/machines/floor_classic.json`, measured by `rtp_sim` over 400,000
  spins; CI re-runs it **weekly** (it was nightly until 2026-09-26). **If the maths moves,
  this number and that sentence change, here and in `STEAM_PAGE.md`, the same day.** A
  published figure that is no longer true is worse than no figure: the whole pitch is
  that the numbers are measured. *(It said 96.53%, four million spins and "every build"
  until 2026-09-30, three errors the Barker had already fixed on the Steam page.)*
- **The Bluesky links** point at `@vulpalazzo.com` — the handle moved from
  `vulpalazzo.bsky.social` on 2026-09-23, verified by the account's permanent id. If
  the handle ever changes again, update both links (hero and footer).
- **The AI disclosure** in the footer mirrors the Steam page's required disclosure.
  **It must stay true** — if the pipeline changes, it changes.

## Screenshots

The screenshots section is in `index.html` with the `hidden` attribute, and stays
hidden until real ones exist — an empty grid is worse than none. When the Marquee's
set lands: put the images in `shots/`, add one `<figure>` per image **with real alt
text**, remove `hidden`.

**The link-preview card is `og.png`** (1200×630): the fox mark, the wordmark and
the approved hook line, drawn with the game's own Cinzel and Barlow files. A
screenshot can replace it later; keep it 1200×630 and keep its `og:image:alt` true.

**"Coming to Steam" is deliberately not a button** — it did nothing, so it no
longer looks clickable. **The day the Steam page exists, it becomes the wishlist
link** and gets the filled gold button back.

## Fonts

Cinzel and Barlow, both SIL Open Font Licence, loaded from Google Fonts (which sets
no cookies). They can be self-hosted if that ever matters. **The game's 14-segment
LED font must never be used here** — it is commercially licensed for the software
only.

## Deploying

GitHub Pages from `main`, root folder, custom domain `vulpalazzo.com` (the `CNAME`
file). DNS at Namecheap: four A records on `@` to GitHub's Pages addresses, and a
`www` CNAME to `bottega-systems.github.io`. **The MX, SPF, DKIM and DMARC records
belong to the company's email and must never be touched when changing the site.**

© 2026 Bottega Systems. The site's content is not open source.
