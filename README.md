<div align="center">

# Agenor E. Oliveira

### Senior Fullstack Web Engineer

**Building production software since 2002**

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Bun-000000?style=for-the-badge&logo=bun&logoColor=white" alt="Bun" />
  <img src="https://img.shields.io/badge/Vue_3-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes" />
</p>

<p>
  <img src="https://img.shields.io/badge/20%2B_years-experience-0A66C2?style=flat-square" alt="20+ years" />
  <img src="https://img.shields.io/badge/20,000%2B-endpoints_in_production-success?style=flat-square" alt="20,000+ endpoints" />
  <img src="https://img.shields.io/badge/remote-worldwide-orange?style=flat-square" alt="Remote worldwide" />
  <img src="https://img.shields.io/badge/async-first-blueviolet?style=flat-square" alt="Async first" />
</p>

**🇺🇸 English** &nbsp;·&nbsp; [🇧🇷 Português](#-português-brasil)

</div>

---

## 👋 About

I build systems that stay up.

For over twenty years I've worked across the whole stack — TypeScript end to
end, **Bun** and **Node.js** on the server, **Vue 3** and **React** on the front
— and just as comfortably in the layer beneath it: **Go** services,
**Kubernetes**, and the databases and pipelines that keep everything running.

What I actually specialize in is the hard part: **distributed systems that hold
thousands of simultaneous connections and keep working when things go wrong.**

---

## ⚡ Scale & Reliability

> The systems I build are measured in endpoints, not page views.

<table>
<tr>
<td width="33%" align="center">

### 🌐
**20,000+**

endpoints under management
in production

</td>
<td width="33%" align="center">

### 🔌
**1,100+**

concurrent live connections
on a single control plane

</td>
<td width="33%" align="center">

### 🔀
**6**

sharded control-plane servers,
horizontally rebalanced

</td>
</tr>
</table>

**What that demands in practice:**

| | Challenge | How I handle it |
|---|---|---|
| 🔌 | **Thousands of concurrent connections** | Long-lived WebSocket sessions with heartbeat, presence tracked in Redis rather than the database — the hot path never touches durable storage |
| ⚙️ | **Distributed processing under load** | A DAG-based task engine that fans commands out across the fleet, tracks dependencies, and reconciles partial failure without losing work |
| 🌊 | **Reconnect storms & thundering herd** | Exponential backoff with jitter on every dial loop, staggered rollouts, and gating per machine, per network and global |
| 📈 | **Horizontal scaling of a control plane** | Sharding a single-server bottleneck into six, with live migration of running nodes and zero downtime |
| 🛡 | **Graceful degradation** | Systems designed so a failing component degrades the feature, not the fleet — partial availability beats total outage |
| 🔍 | **Diagnosing at scale** | Structured logging, real observability, and the patience to find the layer that's actually broken instead of the one everyone is blaming |

**The scaling lesson I keep relearning:** systems rarely fail because a single
request is slow. They fail because ten thousand clients decide to do the same
thing at the same moment. Almost everything above exists to break up that
synchronization.

---

## 🛠 Tech Stack

<details open>
<summary><b>Core — day to day</b></summary>
<br>

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Bun-000000?style=flat-square&logo=bun&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />

</details>

<details open>
<summary><b>Backend & Architecture</b></summary>
<br>

<img src="https://img.shields.io/badge/REST_APIs-005571?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white" />
<img src="https://img.shields.io/badge/Distributed_Systems-4B32C3?style=flat-square" />
<img src="https://img.shields.io/badge/Event_Driven-FF6600?style=flat-square&logo=apachekafka&logoColor=white" />
<img src="https://img.shields.io/badge/Microservices-2496ED?style=flat-square" />
<img src="https://img.shields.io/badge/RBAC-6E4C13?style=flat-square&logo=keycloak&logoColor=white" />

</details>

<details open>
<summary><b>Data</b></summary>
<br>

<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white" />

</details>

<details open>
<summary><b>DevOps & Infrastructure</b></summary>
<br>

<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white" />
<img src="https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white" />
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/MinIO_/_S3-C72E49?style=flat-square&logo=minio&logoColor=white" />

</details>

<details>
<summary><b>Also in the toolbox</b></summary>
<br>

<img src="https://img.shields.io/badge/Wails_v2-DF0000?style=flat-square&logo=go&logoColor=white" />
<img src="https://img.shields.io/badge/Tailscale_/_Headscale-242424?style=flat-square&logo=tailscale&logoColor=white" />
<img src="https://img.shields.io/badge/Windows_Services-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />

</details>

---

## 🚀 Selected Work

<table>
<tr><td>

### 🌐 Distributed Fleet Management Platform
`Go` · `WebSocket` · `Vue 3` · `TypeScript` · `Kubernetes` · `PostgreSQL` · `Redis`

An end-to-end platform for remote configuration, monitoring and command
execution across **20,000+ retail endpoints**, with **1,100+ nodes connected
live** at any given moment.

A Go API with a WebSocket gateway keeps every agent connected; a DAG-based task
engine orchestrates commands across the fleet and handles dependencies and
partial failure; Redis carries real-time presence so the hot path never writes
to disk; a Vue 3 + TypeScript SPA gives operators role-based control with live
updates. All on Kubernetes with Kustomize and ArgoCD.

**Sole architect**, and primary engineer across all four components.

</td></tr>
<tr><td>

### 🔀 Mesh VPN Sharding & Zero-Downtime Live Migration
`Go` · `Headscale` · `Kubernetes`

A single mesh VPN control plane serving the whole fleet hit its memory ceiling.
Under reconnect storms it stopped delivering network maps and the fleet lost
connectivity — an outage misdiagnosed as a client-side bug for days.

I traced the real cause to control-plane memory exhaustion, designed a sharded
architecture splitting one control plane into **six**, and built the tooling to
rebalance across them. Then migrated **300+ production nodes** between shards
**with zero downtime**.

</td></tr>
<tr><td>

### 🕸 Topology-Driven Network Policy Engine
`Go` · `graph modeling`

Network ACLs were hand-written, and every mistake was an isolation bug — the
kind where one customer's machine can reach another's.

I replaced the whole thing with an engine that derives policy automatically from
network topology, using a connected-component model so that transitive access
falls out of the graph instead of out of someone's memory. Hand-written config
is gone, and so is that entire class of bug.

</td></tr>
<tr><td>

### 💻 Cross-Platform Desktop Agent
`Go` · `Wails v2` · `Windows SCM API`

A headless Windows service plus system-tray GUI, deployed across the fleet, with
an S3-backed auto-update pipeline: **jittered rollout** to avoid stampeding the
update server, and gating per machine, per network and global so a bad release
can be stopped mid-flight.

</td></tr>
</table>

---

## 📦 Open Source

<!--
  PREENCHER conforme publicar (Fase 2 do plano-de-acao.md).
  Enquanto não houver repos, DELETE esta seção inteira — seção vazia
  é pior que seção ausente.
-->

| Project | What it is | Stack |
|---|---|---|
| 🧩 [**[repo-name]**](https://github.com/SEU-USUARIO/[repo]) | [One line] | `Bun` `TypeScript` |
| 🎨 [**[repo-name]**](https://github.com/SEU-USUARIO/[repo]) | [One line] | `Vue 3` `TypeScript` |
| ⚙️ [**[repo-name]**](https://github.com/SEU-USUARIO/[repo]) | [One line] | `Go` |

---

## 💬 Working With Me

**🧠 Senior means asking first.** I ask the right questions before writing code,
and I'll tell you plainly when an idea has a problem.

**🛡 Conservative with working code.** I don't rewrite something because I'd have
written it differently. I'd rather read an unfamiliar codebase carefully than
replace it.

**📊 Honest status updates** — including the bad ones. You'll never be surprised
by a deadline.

**🌍 Async-first.** My written English is professional and I work very well with
distributed teams: written specs, PRs, Slack, documentation. My spoken English
is intermediate and improving. **If your team runs on writing, we'll get along
from day one.**

---

## 📫 Reach Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/agenor-e-oliveira-bb0b91168)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:falecom.codeoliveira@gmail.com)

**Open to remote contract and full-time work worldwide.**

</div>

---
---

<div align="center">

## 🇧🇷 Português (Brasil)

[⬆ Back to English](#-about)

</div>

<details>
<summary><h3>📖 Clique para ler o perfil completo em português</h3></summary>

<br>

### 👋 Sobre

**Construo sistemas que ficam de pé.**

Há mais de vinte anos trabalho em todo o stack — TypeScript nas duas pontas,
**Bun** e **Node.js** no servidor, **Vue 3** e **React** no front — e com o mesmo
conforto na camada de baixo: serviços em **Go**, **Kubernetes**, e os bancos e
pipelines que mantêm tudo rodando.

Minha especialidade de verdade é a parte difícil: **sistemas distribuídos que
sustentam milhares de conexões simultâneas e continuam funcionando quando algo
dá errado.**

---

### ⚡ Escala e Confiabilidade

> Os sistemas que construo se medem em endpoints, não em pageviews.

<table>
<tr>
<td width="33%" align="center">

#### 🌐
**20.000+**

endpoints gerenciados
em produção

</td>
<td width="33%" align="center">

#### 🔌
**1.100+**

conexões simultâneas ao vivo
em um único control plane

</td>
<td width="33%" align="center">

#### 🔀
**6**

servidores de control plane
shardeados e rebalanceáveis

</td>
</tr>
</table>

**O que isso exige na prática:**

| | Desafio | Como eu resolvo |
|---|---|---|
| 🔌 | **Milhares de conexões simultâneas** | Sessões WebSocket de longa duração com heartbeat e presença no Redis, não no banco — o hot path nunca toca armazenamento durável |
| ⚙️ | **Processamento distribuído sob carga** | Task engine baseada em DAG que distribui comandos pela frota, controla dependências e reconcilia falha parcial sem perder trabalho |
| 🌊 | **Tempestade de reconexões e efeito manada** | Backoff exponencial com jitter em todo dial loop, rollout escalonado e gates por máquina, por rede e global |
| 📈 | **Escala horizontal do control plane** | Sharding de um gargalo de servidor único em seis, com migração ao vivo dos nós e zero downtime |
| 🛡 | **Degradação graciosa** | Sistemas em que um componente falho degrada a funcionalidade, não a frota — disponibilidade parcial vence indisponibilidade total |
| 🔍 | **Diagnóstico em escala** | Logs estruturados, observabilidade de verdade, e a paciência de achar a camada realmente quebrada em vez da que todo mundo está culpando |

**A lição de escala que eu reaprendo sempre:** sistemas raramente caem porque uma
requisição está lenta. Caem porque dez mil clientes resolvem fazer a mesma coisa
no mesmo instante. Quase tudo acima existe para quebrar essa sincronia.

---

### 🛠 Stack

**Núcleo** — `TypeScript` `Bun` `Node.js` `Vue 3` `React` `Go`

**Backend e Arquitetura** — `APIs REST` `WebSocket` `Sistemas Distribuídos`
`Event-driven` `Microsserviços` `RBAC`

**Dados** — `PostgreSQL` `MySQL` `MongoDB` `Redis` `SQL`

**DevOps e Infra** — `Kubernetes` `Docker` `CI/CD` `ArgoCD` `Traefik` `Nginx`
`Linux` `MinIO/S3`

**Também** — `Wails v2` `Tailscale/Headscale` `Serviços Windows` `Vite` `Git`

---

### 🚀 Trabalhos Selecionados

#### 🌐 Plataforma Distribuída de Gerenciamento de Frota
`Go` · `WebSocket` · `Vue 3` · `TypeScript` · `Kubernetes` · `PostgreSQL` · `Redis`

Plataforma ponta a ponta para configuração remota, monitoramento e execução de
comandos em **mais de 20.000 endpoints de varejo**, com **1.100+ nós conectados
ao vivo** a qualquer momento.

Uma API em Go com gateway WebSocket mantém cada agente conectado; uma task engine
baseada em DAG orquestra comandos pela frota tratando dependências e falha
parcial; o Redis carrega a presença em tempo real para que o hot path nunca
escreva em disco; uma SPA em Vue 3 + TypeScript dá aos operadores controle com
RBAC e atualização ao vivo. Tudo sobre Kubernetes com Kustomize e ArgoCD.

**Arquiteto único** e engenheiro principal nos quatro componentes.

#### 🔀 Sharding de Mesh VPN e Migração ao Vivo sem Downtime
`Go` · `Headscale` · `Kubernetes`

Um único control plane de mesh VPN atendendo a frota inteira bateu no teto de
memória. Sob tempestade de reconexões parava de entregar os network maps e a
frota perdia conectividade — uma indisponibilidade diagnosticada como bug de
cliente durante dias.

Rastreei a causa real até a exaustão de memória do control plane, projetei a
arquitetura shardeada dividindo um control plane em **seis** e construí a
ferramenta de rebalanceamento. Depois migrei **300+ nós de produção** entre
shards **com zero downtime**.

#### 🕸 Motor de Políticas de Rede Dirigido por Topologia
`Go` · `modelagem em grafo`

As ACLs de rede eram escritas à mão, e cada erro virava um bug de isolamento —
daqueles em que a máquina de um cliente alcança a de outro.

Substituí tudo por um motor que deriva a política automaticamente da topologia,
com modelo de componente conexo, de modo que o acesso transitivo emerge do grafo
em vez de emergir da memória de alguém. A configuração manual sumiu, e essa
classe inteira de bug junto.

#### 💻 Agente Desktop Multiplataforma
`Go` · `Wails v2` · `API SCM do Windows`

Serviço headless para Windows e GUI de bandeja, distribuídos pela frota, com
pipeline de auto-update via S3: **rollout com jitter** para não estourar o
servidor de atualização, e gates por máquina, por rede e global, para que um
release ruim possa ser interrompido em pleno voo.

---

### 💬 Trabalhando comigo

**🧠 Sênior significa perguntar antes.** Faço as perguntas certas antes de
escrever código e digo com clareza quando uma ideia tem problema.

**🛡 Conservador com código que funciona.** Não reescrevo algo só porque eu teria
feito diferente. Prefiro ler com cuidado um código alheio a substituí-lo.

**📊 Status honesto** — inclusive o ruim. Você nunca vai ser surpreendido por um
prazo.

**🌍 Async-first.** Meu inglês escrito é profissional e trabalho muito bem com
times distribuídos: specs escritas, PRs, Slack, documentação. Meu inglês falado é
intermediário e melhorando.

---

**Disponível para trabalho remoto, contrato ou tempo integral, no mundo todo.**

</details>
