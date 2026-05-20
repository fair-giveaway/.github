# Welcome to Fair-Giveaway HQ 🚀

### *Ensuring absolute transparency and trust in online giveaways, powered by modern $0 infrastructure.*

---

## 🔍 About Us

**Fair-Giveaway** is an open-source organization dedicated to building open, provably fair, and auditable utility tools for the community. Our flagship platform, **[fairgiveaway.online](https://fairgiveaway.online)**, solves the trust deficit in social media draws (starting with X/Twitter) by conducting all randomizations strictly client-side using cryptographic standards.

We are proof that world-class, high-performance SaaS platforms can be built entirely on a **Full Zero-Cost ($0) Infrastructure Stack**.

---

## 🛠️ The Core Stack

We love fast runtimes, modern styling, and scalable edge database architectures. 

| Layer | Technology | Infrastructure Provider | Cost |
| :--- | :--- | :--- | :--- |
| **Frontend** | Next.js (App Router), TypeScript, Tailwind CSS v4 | Netlify Free Tier | `$0` |
| **Backend** | Bun, ElysiaJS, Puppeteer Headless | Hugging Face Spaces (Docker) | `$0` |
| **Temp Cache** | Upstash Redis (Serverless) | Upstash Free Tier | `$0` |
| **Permanent DB** | MongoDB Atlas (Shared Cluster) | MongoDB M0 Free Tier | `$0` |

---

## 🗂️ Ecosystem Repositories

Our architecture is fully decoupled and isolated per scope to ensure smooth maintenance and open audatibility:

* **[`fairgiveaway-frontend`](https://github.com/fair-giveaway/fairgiveaway-frontend)**: The beautiful user workstation. Built with Next.js and Tailwind v4, utilizing a premium dark-themed visual language with dynamic, platform-scoped routing (`/x`, `/facebook`, etc.) and instant client-side cryptographic shuffling (`window.crypto.getRandomValues`).
* **[`fairgiveaway-backend`](https://github.com/fair-giveaway/fairgiveaway-backend)**: The heavy-lifting engine. Powered by Bun + ElysiaJS to handle high-speed API requests, automated Puppeteer scraping via internal GraphQL streams, and intelligent database bridging.

---

## 🔒 Provably Fair Architecture

We believe transparency shouldn't be a black box. Our system architecture enforces strict data integrity:
1.  **Scrape & Cache**: Participant datasets are safely captured and stored temporarily in **Upstash Redis** with a 15-minute expiration window to handle accidental drop-connections.
2.  **Client Shuffle**: The actual raffle uses a transparent **Fisher-Yates Shuffle** right inside the holder's browser. No backend manipulation possible.
3.  **Perpetual Monument**: Once locked, the summary metadata is permanently written to **MongoDB Atlas**, turning the temporary draw session into an unalterable **Immutable Proof Page**.

---

## 🤝 Contributing

We are entirely open-source! We welcome developers, UI/UX designers, and tech enthusiasts to help expand our platform integration (Facebook, Instagram, TikTok, and CSV imports are currently in the pipeline).

Check out our contribution guidelines inside the respective repositories, grab an issue, and submit a Pull Request!

---

## 💖 Support the Core Maintainer

This project runs entirely on passion and coffee. If our platform helped you host a transparent giveaway or saved your business subscription costs, consider buying us a coffee or becoming a sponsor:

* **Trakteer (Local IDR)**: [trakteer.id/isaacnewton1/link](https://trakteer.id/isaacnewton1/link)
* **Ko-fi (International)**: [ko-fi.com/isaacnewton1](https://ko-fi.com/isaacnewton1)
* **GitHub Sponsors**: [github.com/sponsors/isaacnewton123](https://github.com/sponsors/isaacnewton123)

---

<p align="center">
  Licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>. Made with ⚡ and ☕ by the Fair-Giveaway community.
</p>
