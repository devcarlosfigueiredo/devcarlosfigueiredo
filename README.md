<div align="center">

# José Carlos Figueiredo

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=DevOps+Engineer+%7C+SRE+%7C+Cloud+%26+Observability;AWS+%7C+Azure+%7C+Kubernetes+%7C+Terraform;Prometheus+%7C+Grafana+%7C+CI%2FCD+%7C+IaC" alt="Typing SVG"/>

<h3>DevOps Engineer · SRE · Cloud & Observability</h3>

<p>
  <em>Infraestrutura como código · Observabilidade de produção · Entrega contínua</em><br/>
  🇧🇷 Brasília, Brasil &nbsp;→&nbsp; 🇵🇹 Buscando oportunidades em Portugal
</p>

<!-- Badges de certificação -->
<p>
  <img src="https://img.shields.io/badge/AWS-Solutions_Architect_Associate-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-DevOps_Engineer_Professional-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-Security_Specialty-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
</p>
<p>
  <img src="https://img.shields.io/badge/Azure-AZ--400_DevOps_Expert-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-AZ--104_Administrator-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-AZ--500_Security-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
</p>
<p>
  <img src="https://img.shields.io/badge/Kubernetes-CKA_Certified-326CE5?style=flat-square&logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-DCA_Certified-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Terraform-Associate-7B42BC?style=flat-square&logo=terraform&logoColor=white"/>
  <img src="https://img.shields.io/badge/CompTIA-Network%2B-C8202F?style=flat-square&logo=comptia&logoColor=white"/>
</p>

<!-- Social badges -->
<p>
  <a href="https://linkedin.com/in/devcarlosfigueiredo">
    <img src="https://img.shields.io/badge/LinkedIn-devcarlosfigueiredo-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:devcarlosfigueiredo@gmail.com">
    <img src="https://img.shields.io/badge/Email-devcarlosfigueiredo@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
  <img src="https://komarev.com/ghpvc/?username=devcarlosfigueiredo&style=flat-square&color=58a6ff&label=profile+views"/>
</p>

</div>

---

## 👤 Sobre mim

Engenheiro DevOps com portfólio focado em **observabilidade de produção**, infraestrutura como código e pipelines de entrega contínua. Certificado em AWS, Azure e Kubernetes, com experiência prática em toda a stack SRE: Prometheus, Grafana, Loki, Alertmanager e SLOs baseados no Google SRE Book.

Apaixonado por sistemas resilientes, automação e segurança cloud. Comprometido com documentação técnica de qualidade e commits regulares que evidenciam evolução contínua.

- 🔭 Atualmente desenvolvendo: stack de observabilidade de produção com SLOs e error budgets
- 🌱 Estudando: Zero Trust, hardening Linux, práticas CNCF
- 🎯 Objetivo: primeira oportunidade formal como DevOps/SRE em Portugal
- 📖 Referências: Google SRE Book · CNCF · HashiCorp · AWS Well-Architected

---

## 🚀 Projetos em destaque

### 🔭 [Flask Observability Stack](https://github.com/devcarlosfigueiredo/Flask-Observability-Stack)
> Stack de observabilidade completa de produção para aplicação Flask containerizada

**Stack:** `Prometheus` `Grafana` `Loki` `Alertmanager` `Promtail` `Docker` `SRE`

- SLOs definidos e monitorados: disponibilidade ≥99.5%, latência p99 <500ms, taxa de erro <1%
- Métricas RED via endpoint `/metrics`: requests, latência (histograma), erros
- Error budget burn rate calculado em PromQL para conversas de produto
- Dashboards Grafana como código (JSON versionado) com auto-provisioning
- Pipeline de logs: stdout → Promtail → Loki → Grafana Explore

---

### 🚀 [CI/CD Pipeline — FastAPI](https://github.com/devcarlosfigueiredo/Cicd-pipeline)
> Pipeline CI/CD de 4 estágios com publicação automática no GitHub Container Registry

**Stack:** `FastAPI` `Python 3.12` `Docker` `GitHub Actions` `GHCR` `pytest`

