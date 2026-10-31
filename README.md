# Awesome-Business-Messaging-Whatsapp-Marketing

# Awesome-Business-Messaging-Whatsapp-Marketing

**Top Business Messaging Whatsapp Marketing (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on WhatsApp Business API, Omnichannel Inboxes, Marketing Automation & Self-Hosted Messaging Gateways*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Business Messaging & WhatsApp Marketing**. These tools enable organizations to reach customers on WhatsApp and other messaging channels, automate campaigns, manage shared inboxes, and build conversational commerce flows—from fully managed Business Solution Providers (BSPs) with official Meta API access and compliance handling to self-hosted gateways and unofficial bridges that give teams control over their messaging infrastructure.



**Examples** include Twilio, Infobip, Wati, Gupshup, Respond.io, Trengo, Brevo, MessageBird (Bird), and HubSpot WhatsApp integrations (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted messaging, WhatsApp gateways, and open automation infrastructure. **Critical note**: The open-source landscape splits sharply into two paths—**official Cloud API wrappers** (which still require Meta Business approval and BSP relationships) and **unofficial WhatsApp Web bridges** (Evolution API, MultiWA, OpenBSP) that bypass Meta entirely but carry **real ban risk** and lack business features like templates. No open-source project provides a turnkey BSP replacement with Meta approval and compliance built in.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Twilio](https://www.twilio.com/)**

  **Communication platform (CPaaS)** with WhatsApp Business API access alongside SMS, voice, and email. **Pricing**: Meta message fees plus **5–20% BSP markup**; no setup fee or contract . **Free tier**: Trial credits available. **Best for**: developers wanting mature APIs and sandbox numbers for proof-of-concept work—**trade-off**: per-message markup adds up at volume; number lives in Twilio's account .



- **[Infobip](https://www.infobip.com/)**

  **Enterprise omnichannel communications** with WhatsApp, SMS, and voice across many markets. **Pricing**: Negotiated; contracts and committed volumes typical . **Free tier**: None. **Best for**: enterprises running multi-market campaigns needing direct carrier relationships, formal SLAs, and one accountable vendor—**trade-off**: enterprise sale with committed volume requirements .



- **[Wati](https://www.wati.io/)**

  **WhatsApp-first platform for SMBs** with no-code chatbot builder, shared inbox, broadcast campaigns, and template management. Integrates with Shopify, WooCommerce, HubSpot, and Zapier . **Pricing**: Growth from ~$59/mo; Pro ~$119–149/mo; Business ~$279–349/mo. Applies **~20% markup** on Meta rates and charges per extra agent . **Free tier**: 7-day trial; no permanent free plan. **Best for**: SMBs and e-commerce teams wanting an easy WhatsApp-first setup—**watch for**: per-agent fees and message markup at scale .



- **[Gupshup](https://www.gupshup.io/)**

  **Enterprise conversational messaging** spanning WhatsApp and dozens of channels with bot-building tools. **Pricing**: Usage-based/custom; quote-based for high volume . **Free tier**: None. **Best for**: large organizations and high-throughput programs where reliability and volume pricing matter more than simple UI—**trade-off**: heavier setup, aimed at larger teams .



- **[Respond.io](https://respond.io/)**

  **Omnichannel sales and support inbox** covering WhatsApp, Instagram, Messenger, SMS, and email with workflow builder and AI agent. ISO 27001 certified and official Meta Business Partner; **no markup on Meta fees** . **Pricing**: Starter $79/mo (annual) / $99 monthly; Growth $159/mo; Advanced $279/mo; based on Monthly Active Contacts . **Free tier**: Trial available. **Best for**: teams running real conversations across several channels—**watch for**: contact-based pricing during seasonal spikes .



- **[Trengo](https://trengo.com/)**

  **Shared team inbox** bringing WhatsApp together with email, live chat, and other channels. **Pricing**: Per-seat; entry plans around €299/mo billed annually with conversation caps . **Free tier**: Trial available. **Best for**: multi-channel customer support teams wanting a unified inbox—**trade-off**: marketing/commerce features lighter than WhatsApp-first rivals .



- **[Brevo](https://www.brevo.com/)**

  **Marketing and CRM platform** with WhatsApp campaign capabilities alongside email and SMS. **Pricing**: Tiered by contacts and features. **Free tier**: Limited free tier available. **Best for**: marketing teams wanting WhatsApp alongside email campaigns in one platform.



- **[MessageBird (Bird)](https://bird.com/)**

  **Omnichannel communications platform** with WhatsApp Business API access. **Pricing**: Variable markup; **$600+ setup fee** and 3-month minimum contract reported . **Free tier**: None. **Best for**: teams wanting WhatsApp alongside SMS and voice from one vendor—**watch for**: setup fee and contract commitment make it costly for small volumes .



- **[HubSpot WhatsApp Integration](https://www.hubspot.com/)**

  **Native and third-party WhatsApp** within HubSpot CRM. Native features are limited; third-party connectors like MakeWebBetter add bulk messaging, chatbots, and workflow actions. **Pricing**: MakeWebBetter offers a **free tier** (1 number, 500 messages/month); paid from $25/mo . **Free tier**: Yes, via connector. **Best for**: HubSpot users wanting WhatsApp conversations logged on contact timelines—**note**: native HubSpot WhatsApp lacks out-of-office support without workflow configuration .



## Open-Source GitHub Projects



- **[Evolution API](https://github.com/EvolutionAPI/evolution-api)**

  **Open-source WhatsApp REST API with no Meta approval required** (license per repo) — **the most widely deployed self-hosted WhatsApp gateway** in the open-source ecosystem. **Features**: Connects a real WhatsApp number over HTTP via **QR code pairing** (Baileys library); **no Meta Business verification, no template review, no per-conversation fees**; exposes `POST /message/sendText`, webhook events for incoming messages, group management endpoints, and **multi-instance support** for running several numbers from one server . Postgres persists instances/messages/contacts; Redis handles caching and session state; persistent volume keeps WhatsApp auth data alive across redeploys . **Tech stack**: Node.js, PostgreSQL, Redis. **Deploy**: Self-hosted (Docker, Railway template) . **Trade-off**: **Unofficial WhatsApp Web protocol**—ban risk is real, no templates, no business features like verified profiles. Phone must stay registered. **Not suitable for high-volume marketing** where ban risk is unacceptable. **Best for**: developers and small teams wanting full control over WhatsApp messaging without Meta fees—for internal tools, support bots, and low-volume notifications where the number is expendable.



- **[MultiWA](https://github.com/ribato22/MultiWA)**

  **Open-source WhatsApp Business API Gateway with multi-engine support** (license per repo) — **the most enterprise-ready unofficial WhatsApp gateway** found in this research, with SDKs and a full admin dashboard. **Features**: **Multi-engine adapters** (whatsapp-web.js, Baileys, mock); **TypeScript, Python, and PHP SDKs**; **n8n community node** (`n8n-nodes-multiwa`); Chatwoot bridge; WordPress contact-form plugin; **NestJS backend with Next.js admin dashboard**; BullMQ worker for background jobs; Swagger UI at `/api/docs` . **Tech stack**: NestJS, Next.js, Prisma, BullMQ. **Deploy**: Self-hosted (Docker). **Trade-off**: **Unofficial protocol**—same ban risk as Evolution API. No Meta templates or official business verification. **Best for**: developers wanting a structured, SDK-rich WhatsApp gateway with multi-engine flexibility and n8n integration for automation workflows.



- **[OpenBSP](https://github.com/matiasbattocchia/open-bsp-api)**

  **Open-source WhatsApp + Instagram Business platform** (license per repo) — **the most architecturally complete open-source BSP-style platform**, with an optional unofficial WhatsApp bridge. **Features**: **Official path**: Cloud API integration with templates and business features (requires Meta approval). **Unofficial path**: `open-bsp-whatsmeow` bridge connects plain WhatsApp accounts over **Web multidevice protocol** via QR code or pairing code—no templates, no business features, ban risk on you . **Slack integration**—connects as member (private DMs) or bot (workspace-wide); messages flow both directions with editing, deleting, reactions, threads, and files . Supabase edge functions; Postgres for storage. **Tech stack**: Supabase (Postgres, Edge Functions), TypeScript. **Deploy**: Self-hosted (Supabase project + bridge service). **Trade-off**: **Dual-path complexity**—the official path requires Meta approval; the unofficial path carries ban risk. Slack integration is a unique differentiator but not WhatsApp-specific. **Best for**: teams wanting a platform that supports both official and unofficial WhatsApp channels with Slack integration—especially those who need Slack mirroring of WhatsApp conversations.



### Additional Strong Open-Source Options



- **Chatwoot** — Open-source customer engagement platform (MIT) with WhatsApp channel support via Evolution API or Cloud API integrations. **Note**: Inbox and conversation management layer, not a WhatsApp gateway itself—pairs with Evolution API or official BSPs. **Best for**: teams wanting a self-hosted omnichannel inbox with WhatsApp connectivity.

- **n8n** — Fair-code workflow automation with WhatsApp nodes and community integrations. **Note**: Automation engine, not messaging infrastructure—connects to Evolution API, Twilio, or other providers. **Best for**: teams wanting to chain WhatsApp messages into broader business workflows.

- **Typebot** — Open-source conversational form builder with WhatsApp integration. **Note**: Bot-building tool, not a messaging gateway. **Best for**: creating conversational flows that feed into WhatsApp via automation.



**Frameworks for building custom systems**: Combine **Evolution API** or **MultiWA** as the WhatsApp gateway with **Chatwoot** for inbox management and **n8n** for automation—creating a self-hosted messaging stack. **None of these provide official Meta approval, templates, or compliance** like Twilio or Infobip; those require BSP relationships. **For production marketing at scale, official BSPs remain the safer choice** despite the markup.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- WhatsApp marketing platforms must comply with **Meta's WhatsApp Business Policy**, **opt-in requirements**, and data protection regulations (GDPR, CCPA, etc.). **Unofficial WhatsApp bridges (Evolution API, MultiWA, OpenBSP whatsmeow) violate WhatsApp's Terms of Service** and carry **real risk of number bans**—use only where the number is expendable and messaging volume is low.

- **The "official BSP" vs. "unofficial bridge" distinction is absolute.** **Twilio, Infobip, Wati, Gupshup, Respond.io, Trengo, and MessageBird** are **official BSPs**—they have Meta approval, support templates, and handle compliance. **Evolution API, MultiWA, and OpenBSP's whatsmeow bridge** are **unofficial**—they connect via WhatsApp Web protocol, have **no templates, no business verification, and no ban protection** . **Do not use unofficial bridges for customer-facing marketing campaigns** where a ban would damage your business.

- **Meta's pricing changed in 2025–2026.** Since **July 1, 2025**, Meta charges **per template message** (not per 24-hour conversation); rates updated **January 1, 2026**. **Replies within the customer-initiated 24-hour service window are free**, and **Click-to-WhatsApp ads open a 72-hour free window** . **Model your message mix (marketing vs. utility vs. service) before choosing a provider.**

- **BSP markups vary dramatically.** Twilio adds 5–20%; Wati adds ~20%; **Respond.io adds zero markup**; MessageBird charges $600+ setup and 3-month minimum . **A low subscription fee with a 20% markup can cost more than a higher subscription with no markup** at volume .

- **Wati's per-agent fees and automation-trigger metering** mean the real bill commonly runs above the listed plan . **Respond.io's contact-based pricing** can spike during seasonal campaigns . **Model your actual usage before committing.**

- **HubSpot's native WhatsApp lacks out-of-office support**—it requires workflow configuration with time conditions, and the Customer Agent consumes **100 credits per conversation** regardless of time . **Factor credit consumption into HubSpot WhatsApp budgeting.**

- Self-hosted open-source solutions require proper infrastructure (Postgres, Redis for Evolution API), security hardening for API keys, and ongoing maintenance. **WhatsApp gateway data includes message history and contacts**—ensure your deployment meets your organization's security and privacy requirements, and **accept that unofficial bridges may be shut down by WhatsApp at any time**.



---



**Made for developers, marketing teams, and organizations building transparent business messaging solutions.**

Let's make Business Messaging & WhatsApp Marketing more open, data-driven, and compliant.
