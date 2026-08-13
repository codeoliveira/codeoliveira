
<div align="center">

<h1>Agenor E. Oliveira</h1>

<h3>Software Architect &nbsp;·&nbsp; DevOps & Kubernetes Infrastructure Architect</h3>

<p><i>Designing and building systems that hold thousands of simultaneous connections — since 2002.</i></p>

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Bun-000000?style=for-the-badge&logo=bun&logoColor=white" alt="Bun" />
  <img src="https://img.shields.io/badge/Vue_3-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/Nuxt-00DC82?style=for-the-badge&logo=nuxtdotjs&logoColor=white" alt="Nuxt" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes" />
</p>

<p>
  <img src="https://img.shields.io/badge/20%2B%20years-in%20production-0A66C2?style=flat-square" alt="20+ years" />
  <img src="https://img.shields.io/badge/20,000%2B-endpoints%20managed-2EA043?style=flat-square" alt="20,000+ endpoints" />
  <img src="https://img.shields.io/badge/architecture-first-8957E5?style=flat-square" alt="Architecture first" />
  <img src="https://img.shields.io/badge/remote-worldwide-FB8500?style=flat-square" alt="Remote worldwide" />
  <img src="https://img.shields.io/badge/async-first-0891B2?style=flat-square" alt="Async first" />
</p>

<br>

