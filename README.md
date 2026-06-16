# Free API Explorer

**Curated directory of 305 free APIs — zero authentication required.**

[![GitHub Stars](https://img.shields.io/github/stars/Stevechaapps/api-explorer?style=flat-square&logo=github)](https://github.com/Stevechaapps/api-explorer/stargazers)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Stevechaapps/api-explorer?style=flat-square&logo=git)](https://github.com/Stevechaapps/api-explorer/commits/main)
[![Site](https://img.shields.io/badge/live-site-brightgreen?style=flat-square&logo=cloudflare-pages)](https://free-api-explorer.pages.dev)

Every API in this collection works without API keys, tokens, or signups. Weather forecasts, financial data, AI/ML models, government datasets, geocoding, entertainment, and more — all available with a simple HTTP request.

[**Browse the Directory**](https://free-api-explorer.pages.dev) &middot; [**View Categories**](https://free-api-explorer.pages.dev/categories.html) &middot; [**Sitemap**](https://free-api-explorer.pages.dev/sitemap.xml)

---

## Why This Exists

Finding free APIs is easy. Finding free APIs that don't require authentication is not. Most directories list APIs that need signup, rate-limit keys, or OAuth flows — which kills the ability to prototype quickly or use them in client-side applications.

This directory solves that. Every API was tested and verified to return data with zero authentication. Use them in:

- **Client-side JavaScript apps** — fetch straight from the browser, no proxy needed
- **Hackathons and prototypes** — working in minutes, not hours
- **CI/CD pipelines** — no credential management
- **Education and tutorials** — students write code, not configure auth
- **Serverless functions** — fewer environment variables to manage

## What's Inside

| Category | APIs | Category | APIs |
|---|---|---|---|
| [Development](https://free-api-explorer.pages.dev/category/development.html) | 34 | [Entertainment](https://free-api-explorer.pages.dev/category/entertainment.html) | 30 |
| [Finance](https://free-api-explorer.pages.dev/category/finance.html) | 22 | [Government](https://free-api-explorer.pages.dev/category/government.html) | 20 |
| [Data](https://free-api-explorer.pages.dev/category/data.html) | 19 | [Fun](https://free-api-explorer.pages.dev/category/fun.html) | 17 |
| [Education](https://free-api-explorer.pages.dev/category/education.html) | 14 | [Science](https://free-api-explorer.pages.dev/category/science.html) | 14 |
| [Utility](https://free-api-explorer.pages.dev/category/utility.html) | 12 | [Weather](https://free-api-explorer.pages.dev/category/weather.html) | 12 |
| [Health](https://free-api-explorer.pages.dev/category/health.html) | 12 | [Transportation](https://free-api-explorer.pages.dev/category/transportation.html) | 11 |
| [Geocoding](https://free-api-explorer.pages.dev/category/geocoding.html) | 8 | [Sports](https://free-api-explorer.pages.dev/category/sports.html) | 8 |
| [News](https://free-api-explorer.pages.dev/category/news.html) | 8 | [Food](https://free-api-explorer.pages.dev/category/food.html) | 8 |
| [Media](https://free-api-explorer.pages.dev/category/media.html) | 7 | [Security](https://free-api-explorer.pages.dev/category/security.html) | 5 |
| [Animals](https://free-api-explorer.pages.dev/category/animals.html) | 5 | [AI](https://free-api-explorer.pages.dev/category/ai.html) | 3 |
| [Music](https://free-api-explorer.pages.dev/category/music.html) | 2 | [Environment](https://free-api-explorer.pages.dev/category/environment.html) | 2 |

[**Browse all 40 categories →**](https://free-api-explorer.pages.dev/categories.html)

## Quick Start

```js
// No API key. No signup. Just fetch.
fetch('https://api.open-meteo.com/v1/forecast?latitude=52.52&longitude=13.41&current=temperature_2m')
  .then(res => res.json())
  .then(console.log);
```

```bash
# Works with curl too
curl -s 'https://api.open-meteo.com/v1/forecast?latitude=52.52&longitude=13.41&current=temperature_2m' | jq
```

Every API on this site works exactly like this. Pick one, copy the URL, make a request.

## Featured APIs

| API | What It Does | Try It |
|---|---|---|
| [Open-Meteo Weather](https://free-api-explorer.pages.dev/api/open-meteo-weather.html) | Global weather forecasts, no rate limits | [Request](https://api.open-meteo.com/v1/forecast?latitude=52.52&longitude=13.41&current=temperature_2m,wind_speed_10m&hourly=temperature_2m,relative_humidity_2m,wind_speed_10m) |
| [Frankfurter Exchange](https://free-api-explorer.pages.dev/api/frankfurter-currency-exchange.html) | ECB currency rates, updates daily | [Request](https://api.frankfurter.app/latest?from=USD&to=EUR) |
| [JokeAPI](https://free-api-explorer.pages.dev/api/jokeapi.html) | Programmer jokes, multiple categories | [Request](https://v2.jokeapi.dev/joke/Programming?type=single) |
| [Rest Countries](https://free-api-explorer.pages.dev/api/rest-countries.html) | Country data, population, languages | [Request](https://restcountries.com/v3.1/name/deutschland) |
| [NASA Open APIs](https://free-api-explorer.pages.dev/api/nasa-open-apis.html) | Astronomy pic of the day, Mars rover | [Request](https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY) |
| [CoinGecko](https://free-api-explorer.pages.dev/api/coingecko.html) | Crypto prices, market data | [Request](https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd) |

[**View all 305 APIs →**](https://free-api-explorer.pages.dev)

## Geographic Coverage

APIs are tagged by geographic region so you can find data relevant to your location:

- **🌍 Global** — 150+ APIs working worldwide
- **🇺🇸 United States** — US government data, weather, transportation
- **🇪🇺 Europe** — EU bank rates, UK police data, Swiss transport, Berlin transit
- **🇨🇦 Canada** — BC open data, Ottawa transport, Canadian government
- **🇧🇷 Brazil** — Brazilian bank data, postal codes
- **🇩🇪 Germany** — German weather service, Nager.Date holidays
- **🇫🇷 France** — French address search, Paris transport
- **🇵🇱 Poland** — Polish government open data
- **🇳🇴 Norway** — Norwegian weather service
- **🇨🇿 Czech Republic** — Czech National Bank

[Browse by region →](https://free-api-explorer.pages.dev)

## Architecture

```
money/
├── server.js              # Express server (dynamic fallback)
├── public/
│   ├── index.html          # Homepage with search & categories
│   ├── categories.html     # All 40 categories
│   ├── sitemap.xml         # Full XML sitemap for search engines
│   ├── styles.css          # Responsive styles
│   ├── api/                # 305 static API detail pages
│   │   ├── open-meteo-weather.html
│   │   ├── frankfurter-currency-exchange.html
│   │   └── ...
│   ├── category/           # Static category listing pages
│   │   ├── weather.html
│   │   ├── finance.html
│   │   └── ...
│   └── guides/             # Developer guides and tutorials
└── README.md
```

The site is fully static. Every API page is a standalone HTML file with its own meta tags, JSON-LD structured data, and canonical URL — no JavaScript required for content. This makes every page independently indexable by search engines.

## Running Locally

```bash
git clone https://github.com/Stevechaapps/api-explorer.git
cd api-explorer
npm install
node server.js
# Opens at http://localhost:3001
```

The server is optional — all static files work directly from the `public/` directory.

## SEO & Discoverability

This project is designed to be crawled and indexed efficiently:

- **XML Sitemap** — [`/sitemap.xml`](https://free-api-explorer.pages.dev/sitemap.xml) lists every API page and category
- **Structured Data** — Every page includes JSON-LD `FAQPage` and `WebSite` schema
- **Canonical URLs** — Every page self-references its canonical
- **Semantic HTML** — Proper heading hierarchy, breadcrumbs, and ARIA landmarks
- **No JavaScript dependency** — Content is fully available to crawlers

## Donate

If this directory saves you time, consider buying a coffee.

[![Donate via PayPal](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donate?hosted_button_id=XR297MKXBAMBS)

Your support keeps the site updated with new APIs and helps cover hosting costs.

## License

MIT — use the code, fork the repo, build your own directory.

---

**[Browse APIs](https://free-api-explorer.pages.dev)** &middot; **[Categories](https://free-api-explorer.pages.dev/categories.html)** &middot; **[Sitemap](https://free-api-explorer.pages.dev/sitemap.xml)**
