<div align="center">

# 💫 Yonatan Valencia

**Sr. Software & AI Integration Engineer @ Globant**

*Designing scalable architectures, agentic AI workflows, and self-hosted ecosystems.*

[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/yvalenta#8336)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yvalenta)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/yvalenciat)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/valencia_ynt)

</div>

---

## 🔭 About Me

With over a decade of experience in the **Ruby on Rails** ecosystem and backend engineering, I currently specialize in the convergence of traditional software engineering and **Artificial Intelligence**.

I build agentic workflows (LangChain, n8n, Anthropic Claude, Gemini, Amazon Bedrock) and design robust DevOps infrastructures — from zero-downtime **Kamal 2** deploys to a fully self-hosted **home lab** exposed through a single Cloudflare Tunnel with no open ports. When I'm not optimizing containers or integrating APIs, I enjoy structured swim training and exploring the intersection of technology and brand development within the hospitality and gastronomy sector — currently building the digital presence for **Resplandor**, a Colombian restaurant in Medellín.

---

## 🌌 Skills & Projects Constellation

<div align="center">
  <img src="./skills-projects-graph.svg" alt="Skills and Projects Map" width="90%">
  <br>
  <p><i>An interconnected view of my tech stack, projects, and areas of expertise.</i></p>
</div>

---

## 💻 Tech Stack

<div align="center">

### ⚡ Core & Frameworks
![Ruby](https://img.shields.io/badge/Ruby-%23CC342D.svg?style=flat-square&logo=ruby&logoColor=white)
![Rails](https://img.shields.io/badge/Rails%208.1-%23CC0000.svg?style=flat-square&logo=ruby-on-rails&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Hotwire](https://img.shields.io/badge/Hotwire-FF5F5F?style=flat-square&logo=turbo&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white)

### 🎨 Frontend & Design Systems
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS_v4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![DaisyUI](https://img.shields.io/badge/DaisyUI-5A0EF8?style=flat-square&logo=daisyui&logoColor=white)
![Alpine.js](https://img.shields.io/badge/Alpine.js-8BC0D0?style=flat-square&logo=alpinedotjs&logoColor=black)
![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=flat-square&logo=googlefonts&logoColor=white)
![Figma](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=flat-square&logo=canva&logoColor=white)

### 🧠 AI & Agentic Workflows
![Anthropic Claude](https://img.shields.io/badge/Anthropic%20Claude-191919?style=flat-square&logo=anthropic&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Amazon Bedrock](https://img.shields.io/badge/Amazon%20Bedrock-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

### ☁️ Cloud, Infra & Data
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kamal](https://img.shields.io/badge/Kamal%202-CC0000?style=flat-square&logo=ruby&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare%20Tunnels-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%2017-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![ElasticSearch](https://img.shields.io/badge/ElasticSearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)

</div>

---

## 🏠 Home Lab: AI-Assisted Infrastructure

> A personal learning environment where I explore infrastructure, networking, and container orchestration end-to-end. Everything is designed, debugged, and documented with AI assistance.

<div align="center">
  <img src="./homelab-architecture.svg" alt="Home Lab Architecture" width="90%">
</div>

### 🏗️ Architecture Breakdown

| Layer | Tool | Primary Function |
| :--- | :--- | :--- |
| **Tunnel** | Cloudflare Tunnel (`homelab-tunnel`) + `cloudflared` | Secure public exposure — zero open ports (Zero Trust). One named tunnel routes every subdomain. |
| **Reverse proxy** | Docker network aliases + nginx-proxy-manager | Hostname routing to containers and TLS certificate management. |
| **Containers** | Docker + Portainer | Execution, isolation, and management of all services. |
| **Deploy** | Kamal 2 + Thruster | Zero-downtime Rails deploys, remote `amd64` builds over SSH, extended drain window for long-running AI jobs. |
| **Database** | Supabase (PostgreSQL 17) | External managed Postgres via AWS pooler, shared across dev and prod environments. |
| **Monitoring** | Netdata + Uptime Kuma | Real-time telemetry (CPU, memory, SSH sessions, Nginx traffic) and public status page. |

### 🌐 Published via the tunnel

| App | Route | Type |
| :--- | :--- | :--- |
| Advance Fitness App | `advance-fitness-app.ynt.codes` | Public |
| CV / Portfolio | `cv.ynt.codes` | Public |
| Loan Calculator | `loan_calculator.ynt.codes` | Public + private hostname |
| Portainer | `portainer.ynt.codes` | Public + private hostname |

### 🔍 Key Engineering Learnings
* Deploying a single persistent outbound tunnel with `cloudflared` to bypass **CGNAT** restrictions, eliminating the need for any open port on the home network.
* Architecting internal **Docker** networking so a freshly deployed Kamal container re-joins the right `network-alias` inside the proxy network without manual intervention.
* Tuning **Kamal's `drain_timeout`** well above the default so in-flight AI plan generations (up to ~120s) survive a mid-generation deploy instead of leaving jobs stuck.
* Running dev and prod against the **same external Postgres instance** safely, with clear guardrails around `DATABASE_URL` vs `DEV_DATABASE_URL`.

---

## 🤖 The AI Integration Ecosystem

Beyond the Home Lab, Artificial Intelligence is the core of my professional workflow, acting not as a replacement, but as an engineering accelerator.

```text
  ┌─────────────────────────────────────────────────────┐
  │              AI Integration Stack                   │
  │                                                     │
  │  LangChain ────────► Agent Orchestration            │
  │  Anthropic Claude ─► Reasoning & Generation          │
  │  Gemini 2.5 Flash ─► Primary provider (multi-model)  │
  │  Amazon Bedrock ───► Multi-model API Gateway         │
  │  RAG Pipelines ────► Embeddings + Vector Search      │
  │  n8n ───────────────► Multi-step Agentic Workflows   │
  └─────────────────────────────────────────────────────┘
```

Flagship application: **Advance Fitness**, a gym management platform (Rails 8.1 · Ruby 4.0.5) with AI-generated, editable training and nutrition plans through a multi-provider adapter layer (Gemini by default, Claude as fallback), deployed via Kamal 2 on the home lab and backed by Supabase.

---

## 🎨 Brand & Business

Alongside engineering, I design and build the digital presence for small hospitality and e-commerce brands — single-file, high-conversion landing pages with a distinct brand system per client.

| Project | Description |
| :--- | :--- |
| **Resplandor** | Colombobian estaurant-bar (Medellín) — full brand system, animated signature visual, WhatsApp-first landing page. |
| **FungiLab** | Functional mushroom supplement brand — product-focused landing with animated visual components. |

**Stack:** single-file HTML · Tailwind CSS (JIT via CDN) with custom brand tokens · Alpine.js · Lucide Icons · AOS scroll animations · Google Fonts.

