# cubiq-ai-context
Centralized knowledge base for AI agents working with Cubiq projects.

# 🤖 Cubiq AI Context & Memory

> **We are a Product-oriented Software Factory, a Digital Platform for SMBs, and Backend-as-a-Service for Startups. AI-driven, managed by humans: we create, operate, and scale digital businesses in LATAM 🚀**

---

## 📌 About This Repository

This repository centralizes all the **institutional memory, guidelines, and context** necessary for Artificial Intelligences (LLMs) to work in alignment with **Cubiq**.

It functions as a **Single Source of Truth** for AI agents, code assistants (Cursor, Copilot), and automation workflows. The goal is to ensure consistency, quality, and adherence to our identity across all interactions.
---

## 🏢 What is Cubiq

### Visão Geral

Cubiq is a company founded in Uruguay, by Nicolas Erramuspe (https://www.linkedin.com/in/nicolas-erramuspe/) and Bruno Tassano (https://www.linkedin.com/in/bruno-tassano-7960a4b5/), in November 2025.
The domain where it lives is at https://www.cubiq.lat

Cubiq is a product-led software factory, it builds its own products withs its own sets of libraries and tecnologies created to quickly prototype and launch digital projects, and it also servers other startups whit the APIs they build for themselves (headless-ly used by their products) acting as a backend-as-a-service providers at the product level. With lots of cool APIs that can be founded at https://api.cubiq.lat/docs


Basically they self-host their API which is 

### Tech Stack

* Svelte & Sveltekit for web projects (using Typescript).
* Nestjs for their self-hosted API (in an Ubuntu Server via Cloudflare tunnels).
* Tailscale for server orchestration and development access to the API server.
* Docker for fast and standarized deployment of the Nestjs API.
* Telegram API with a Bot in a Managment Group chat to interact, query the API and receive alerts.
* Figma for design.
* Tauri (with Sveltekit) as an app development framework.
* Supabase Managed Postgres database.
* For AI:
    * Opencode (https://opencode.ai/) as an ai coding agent connected to Fireworks AI (https://fireworks.ai/) and/or OpenRouter (https://openrouter.ai/) APIs, used by developers in the command line.
    * Gemini-cli for some free coding command-line agentic coding stuff.
    * Transformers.js for local AI (we use it on our front-ends but mainly in our NestJS API; for example for spam detection in the CMS.Comments endpoints).
    * Claude in the web. 
      


## Reference programmers and company philosophy

* DHH and 37Signals.

### Current Products
 * TapTapGO: Craft beer marketplace with benefits for clients (can find hard to find beers, earn cashback for buying in the app they can use in local bars associated), trying to solve customer reach for breweries and client managment, so they can focus in producing great beers).
 * Betizen.org: Casinos listings with focus on transparency ("The first Casino, Binary, and Forex listings site with the right incentives: karma, merit, and proof-of-work.").
 * Forex Affiliate Product (no name yet).
 * Appointment scheduling and client management software for beauty salons and clinics.
 * Payments API & Solutions for LATAM.

### Tone of Voice Guidelines when Writting Articles
* **Authority:** We speak as experts who master the technology and business ecosystem in LATAM.
* **Direct and Practical:** We avoid excessive technical jargon. The focus is on value and results.
* **Human and Trustworthy:** We value human curation within our automated processes.
* **Ambition:** Focused on "create, operate, and scale."

### Strategic Objectives & Roadmap

Cubiq's goal is to first develop a series of products—including Betizen (iGaming affiliation), our Forex affiliation product, the TapTapGo craft beer marketplace, and our SaaS for client management and scheduling for beauty salons and clinics—by January 2027. The objective is to build a business with a sustainable foundation focused on predictable revenue. From there, once our APIs are online and these products are established in the market or at least "live", we will foster the "Cubiq Laboratory" branch, where we will experiment with creating non-linear, asymmetric revenue projects.

The idea is to build a small development and design team that will allow us to execute for both arms of Cubiq, heavily investing time in create the agentic AI tools and processes so we can cut costs, maximize experimentation and revenue.

All our headless front-ends (apps, websites, dashboards) will consume our Nest APIs (the "heart" of Cubiq). That same API will be used in our back-end-as-a-service product.