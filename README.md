# FlagBridge — Marketing Site

The public-facing marketing and landing page for [FlagBridge](https://github.com/flagbridge/flagbridge), the open-source feature flag platform with product intelligence.

**Package:** `@flagbridge/web`

[![License](https://img.shields.io/badge/license-Apache%202.0-green)](LICENSE)

---

## Stack

- **Framework:** Next.js (App Router)
- **Styling:** Tailwind CSS
- **i18n:** next-intl — English and PT-BR supported out of the box
- **Deploy:** Vercel (default) or self-hosted via Docker

---

## Development

```bash
pnpm install
pnpm dev       # starts dev server at http://localhost:3000
pnpm build     # production build (static export via next export)
```

---

## Deployment

### Vercel (recommended)

Connect the repository to a Vercel project. No additional configuration is required — the build command is `pnpm build` and the output directory is `out`.

### Self-hosted (Docker)

```bash
docker build -t flagbridge-web .
docker run -p 3000:3000 flagbridge-web
```

The Dockerfile produces a static export served by a lightweight HTTP server.

---

## Internationalization

Content is managed through `next-intl`. Locale files are located under `messages/`. Add or edit keys there to update copy without touching component code.

Supported locales: `en`, `pt-BR`.

---

## Related

- [flagbridge/flagbridge](https://github.com/flagbridge/flagbridge) — Go API server (main repo)
- [flagbridge/admin](https://github.com/flagbridge/admin) — Admin dashboard UI
- [flagbridge/docs](https://github.com/flagbridge/docs) — Documentation site

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.