**🇺🇸 English** &nbsp;&nbsp;|&nbsp;&nbsp; [🇧🇷 Português](#-português-brasil)

</div>

<br>

<div align="center">

`─────────────────────────  ⚙  ─────────────────────────`

</div>

<br>

<div align="center">

## 🧭 What I Do

<i>Three roles, one job: making sure the system still works at scale.</i>

</div>

<table>
<tr>
<td width="33%" valign="top">

<div align="center">

### 🏛
**Software Architect**

</div>

I design the system before it exists — service boundaries, data flow, failure
modes, and the trade-offs someone will have to live with in year three.

Distributed architecture, event-driven design, multi-tenant SaaS, RBAC, and
API contracts that survive contact with real clients.

</td>
<td width="33%" valign="top">

<div align="center">

### 🧱
**Fullstack Engineer**

</div>

I ship the whole thing, not a slice of it. TypeScript end to end — **Bun** and
**Node.js** on the server, **Vue 3 / Nuxt** and **React / Next.js** on the front
— plus **Go** services where a single static binary and real concurrency matter.

Web, desktop and mobile from one head.

</td>
<td width="33%" valign="top">

<div align="center">

### ☸️
**DevOps & Infra Architect**

</div>

I don't hand the system to someone else to run. **Kubernetes** cluster design
and orchestration with **Rancher**, GitOps delivery via **ArgoCD**, CI/CD for
every component, ingress, TLS, storage and observability.

I own it in production.

</td>
</tr>
</table>

<br>

<div align="center">

`─────────────────────────  ⚡  ─────────────────────────`

</div>

<br>

<div align="center">

## ⚡ Scale & Reliability

<i>The systems I build are measured in endpoints and concurrent connections — not pageviews.</i>

</div>

<br>

<table>
<tr>
<td width="25%" align="center">

# 🌐
### 20,000+
**endpoints**
<br>under management in production

</td>
<td width="25%" align="center">

# 🔌
### 1,100+
**live connections**
<br>concurrent on a single control plane

</td>
<td width="25%" align="center">

# 🔀
### 6
**sharded servers**
<br>horizontally rebalanced, zero downtime

</td>
<td width="25%" align="center">

# 📅
### 20+
**years**
<br>shipping production software

</td>
</tr>
</table>

<br>

**What that actually demands, and how I handle it:**

<table>
<tr>
<th width="4%"></th>
<th width="30%">Challenge</th>
<th width="66%">Approach</th>
</tr>
<tr><td align="center">🔌</td><td><b>Thousands of simultaneous connections</b></td><td>Long-lived WebSocket sessions with heartbeat; presence tracked in <b>Redis</b>, never in the database — the hot path never touches durable storage</td></tr>
<tr><td align="center">⚖️</td><td><b>Load balancing across processing nodes</b></td><td><b>Stateless APIs</b> by design: no session affinity, no local state, any node answers any request — so scaling out is adding a replica, not a migration project</td></tr>
<tr><td align="center">🗄</td><td><b>Databases that outgrow one server</b></td><td><b>Horizontal sharding</b> with deterministic routing, per-tenant isolation, and live rebalancing between shards while traffic keeps flowing</td></tr>
<tr><td align="center">⚙️</td><td><b>Distributed processing under load</b></td><td>A <b>DAG-based task engine</b> that fans work across the fleet, resolves dependencies, and reconciles partial failure without losing jobs</td></tr>
<tr><td align="center">🌊</td><td><b>Reconnect storms and thundering herd</b></td><td>Exponential <b>backoff with jitter</b> on every dial loop, staggered rollouts, and gating per machine, per network and global</td></tr>
<tr><td align="center">📈</td><td><b>Scaling a control plane horizontally</b></td><td>Sharding a single-server bottleneck into six, with <b>live migration</b> of running nodes and no service interruption</td></tr>
<tr><td align="center">🛡</td><td><b>Graceful degradation</b></td><td>Designed so a failing component degrades <i>a feature</i>, not <i>the fleet</i> — partial availability always beats total outage</td></tr>
<tr><td align="center">🔍</td><td><b>Diagnosing at scale</b></td><td>Structured logging, real observability, and the patience to find the layer that is actually broken instead of the one everyone is blaming</td></tr>
</table>

<br>

<div align="center">

> ### 💡
> **The scaling lesson I keep relearning**
>
> Systems rarely fail because one request is slow.
> They fail because ten thousand clients decide to do the same thing at the same moment.
>
> *Almost everything above exists to break up that synchronization.*

</div>

<br>

<div align="center">

`─────────────────────────  🎯  ─────────────────────────`

</div>

<br>

<div align="center">

## 🎯 What I Build

<i>Four platforms, one architecture mindset.</i>

</div>

<table>
<tr>
<td width="50%" valign="top">

### ☁️ SaaS Platforms
`Multi-tenant` · `Sharded` · `Stateless`

Multi-tenant SaaS designed to scale sideways instead of upward:

- **Database sharding** with deterministic routing and per-tenant isolation
- **Stateless APIs** load-balanced across multiple processing nodes — no sticky sessions, no node that matters more than another
- Horizontal scaling as a routine operation, not a rescue mission
- Tenant onboarding, quotas, RBAC and billing boundaries baked into the model

</td>
<td width="50%" valign="top">

### 🌐 Distributed Systems
`Real-time` · `Fleet-scale` · `Fault-tolerant`

Systems where thousands of agents stay connected and take orders:

- WebSocket gateways holding **1,100+ concurrent live connections**
- **DAG-based task orchestration** across the whole fleet
- Presence and coordination in Redis, durable state in PostgreSQL
- Built assuming the network fails, because it does

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 💻 Desktop Applications
`Windows` · `Linux` · `macOS`

Cross-platform software that runs on the user's own machine:

- **Go** for headless services, agents and native OS integration — one static binary per platform
- **Electron** when the product needs a rich UI and a shared web codebase
- Native OS integration: Windows services (SCM API), system tray, autostart, privilege handling
- Auto-update pipelines with **jittered rollout** and staged gating, so a bad release can be stopped mid-flight

</td>
<td width="50%" valign="top">

### 📱 Mobile Applications
`Flutter` · `iOS` · `Android`

Mobile apps from a single codebase:

- **Flutter** for iOS and Android, sharing the same backend contracts as web and desktop
- Offline-first behavior, sync and conflict resolution
- Real-time features over the same WebSocket infrastructure
- Same API envelope, same auth, same RBAC — one system, many faces

</td>
</tr>
</table>

<br>

<div align="center">

`─────────────────────────  🛠  ─────────────────────────`

</div>

<br>

<div align="center">

## 🛠 Tech Stack

<i>Grouped by layer. Everything here is something I'd defend in a technical conversation.</i>

</div>

<br>

<details open>
<summary><b>&nbsp;⭐&nbsp; Core — day to day</b></summary>
<br>
<div align="center">

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Bun-000000?style=for-the-badge&logo=bun&logoColor=white" />
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Nuxt-00DC82?style=for-the-badge&logo=nuxtdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" />

<br><br>

<img src="https://img.shields.io/badge/SSR_/_SSG-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" />
<img src="https://img.shields.io/badge/SPA_Architecture-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" />

</div>
</details>

<details open>
<summary><b>&nbsp;🏛&nbsp; Architecture & Backend</b></summary>
<br>
<div align="center">

<img src="https://img.shields.io/badge/Distributed_Systems-4B32C3?style=flat-square" />
<img src="https://img.shields.io/badge/Multi--tenant_SaaS-0EA5E9?style=flat-square" />
<img src="https://img.shields.io/badge/Database_Sharding-DC2626?style=flat-square" />
<img src="https://img.shields.io/badge/Stateless_APIs-059669?style=flat-square" />
<img src="https://img.shields.io/badge/Load_Balancing-7C3AED?style=flat-square" />
<img src="https://img.shields.io/badge/Microservices-2496ED?style=flat-square" />
<img src="https://img.shields.io/badge/Event--Driven-FF6600?style=flat-square&logo=apachekafka&logoColor=white" />
<img src="https://img.shields.io/badge/REST_APIs-005571?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white" />
<img src="https://img.shields.io/badge/RBAC-6E4C13?style=flat-square&logo=keycloak&logoColor=white" />

</div>
</details>

<details open>
<summary><b>&nbsp;☸️&nbsp; DevOps, Infrastructure & Orchestration</b></summary>
<br>
<div align="center">

<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Rancher-0075A8?style=for-the-badge&logo=rancher&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white" />

<br><br>

<img src="https://img.shields.io/badge/Cluster_Orchestration-326CE5?style=flat-square&logo=rancher&logoColor=white" />
<img src="https://img.shields.io/badge/GitOps-EF7B4D?style=flat-square&logo=argo&logoColor=white" />
<img src="https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/Kustomize-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white" />
<img src="https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white" />
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/MinIO_/_S3-C72E49?style=flat-square&logo=minio&logoColor=white" />
<img src="https://img.shields.io/badge/Observability-F46800?style=flat-square&logo=grafana&logoColor=white" />

</div>
</details>

<details open>
<summary><b>&nbsp;🗄&nbsp; Data</b></summary>
<br>
<div align="center">

<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-CC2927?style=flat-square&logo=databricks&logoColor=white" />
<img src="https://img.shields.io/badge/Schema_Design-336791?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Query_Tuning-336791?style=flat-square&logo=postgresql&logoColor=white" />

</div>
</details>

<details open>
<summary><b>&nbsp;💻&nbsp; Desktop & Mobile</b></summary>
<br>
<div align="center">

<img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" />
<img src="https://img.shields.io/badge/Electron-47848F?style=for-the-badge&logo=electron&logoColor=white" />
<img src="https://img.shields.io/badge/Wails_v2-DF0000?style=for-the-badge&logo=go&logoColor=white" />

<br><br>

<img src="https://img.shields.io/badge/Windows-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/macOS-000000?style=flat-square&logo=apple&logoColor=white" />
<img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white" />
<img src="https://img.shields.io/badge/iOS-000000?style=flat-square&logo=apple&logoColor=white" />
<img src="https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white" />

</div>
</details>

<details>
<summary><b>&nbsp;🧰&nbsp; Also in the toolbox</b></summary>
<br>
<div align="center">

<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Tailscale_/_Headscale-242424?style=flat-square&logo=tailscale&logoColor=white" />
<img src="https://img.shields.io/badge/Windows_Services-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" />
<img src="https://img.shields.io/badge/Mesh_Networking-242424?style=flat-square&logo=wireguard&logoColor=white" />

</div>
</details>

<br>

<div align="center">

`─────────────────────────  🚀  ─────────────────────────`

</div>

<br>

<div align="center">

## 🚀 Selected Work

<i>Four projects, and what was actually hard about each one.</i>

</div>

<br>

<table>
<tr><td>

### 🌐 &nbsp;Distributed Fleet Management Platform

<sub>`Go` · `WebSocket` · `Vue 3` · `TypeScript` · `Kubernetes` · `Rancher` · `PostgreSQL` · `Redis`</sub>

An end-to-end platform for remote configuration, monitoring and command
execution across **20,000+ retail endpoints**, with **1,100+ nodes connected
live** at any given moment.

A **Go API with a WebSocket gateway** keeps every agent connected. A
**DAG-based task engine** orchestrates commands across the fleet, resolving
dependencies and reconciling partial failure. **Redis** carries real-time
presence so the hot path never writes to disk. A **Vue 3 + TypeScript SPA**
gives operators role-based control with live updates. It all runs on
**Kubernetes**, orchestrated with **Rancher** and delivered via **ArgoCD**.

> **Sole architect** — and primary engineer across all four components.

</td></tr>
<tr><td>

### 🔀 &nbsp;Mesh VPN Sharding & Zero-Downtime Live Migration

<sub>`Go` · `Headscale` · `Kubernetes`</sub>

A single mesh VPN control plane serving the entire fleet hit its memory ceiling.
Under reconnect storms it stopped delivering network maps and the fleet lost
connectivity — an outage that had been misdiagnosed as a client-side bug for
days.

I traced the real cause to **control-plane memory exhaustion**, designed a
sharded architecture splitting one control plane into **six**, and built the
tooling to rebalance across them.

> Then migrated **300+ production nodes** between shards — **with zero downtime**.

</td></tr>
<tr><td>

### 🕸 &nbsp;Topology-Driven Network Policy Engine

<sub>`Go` · `graph modeling`</sub>

Network ACLs were written by hand, and every mistake was an isolation bug — the
kind where one customer's machine can reach another's.

I replaced the whole thing with an engine that **derives policy automatically
from network topology**, using a connected-component model so transitive access
falls out of the graph instead of out of someone's memory.

> Hand-written configuration is gone, and that entire class of bug went with it.

</td></tr>
<tr><td>

### 💻 &nbsp;Cross-Platform Desktop Agent

<sub>`Go` · `Wails v2` · `Windows SCM API`</sub>

A headless **Windows service** plus **system-tray GUI**, deployed across the
whole fleet, with an S3-backed auto-update pipeline: **jittered rollout** so
20,000 machines don't stampede the update server at once, and gating per
machine, per network and global.

> A bad release can be stopped mid-flight, before it reaches the fleet.

</td></tr>
</table>

<br>

<div align="center">

`─────────────────────────  📦  ─────────────────────────`

</div>

<br>

<div align="center">

## 📦 Open Source

</div>

<!--
  PREENCHER conforme publicar (Fase 2 do plano-de-acao.md).
  Enquanto não houver repos, DELETE esta seção inteira (do "─── 📦 ───"
  até o próximo divisor) — seção vazia é pior que seção ausente.
-->

<table>
<tr>
<th width="25%">Project</th>
<th width="50%">What it is</th>
<th width="25%">Stack</th>
</tr>
<tr>
<td>🧩 <a href="https://github.com/SEU-USUARIO/[repo]"><b>[repo-name]</b></a></td>
<td>[One line]</td>
<td><sub><code>Bun</code> <code>TypeScript</code></sub></td>
</tr>
<tr>
<td>🎨 <a href="https://github.com/SEU-USUARIO/[repo]"><b>[repo-name]</b></a></td>
<td>[One line]</td>
<td><sub><code>Vue 3</code> <code>TypeScript</code></sub></td>
</tr>
<tr>
<td>⚙️ <a href="https://github.com/SEU-USUARIO/[repo]"><b>[repo-name]</b></a></td>
<td>[One line]</td>
<td><sub><code>Go</code></sub></td>
</tr>
</table>

<br>

<div align="center">

`─────────────────────────  💬  ─────────────────────────`

</div>

<br>

<div align="center">

## 💬 Working With Me

</div>

<table>
<tr>
<td width="50%" valign="top">

#### 🧠 &nbsp;Senior means asking first

I ask the right questions before writing code, and I'll tell you plainly when
an idea has a problem — preferably before it's expensive.

</td>
<td width="50%" valign="top">

#### 🛡 &nbsp;Conservative with working code

I don't rewrite something because I'd have written it differently. I'd rather
read an unfamiliar codebase carefully than replace it.

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 📊 &nbsp;Honest status — including the bad news

You won't be surprised by a deadline. If something is going wrong, you hear it
while there's still time to react.

</td>
<td width="50%" valign="top">

#### 🌍 &nbsp;Async-first

Written English is professional; I work very well with distributed teams —
specs, PRs, Slack, documentation. Spoken English is intermediate and improving.

</td>
</tr>
</table>

<div align="center">

**If your team runs on writing, we'll get along from day one.**

</div>

<br>

<div align="center">

`─────────────────────────  📫  ─────────────────────────`

</div>

<br>

<div align="center">

## 📫 Reach Me

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/agenor-e-oliveira-bb0b91168)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:falecom.codeoliveira@gmail.com)

