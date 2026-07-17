# Bethel International Ministry — brand & build notes

## Brief
Lovable rebuild (CLAUDE.md §0 case B). Kuruman, Northern Cape. Real branding: deep
purple + gold. Palette `purple` in generate.py.

## Phase 1 — v1
Hero "A DWELLING PLACE / FOR GOD", scripture Zechariah 8:23, moments heading
"Preaching · Teaching · Transforming Lives".

Fixed at v1 time (before any operator feedback): the generator's default Pexels
queries returned the same mismatched stock photos already caught on the previous
build (African The Apostolic) — an all-white choir, a Spanish-language Bible, US
election-canvassing volunteers with American flags. Replaced with vetted, explicitly
Black African photography and patched `generate.py`'s default queries so future
builds don't inherit this.

## Phase 2 — real content pass (from operator's Lovable screenshots)
Old site: `ministrybethelinternational.lovable.app`. Restructured the page's IA to
match their real site's nav exactly: About · Vision · Pastor · Visit · Contact.

- **Pastor name correction**: the original brief said "Pastor Nocebs Mafu" — almost
  certainly a mis-transcription. Their real site consistently says **Nonceba Mafu**
  across multiple mentions (monogram "NM", full name x2, "Pastor Nonceba" CTA) and
  refers to her as "she/her" (Senior Pastor). Used Nonceba Mafu throughout; flagged
  the correction to the operator rather than silently overriding what they'd given.
- **Real logo**: no source file was supplied — cropped the circular gold "open door"
  crest directly out of their hero screenshot (at native 2880×1800 resolution),
  applied a circular alpha mask so it composites cleanly onto our dark background.
  Also re-cropped a favicon from the same source. If they ever send the original
  vector/source file, swap it in for a cleaner edge.
- **About** (`#about`, was "Welcome"): real "The door is open" framing, kept our
  pastor-led welcome paragraph with the corrected name.
- **Vision & Mission** (`#vision`, new section, replaced the generic "what to expect"
  cards): their real vision (3 bullets + Isaiah 57:15 / 1 John 5:4 / Zechariah 8:23)
  and mission (2 bullets + Exodus 16:23–25), plus the Preaching/Teaching/Transforming
  Lives three-card row directly below (matches how it reads on their real site — no
  section break between Vision&Mission and the pillar cards in the screenshots).
- **Pinned scripture**: replaced the short Zechariah 8:23 excerpt with their full
  real quote ("In those days ten men from every language and nation...").
- **Pastor section** (`#pastor`, new): their real bio copy, "NM" monogram card,
  "Reach out to Pastor Nonceba" CTA → Contact.
- **Contact section** (`#contact`, replaced the generic "Bring everything" CTA):
  real Call (076 632 0816), WhatsApp (073 141 0296, wired to wa.me), Email
  (mafunonceba@gmail.com) — all live links, not just display text.
- Minor fire-metaphor copy cleanup in the Give section ("Fuel the fire" →
  "Sow into the vision") since it no longer fit next to real, specific content.

## Phase 2 — photography removed entirely
The operator reviewed the live site and asked for the stock photography to come out,
specifically flagging the About-section congregation photo, and pointed at their real
Lovable site as the reference: it uses zero photos, just type + the purple/gold
palette + the crest logo, and reads as elegant that way. This is a deliberate,
church-specific departure from CLAUDE.md §7's "images mandatory" floor — the client's
own direction and reference material override the general default for this build.

- Removed hero.jpg, welcome.jpg, moment-1/2/3.jpg, visit.jpg from disk and every
  reference to them. Hero and Contact sections now run on pure gradient (existing
  `.hero-glow` radial glows + the ember canvas particle effect carry the atmosphere).
- The About section's old image slot now shows their real crest logo large, with the
  short Zechariah 8:23 quote beneath it — reinforces the brand instead of leaving a
  gap, without using a photo.
- Removed the Moments/gallery section entirely rather than replace it with a
  non-photo substitute — it doesn't exist on their real site either.
- The Pastor section was already photo-free (their real site uses an "NM" monogram
  card too, not a headshot) — no change needed there.

## Still open — nothing in the screenshots
No service times or physical address appear anywhere on their real site. Times &
Place section (`#times`) is untouched — still the original placeholder, not
confirmed either way. Do not invent; ask the operator directly if/when needed.
