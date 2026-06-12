# Crawlora — Make custom app

The app definition for **Crawlora on [Make](https://make.com)** — get structured web data and page
content from the public web in your scenarios. This repo holds the JSON/IML for Make's **app
builder**.

## Modules

| Module | Type | Endpoint |
| --- | --- | --- |
| **Get Page Content** | action | `POST /web/scrape` |
| **Web Search** | search | `GET /bing/search` · `GET /brave/search` (engine select) |
| **Find Website Contacts** | action | `POST /contact` |
| **Make an API Call** | universal | call any Crawlora endpoint by path |

Authentication is an **API-key connection** (`x-api-key` header), validated with a cheap, key-only
call to `GET /google/suggest`. Get a key from your
[Crawlora dashboard](https://crawlora.net/app/api-keys) — new accounts include a free monthly credit
allowance, no card required.

## Building the app in Make

In **Make → Custom apps → Create a new app**, fill each section from these files:

1. **App metadata** — [`app.json`](app.json) (name, label, description, theme, site).
2. **Base** — [`base.json`](base.json) (base URL + the `x-api-key` header from the connection +
   error handling).
3. **Connection** (API key) — [`connection/communication.json`](connection/communication.json) and
   [`connection/parameters.json`](connection/parameters.json).
4. **Modules** — create one module per file in [`modules/`](modules) and paste each top-level key
   into the matching builder tab: `communication` → **Communication**, `mappableParameters` →
   **Mappable parameters**, `interface` → **Interface**, `samples` → **Samples**. The `moduleType`
   field says whether to create an Action, Search, or Universal module.

## Links

- API documentation: https://docs.crawlora.net
- Crawlora: https://crawlora.net

## License

[MIT](./LICENSE)
