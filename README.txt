YOINK — the site
================

One file. Drop the folder on Vercel / Netlify / GitHub Pages and it works.

  index.html    the whole site
  og.png        the social card (referenced as /og.png)
  vercel.json   two security headers, nothing else

WHEN THE TOKEN IS LIVE
----------------------
Open index.html, find CONFIG near the bottom, and fill in:

  ca:      '0x...'                       the contract address
  swap:    'https://.../swap?token='     the swap, with the address appended
  swapUrl: ''                            or a full URL instead of the above
  pool:    ''                            optional, skips the lookup
  explorer:'https://...'                 optional
  x:       'https://x.com/...'           optional

That is the only edit. The address bar, every SWAP button, the pool lookup,
the price stats and the GeckoTerminal chart all read from it.

IF VERCEL SHOWS 404
-------------------
The file in the repository root must be named exactly index.html.
Chrome sometimes downloads it as index_1.html — rename it in the GitHub UI.
