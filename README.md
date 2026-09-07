# Crescendo

A single-file search tool for music business students: it surfaces a curated set of trusted music-industry publishers (with academic literature available as an opt-in extra), then builds ready-to-use Harvard references and quote citations.

Built by **[Jack Abraham](https://jackabraham.studio)** — [GitHub](https://github.com/Jackalackalack) · [LinkedIn](https://www.linkedin.com/in/jackcabraham/)

## What it does

1. Google-style homepage with a single search bar and rotating example prompts (e.g. "demographic data for dance music audiences in the UK").
2. Lists all 30 curated music-industry sources — UK & global trade bodies, data & analyst firms, general trade press, dance/electronic press, live & touring, and rights/platforms — each with a one-click "search this source" link (opens a Google site-search in a new tab) and a category filter to narrow the list.
3. A "Cite an article from here" button opens a small form: paste in the author/org, year, title and URL of whatever you found via the search link, optionally paste a quote too, and it generates a fully formatted Harvard reference (and, if you added a quote, an in-text citation plus a copy-ready block for pasting into an essay).
4. Academic literature search (via the free Crossref API, with a client-side relevance filter to cut down on off-topic results) is available as an opt-in toggle — off by default to keep results focused.
5. Toggle between a single interleaved feed or a split view, and sort academic results by relevance or publication date.
6. Keeps a running, alphabetised reading list/bibliography that can be edited (items can be removed) and copied in one click.

## How it's built

Everything lives in one self-contained file, `crescendo-search.html` (or `index.html` once deployed) — no build step, no install, no server. It runs entirely in the browser and calls the free, key-free Crossref API directly from client-side JavaScript.

Two earlier features — auto-matching a live article per industry source, and a second academic source — were removed after live testing showed the APIs behind them (GDELT and Semantic Scholar) don't send CORS headers permitting browser-side fetches from another origin, so those calls silently failed 100% of the time in a real browser. Rather than ship dead functionality, the tool now relies only on APIs confirmed to work client-side (Crossref), plus the manual citation/quote-capture flow for industry sources.

## Running it

Open `crescendo-search.html` (or the deployed `index.html`) in any modern browser. An internet connection is needed for live Crossref search results.

## License

MIT — see [LICENSE](LICENSE). Free to use, modify and share, including for teaching and coursework; just keep the copyright notice attached to any copies.
