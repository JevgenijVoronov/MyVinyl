# MyVinyl

My vinyl collection, displayed as covers on wooden shelves.

- `index.html`, `styles.css`, `app.js` — the page: "All" shelf (custom order) and "Artist" shelves by first letter, search, and a detail card with tracklist and a YouTube Music link.
- `data/collection.csv` — collection export from Discogs.
- `scripts/build-data.mjs` — pulls covers, genres, tracklists and original release year from the Discogs API → `data/collection.js`, `covers/`.

Update after a new export:

```bash
cp ~/Downloads/<new-export>.csv data/collection.csv
node scripts/build-data.mjs
```

View locally: `npx http-server -p 8080`, then open http://localhost:8080
