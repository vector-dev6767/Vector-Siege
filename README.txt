VECTOR SIEGE — ready-to-upload website
======================================

Two files. No build step, no dependencies, no server code.

  index.html   the landing page
  play.html    the game

index.html links to play.html with a relative path, so as long as the two
files sit in the same folder, everything works.


HOW TO GET A URL WITHOUT "claude" IN IT
---------------------------------------

Option 1 — Netlify Drop  (fastest, no account needed to start)
  1. Go to  app.netlify.com/drop
  2. Drag this whole folder onto the page
  3. You get a URL instantly, e.g.  merry-otter-8fa21c.netlify.app
  4. Free account lets you rename it to  vector-siege.netlify.app

Option 2 — GitHub Pages  (free, permanent, your own name in the URL)
  1. Make a repo called  vector-siege
  2. Upload index.html and play.html
  3. Settings -> Pages -> Source: main branch, / (root)
  4. Live at  yourname.github.io/vector-siege

Option 3 — itch.io  (best if you want players to find it)
  1. Zip index.html + play.html together
  2. itch.io -> Upload new project
  3. Kind of project: HTML
  4. Tick "This file will be played in the browser"
  5. Live at  yourname.itch.io/vector-siege

Option 4 — your own domain
  Buy a domain (~$10/yr) and point it at any of the above.
  Netlify and GitHub Pages both support custom domains for free,
  with HTTPS included automatically.


NOTES
-----

* Every option above serves over HTTPS by default.

* The game is fully offline-capable — no network requests at all.
  You can also just double-click play.html to play it locally.

* index.html loads two fonts from Google Fonts. If you want the landing
  page to work with no internet either, delete the <link> tag near the
  top of index.html; it falls back to system fonts automatically.

* Save data (coins, upgrades, skins, high score) lives in the browser's
  localStorage and is tied to the domain. Moving to a new URL starts
  players fresh — that's expected.

* Admin code: VectorSiegeW  (bottom-left of the home screen)
