# EnConvert bundle for Langflow

`lfx-enconvert` adds six [EnConvert](https://www.enconvert.com) components to Langflow.
EnConvert renders web pages and files into agent-ready data, and puts a `render_quality`
honesty score (0.0–1.0) on every read — so a blocked or empty page comes back flagged, not trusted.

## Components

| Component | Endpoint | What it does |
|-----------|----------|--------------|
| **Perceive URL** | `POST /v2/perceive` | A page → markdown, structured data, screenshot, PDF, links… with a `render_quality` score |
| **Web Search** | `POST /v2/search` | Web / news / images / scholar / patents / maps results |
| **Discover URLs** | `POST /v2/discover` | Map a site (sitemap, crawl, hybrid) into a list of URLs |
| **Extract Structured** | `POST /v2/distill` | Typed data from pages against a JSON schema |
| **Convert File to Markdown** | `POST /v1/convert/anything-to-markdown` | Any file URL → clean markdown |
| **Convert File to PDF** | `POST /v1/convert/anything-to-pdf` | Any file URL → PDF |

## Install

```bash
pip install lfx-enconvert
```

Langflow auto-discovers the bundle at server start. The six components appear under the
**EnConvert** bundle in the component sidebar — no config, no manual registration.

## API key

Each component has an **EnConvert API Key** field. Use a **private** key (`sk_…`) from your
[dashboard](https://www.enconvert.com/dashboard/api-keys); public `pk_` keys are rejected.
Store it once as a Langflow **global variable** and select it in the key field, so it never
lives in the flow JSON.

## Publishing / distribution

Building, publishing to PyPI, the single-file drop-in route, and the optional core PR are all in
the **[deploy guide](../langflow-enconvert-deploy/README.md)**.

## Licence

[MIT](LICENSE)
