# cubiq-ai-context
Centralized knowledge base for AI agents working with Cubiq projects.

## 📌 About This Repository

This repository centralizes all the **institutional memory, guidelines, and context** necessary for Artificial Intelligences (LLMs) to work in alignment with **Cubiq**.

It functions as a **Single Source of Truth** for AI agents, code assistants (Cursor, Copilot), and automation workflows. The goal is to ensure consistency, quality, and adherence to our identity across all interactions. 

## 🏢 What is Cubiq?

> **Cubiq is a Product-oriented Software Factory, a Digital Platform for SMBs, and Backend-as-a-Service for Startups. AI-driven, managed by humans: we create, operate, and scale digital businesses in LATAM 🚀**


### General vision

Cubiq is a product-led software factory, we build our own products, we are develping a platform, api + libraries to be effective in doing so. With the help of AI we want to quickly be able to prototype and launch digital projects (like a Factory, build the machine that builds machines), and it also serves other startups whit the APIs we build for ourselves (headless-ly used by their products) acting as a backend-as-a-service providers at the product level. With lots of cool APIs that can be founded at https://api.cubiq.lat/docs
So we have a specific Tech-Stack we use, some Current Products being developed or "produced", some Strategic Objectives, a Tone of voice for articles, some existing companies and programmers we like and use as mentors, and a history of our Milestones. All that can be founded below. 

Cubiq is a company founded in Uruguay, by Nicolas Erramuspe (https://www.linkedin.com/in/nicolas-erramuspe/) and Bruno Tassano (https://www.linkedin.com/in/bruno-tassano-7960a4b5/), in November 2025.
The domain where it lives is at https://www.cubiq.lat

### Tech Stack

* Svelte & Sveltekit for web projects (using Typescript), with Tailwind CSS v4 + DaisyUI for UI.
* Nestjs for their self-hosted API (in an Ubuntu Server via Cloudflare tunnels).
* Tailscale for server orchestration and development access to the API server.
* Docker for fast and standarized deployment of the Nestjs API.
* Telegram API with a Bot in a Managment Group chat to interact, query the API and receive alerts.
* Figma for design.
* Tauri (with Sveltekit) as an app development framework.
* Supabase Managed Postgres database.
* Github, were all our private and public repos live.
* For AI:
    * Opencode (https://opencode.ai/) as an ai coding agent connected to Fireworks AI (https://fireworks.ai/) and/or OpenRouter (https://openrouter.ai/) APIs, used by developers in the command line.
    * Gemini-cli for some free coding command-line agentic coding stuff.
    * Transformers.js for local AI (we use it on our front-ends but mainly in our NestJS API; for example for spam detection in the CMS.Comments endpoints).
    * Claude in the web. 

## Repositories

| Repo | Description |
|------|-------------|
| [cubiq-front](https://github.com/minimo-io/cubiq-front) | Cubiq.lat front-end site and dashboards (private) |
| [cubiq-api](https://github.com/minimo-io/cubiq-api) | Core APIs - the brain powering all products and BaaS (private) |
| [taptapgo-app](https://github.com/minimo-io/taptapgo-app) | TapTapGO craft beer marketplace app (private) |
| [betizen-ssg](https://github.com/minimo-io/betizen-ssg) | iGaming affiliate site (private) |
| [cubiq-ai-context](https://github.com/cubiq-lat/cubiq-ai-context) | This repo - general context for AI agents (public) |

## API Reference

* API Docs: https://api.cubiq.lat/docs
* Main API URL: https://api.cubiq.lat
* Postman Collection: https://documenter.getpostman.com/view/44402542/2sBXVhBqLM

## Current Products
 * TapTapGO: Craft beer marketplace with benefits for clients (can find hard to find beers, earn cashback for buying in the app they can use in local bars associated), trying to solve customer reach for breweries and client managment, so they can focus in producing great beers).
 * Betizen.org: Casinos listings with focus on transparency ("The first Casino, Binary, and Forex listings site with the right incentives: karma, merit, and proof-of-work.").
 * Forex Affiliate Product (no name yet).
 * Appointment scheduling and client management software for beauty salons and clinics.
 * Payments API & Solutions for LATAM.

### Strategic Objectives & Roadmap

Cubiq's goal is to first develop a defined series of products—including Betizen (iGaming affiliation), our Forex affiliation product, the TapTapGo craft beer marketplace, and our SaaS for client management and scheduling for beauty salons and clinics—by January 2027. The objective is to build a business with a sustainable foundation focused on predictable revenue. From there, once our APIs are online and these products are established in the market or at least "live", we will foster the "Cubiq Laboratory" branch, where we will experiment with creating non-linear, asymmetric revenue projects.

The idea is to build a small development and design team that will allow us to execute for both arms of Cubiq, heavily investing time in create the agentic AI tools and processes so we can cut costs, maximize experimentation and revenue.

All our headless front-ends (apps, websites, dashboards) will consume our Nest APIs (the "heart" of Cubiq). That same API will be used in our back-end-as-a-service product.

### Tone of Voice Guidelines when Writting Articles
* **Authority:** We speak as experts who master the technology and business ecosystem in LATAM.
* **Direct and Practical:** We avoid excessive technical jargon. The focus is on value and results.
* **Human and Trustworthy:** We value human curation within our automated processes.
* **Ambition:** Focused on "create, operate, and scale."

## Reference programmers and companies

* DHH and 37Signals.

# History of Milestones

* **March 2026**: A 1yr development cycle of three products in the niches of Forex Affiliation, SaaS and Craft-Beer Marketplace is setup. Funded by the founders, 1/2 and 1/2. The goal is to have the three products plus the APIs live by Jan 2027.
* **January 2026**: Bruno joins as a Co-Founder.
* **November 2025**: Nicolas Founded Cubiq and launched the site and initial dashboards. Idea switch to become the Product-Led Software factory.