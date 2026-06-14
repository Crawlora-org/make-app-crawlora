# Crawlora for Make

Crawlora is a structured web-data API. These modules return clean JSON and page content from the public web — search, page content and contacts, maps and geocoding, product and marketplace data, reviews, financial quotes, social profiles, and more — so you can build them straight into your scenarios.

## Getting started

1. Get an API key from your [Crawlora dashboard](https://crawlora.net/app/api-keys). New accounts include a free monthly credit allowance — no card required.
2. Add a **Crawlora** connection and paste the key; Make validates it with a single lightweight call.
3. Drop any module into a scenario and map its fields.

Full API reference: **[docs.crawlora.net](https://docs.crawlora.net)**.

## Modules

| Module | What it does |
| --- | --- |
| **Get Page Content** | Fetch a public web page as clean Markdown, HTML, links, or page metadata. |
| **Web Search** | Run a web search (Bing or Brave) and return ranked results. |
| **Get Search Suggestions** | Autocomplete query suggestions for a search term (Google or Bing). |
| **Find Website Contacts** | Find public emails, phone numbers, and social profiles for a website. |
| **Geocode an Address** | Convert a free-form address or place name into coordinates. |
| **Reverse Geocode Coordinates** | Convert latitude/longitude into a structured address. |
| **Check Site Accessibility** | Check whether a public page is reachable and what bot-protection it presents. |
| **Find Local Businesses** | Find local businesses for a query (live map search or the stored dataset). |
| **Get Product Details** | Normalized product or app details by identifier (Amazon, eBay, App Store, Google Play). |
| **Search a Marketplace** | Search a marketplace for products (Amazon, eBay). |
| **Get Reviews** | Public reviews for a business, app, or listing (Trustpilot, App Store, Google Play, Product Hunt, Airbnb). |
| **Get Financial Quote** | Latest quote for a stock, index, or crypto (Yahoo Finance, Google Finance, CoinGecko). |
| **Get Social Profile** | Public profile or recent posts by handle (YouTube, TikTok, Instagram, Reddit, LinkedIn). |
| **Make an API Call** | Call any Crawlora endpoint by path — for anything not covered by a dedicated module. |

Multi-source modules pick their data source from a dropdown, so a single module covers several sites.

## Tips

- **Identifiers vary by source.** App Store uses the **bundle ID** (e.g. `com.company.app`), not the numeric track ID; Google Play uses the **package name**; Trustpilot uses the **domain** (e.g. `amazon.com`).
- **Get Social Profile (YouTube)** expects the **channel ID** (starts with `UC`), not an `@handle`.
- Only public data is returned. Use the API in line with Crawlora's terms and applicable law.

## Support

Questions or partnership: **hi@crawlora.net** · Docs: **[docs.crawlora.net](https://docs.crawlora.net)** · Site: **[crawlora.net](https://crawlora.net)**
