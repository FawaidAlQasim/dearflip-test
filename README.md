# DearFlip trial build — for evaluation only

This is the **official free Lite version** of DearFlip, cloned directly from
their public repo (`github.com/dearhive/dearflip-js-flipbook`), so what
you're testing is the real thing, not a recreation.

## Important limitation before you test

The Lite version on GitHub is **v1.7** — DearHive's own README says this
is "old version... commercial version is 2.x." So:

- This is genuinely useful for judging the core experience: RTL, layout,
  general feel, whether the 3D page-turn looks good for a religious text.
- It is **not** a perfect preview of what you'd get if you paid — the
  current v2.x commercial version has had years of improvements since v1.7
  that this trial simply doesn't include. Some rough edges you might hit
  here (fonts, an animation quirk, a control that behaves oddly) may
  already be fixed in the version you'd actually be buying.
- The license (CC BY-NC-ND) explicitly permits this kind of testing/trial
  use — see the LICENSE file included in `dflip/`.

## How to test it

1. Put a copy of your PDF in this same folder, named `book.pdf` (or edit
   the `source="book.pdf"` attribute in `index.html` to point at a
   different filename/URL).
2. Upload this whole folder (`index.html` + the `dflip/` folder) to GitHub
   Pages — either as a new folder in your existing repo (e.g.
   `yourrepo/dearflip-test/`) or as a totally separate test repo, so it
   doesn't interfere with your current custom build.
3. Visit the page. It should auto-detect RTL from the `direction` option
   set in the script (no PDF metadata detection needed, unlike our custom
   build — you tell it directly).

## What to specifically compare against our custom build

- **RTL binding** — does the book open on the right and flip the correct
  direction, out of the box?
- **Click/swipe direction** — tap/swipe both halves of the book; DearFlip
  handles this natively, so if it's correct here with zero extra code,
  that's exactly the pain point our custom build had to hand-solve.
- **Large PDF performance** — test with your actual 1124-page book. DearFlip
  advertises automatic partial/lazy loading; watch whether it noticeably
  loads faster than "render everything" would, and whether flipping through
  hundreds of pages stays smooth.
- **Mobile behavior** — rotate the phone, try fullscreen, lock/unlock the
  screen mid-session — the exact three things that gave us the most trouble
  in the custom build.
- **Table of contents** — click the outline/bookmark toolbar button; it
  should read the PDF's own bookmarks automatically.
- **Visual fit** — the theming here is minimal (just a dark green
  background matching your site's palette via `backgroundColor` and
  `dir="rtl"` for the surrounding page). If you like the underlying
  experience, visual polish is a separate, smaller task from the RTL/
  performance/mobile fundamentals this trial is really testing.

## If you decide to purchase

Everything in this test folder (`index.html`, your Arabic UI text
translations, the option settings) carries over directly — you'd just swap
the `dflip/` folder for the licensed v2.x version's files and keep
everything else as-is.
