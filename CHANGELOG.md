# Changelog

All notable changes to `lfx-enconvert` are documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.1] - 2026-08-27

### Added

- First release: the **EnConvert** bundle for Langflow with six components.
  - **Perceive URL** — `POST /v2/perceive`, with a `render_quality` score on every read.
  - **Web Search** — `POST /v2/search`.
  - **Discover URLs** — `POST /v2/discover`.
  - **Extract Structured** — `POST /v2/distill`.
  - **Convert File to Markdown** — `POST /v1/convert/anything-to-markdown` (fetches the file URL, then converts).
  - **Convert File to PDF** — `POST /v1/convert/anything-to-pdf` (fetches the file URL, then converts).
- Pip-installable extension bundle, auto-discovered by Langflow at server start via the
  `langflow.extensions` entry point.
- Private-key (`sk_`) auth over the `X-API-Key` header; public `pk_` keys are rejected with a clear message.
