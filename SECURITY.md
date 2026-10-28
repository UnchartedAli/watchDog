# Security policy

## Reporting a vulnerability
Please **do not open a public issue**. Use GitHub's *Security → Report a vulnerability* (private advisory) on this repository.

## Things to know when you deploy
- The worker **refuses to run** until `WEBHOOK_SECRET` (16+ characters) is set. Telegram updates are accepted only with that secret.
- API keys you add from the bot (`/myai`, `/backup`) are stored **AES-GCM encrypted** (key derived from `ENC_KEY`, or `WEBHOOK_SECRET` if `ENC_KEY` is empty). Set a separate `ENC_KEY`.
- Never commit `.dev.vars`, tokens or keys. If a token ever leaked, revoke it in @BotFather (`/revoke`) and rotate the other secrets.
- Owner-only commands check `OWNER_ID`; keep that id correct.
