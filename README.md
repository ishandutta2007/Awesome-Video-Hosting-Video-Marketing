# Awesome-Video-Hosting-Video-Marketing

# Top Video Hosting & Video Marketing Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Self-Hosted Video Platforms, Marketing Analytics & Privacy-First Media CMS*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Video Hosting & Video Marketing**. These tools enable organizations to upload, transcode, embed, and analyze video content—turning video from a static asset into a measurable, engagement-driven channel for marketing, sales, and customer education.

**Examples** include HubSpot Video Hosting, Wistia, Vidyard, Vimeo, Loom, Brightcove, Hippo Video, SproutVideo, Synthesia, and Cincopa (the category leaders).

**Open-source emphasis**: Video Hosting & Marketing is a domain where open-source tooling is **surprisingly mature for hosting and CMS workflows but still catching up on conversion-focused marketing analytics**. **Mave Core** is the strongest self-hosted Mux alternative—a complete platform with upload, FFmpeg-based HLS transcoding, S3-compatible storage, embeddable player, and ClickHouse-backed analytics (views, drop-off, sources) . **Hovod** offers a similar self-hosted Mux alternative in a single Docker container with AI transcription (Whisper), multi-tenancy, and optional Stripe billing . For marketing-specific analytics, **Vidalytics** is the only open-source player explicitly built for conversion tracking—play rate, retention, CTA clicks, and split testing . For YouTube-style media portals, **MediaCMS** provides a full-featured video CMS with HLS adaptive streaming, subtitles, and REST API . The critical gap: **no open-source project replicates Wistia's or Vidyard's turnkey marketing integrations** (HubSpot/Salesforce sync, lead capture forms, account-based marketing) out of the box.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[HubSpot Video Hosting](https://www.hubspot.com/)**  
  Video hosting integrated with HubSpot CRM; embed videos in landing pages, emails, and blogs with lead capture forms and viewer analytics tied directly to contact records.

- **[Wistia](https://wistia.com/)**  
  Video hosting and marketing platform known for customizable players, lead capture (turnstile gates), video SEO, and channel analytics; deeply integrated with HubSpot and Salesforce for attribution.

- **[Vidyard](https://www.vidyard.com/)**  
  Video hosting and async communication platform with AI avatars, Video Agent automation, and CRM integrations for sales enablement and training.

- **[Vimeo](https://vimeo.com/)**  
  Video hosting platform with privacy controls, customizable embeds, and marketing features (Vimeo Create for social video); popular for portfolios and brand content.

- **[Loom](https://www.loom.com/)**  
  Asynchronous video messaging tool for quick screen and webcam recordings; now part of Atlassian with AI-powered summaries and integrations.

- **[Brightcove](https://www.brightcove.com/)**  
  Enterprise video platform for OTT and live streaming; provides video monetization, analytics, and distribution at scale.

- **[Hippo Video](https://www.hippovideo.io/)**  
  Video marketing platform with screen recording, webcam capture, and personalized video for sales outreach; integrates with CRM and marketing automation.

- **[SproutVideo](https://sproutvideo.com/)**  
  Video hosting platform with privacy controls, lead capture forms, and detailed viewer analytics; positioned for businesses wanting professional hosting without YouTube.

- **[Synthesia](https://www.synthesia.io/)**  
  AI video generation platform for creating videos with digital avatars from text—no cameras, actors, or studios required; popular for training and product explainers.

- **[Cincopa](https://www.cincopa.com/)**  
  Video hosting and marketing platform with customizable players, lead capture, and analytics; supports video galleries and playlists.

## Open-Source GitHub Projects

### Self-Hosted Video Platforms (Mux Alternatives)

- **[Mave Core](https://github.com/maveio/core)**  
  The most complete open-source **video infrastructure platform** available (AGPL-3.0-or-later, v0.x) . Features: resumable uploads, **adaptive HLS transcoding via FFmpeg** (versioned DAG pipeline), S3-compatible storage (MinIO bundled, but AWS S3/Cloudflare R2/Backblaze B2 supported), embeddable player (web components, iframe, React, Vue), and **ClickHouse-backed analytics** for views, drop-off, and viewing sources. Includes PostgreSQL, ClickHouse, MinIO, tusd, and Caddy in a single `docker compose up` deployment (requires 4 CPU cores, 8GB RAM, 20GB disk minimum). **The best open-source foundation for a self-hosted video hosting platform**—but it is infrastructure, not a turnkey marketing tool with CRM integrations.

- **[Hovod](https://hub.docker.com/r/synapsr/hovod)**  
  Self-hosted, single-container **open-source Mux alternative** (Node.js/Fastify/React/FFmpeg) . Features: drag-drop or URL import, adaptive HLS transcoding (360p–4K, hardware-adaptive), S3-compatible storage, built-in dashboard with analytics (views, watch time, retention curves), **AI processing via Whisper** for transcription and auto-subtitles, multi-tenancy with roles and API keys, optional Stripe billing, comments/reactions, and webhooks. All-in-one image includes MariaDB and Redis—only S3 storage is required externally. **The fastest path to a working self-hosted video platform** with AI features, though smaller community than Mave Core.

### Video Marketing Analytics

- **[Vidalytics](https://github.com/vidalytics/Vidalytics)**  
  The only open-source **video analytics and optimization platform built for marketers** . Tracks play rate, unmute rate, retention, engagement drop-off, **CTA clicks, and conversions**—with breakdowns by viewer segment (new vs returning, buyers vs non-buyers, device, geography). Features: interactive and shoppable videos (Shopify integration), play gates for lead capture, exit CTAs, **AI-powered performance insights** (Vids AI, Script Analyzer), industry benchmarks, and split testing. Full REST API for uploads, analytics export, and embed customization. Integrations: Zapier, Make.com, Facebook Pixel, GA, Tag Manager, HubSpot, ActiveCampaign. **This is the closest open-source equivalent to Wistia or Vidyard for marketing use cases**—but it is a commercial platform with open-source code, not a fully free self-hosted product (pricing tiers from free to Enterprise).

### Video CMS Platforms (YouTube Alternatives)

- **[MediaCMS](https://github.com/mediacms-io/mediacms)**  
  Modern, fully featured **open-source video and media CMS** (Django/Python + React, AGPL-3.0) . Features: video/audio/image/PDF support, **HLS adaptive streaming**, multiple transcoding profiles (240p–1080p, h264/h265/vp9), **automatic transcription via Whisper**, multilingual subtitles, playlists, categories/tags, configurable access (public/private/unlisted), REST API (Swagger), and responsive design with light/dark themes. Docker Compose deployment (4GB RAM/2-4 CPUs recommended for small installs) . **The strongest open-source option for building a YouTube-like media portal** for education, community, or sensitive content—not a marketing-focused player.

- **[PeerTube](https://github.com/Chocobozzz/PeerTube)**  
  Free, decentralized, **federated video platform** (AGPL-3.0) developed by Framasoft as an alternative to YouTube/Vimeo . Uses **P2P (WebRTC) to share load among viewers** and allows instances to cache each other's videos. Features: live streaming, video upload/transcoding, playlists, subtitles, federation via ActivityPub (follow channels from Mastodon), customizable interface, no ads, no data mining. **The best option for community-owned, privacy-first video hosting**—but federation adds complexity not needed for a single-organization marketing site.

### Additional Strong Open-Source Options

- **CinemataCMS** — Privacy-first video CMS for advocacy and social issue films (OTF security-audited, built by Southeast Asian developers) . Built for human rights documentation, activist archiving, and film festivals where secure hosting and access controls are essential. **Niche but important for sensitive content**—not a general marketing video platform.
- **Owncast** — Free, open-source **live streaming** server (Go/React) with built-in chat and fediverse integration . **Live-focused**—for real-time broadcasts, not on-demand video hosting or marketing analytics.
- **MediaMTX** — Open-source **media server** (Go) supporting SRT, WebRTC, RTMP, HLS, and more . **Infrastructure-level**—useful as a streaming backend, not a complete video platform.
- **Jellyfin** — Open-source media server (.NET) for personal media libraries . **Not for marketing or public video hosting**—designed for personal/家庭 media streaming, not business use cases.

**Frameworks for building custom systems**: For a **self-hosted Mux-like video infrastructure**, Mave Core provides the most complete open-source foundation with encoding pipeline and analytics , while Hovod offers a simpler single-container alternative with AI transcription . For **marketing-focused video analytics**, Vidalytics is the only open-source option with conversion tracking . For a **YouTube-style media portal**, MediaCMS  or PeerTube . No open-source project replicates the **turnkey CRM integrations and lead capture workflows** of Wistia or Vidyard—organizations requiring those should evaluate commercial platforms or build custom integrations atop Mave Core or Vidalytics.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Video hosting platforms handling uploaded content and viewer data must comply with applicable privacy regulations (GDPR, CCPA) and content licensing laws; self-hosted solutions place full responsibility for storage, bandwidth, and content moderation on the operator.
- **Open-source video hosting is mature for infrastructure and CMS workflows**—Mave Core and Hovod provide production-ready self-hosted platforms , and MediaCMS/PeerTube serve media portal needs . However, **no open-source project replicates the turnkey marketing integrations and lead capture** of Wistia or Vidyard out of the box; Vidalytics comes closest but is a commercial platform with open-source code . Organizations requiring deep CRM sync and marketing automation should evaluate commercial platforms.
- Verify license terms for commercial use; Mave Core uses AGPL-3.0-or-later , MediaCMS uses AGPL-3.0 , PeerTube uses AGPL-3.0 , and Vidalytics is open-source code with commercial pricing tiers .
