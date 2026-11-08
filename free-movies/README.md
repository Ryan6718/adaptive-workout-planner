# OpenReel

A free, ad-free classic movie site. It streams public-domain and freely licensed
films from the [Internet Archive](https://archive.org/details/feature_films), so
there is nothing to license and no ads, tracking or accounts.

## Features

- Browse popular films or filter by genre (comedy, horror, sci-fi, noir, western, drama, silent, cartoons)
- Search by title or subject
- Watch in a built-in player (the Internet Archive's embed player)
- Works on phones and desktops

## Run it

It's a single static file with no build step or backend.

- **Locally:** open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.
- **Hosting (free):** deploy this folder to GitHub Pages, Netlify or Cloudflare Pages.

## How it works

The page calls the Internet Archive's public search API
(`archive.org/advancedsearch.php`) for items in the `feature_films` and
`classic_cartoons` collections. It loads posters from `archive.org/services/img/<id>`
and plays films through `archive.org/embed/<id>`.
