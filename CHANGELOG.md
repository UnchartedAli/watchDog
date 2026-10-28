# Changelog

## 1.0.0 — first public release
- Added **YAprice** (rates in toman, panel + bot), **YAProxy** (MTProto proxies), **YAconfig** (free V2Ray configs) and **YA Dojo** (owner feedback → versioned behaviour rules).
- Keywords: typing a currency/gold name, "proxy" or "config" in chat answers with prices / proxies / configs and glass buttons.
- **Several backup AI providers** (each with several API keys) managed from the bot with `/backup`.
- Removed the whisper ("najva") feature.
- Fail-closed security: the worker will not run without `WEBHOOK_SECRET`; "missing == missing" comparisons no longer pass.
- TMDB key is no longer sent to the browser (server-side proxy `/yatmdb/…`).
- Public build: playful modes are mild by design (no profanity, no ethnic/family insults); no personal links, donation or branding baked in.
