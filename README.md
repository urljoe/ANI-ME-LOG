# Ani-Me Log

A single-page viewer that reads any number of sources (JSON or RSS/Atom feeds) and lists what they contain.
Titles that appear in more than one source are merged automatically, so nothing shows twice.

## What’s in this repo

| File | Purpose |
|---|---|
| `index.html` | The whole app (no install, no build step) |
| `sources.json` | Optional list of sources loaded for everyone who opens the site |
| `README.md` | This guide |

## Put it on GitHub

1. Sign in at github.com and click **New repository**. Name it (for example `ani-me-log`), keep it **Public**, and create it.
2. Click **Add file → Upload files**, drag in `index.html`, `sources.json` and `README.md`, then **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/ani-me-log/`.

## Where to find sources

A source is any URL that returns a list of titles as JSON or RSS/Atom.

- **Jikan** (MyAnimeList data, free, no key): `https://api.jikan.moe/v4/top/anime`, `https://api.jikan.moe/v4/seasons/now`. Docs: https://docs.api.jikan.moe
- **Kitsu** (free JSON API): `https://kitsu.io/api/edge/anime?sort=-userCount`. Docs: https://kitsu.docs.apiary.io
- **RSS/Atom feeds** from any site you’re allowed to use (news, release or blog feeds). Look for an RSS icon or add `/feed` or `/rss` to the site address.
- **Your own list**: host a `.json` file (even in this repo) shaped like `[{"title":"…","image":"…","url":"…"}]`.

Only add sources you have the right to access. The app lists what a source publishes; it doesn’t host or download anything.

## Using it

- **Sources → Add source**: paste a URL, or paste JSON/RSS text, or import a file. There’s no limit on how many you add.
- **Reload / Refresh all** re-reads every source.
- **Duplicates** shows titles found more than once. Matching ignores case, punctuation, accents and tags like “(Dub)”.
- **Export sources** downloads your list; commit it as `sources.json` to share it with everyone who opens your site.

## If a source won’t load

Browsers block some sites from being read by other pages (CORS). The error will say so. Either choose a source that allows it (Jikan and Kitsu do), or set a CORS proxy under **Sources → CORS proxy**.

Your sources are saved in your own browser (localStorage), so each visitor has their own list on top of `sources.json`.

---
thewiltedpetals.blooms
