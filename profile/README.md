# The Hmars News

<div align="center">
  <img src="https://raw.githubusercontent.com/theHmars/frontend/master/public/assets/fallback.webp" alt="The Hmars News Banner" width="100%">
</div>

Welcome to the official GitHub organization for **The Hmars News**. 

Visit our live publication: [https://thehmars.onrender.com/](https://thehmars.onrender.com/)

*Our old subdomain had to be dropped because the Render account connected to that repository was suspended. Additionally, please be aware that this is primarily an experimental project exploring the capabilities of fully autonomous LLM journalism*

We are a fully autonomous, AI-driven digital newsroom focused on delivering high-velocity, high-quality journalism for the Mizo, Hmar, Kuki, and Thadou communities, as well as broader Northeast India and the globe.

## Our Architecture

Our newsroom operates on a modern, decoupled architecture split across three primary repositories:

1. **[`engine`](https://github.com/theHmars/engine)**
   The heart of our autonomous pipeline. This repository houses the Python-based AI agents (Editor-in-Chief, Social Curator, Writer, etc.) that continuously scrape, triage, deduplicate, and produce news articles. It also handles automated social media broadcasting to platforms like Facebook.
   
2. **`content` (Private Repository)**
   Our immutable "source of truth" database. This repository is kept private to protect raw data. It purely stores the generated Markdown articles and the site's JSON indices. It acts as the secure bridge between the backend `engine` and the `frontend`, keeping our data version-controlled and distinct from our application logic.

3. **[`frontend`](https://github.com/theHmars/frontend)**
   The face of our newsroom. Built with [Astro](https://astro.build/), this repository consumes the markdown files from the `content` repo to statically generate an incredibly fast, dynamic, and SEO-optimized web application deployed on Render.

## The AI Pipeline

Our autonomous newsroom is powered by a multi-agent system:
* **Triage Agent:** Filters incoming raw news streams to find the most relevant and high-priority stories.
* **Deduplication Agent:** Prevents spam and merges conflicting reports into single, coherent sources of truth.
* **Writer Agent:** Transforms raw data into engaging, professional markdown articles.
* **Social Curator:** Automatically selects the most engaging stories and schedules them for our social media channels.

---

*This ecosystem is entirely automated via GitHub Actions, running completely autonomously several times a day.*
