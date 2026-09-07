# Crescendo

A single-file search tool for music business students: it searches a curated set of trusted music-industry publishers (with academic literature available as an opt-in extra), then builds ready-to-use Harvard references and quote citations.

Built by **[Jack Abraham](https://jackabraham.studio)** — [GitHub](https://github.com/Jackalackalack) · [LinkedIn](https://www.linkedin.com/in/jackcabraham/)

## What it does

1. Google-style homepage with a single search bar and rotating example prompts (e.g. "demographic data for dance music audiences in the UK").
2. Surfaces a likely matching article from each of 30 curated music-industry sources — UK & global trade bodies, data & analyst firms, general trade press, dance/electronic press, live & touring, and rights/platforms — via the free GDELT news index, with a one-click "search this source for other results" link and a category filter to narrow the list.
3. Academic literature (Semantic Scholar + Crossref, with an off-topic-result filter) is available as an opt-in toggle for when a proper lit review is needed — off by default to keep results focused and avoid paywalled academic noise.
4. Toggle between a single interleaved feed or a split view, and sort academic results by relevance or publication date.
5. Generates Harvard-format references automatically for every result, plus a quote-capture tool that formats a pasted quote with an in-text citation and full reference, ready to copy into an essay.
6. Keeps a running, alphabetised reading list/bibliography that can be edited (items can be removed) and copied in one click.

## How it's built

Everything lives in one self-contained file, `crescendo-search.html` — no build step, no install, no server. It runs entirely in the browser and calls public, key-free APIs (Semantic Scholar, Crossref, GDELT) directly from client-side JavaScript.

## Running it

Open `crescendo-search.html` in any modern browser. An internet connection is needed for live search results.

## License

MIT — see [LICENSE](LICENSE). Free to use, modify and share, including for teaching and coursework; just keep the copyright notice attached to any copies.
