# 💫 About Me

🔭 Sr. Software & AI Integration Engineer at **Globant**  
🐶 Passionate about animal welfare causes and looking to collaborate in any way possible  
💬 10+ years in Ruby on Rails · building agentic AI workflows with LangChain & Anthropic Claude  
🏠 Home lab enthusiast — self-hosted infra with Docker, Portainer & Cloudflare Tunnels, AI-assisted  

---

## 🌐 Socials

[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/yvalenta#8336)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=flat-square&logo=instagram&logoColor=white)](https://instagram.com/valencia_ynt)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=flat-square&logo=twitter&logoColor=white)](https://twitter.com/yvalenciat)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/yvalenta)

---

## 💻 Tech Stack

**Core languages & frameworks**  
![Ruby](https://img.shields.io/badge/Ruby-%23CC342D.svg?style=flat-square&logo=ruby&logoColor=white)
![Rails](https://img.shields.io/badge/Rails-%23CC0000.svg?style=flat-square&logo=ruby-on-rails&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

**AI & Agentic**  
![Anthropic Claude](https://img.shields.io/badge/Anthropic%20Claude-191919?style=flat-square&logo=anthropic&logoColor=white)
![Amazon Bedrock](https://img.shields.io/badge/Amazon%20Bedrock-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Agentic Workflows](https://img.shields.io/badge/Agentic%20Workflows-6C63FF?style=flat-square&logoColor=white)

**Cloud & Infrastructure**  
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0080FF?style=flat-square&logo=digitalocean&logoColor=white)
![Heroku](https://img.shields.io/badge/Heroku-430098?style=flat-square&logo=heroku&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Portainer](https://img.shields.io/badge/Portainer-13BEF9?style=flat-square&logo=portainer&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-D42029?style=flat-square&logo=apache&logoColor=white)

**Databases**  
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405e?style=flat-square&logo=sqlite&logoColor=white)
![ElasticSearch](https://img.shields.io/badge/ElasticSearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)

**Monitoring & Tooling**  
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=flat-square&logo=datadog&logoColor=white)
![Netdata](https://img.shields.io/badge/Netdata-00AB44?style=flat-square&logo=netdata&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black)

---

## 🏠 Home Lab — AI-Assisted Self-Hosted Infrastructure

> A personal learning environment where I explore infrastructure, networking, and AI integration end-to-end.  
> Everything here was designed, debugged, and documented with AI assistance — demonstrating what a modern AI-integrated engineer workflow looks like in practice.

### Architecture

Public internet reaches my apps without a single open port on my router.  
The key insight: **Cloudflare Tunnel creates an outbound-only encrypted connection**, so traffic flows in without exposing anything.

```
  [ Internet ]
       │  HTTPS (DNS + TLS via Cloudflare)
       ▼
  [ Cloudflare Edge ]
       │  encrypted tunnel (outbound from server)
       ▼
  [ cloudflared daemon ]  ← runs inside my Ubuntu server
       │
       ▼
  ┌─────────────────────────────────────────────┐
  │              Docker Engine                  │
  │                                             │
  │  ┌──────────────────┐  ┌─────────────────┐ │
  │  │ nginx-proxy-mgr  │  │    Portainer    │ │
  │  │   :80 / :443     │  │     :9000       │ │
  │  └────────┬─────────┘  └─────────────────┘ │
  │           │ routes by hostname              │
  │    ┌──────┴──────────────────┐              │
  │    ▼                         ▼              │
  │  [ cv_app :80 ]   [ loan_calculator :80 ]  │
  │                                             │
  │  [ Netdata ]  CPU · SSH · nginx traffic     │
  └─────────────────────────────────────────────┘
```

### Live services

| Domain | App | Stack |
|--------|-----|-------|
| [cv.ynt.codes](https://cv.ynt.codes) | Personal CV & landing page | HTML · self-contained |
| [loan_calculator.ynt.codes](https://loan_calculator.ynt.codes) | Loan calculator app | React |
| [portainer.ynt.codes](https://portainer.ynt.codes) | Container management UI | Portainer (access-protected) |

### Layer breakdown

| Layer | Tool | What it does |
|-------|------|-------------|
| **Tunnel** | Cloudflare Tunnels + `cloudflared` | Secure public exposure — zero open ports |
| **Reverse proxy** | nginx-proxy-manager | Routes hostnames to containers, manages TLS |
| **Containers** | Docker + Portainer | Runs and manages all services |
| **Monitoring** | Netdata | Real-time CPU, memory, SSH sessions, nginx traffic |
| **OS** | Ubuntu Server | Host system |

### What I learned building this

- How **CGNAT** works and why it blocks traditional port forwarding — and how Cloudflare Tunnels bypasses it entirely
- The difference between **Published applications** (public) and **Private hostnames** (internal/WARP-only) in Cloudflare
- How `cloudflared` establishes a persistent outbound tunnel and why this is more secure than opening ports
- Practical **Docker networking**: container-to-container communication via service names, not IPs
- How **nginx-proxy-manager** routes by `Host` header instead of port, enabling multiple apps on a single server
- **Netdata** as a zero-config monitoring solution for self-hosted environments

### AI in my workflow

I used Claude as a pair-programmer and architecture advisor throughout this setup:

- **Diagnosing issues**: pasted error logs and config snippets to debug tunnel connectivity and Docker networking
- **Explaining concepts**: understanding CGNAT, BGP routing, and how Cloudflare's edge network operates
- **Generating configs**: `docker-compose.yml` structures, nginx rules, Netdata alert thresholds
- **Security review**: validating what's safe to expose publicly vs what needs Cloudflare Access protection
- **Documenting decisions**: turning rough notes into structured architecture docs

> This is what AI-integrated engineering looks like in 2025 — not replacing the engineer, but accelerating every step of the learning and building process.

---

## 🤖 AI Integration Skills

Beyond the home lab, AI is central to my professional work:

```
  ┌─────────────────────────────────────────────────────┐
  │              AI Integration Stack                   │
  │                                                     │
  │  LangChain ──► Chain / Agent orchestration          │
  │  Anthropic Claude ──► Reasoning · text · code gen   │
  │  Amazon Bedrock ──► Multi-model API gateway         │
  │  RAG pipelines ──► Embeddings + vector search       │
  │  Agentic workflows ──► Tool use · multi-step tasks  │
  └─────────────────────────────────────────────────────┘
```

**What I build:**
- CV parsing and enrichment pipelines using Claude Sonnet + LangChain
- Agentic workflows that read, transform, and export structured data
- Multi-model integrations via Amazon Bedrock
- AI-assisted backends in Ruby on Rails and Node.js/Express

---

## 📊 GitHub Stats

![Stats](https://github-readme-stats.vercel.app/api?username=yvalenta&theme=vision-friendly-dark&hide_border=true&include_all_commits=true&count_private=true)

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=yvalenta&theme=vision-friendly-dark&hide_border=true)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=yvalenta&theme=vision-friendly-dark&hide_border=true&include_all_commits=true&count_private=true&layout=compact)

---

### ✍️ Random Dev Quote

![Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark)

---

[![Visit count](https://visitcount.itsvg.in/api?id=yvalenta&icon=6&color=11)](https://visitcount.itsvg.in)