<br>

**🌍 Open to remote contract and full-time work worldwide.**

</div>

<br>
<br>

<div align="center">

`═══════════════════════  🇧🇷  ═══════════════════════`

## 🇧🇷 Português (Brasil)

[⬆ Back to English](#-what-i-do)

</div>

<details>
<summary><b>&nbsp;📖&nbsp; Clique para ler o perfil completo em português</b></summary>

<br>

<div align="center">

### Agenor E. Oliveira
#### Arquiteto de Software &nbsp;·&nbsp; Arquiteto de Infraestrutura DevOps com Kubernetes

<i>Projetando e construindo sistemas que sustentam milhares de conexões simultâneas — desde 2002.</i>

</div>

<br>

### 🧭 O que eu faço

<table>
<tr>
<td width="33%" valign="top">

<div align="center">

**🏛 Arquiteto de Software**

</div>

Projeto o sistema antes de ele existir — fronteiras de serviço, fluxo de dados,
modos de falha e os trade-offs com que alguém vai ter de conviver no terceiro
ano.

Arquitetura distribuída, event-driven, SaaS multi-tenant, RBAC e contratos de
API que sobrevivem ao contato com clientes reais.

</td>
<td width="33%" valign="top">

<div align="center">

**🧱 Engenheiro Fullstack**

</div>

Entrego o sistema inteiro, não uma fatia. TypeScript nas duas pontas — **Bun** e
**Node.js** no servidor, **Vue 3 / Nuxt** e **React / Next.js** no front — mais
serviços em **Go** onde binário estático único e concorrência importam de verdade.

Web, desktop e mobile da mesma cabeça.

</td>
<td width="33%" valign="top">

<div align="center">

**☸️ Arquiteto DevOps/Infra**

</div>

Não entrego o sistema para outra pessoa operar. Projeto e orquestro clusters
**Kubernetes** com **Rancher**, entrega GitOps via **ArgoCD**, CI/CD para cada
componente, ingress, TLS, storage e observabilidade.

Eu opero em produção.

</td>
</tr>
</table>

---

### ⚡ Escala e Confiabilidade

> Os sistemas que construo se medem em endpoints e conexões simultâneas — não em pageviews.

<table>
<tr>
<td width="25%" align="center">

# 🌐
### 20.000+
**endpoints**
<br>gerenciados em produção

</td>
<td width="25%" align="center">

# 🔌
### 1.100+
**conexões ao vivo**
<br>simultâneas num único control plane

</td>
<td width="25%" align="center">

# 🔀
### 6
**servidores shardeados**
<br>rebalanceados sem downtime

</td>
<td width="25%" align="center">

# 📅
### 20+
**anos**
<br>entregando software em produção

</td>
</tr>
</table>

<br>

**O que isso exige na prática:**

<table>
<tr>
<th width="4%"></th>
<th width="30%">Desafio</th>
<th width="66%">Como eu resolvo</th>
</tr>
<tr><td align="center">🔌</td><td><b>Milhares de conexões simultâneas</b></td><td>Sessões WebSocket de longa duração com heartbeat; presença no <b>Redis</b>, nunca no banco — o hot path não toca armazenamento durável</td></tr>
<tr><td align="center">⚖️</td><td><b>Balanceamento entre nós de processamento</b></td><td><b>APIs stateless</b> por projeto: sem afinidade de sessão, sem estado local, qualquer nó responde qualquer requisição — escalar é adicionar réplica, não fazer migração</td></tr>
<tr><td align="center">🗄</td><td><b>Bancos que não cabem num servidor</b></td><td><b>Sharding horizontal</b> com roteamento determinístico, isolamento por tenant e rebalanceamento ao vivo com o tráfego rodando</td></tr>
<tr><td align="center">⚙️</td><td><b>Processamento distribuído sob carga</b></td><td><b>Task engine baseada em DAG</b> que distribui trabalho pela frota, resolve dependências e reconcilia falha parcial sem perder jobs</td></tr>
<tr><td align="center">🌊</td><td><b>Tempestade de reconexões e efeito manada</b></td><td><b>Backoff exponencial com jitter</b> em todo dial loop, rollout escalonado e gates por máquina, por rede e global</td></tr>
<tr><td align="center">📈</td><td><b>Escala horizontal do control plane</b></td><td>Sharding de um gargalo de servidor único em seis, com <b>migração ao vivo</b> dos nós e sem interrupção de serviço</td></tr>
<tr><td align="center">🛡</td><td><b>Degradação graciosa</b></td><td>Projetado para que um componente falho degrade <i>uma funcionalidade</i>, não <i>a frota</i> — disponibilidade parcial sempre vence indisponibilidade total</td></tr>
<tr><td align="center">🔍</td><td><b>Diagnóstico em escala</b></td><td>Logs estruturados, observabilidade de verdade, e a paciência de achar a camada realmente quebrada em vez da que todo mundo está culpando</td></tr>
</table>

<br>

<div align="center">

> ### 💡
> **A lição de escala que eu reaprendo sempre**
>
> Sistemas raramente caem porque uma requisição está lenta.
> Caem porque dez mil clientes resolvem fazer a mesma coisa no mesmo instante.
>
> *Quase tudo acima existe para quebrar essa sincronia.*

</div>

---

### 🎯 O que eu construo

<table>
<tr>
<td width="50%" valign="top">

#### ☁️ Plataformas SaaS
<sub>`Multi-tenant` · `Shardeado` · `Stateless`</sub>

SaaS multi-tenant projetado para crescer para o lado, não para cima:

- **Sharding de banco** com roteamento determinístico e isolamento por tenant
- **APIs stateless** balanceadas entre múltiplos nós de processamento — sem sessão grudada, sem nó que importa mais que outro
- Escala horizontal como operação de rotina, não como operação de resgate
- Onboarding de tenant, quotas, RBAC e fronteiras de cobrança no modelo

</td>
<td width="50%" valign="top">

#### 🌐 Sistemas Distribuídos
<sub>`Tempo real` · `Escala de frota` · `Tolerante a falha`</sub>

Sistemas onde milhares de agentes ficam conectados e recebem ordens:

- Gateways WebSocket com **1.100+ conexões simultâneas ao vivo**
- **Orquestração de tarefas em DAG** por toda a frota
- Presença e coordenação no Redis, estado durável no PostgreSQL
- Construídos assumindo que a rede falha, porque ela falha

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 💻 Software Desktop
<sub>`Windows` · `Linux` · `macOS`</sub>

Software multiplataforma que roda na máquina do usuário:

- **Go** para serviços headless, agentes e integração nativa com o SO — um binário estático por plataforma
- **Electron** quando o produto pede UI rica e código web compartilhado
- Integração nativa: serviços Windows (API SCM), bandeja do sistema, autostart, privilégios
- Pipeline de auto-update com **rollout com jitter** e gates escalonados, para interromper um release ruim em pleno voo

</td>
<td width="50%" valign="top">

#### 📱 Aplicativos Mobile
<sub>`Flutter` · `iOS` · `Android`</sub>

Apps mobile a partir de um único código-fonte:

- **Flutter** para iOS e Android, compartilhando os mesmos contratos de backend do web e do desktop
- Comportamento offline-first, sincronização e resolução de conflito
- Recursos em tempo real sobre a mesma infraestrutura WebSocket
- Mesmo envelope de API, mesma autenticação, mesmo RBAC — um sistema, várias faces

</td>
</tr>
</table>

---

### 🛠 Stack

**⭐ Núcleo** — `TypeScript` `Bun` `Node.js` `Vue 3` `Nuxt` `React` `Next.js`
`Go` `SSR/SSG` `Vite`

**🏛 Arquitetura e Backend** — `Sistemas Distribuídos` `SaaS Multi-tenant`
`Sharding de Banco` `APIs Stateless` `Load Balancing` `Microsserviços`
`Event-Driven` `APIs REST` `WebSocket` `RBAC`

**☸️ DevOps, Infra e Orquestração** — `Kubernetes` `Rancher`
`Orquestração de Clusters` `Docker` `ArgoCD` `GitOps` `CI/CD` `Kustomize`
`Helm` `Traefik` `Nginx` `Linux` `MinIO/S3` `Observabilidade`

**🗄 Dados** — `PostgreSQL` `MySQL` `MongoDB` `Redis` `SQL` `Modelagem`
`Tuning de Query`

**💻 Desktop e Mobile** — `Flutter` `Electron` `Wails v2` `Dart` `Windows`
`Linux` `macOS` `Android` `iOS`

**🧰 Também** — `Git` `Tailscale/Headscale` `Serviços Windows` `Bootstrap`
`Mesh Networking`

---

### 🚀 Trabalhos Selecionados

#### 🌐 Plataforma Distribuída de Gerenciamento de Frota
<sub>`Go` · `WebSocket` · `Vue 3` · `TypeScript` · `Kubernetes` · `Rancher` · `PostgreSQL` · `Redis`</sub>

Plataforma ponta a ponta para configuração remota, monitoramento e execução de
comandos em **mais de 20.000 endpoints de varejo**, com **1.100+ nós conectados
ao vivo** a qualquer momento.

Uma **API em Go com gateway WebSocket** mantém cada agente conectado. Uma
**task engine baseada em DAG** orquestra comandos pela frota, resolvendo
dependências e reconciliando falha parcial. O **Redis** carrega a presença em
tempo real para que o hot path nunca escreva em disco. Uma **SPA em Vue 3 +
TypeScript** dá aos operadores controle com RBAC e atualização ao vivo. Tudo
sobre **Kubernetes**, orquestrado com **Rancher** e entregue via **ArgoCD**.

> **Arquiteto único** — e engenheiro principal nos quatro componentes.

#### 🔀 Sharding de Mesh VPN e Migração ao Vivo sem Downtime
<sub>`Go` · `Headscale` · `Kubernetes`</sub>

Um único control plane de mesh VPN atendendo a frota inteira bateu no teto de
memória. Sob tempestade de reconexões parava de entregar os network maps e a
frota perdia conectividade — indisponibilidade diagnosticada como bug de cliente
durante dias.

Rastreei a causa real até a **exaustão de memória do control plane**, projetei a
arquitetura shardeada dividindo um control plane em **seis** e construí a
ferramenta de rebalanceamento.

> Depois migrei **300+ nós de produção** entre shards — **com zero downtime**.

#### 🕸 Motor de Políticas de Rede Dirigido por Topologia
<sub>`Go` · `modelagem em grafo`</sub>

As ACLs de rede eram escritas à mão, e cada erro virava um bug de isolamento —
daqueles em que a máquina de um cliente alcança a de outro.

Substituí tudo por um motor que **deriva a política automaticamente da
topologia**, com modelo de componente conexo, de modo que o acesso transitivo
emerge do grafo em vez de emergir da memória de alguém.

> A configuração manual sumiu, e essa classe inteira de bug foi junto.

#### 💻 Agente Desktop Multiplataforma
<sub>`Go` · `Wails v2` · `API SCM do Windows`</sub>

Serviço headless para **Windows** e **GUI de bandeja**, distribuídos por toda a
frota, com pipeline de auto-update via S3: **rollout com jitter** para que 20.000
máquinas não estourem o servidor de atualização de uma vez, e gates por máquina,
por rede e global.

> Um release ruim pode ser interrompido em pleno voo, antes de alcançar a frota.

---

### 💬 Trabalhando comigo

<table>
<tr>
<td width="50%" valign="top">

**🧠 Sênior significa perguntar antes**

Faço as perguntas certas antes de escrever código e digo com clareza quando uma
ideia tem problema — de preferência antes de ficar caro.

</td>
<td width="50%" valign="top">

**🛡 Conservador com código que funciona**

Não reescrevo algo só porque eu teria feito diferente. Prefiro ler com cuidado
um código alheio a substituí-lo.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**📊 Status honesto — inclusive a má notícia**

Você não vai ser surpreendido por um prazo. Se algo está indo mal, você fica
sabendo enquanto ainda dá tempo de reagir.

</td>
<td width="50%" valign="top">

**🌍 Async-first**

Inglês escrito profissional; trabalho muito bem com times distribuídos — specs,
PRs, Slack, documentação. Inglês falado intermediário e melhorando.

</td>
</tr>
</table>

<div align="center">

<br>

**🌍 Disponível para trabalho remoto, contrato ou tempo integral, no mundo todo.**

</div>

</details>