- Pipeline: Lint (black + flake8) → Testes (pytest ≥80%) → Build & Push GHCR → Deploy
- Tagging semântico: `latest` + `sha-<commit>` + `branch` — rastreabilidade total
- Layer caching com GitHub Actions Cache — builds mais rápidos
- Imagem com non-root user, multi-stage build, dependências pinadas

---

### 🏗️ [Terraform AWS Infrastructure](https://github.com/devcarlosfigueiredo/Terraform-aws-infra)
> Infraestrutura AWS completa provisionada 100% como código

**Stack:** `Terraform` `AWS EC2` `VPC` `S3` `IAM` `Docker` `IaC`

- Módulos independentes: VPC, Subnet pública, Internet Gateway, Route Table, Elastic IP
- EC2 com Docker provisionado via `user_data`; Nginx containerizado na porta 80
- Ambientes dev/prod separados via `terraform.tfvars`; volume EBS encriptado por padrão

---

### 🐳 [Flask API + Docker Compose](https://github.com/devcarlosfigueiredo/flask-api-docker)
> API REST multi-container com arquitetura de produção

**Stack:** `Flask` `Docker Compose` `Nginx` `PostgreSQL` `Gunicorn` `Python`

- Stack: Nginx (1.27-alpine) → Flask + Gunicorn → PostgreSQL (16-alpine)
- Multi-stage Dockerfile; non-root user; `depends_on` com `service_healthy`
- Porta da API não exposta ao host — tráfego 100% via Nginx

---

### ⚙️ [TaskFlow API](https://github.com/devcarlosfigueiredo/TaskFlow-API)
> API REST de tarefas com pipeline CI/CD de 5 estágios

**Stack:** `Python 3.12` `Flask` `Docker` `GitHub Actions` `CI/CD` `Pytest`

- Pipeline: Lint → Testes (≥80% cobertura) → Build Docker → Push Docker Hub → Deploy
- Dockerfile multi-stage — imagem de produção sem dependências de desenvolvimento

---

## 🛠️ Stack & tecnologias

**Observabilidade SRE**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F5A623?style=flat-square&logo=grafana&logoColor=white)
![Alertmanager](https://img.shields.io/badge/Alertmanager-E6522C?style=flat-square&logo=prometheus&logoColor=white)

**Infraestrutura & Cloud**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=FF9900)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**CI/CD & Automação**

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.12-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

---

## 📜 Certificações

| Cloud | Containers & IaC | Infra & Redes |
|---|---|---|
| ✅ AWS Solutions Architect Associate | ✅ CKA — Certified Kubernetes Administrator | ✅ CompTIA Network+ |
| ✅ AWS DevOps Engineer Professional | ✅ DCA — Docker Certified Associate | ✅ LPI Linux Essentials |
| ✅ AWS Security Specialty | ✅ HashiCorp Terraform Associate | ✅ ITIL Foundations |
| ✅ AWS Cloud Practitioner | | |
| ✅ AZ-400 — Azure DevOps Engineer Expert | | |
| ✅ AZ-104 — Azure Administrator Associate | | |
| ✅ AZ-500 — Azure Security Engineer | | |
| ✅ AZ-900 — Azure Fundamentals | | |

---

## 📊 GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=devcarlosfigueiredo&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true"/>
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=devcarlosfigueiredo&layout=compact&theme=github_dark&hide_border=true&langs_count=6"/>

</div>

<div align="center">
<img src="https://github-readme-streak-stats.herokuapp.com/?user=devcarlosfigueiredo&theme=github-dark-blue&hide_border=true"/>
</div>

---

## 📚 Formação & atividades

- 🎓 **Tecnólogo em Segurança da Informação** — Gran Faculdade (2026, em curso)
- 📖 Estudo contínuo de SRE, Google SRE Book, Zero Trust e hardening Linux
- 🌐 Comunidades ativas: HashiCorp, CNCF, Prometheus, AWS Community
- 💬 Idiomas: Português (nativo) · Inglês técnico (leitura/escrita)

---

<div align="center">

<sub>Commits regulares · Documentação técnica detalhada · Portfólio em construção contínua</sub>

</div>
<div align="center">

