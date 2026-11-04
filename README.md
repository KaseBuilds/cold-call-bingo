# ☎️ Cold Call Bingo

Bingo for SDRs. Tap the squares as your cold calls go sideways. Five in a row wins.

Made by an SDR, for SDRs.

## Play

**Play free:** https://kasebuilds.github.io/cold-call-bingo/

- A fresh card every time you tap **New card**, drawn from a pool of real cold-calling moments
- Tap a square when it happens to you
- Get five in a row for BINGO, confetti and a shareable image of your winning card
- Got a cursed cold-call moment? **Submit a square.** The best ones join the game with your first name on them.

## Run a team "Bingo Friday"

Share the link before a call blitz. Everyone plays their own card. The first to post their BINGO image in the team channel wins coffee.

## How it's built

One self-contained `index.html`. No build step, no framework, no tracking beyond optional page counts. Your card is saved only in your own browser.

## Setup notes (for the maintainer)

All settings are at the top of the `<script>` in `index.html`:

| Setting | What it does |
|---|---|
| `SITE_URL` | Printed at the bottom of every share image, e.g. `kasebuilds.github.io/cold-call-bingo` |
| `FORM_ACTION`, `FORM_SQUARE_FIELD`, `FORM_NAME_FIELD` | Connect "Submit a square" to a Google Form so submissions land in a sheet |
| `COMMUNITY` | Approved community squares, with first-name credit |

**Hooking up the Google Form:** make a form with two short-answer questions ("Your square", "First name"). Click ⋮ → *Get pre-filled link*, fill both with test text, copy the link. The `entry.NNNN` numbers in it are your field IDs. Take the form's URL, swap `/viewform` for `/formResponse`, and that's `FORM_ACTION`.

**Page counts (optional):** sign up free at goatcounter.com, then paste its one-line script where `index.html` says `ANALYTICS`.

## License

MIT. Fork it, remix the squares for your team.
