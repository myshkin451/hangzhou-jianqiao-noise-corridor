# Hangzhou Jianqiao Noise Corridor Map

A bilingual, public-source screening map for possible aircraft-noise exposure
around Hangzhou Jianqiao Airport. The page is designed for renters, home
buyers, and newcomers to Hangzhou who need a practical first-pass check before
visiting a compound.

Expected public URL:

<https://myshkin451.github.io/hangzhou-jianqiao-noise-corridor/>

## What It Does

- Shows a broad, inferred noise-risk corridor around Jianqiao Airport.
- Rates clicked or searched locations as red, orange, yellow, or outer area.
- Supports Chinese and English in the same static page.
- Lets users copy a shareable link for the current language, risk model, and
  selected point.
- Provides an opt-in "rate my location" button using browser geolocation.
- Includes an on-site listening checklist for real housing decisions.

## What It Is Not

- Not an official flight path.
- Not a military, government, legal, engineering, or acoustic assessment.
- Not a decibel contour map or environmental-impact report.
- Not a replacement for repeated on-site listening.

Military airfields do not publish exact routes, training schedules, or real-time
tracks. This project intentionally describes itself as a practical screening
tool rather than an authoritative map.

## Sources

- Hangzhou public complaint record:
  <https://yst.hangzhou.com.cn/question.php?question_id=181113171468>
- Article mentioning Jianqiao runway dimensions:
  <https://www.cgejournal.com/article/id/9496>
- Nominatim usage policy:
  <https://operations.osmfoundation.org/policies/nominatim/>
- OpenStreetMap copyright:
  <https://www.openstreetmap.org/copyright>

## Privacy

Searches are sent directly from the browser to Nominatim only after the user
submits a query. The geolocation button only runs after the user clicks it and
grants browser permission. This static page has no server-side collection layer.

Users should avoid entering names, phone numbers, room numbers, or other private
information into the search box.

## Files

- `index.html` - the complete static app.
- `.nojekyll` - tells GitHub Pages to publish static files directly.
- `robots.txt` and `sitemap.xml` - basic search-engine discoverability.
- `NOTICE.md` - source, attribution, and limitation notices.
- `LICENSE` - MIT license for the code.

## Local Preview

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Open:

<http://127.0.0.1:8765/>

## Publish With GitHub Pages

The simplest release path is a public GitHub repository named
`hangzhou-jianqiao-noise-corridor`, published from the `main` branch root.

```bash
gh repo create myshkin451/hangzhou-jianqiao-noise-corridor --public --source=. --remote=origin --push
gh api --method POST /repos/myshkin451/hangzhou-jianqiao-noise-corridor/pages -f 'source[branch]=main' -f 'source[path]=/'
```

If the Pages endpoint says the site already exists, update it instead:

```bash
gh api --method PUT /repos/myshkin451/hangzhou-jianqiao-noise-corridor/pages -f 'source[branch]=main' -f 'source[path]=/'
```