# José Carlos Figueiredo

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=DevOps+Engineer+%7C+SRE+%7C+Cloud+%26+Observability;AWS+%7C+Azure+%7C+Kubernetes+%7C+Terraform;Prometheus+%7C+Grafana+%7C+CI%2FCD+%7C+IaC" alt="Typing SVG"/>

<h3>DevOps Engineer · SRE · Cloud & Observability</h3>

<p>
  <em>Infraestrutura como código · Observabilidade de produção · Entrega contínua</em><br/>
  🇧🇷 Brasília, Brasil &nbsp;→&nbsp; 🇵🇹 Buscando oportunidades em Portugal
</p>

<!-- Badges de certificação -->
<p>
  <img src="https://img.shields.io/badge/AWS-Solutions_Architect_Associate-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-DevOps_Engineer_Professional-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS-Security_Specialty-FF9900?style=flat-square&logo=amazonaws&logoColor=white"/>
</p>
<p>
  <img src="https://img.shields.io/badge/Azure-AZ--400_DevOps_Expert-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-AZ--104_Administrator-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-AZ--500_Security-0078D4?style=flat-square&logo=microsoftazure&logoColor=white"/>
</p>
<p>
  <img src="https://img.shields.io/badge/Kubernetes-CKA_Certified-326CE5?style=flat-square&logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-DCA_Certified-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Terraform-Associate-7B42BC?style=flat-square&logo=terraform&logoColor=white"/>
  <img src="https://img.shields.io/badge/CompTIA-Network%2B-C8202F?style=flat-square&logo=comptia&logoColor=white"/>
</p>

<!-- Social badges -->
<p>
  <a href="https://linkedin.com/in/devcarlosfigueiredo">
    <img src="https://img.shields.io/badge/LinkedIn-devcarlosfigueiredo-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  <a href="mailto:devcarlosfigueiredo@gmail.com">
    <img src="https://img.shields.io/badge/Email-devcarlosfigueiredo@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
  <img src="https://komarev.com/ghpvc/?username=devcarlosfigueiredo&style=flat-square&color=58a6ff&label=profile+views"/>
</p>

</div>

---

## 👤 Sobre mim

Engenheiro DevOps com portfólio focado em **observabilidade de produção**, infraestrutura como código e pipelines de entrega contínua. Certificado em AWS, Azure e Kubernetes, com experiência prática em toda a stack SRE: Prometheus, Grafana, Loki, Alertmanager e SLOs baseados no Google SRE Book.

Apaixonado por sistemas resilientes, automação e segurança cloud. Comprometido com documentação técnica de qualidade e commits regulares que evidenciam evolução contínua.

- 🔭 Atualmente desenvolvendo: stack de observabilidade de produção com SLOs e error budgets
- 🌱 Estudando: Zero Trust, hardening Linux, práticas CNCF
- 🎯 Objetivo: primeira oportunidade formal como DevOps/SRE em Portugal
- 📖 Referências: Google SRE Book · CNCF · HashiCorp · AWS Well-Architected

---

## 🚀 Projetos em destaque

### 🔭 [Flask Observability Stack](https://github.com/devcarlosfigueiredo/Flask-Observability-Stack)
> Stack de observabilidade completa de produção para aplicação Flask containerizada

**Stack:** `Prometheus` `Grafana` `Loki` `Alertmanager` `Promtail` `Docker` `SRE`

- SLOs definidos e monitorados: disponibilidade ≥99.5%, latência p99 <500ms, taxa de erro <1%
- Métricas RED via endpoint `/metrics`: requests, latência (histograma), erros
- Error budget burn rate calculado em PromQL para conversas de produto
- Dashboards Grafana como código (JSON versionado) com auto-provisioning
- Pipeline de logs: stdout → Promtail → Loki → Grafana Explore

---

### 🚀 [CI/CD Pipeline — FastAPI](https://github.com/devcarlosfigueiredo/Cicd-pipeline)
> Pipeline CI/CD de 4 estágios com publicação automática no GitHub Container Registry

**Stack:** `FastAPI` `Python 3.12` `Docker` `GitHub Actions` `GHCR` `pytest`

