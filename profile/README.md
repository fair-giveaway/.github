<p align="center">
  <img src="https://raw.githubusercontent.com/fair-giveaway/fairgiveaway-frontend/refs/heads/master/public/logo.png" alt="FairGiveaway Logo" width="100" height="100" style="border-radius: 20px;" />
</p>

<h1 align="center">Fair-Giveaway</h1>

<p align="center">
  <strong>Provably fair, open-source giveaway winner selection for social media.</strong><br/>
  <em>Trust Built into the Code.</em>
</p>

<p align="center">
  <a href="https://fairgiveaway.online">Website</a> •
  <a href="https://api.fairgiveaway.online/docs">API Docs</a> •
  <a href="https://x.com/FairGiveaway">X (Twitter)</a> •
  <a href="https://github.com/orgs/fair-giveaway/discussions">Discussions</a>
</p>

---

## About

**Fair-Giveaway** is an open-source organization building transparent, auditable, and provably fair tools for the online giveaway ecosystem. Our flagship platform, [fairgiveaway.online](https://fairgiveaway.online), eliminates the trust deficit in social media giveaways by conducting all randomization client-side using the Web Crypto API.

Every draw is cryptographically secure, every result is permanently recorded, and every participant list is publicly auditable.

---

## Architecture

```
┌──────────────────────────────────────────────────────────────────┐
│                         How It Works                             │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1. SCRAPE & CACHE          2. CLIENT SHUFFLE                    │
│  ┌─────────────────┐       ┌─────────────────┐                  │
│  │  Tweet URL       │──────▶│  Fisher-Yates   │                  │
│  │  Puppeteer +     │       │  Shuffle using   │                  │
│  │  GraphQL Stream  │       │  crypto.getRandom│                  │
│  │       ▼          │       │  Values()        │                  │
│  │  Upstash Redis   │       │  (in browser)    │                  │
│  │  (15 min TTL)    │       └────────┬─────────┘                  │
│  └─────────────────┘                │                            │
│                                     ▼                            │
│                        3. PERMANENT RECORD                       │
│                        ┌─────────────────┐                       │
│                        │  MongoDB Atlas   │                       │
│                        │  Immutable Proof │                       │
│                        │  Public Audit    │                       │
│                        └─────────────────┘                       │
└──────────────────────────────────────────────────────────────────┘
```

---

## Tech Stack

| Layer        | Technology                                        | Provider      |
| :----------- | :------------------------------------------------ | :------------ |
| **Frontend** | Next.js (App Router), TypeScript, Tailwind CSS v4 | Netlify       |
| **Backend**  | Bun, ElysiaJS, Puppeteer Headless                 | VPS (Docker)  |
| **Cache**    | Upstash Redis (Serverless)                        | Upstash       |
| **Database** | MongoDB Atlas                                     | MongoDB Cloud |
| **Email**    | Nodemailer + Zoho Mail SMTP                       | Zoho          |

---

## Repositories

| Repository                                                                        | Description                                                                                                                             |
| :-------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| [`fairgiveaway-frontend`](https://github.com/fair-giveaway/fairgiveaway-frontend) | Next.js frontend with premium dark-mode UI, platform-scoped routing, client-side cryptographic shuffling, and public draw verification. |
| [`fairgiveaway-backend`](https://github.com/fair-giveaway/fairgiveaway-backend)   | ElysiaJS API server with Puppeteer scraping, anti-bot verification, session management, and permanent result storage.                   |
| [`.github`](https://github.com/fair-giveaway/.github)                             | Organization profile, community health files, and shared configuration.                                                                 |

---

## Contributing

We welcome developers, designers, and community members! Check out the contribution guidelines in each repository, pick an issue, and submit a Pull Request.

- 💬 [GitHub Discussions](https://github.com/orgs/fair-giveaway/discussions) — Questions, ideas, and feedback
- 🐛 [Frontend Issues](https://github.com/fair-giveaway/fairgiveaway-frontend/issues) — UI bugs and feature requests
- 🐛 [Backend Issues](https://github.com/fair-giveaway/fairgiveaway-backend/issues) — API bugs and feature requests

---

## Support the Project

If FairGiveaway has helped you host a transparent giveaway, consider supporting the maintainer:

- **Trakteer (IDR)**: [trakteer.id/isaacnewton1/link](https://trakteer.id/isaacnewton1/link)
- **Ko-fi (International)**: [ko-fi.com/isaacnewton1](https://ko-fi.com/isaacnewton1)
- **GitHub Sponsors**: [github.com/sponsors/isaacnewton123](https://github.com/sponsors/isaacnewton123)

---

<p align="center">
  Licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.<br/>
  Made with ⚡ and ☕ by the Fair-Giveaway community.
</p>
