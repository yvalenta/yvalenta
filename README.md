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

I build agentic workflows (leveraging LangChain and Anthropic Claude) and design robust DevOps infrastructures. When I'm not optimizing Docker containers or integrating complex APIs, I enjoy structured swim training and exploring the intersection of technology and brand development within the hospitality and gastronomy sector.

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
![Rails](https://img.shields.io/badge/Rails-%23CC0000.svg?style=flat-square&logo=ruby-on-rails&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

### 🧠 AI & Agentic Workflows
![Anthropic Claude](https://img.shields.io/badge/Anthropic%20Claude-191919?style=flat-square&logo=anthropic&logoColor=white)
![Amazon Bedrock](https://img.shields.io/badge/Amazon%20Bedrock-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)

### ☁️ Cloud, Infra & Data
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
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
| **Tunnel** | Cloudflare Tunnels + `cloudflared` | Secure public exposure — zero open ports (Zero Trust). |
| **Reverse proxy** | nginx-proxy-manager | Hostname routing to containers and TLS certificate management. |
| **Containers** | Docker + Portainer | Execution, isolation, and management of all services. |
| **Monitoring** | Netdata | Real-time telemetry (CPU, memory, SSH sessions, Nginx traffic). |

### 🔍 Key Engineering Learnings
* Deploying persistent outbound tunnels with `cloudflared` to bypass **CGNAT** restrictions, drastically improving security by eliminating the need for open ports.
* Architecting internal **Docker** networking to enable container-to-container communication via isolated service names.
* Implementing `Host` header routing with **Nginx Proxy Manager**, allowing multiple independent applications to run efficiently on a single base host (Ubuntu Server).

---

## 🤖 The AI Integration Ecosystem

Beyond the Home Lab, Artificial Intelligence is the core of my professional workflow, acting not as a replacement, but as an engineering accelerator.

```text
  ┌─────────────────────────────────────────────────────┐
  │              AI Integration Stack                   │
  │                                                     │
  │  LangChain ────────► Agent Orchestration            │
  │  Anthropic Claude ─► Reasoning & Generation         │
  │  Amazon Bedrock ───► Multi-model API Gateway        │
  │  RAG Pipelines ────► Embeddings + Vector Search     │
  └─────────────────────────────────────────────────────┘