- Pipeline: Lint (black + flake8) → Testes (pytest ≥80%) → Build & Push GHCR → Deploy
- Tagging semântico: `latest` + `sha-<commit>` + `branch` — rastreabilidade total
- Layer caching com GitHub Actions Cache — builds mais rápidos
- Imagem com non-root user, multi-stage build, dependências pinadas

---

### 🏗️ [Terraform AWS Infrastructure](https://github.com/devcarlosfigueiredo/Terraform-aws-infra)
> Infraestrutura AWS completa provisionada 100% como código

**Stack:** `Terraform` `AWS EC2` `VPC` `S3` `IAM` `Docker` `IaC`

- Módulos independentes: VPC, Subnet pública, Internet Gateway, Route Table, Elastic IP
- EC2 com Docker provisionado via `user_data`; Nginx containerizado na porta 80
- Ambientes dev/prod separados via `terraform.tfvars`; volume EBS encriptado por padrão

---

### 🐳 [Flask API + Docker Compose](https://github.com/devcarlosfigueiredo/flask-api-docker)
> API REST multi-container com arquitetura de produção

**Stack:** `Flask` `Docker Compose` `Nginx` `PostgreSQL` `Gunicorn` `Python`

- Stack: Nginx (1.27-alpine) → Flask + Gunicorn → PostgreSQL (16-alpine)
- Multi-stage Dockerfile; non-root user; `depends_on` com `service_healthy`
- Porta da API não exposta ao host — tráfego 100% via Nginx

---

### ⚙️ [TaskFlow API](https://github.com/devcarlosfigueiredo/TaskFlow-API)
> API REST de tarefas com pipeline CI/CD de 5 estágios

**Stack:** `Python 3.12` `Flask` `Docker` `GitHub Actions` `CI/CD` `Pytest`

- Pipeline: Lint → Testes (≥80% cobertura) → Build Docker → Push Docker Hub → Deploy
- Dockerfile multi-stage — imagem de produção sem dependências de desenvolvimento

---

## 🛠️ Stack & tecnologias

**Observabilidade SRE**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F5A623?style=flat-square&logo=grafana&logoColor=white)
![Alertmanager](https://img.shields.io/badge/Alertmanager-E6522C?style=flat-square&logo=prometheus&logoColor=white)

**Infraestrutura & Cloud**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=FF9900)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**CI/CD & Automação**

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Python](https://img.shields.io/badge/Python_3.12-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

---

## 📜 Certificações

| Cloud | Containers & IaC | Infra & Redes |
|---|---|---|
| ✅ AWS Solutions Architect Associate | ✅ CKA — Certified Kubernetes Administrator | ✅ CompTIA Network+ |
| ✅ AWS DevOps Engineer Professional | ✅ DCA — Docker Certified Associate | ✅ LPI Linux Essentials |
| ✅ AWS Security Specialty | ✅ HashiCorp Terraform Associate | ✅ ITIL Foundations |
| ✅ AWS Cloud Practitioner | | |
| ✅ AZ-400 — Azure DevOps Engineer Expert | | |
| ✅ AZ-104 — Azure Administrator Associate | | |
| ✅ AZ-500 — Azure Security Engineer | | |
| ✅ AZ-900 — Azure Fundamentals | | |

---

## 📊 GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=devcarlosfigueiredo&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true"/>
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=devcarlosfigueiredo&layout=compact&theme=github_dark&hide_border=true&langs_count=6"/>

</div>

<div align="center">
<img src="https://github-readme-streak-stats.herokuapp.com/?user=devcarlosfigueiredo&theme=github-dark-blue&hide_border=true"/>
</div>

---

## 📚 Formação & atividades

- 🎓 **Tecnólogo em Segurança da Informação** — Gran Faculdade (2026, em curso)
- 📖 Estudo contínuo de SRE, Google SRE Book, Zero Trust e hardening Linux
- 🌐 Comunidades ativas: HashiCorp, CNCF, Prometheus, AWS Community
- 💬 Idiomas: Português (nativo) · Inglês técnico (leitura/escrita)

---

<div align="center">

<sub>Commits regulares · Documentação técnica detalhada · Portfólio em construção contínua</sub>

</div>
