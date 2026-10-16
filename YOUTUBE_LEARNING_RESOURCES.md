# YouTube Learning Resources — DevOps, Cloud, DevSecOps, SRE, System Design & AI

> **An integrated, project-first video guide for 2026–2027 (updated 16 October 2026).**  
> **Time:** 12 months at approximately 15 hours/week, with **no more than 3–4 hours/week of videos**.  
> **Primary cloud:** AWS · **IaC:** Terraform · **Delivery:** GitHub Actions/Jenkins + Argo CD · **Runtime:** Docker/Kubernetes/EKS.  
> **Primary YouTube educators:** [Tech Tutorials with Piyush](https://www.youtube.com/@TechTutorialswithPiyush) · [Vishakha Sadhwani](https://www.youtube.com/@vishakha.sadhwani) · [TechWorld with Nana](https://www.youtube.com/@TechWorldwithNana) · [Anton Putra](https://www.youtube.com/@AntonPutra).  
> **Last curated:** 16 October 2026. Video availability, course names, tool versions, and cloud prices can change.

[Start here](#start-here) · [12-month video map](#12-month-video-map) · [Primary creators](#the-four-primary-creators) · [Linux / freeCodeCamp](#linux-and-shell-specialization---freecodecamp) · [System design](#system-design-video-track) · [More channels](#additional-youtube-channels) · [Advanced engineering videos](#advanced-specialist-videos-and-practice-labs--new-october-2026) · [Portfolio](#one-evolving-portfolio-project) · [Track progress](#master-progress-tracker) · [Directory](#source-and-channel-directory)

---

## Start here

### Who this is for

A professional with **10+ years in IT**, an earlier **DevOps-designated role with limited practical DevOps exposure**, about **four recent years in manual QA**, **CKA and CKAD**, and a **product-company DevOps/Cloud Engineer** career goal. The objective is **recent demonstrable implementation and troubleshooting ability**, not another full beginner Kubernetes course.

### How to use the list

1. **Pick one primary teaching resource** for a skill. Watch an additional creator only when they clarify a problem or show a meaningfully different design.
2. **Watch → reproduce → change → break → troubleshoot → document**. For each hour of video, allocate at least two hours to independent practice.
3. **Skip material you can already demonstrate**, especially basic CKA/CKAD subjects. Never present a guided lab as workplace production experience.
4. Prefer **current official docs** when YouTube commands, Kubernetes APIs, IAM patterns, Terraform providers, Helm charts, or AWS services have changed.
5. Use **local `kind`/`k3d` and temporary AWS sandbox infrastructure**. Enable budgets and remove EKS, NAT gateways, load balancers, disks and other chargeable resources when finished.
6. **Do not buy overlapping bootcamps solely for more videos.** The complementary paid learning spine remains Adrian Cantrill (AWS architecture) plus KodeKloud (interactive labs), when needed.

**Link labels:** **Video** = an individual YouTube watch page; **Playlist** = YouTube playlist; **Catalog** = creator's official index; **Code** = GitHub reference; **Channel** = channel page from which to choose relevant uploads. Channel/catalog links are intentional where an exact individual video was not reliably verified.

### Recommended priority

| Priority | Use this creator for | Avoid duplication with |
|---|---|---|
| **1. Anton Putra** | AWS Terraform, EKS, Kubernetes operations, autoscaling, secure CI/CD, observability | Piyush's Terraform/EKS walkthroughs |
| **2. Piyush Sachdeva** | 30-day AWS Terraform, Terraform drift, EKS GitOps, observability, troubleshooting, AIOps | Anton's Terraform/GitOps labs |
| **3. TechWorld with Nana** | Clear explanations for Docker, CI/CD, Argo CD, security and monitoring | Existing CKA/CKAD fundamentals |
| **4. Vishakha Sadhwani** | Full-system DevOps design and an end-to-end AIOps integration case study | Existing AWS/EKS implementations |
| **Specialist channels** | Networking, Linux, secure software supply chains, SRE, instrumentation, platform engineering and AI | Broad, repetitive bootcamps |

---

**New creator picks:** [Kunal / Ashish Pratap / Cloud X Berry](#additional-creators--kunal-kushwaha-ashish-pratap-singh-and-cloud-x-berry) · **Course index:** [Optional paid and free courses](#course-recommendation-index--non-youtube-optional-curated)

**Master course roadmap:** [README.md](./README.md) · **Specialist paid video options:** [Pluralsight / O'Reilly below](#paid-specialist-video-companions--pluralsight-and-oreilly-optional).

## 12-month video map

**Core strategy:** deepen Linux, AWS and architectural fundamentals first; build repeatable cloud infrastructure and delivery; make security intrinsic; operate the service; then integrate AI safely. **System design runs as a parallel 1–2 hour/week track** inside the same 15-hour weekly budget.

| Month | Main learning objective | Must-watch or selected video resource | Independent engineering output |
|---|---|---|---|
| **1** | Linux, networking, Python, Git, troubleshooting | [freeCodeCamp Linux Server (video)](https://www.youtube.com/watch?v=WMy3OzvBWc0); [50 Linux commands (video)](https://www.youtube.com/watch?v=ZtqBQ68cfJc) only for gaps; [Practical Networking (video)](https://www.youtube.com/watch?v=LkolbURrtTs) | Tested Linux health-check tooling and incident notes |
| **2** | AWS networking, IAM, core architecture + system design | [Anton AWS/Terraform playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA); [KodeKloud System Design for Beginners (video)](https://www.youtube.com/watch?v=SE2KF-vxvS0); [Cloud X Berry: proxy vs LB vs gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) | Secure AWS VPC/IAM/network design and an HLD diagram |
| **3** | Terraform modules, state, drift, IaC + scalability | [Piyush AWS Terraform playlist](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp); [Anton Terraform playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA); [ByteByteGo channel](https://www.youtube.com/@ByteByteGo) for caching/scaling | Reusable Terraform modules, remote state, CI checks and capacity estimates |
| **4** | CI/CD, images, EKS, Helm, Argo CD + traffic design | [Piyush EKS GitOps](https://www.youtube.com/watch?v=c_a5e2Dnxkk); [Anton EKS playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXnKY6XmeifEpjIfkWRo9v2l); [Nana Argo CD](https://www.youtube.com/watch?v=MeU5_k9ssrs); [ByteByteGo rate limiter](https://www.youtube.com/watch?v=YXkOdWBwqaA) | Automated EKS delivery, traffic routing and a rollback test |
| **5** | IAM, cloud hardening, secure SDLC | [Anton indexed EKS/IAM/security lessons (catalog)](https://github.com/antonputra/tutorials/blob/main/docs/contents.md); [OpenSSF supply-chain policy discussion (video)](https://www.youtube.com/watch?v=pHDCwjAHJiE) | Threat model and least-privilege AWS/K8s design |
| **6** | DevSecOps, SAST/SCA, image/IaC scanning, SBOM/signing | [Nana DevSecOps with GitHub Actions/Docker Scout (video)](https://www.youtube.com/watch?v=gLJdrXPn0ns); [Vishakha security refresh (playlist)](https://www.youtube.com/playlist?list=PLXkUFcIv0_b41OfwBdph_HYGO_mC7r2un) | Security-gated CI/CD, admission checks, signed images |
| **7** | Prometheus, Grafana, metrics, logs, traces + design | [Piyush Observability playlist](https://www.youtube.com/playlist?list=PLl4APkPHzsUWC89lwHRGxk1GDtS7dkUsE); [Grafana OTel demo](https://www.youtube.com/watch?v=cX74hkdI1zM); [Hello Interview videos](https://www.youtube.com/@hello_interview/videos) for system design | Instrumentation, dashboards, alerts, traces and monitoring-system HLD |
| **8** | SRE, troubleshooting, incident response + resilience design | [Piyush Kubernetes troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc); [Anton operations catalog](https://github.com/antonputra/tutorials/blob/main/docs/contents.md); [Hussein Nasser](https://www.youtube.com/@hnasr) | Three failure investigations, SLOs, recovery runbooks and DR design |
| **9** | Platform engineering, multi-environment GitOps | [Anton Argo CD (playlist)](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkktZoHhmL6sbg7ELNjv9Xw); [DevOps Toolkit channel](https://www.youtube.com/@DevOpsToolkit) | Self-service app template, access controls, promotion workflows |
| **10** | Advanced AWS DevOps, AI-assisted operations | [Vishakha end-to-end DevOps/AIOps introduction (video)](https://www.youtube.com/watch?v=UBzYwNbFCKs); [Piyush AI cost anomaly agent (video)](https://www.youtube.com/watch?v=hULkzJMHf7U) | Evidence-backed read-only operational analysis prototype |
| **11** | AI workload deployment, logging and model operations | [Vishakha DevOps project implementation (video)](https://www.youtube.com/watch?v=abkv1MSk1lU); [CNCF channel](https://www.youtube.com/@cncf) for KServe/cloud-native AI talks | Containerized inference endpoint with tests/monitoring |
| **12** | AIOps, AI security, portfolio and interviewing | [Vishakha AIOps part 4 (video)](https://www.youtube.com/watch?v=WyLWj5MjzCE); [Piyush AI observability catalog](https://www.piyushsachdeva.com/youtube-videos/All) | Read-only AI incident assistant with evaluations |

> **Start applying from Months 4–6** once you can independently explain a working Terraform + CI/CD + EKS project. The 12-month timeline is for depth and specialization, not a prerequisite for interviewing.

---

> **Course substitution rule (October 2026):** If you take Pluralsight Linux Diagnostics, skip redundant freeCodeCamp troubleshooting lectures; if you take Pluralsight observability, skip overlapping paid O'Reilly observability video; keep the hands-on capstone either way.


### Curated 2026 video additions by month (quick access)

| Month | Added videos / playlist | Priority |
|---|---|---|
| **1** | [Kunal Networking](https://www.youtube.com/watch?v=IPvYjXCsTg8) · [Kunal Git/GitHub](https://www.youtube.com/watch?v=apGV9Kg7ics) · [Cloud X Berry networking](https://www.youtube.com/watch?v=TR0RU2pmMeA) · [Cloud X Berry Linux directories](https://www.youtube.com/watch?v=qvjRcZcW8CY) | Watch targeted chapters + troubleshoot |
| **2** | [Ashish Pratap Singh — 30 System Design Concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk) · [Cloud X Berry proxy vs LB vs gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) | HLD with security and HA tradeoffs |
| **3** | [Cloud X Berry — Backend Ecosystem](https://www.youtube.com/watch?v=mZ27vUoOEB0) · [ByteByteGo — Caching Pitfalls](https://www.youtube.com/watch?v=wh98s0XhMmQ) | Document caching/database bottlenecks |
| **4** | [Kunal — GitHub Actions](https://www.youtube.com/watch?v=62N8UiWUdQo) · [Kunal — Argo CD](https://www.youtube.com/watch?v=8YLsQIG2Svo) · [Nana — Argo CD](https://www.youtube.com/watch?v=MeU5_k9ssrs) | Secure pipeline and GitOps rollback |
| **5–6** | [ByteByteGo — Rate Limiter](https://www.youtube.com/watch?v=YXkOdWBwqaA) · [Nana — DevSecOps](https://www.youtube.com/watch?v=gLJdrXPn0ns) | Rate limit and supply-chain scan |
| **7–8** | [Kunal networking revisit](https://www.youtube.com/watch?v=IPvYjXCsTg8) · [Ashish — System Design Interview Approach](https://www.youtube.com/watch?v=l3X1t3kpmwY) | Diagnose distributed failures; mock interviews |
| **9–12** | [DevOps Toolkit](https://www.youtube.com/@DevOpsToolkit) · [ByteByteGo](https://www.youtube.com/@ByteByteGo) · [Hugging Face](https://www.youtube.com/@huggingface) | Platform design and read-only AI operations |
| **1 / advanced** | [Brendan Gregg — Linux Systems Performance](https://www.youtube.com/watch?v=fhBHvsi0Ql0) | CPU, memory, I/O diagnosis with evidence |
| **4–5 / advanced** | [GitHub Actions → AWS OIDC](https://www.youtube.com/watch?v=Sdzd4N6L5Hg) · [official GitHub docs](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) | Least-privilege, short-lived CI/CD credentials |
| **5–6 / advanced** | [Liz Rice — eBPF](https://www.youtube.com/watch?v=ZXDhKUeUUSs) · [Kunal + Cilium](https://www.youtube.com/watch?v=yQoVOumoY5k) · [Cosign + Kyverno](https://www.youtube.com/watch?v=HLb1Q086u6M) | Network policy, flow visibility and signed-image enforcement |
| **7–8 / advanced** | [CNCF — OpenTelemetry hands-on](https://www.youtube.com/watch?v=8CKgAyenEjo) · [OTel Demo](https://opentelemetry.io/docs/demo/) | End-to-end tracing and documented incident analysis |
| **9 / advanced** | [Platform team talk](https://www.youtube.com/watch?v=9lPp-6nJ8bI) · [Backstage video](https://www.youtube.com/watch?v=JbX6V9fz5QA) · [FinOps foundation](https://www.finops.org/training-certification/recommended/new-to-finops/) | A usable developer template and cost controls |

## The four primary creators

### 1. Tech Tutorials with Piyush — Terraform, drift, GitOps, observability and AIOps

**Creator links:** [YouTube channel](https://www.youtube.com/@TechTutorialswithPiyush) · [official all-videos catalog](https://www.piyushsachdeva.com/youtube-videos/All) · [GitHub](https://github.com/piyushsachdeva)

| Months | Video / resource | Type | What to extract | Practice task |
|---|---|---|---|---|
| 1 | [Linux / troubleshooting videos on official catalog](https://www.piyushsachdeva.com/youtube-videos/All) | Catalog | Frequently used operations commands | Find a failed service's root cause with logs |
| 3 | [30 Days of AWS Terraform](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp) | Playlist | Resources, data sources, modules, EKS, state, real projects | Build reusable VPC/IAM modules |
| 3 | [Terraform AWS companion code](https://github.com/piyushsachdeva/Terraform-Full-Course-Aws) | Code | Working samples and practice tasks | Refactor tutorial resources into your own module layout |
| 3, 9 | [Terraform drift detection and remediation](https://www.youtube.com/watch?v=nRgNIy-SDEw) | Video | Drift detection and reconciliation workflow | Detect a manual lab change; inspect a plan before fixing it |
| 4 | [GitOps with Terraform and Argo CD on EKS](https://www.youtube.com/watch?v=c_a5e2Dnxkk) | Video | Installation, App of Apps, configuration sync | Make one source-controlled deployment and test rollback |
| 4, 9 | [GitOps project series](https://www.youtube.com/playlist?list=PLl4APkPHzsUWf8xh_13gKjojsfaUpYeAb) | Playlist | Multi-repo or multi-environment delivery patterns | Separate app and deployment configuration repositories |
| 7 | [Observability Zero to Hero](https://www.youtube.com/playlist?list=PLl4APkPHzsUWC89lwHRGxk1GDtS7dkUsE) | Playlist | Logs, metrics, traces, OpenTelemetry | Trace a request through several services |
| 8 | [Troubleshooting Kubernetes issues](https://www.youtube.com/watch?v=6hqXrYlf5qc) | Video | Structured diagnostic approach | Diagnose FailedScheduling, CrashLoopBackOff and a bad ingress |
| 8 | [SLO, SLI, SLA and error-budget lessons](https://www.piyushsachdeva.com/youtube-videos/All) | Catalog | Reliability measures | Define a request-success SLI and an alert policy |
| 10–12 | [Elastic + Amazon Bedrock cost anomaly agent](https://www.youtube.com/watch?v=hULkzJMHf7U) | Video | AI-driven cost analysis and alerting | Validate anomaly explanations against billing data |
| 10–12 | [AI observability agent videos](https://www.piyushsachdeva.com/youtube-videos/All) | Catalog | Kubernetes / Elastic / Bedrock architecture | Implement read-only suggestions and prompt-injection tests |
| Optional | [10 Weeks of CloudOps](https://github.com/piyushsachdeva/10weeksofcloudops) | Code | Extra challenges | Select one unique project, do not repeat the full course |

**Best value:** the Terraform → GitOps → observability sequence, not another CKA course. **Watch out for:** auto-remediation demonstrations. In your portfolio, drift detection should alert and create a reviewed change rather than auto-apply an unreviewed infrastructure modification.

### 2. Vishakha Sadhwani — system design, end-to-end delivery and AIOps

**Creator links:** [YouTube channel](https://www.youtube.com/@vishakha.sadhwani) · [60DaysToCloud curriculum](https://github.com/vishakhasadhwani/60DaysToCloud)

| Months | Video / resource | Type | What to extract | Practice task |
|---|---|---|---|---|
| 1 (optional) | [All DevOps concepts overview](https://www.youtube.com/watch?v=C4IAGERO3o8) | Video | Big-picture DevOps vocabulary | Map existing skills and select actual gaps |
| 1–3 (optional) | [60DaysToCloud](https://github.com/vishakhasadhwani/60DaysToCloud) | Code | AWS, Linux, IaC and CI/CD mini-project sequence | Do only modules that expose weak areas |
| 4 | [Complete DevOps + AIOps — introduction](https://www.youtube.com/watch?v=UBzYwNbFCKs) | Video | End-to-end problem statement and workflow | Draw a service/deployment architecture |
| 4 | [Architecture walkthrough](https://www.youtube.com/watch?v=GD4mVxHWwzM) | Video | Component boundaries and design choices | Record tradeoffs and trust boundaries |
| 4–7 | [Hands-on DevOps project implementation](https://www.youtube.com/watch?v=abkv1MSk1lU) | Video | Terraform, CI/CD, GitOps, monitoring integration | Adapt stages to your existing capstone |
| 5–6 | [Cloud DevOps crash-course playlist](https://www.youtube.com/playlist?list=PLXkUFcIv0_b41OfwBdph_HYGO_mC7r2un) | Playlist | Kubernetes/cloud-security explanations | Enforce pod-level restrictions and policy checks |
| 10–12 | [Full AIOps Project — Part 4](https://www.youtube.com/watch?v=WyLWj5MjzCE) | Video | Bedrock, Lambda, CloudWatch, Prometheus, Streamlit | Build read-only incident summarization with evidence links |

**Best value:** understanding how complete DevOps and AIOps systems fit together. **Watch out for:** tutorial projects that are deliberately simplified; apply secure AWS IAM, secrets isolation, tests, telemetry and operational review before calling the project production-style.

### 3. TechWorld with Nana — explanations, CI/CD, GitOps and security foundations

**Creator link:** [TechWorld with Nana channel](https://www.youtube.com/@TechWorldwithNana)

| Months | Video / resource | Type | What to extract | Practice task |
|---|---|---|---|---|
| 1 | [DevOps roadmap and concepts](https://www.youtube.com/watch?v=9pZ2xmsSDdo) | Video | How delivery components fit together | Sketch your target toolchain |
| 2–4 | [Docker Tutorial for Beginners — full course](https://www.youtube.com/watch?v=3c-iBn73dDE) | Video | Images, Dockerfiles, Compose, volumes and debugging | Create a multi-stage, non-root container image |
| 2–4 (refresh only) | [Kubernetes full tutorial](https://www.youtube.com/watch?v=X48VuDVv0do) | Video | Architecture, storage, ingress, services | Watch only unfamiliar portions; you hold CKA/CKAD |
| 4 | [GitHub Actions + Docker CI pipeline](https://www.youtube.com/watch?v=R8_veQiYBjI) | Video | Triggers, jobs, workflows, build/publish | Extend with tests, OIDC and signed artifacts |
| 4 | [Jenkins Pipeline tutorial](https://www.youtube.com/watch?v=7KCS70sCoK0) | Video | Pipeline-as-code | Reimplement one GitHub Actions pipeline in Jenkins if needed |
| 4 | [Argo CD tutorial for beginners](https://www.youtube.com/watch?v=MeU5_k9ssrs) | Video | GitOps reconciliation and rollback | Git-based controlled deployment |
| 5–6 | [DevSecOps tutorial — GitHub Actions + Docker Scout](https://www.youtube.com/watch?v=gLJdrXPn0ns) | Video | SAST, scanning, vulnerability review | Add scanning and enforce a failing security gate |
| 7 | [Prometheus architecture explained](https://www.youtube.com/watch?v=h4Sl21AKiDg) | Video | Scraping, exporters and Alertmanager | Add useful application metrics and alert rules |
| 7 | [Nana's Prometheus series and walkthrough](https://dev.to/techworld_with_nana/complete-prometheus-monitoring-tutorial-for-beginners-eoe) | Creator article/video index | Prometheus Operator, scrape targets | Deploy monitoring and a custom exporter |

**Best value:** conceptual clarity before running projects. **Watch out for:** some popular full-length videos are from 2020–2021, so use them for concepts and update Helm, Kubernetes, Jenkins and security configurations against current documentation.

### 4. Anton Putra — AWS/EKS operations, Terraform, GitOps, security and benchmarks

**Creator links:** [YouTube channel](https://www.youtube.com/@AntonPutra) · [official tutorials repository](https://github.com/antonputra/tutorials) · [numbered lesson index](https://github.com/antonputra/tutorials/blob/main/docs/contents.md)

| Months | Video / resource | Type | What to extract | Practice task |
|---|---|---|---|---|
| 2–3 | [Terraform Tutorial on AWS](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA) | Playlist | VPCs, modules, remote state | Build segregated subnets and reusable IaC |
| 3–4 | [AWS EKS Kubernetes full course](https://www.youtube.com/playlist?list=PLiMWaCMwGJXnKY6XmeifEpjIfkWRo9v2l) | Playlist | EKS integration, storage, IAM, networking | Provision private-capable EKS infrastructure |
| 4, 9 | [Argo CD tutorials](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkktZoHhmL6sbg7ELNjv9Xw) | Playlist | Deployment and operations | Add environment promotion and notifications |
| 4–6 | [Lesson 268 — Secure AWS EKS CI/CD with Argo CD + GitHub Actions](https://github.com/antonputra/tutorials/blob/main/docs/contents.md) | Catalog | CI/CD and security integration | CI with short-lived cloud credentials and review gates |
| 5–6 | [Lesson 166 — HardenEKS and EKS IAM/RBAC lessons](https://github.com/antonputra/tutorials/blob/main/docs/contents.md) | Catalog | Kubernetes security checks and access boundaries | Harden IAM, RBAC, policies and network access |
| 7 | [Prometheus/Grafana EKS monitoring lessons](https://github.com/antonputra/tutorials/blob/main/docs/contents.md) | Catalog | EKS application/container monitoring | Add recording rules, alerts and debugging dashboards |
| 8 | [Kubernetes troubleshooting lessons 193–194](https://github.com/antonputra/tutorials/blob/main/docs/contents.md) | Catalog | Deployment, Service, Ingress, TLS troubleshooting | Diagnose a broken ingress and cert renewal |
| 8–9 | [Kubernetes autoscaling and Karpenter lessons](https://github.com/antonputra/tutorials/blob/main/docs/contents.md) | Catalog | HPA/VPA/node scaling tradeoffs | Verify load handling and budget impact |
| 8–9 (optional) | [Performance benchmark playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXmcDLvMQeORJ-j_jayKaLVn) | Playlist | Methodology, latency/throughput tradeoffs | Repeat one experiment with controlled load and limits |

**Best value:** practical AWS cloud engineering beyond Kubernetes exams. **Watch out for:** direct copy/paste of security groups, broad IAM roles, public EKS API endpoints and expensive AWS architecture. Validate independently before deployment.


---

## Additional creators — Kunal Kushwaha, Ashish Pratap Singh and Cloud X Berry

These are **curated supplements**, not three more bootcamps to complete. For your experienced DevOps/Cloud transition, the highest-value material is networking, Git collaboration, CI/CD/GitOps and infrastructure system design. Follow the practice exercises after each video.

### Kunal Kushwaha — Git, Linux, networking, Docker, Kubernetes and GitOps

**Channel:** [Kunal Kushwaha](https://www.youtube.com/@KunalKushwaha) · **Full series:** [DevOps Bootcamp playlist](https://www.youtube.com/playlist?list=PL9gnSGHSqcnoqBXdMwUTRod4Gi3eac2Ak) · **Exercises:** [DevOps-Bootcamp repository](https://github.com/kunal-kushwaha/DevOps-Bootcamp).

| Priority / month | Direct video | What to learn | Independent follow-up |
|---|---|---|---|
| **1 — Month 1** | [Computer Networking — OSI Model and real examples](https://www.youtube.com/watch?v=IPvYjXCsTg8) | DNS, TCP/IP, ports, layers, request flow | Use `dig`, `curl -v`, `ss`, `ip route`, `tcpdump` and TLS tests to diagnose a connectivity failure |
| **2 — Month 1** | [Complete Git and GitHub Tutorial](https://www.youtube.com/watch?v=apGV9Kg7ics) | Branches, merges, commits, collaboration | Open a pull request with automated checks and resolve a merge conflict |
| Optional refresher — Month 1 | [Introduction to Linux and Terminal Commands](https://www.youtube.com/watch?v=iwolPf6kN-k) | Shell, permissions, commands, processes | Debug a failed systemd service without following a recorded solution |
| **3 — Month 4** | [Introduction to GitHub Actions CI/CD](https://www.youtube.com/watch?v=62N8UiWUdQo) | Workflow jobs, triggers, quality gates | Test, scan and publish a container through a CI workflow; use scoped credentials |
| **4 — Month 4** | [Introduction to Argo CD and GitOps](https://www.youtube.com/watch?v=8YLsQIG2Svo) | Desired-state synchronization, promotion, rollback | Use Argo CD to deploy from Git and demonstrate a safe rollback |
| Optional — Month 4 | [Docker Tutorial for Beginners](https://www.youtube.com/watch?v=17Bl31rlnRM) | Container images and runtime basics | Build a multi-stage non-root image |
| Optional — Month 4 | [Kubernetes Architecture Simplified](https://www.youtube.com/watch?v=KVBON1lA9N8) | K8s architecture refresh | Skip if you can independently troubleshoot scheduling, DNS and controllers |

**Recommendation:** Prioritize networking, Git, GitHub Actions and Argo CD. Avoid rewatching all Kubernetes basics merely because they appear in the bootcamp.

### Ashish Pratap Singh — system-design fundamentals and interview framework

**Channel:** [Ashish Pratap Singh](https://www.youtube.com/@ashishps_1) · [System Design playlist](https://www.youtube.com/playlist?list=PLCZ2MME8uzMhow9-hAsSm2-dvfF4ag6wy).

| Months | Direct video | Apply it to DevOps/Cloud |
|---|---|---|
| **2–3** | [System Design Was HARD Until I Learned These 30 Concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk) | Design an AWS web app and defend caching, API gateway, replicas, queues, retries and rate limits |
| **8–9** | [How I Mastered System Design Interviews](https://www.youtube.com/watch?v=l3X1t3kpmwY) | Practice a 40-minute design of a secure CI/CD platform or monitoring system |
| Throughout | [System Design playlist](https://www.youtube.com/playlist?list=PLCZ2MME8uzMhow9-hAsSm2-dvfF4ag6wy) | Select topics that address architecture-review gaps; do not memorize diagrams |

**Name clarification:** Ashish **Pratap Singh** is the system-design educator. Per your request, the other creator's AWS CloudOps material is **not included**.

### Cloud X Berry — short networking, Linux and backend architecture explanations

**Channel:** [Cloud X Berry](https://www.youtube.com/@TheCloudXBerry). This is the identified channel for the earlier “Cloud Berry / Code Berry” questions; a similarly spelled name does not guarantee it is the same creator.

| Months | Direct video | Learning objective |
|---|---|---|
| **1** | [20 Networking Topics Every Developer Should Know](https://www.youtube.com/watch?v=TR0RU2pmMeA) | Trace DNS, routing, TCP and TLS for one HTTP request; annotate failure points |
| **1** | [Linux File Directories Explained](https://www.youtube.com/watch?v=qvjRcZcW8CY) | Explain `/etc`, `/var/log`, `/proc`, `/sys`, `/home`, `/tmp` and where failures leave evidence |
| 1 (optional) | [Every Core Linux Concept Explained](https://www.youtube.com/watch?v=ToS3YSLyjWI) | Refresh kernel, process, filesystem and shell vocabulary |
| **2** | [Reverse Proxy vs Load Balancer vs API Gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) | Compare ALB, NGINX ingress and API Gateway in an AWS traffic flow |
| **3–4** | [The Backend Ecosystem Explained](https://www.youtube.com/watch?v=mZ27vUoOEB0) | Connect app code, DB, Redis, Kafka, Docker, Kubernetes, CI/CD and telemetry |
| 3–4 (optional) | [Backend Interview Fundamentals](https://www.youtube.com/watch?v=PsM_4WTuI8Y) | Review authentication, indexes, transactions, retries, idempotency and rate limits |
| 2 (optional) | [System Design Explained in 4 Minutes](https://www.youtube.com/watch?v=NkO7B2eXdLw) | Quick orientation only; then practice full system design |

**Time budget:** Cloud X Berry is a 20–45-minute/week *optional* refresher; your labs, not your watch time, determine progress.

---

## Linux and shell specialization - freeCodeCamp

**Primary choice for Month 1:** the Linux Server Course. Since you already have CKA/CKAD, you need Linux operations and failure diagnosis more than another beginner certification overview. **Do not watch four full Linux courses.** Choose the primary and a scripting supplement; use the others only where a skills check reveals gaps.

| Order | Course / link | Recommended use | Practical result |
|---|---|---|---|
| **1 - primary** | [freeCodeCamp: Linux Server Course - System Configuration and Operation (Shawn Powers)](https://www.youtube.com/watch?v=WMy3OzvBWc0) | Month 1: boot, services, processes, permissions, storage/LVM, logs, networking, server configuration. Published in 2021; verify version-sensitive details. | Diagnose failed `systemd` service, full disk, permission and network issues. |
| **2 - essential supplement** | [freeCodeCamp: Bash Scripting Tutorial for Beginners (Herbertech)](https://www.youtube.com/watch?v=tK9Oc6AEnR4) | Month 1: Bash variables, conditions, loops, functions, text processing and exit codes. | Tested service-health and log-analysis scripts; add ShellCheck. |
| 3 - if CLI is rusty | [freeCodeCamp: The 50 Most Popular Linux & Terminal Commands (Colt Steele)](https://www.youtube.com/watch?v=ZtqBQ68cfJc) | Selected chapters only: `grep`, `find`, pipes, `ps`, `top`, `chmod`, `chown`, `tar`. | Command-line diagnostic cheat sheet. |
| 4 - alternative | [freeCodeCamp: Introduction to Linux - Full Course for Beginners](https://www.youtube.com/watch?v=sWbUDq4S6Y8) | Replace, not add to, the command refresher if you need a more systematic beginning. | Explain filesystem, user/process and shell fundamentals. |

**Free additional practice:** [MIT Missing Semester](https://missing.csail.mit.edu/2026/) for shell, Git and debugging; [SadServers](https://sadservers.com/scenarios) for diagnosing broken machines; [KodeKloud Linux labs](https://kodekloud.com/) for exercises.

**Month 1 competency gate**

- [ ] Diagnose failed `systemd` service startup from `journalctl` and exit status.
- [ ] Investigate a DNS/TCP/TLS problem using `dig`, `ss`, `curl` and `openssl`.
- [ ] Write scripts with input validation, error handling, logging, meaningful return codes and tests.
- [ ] Complete at least six SadServers Linux/network troubleshooting challenges.
- [ ] Document symptom, hypothesis, evidence, root cause and safe recovery for two failures.

---

## System design video track

**Goal:** learn to explain the architecture of systems you deploy, not just write Terraform and Kubernetes YAML. For DevOps/Cloud/SRE interviews, prioritize **high-level infrastructure design** (reliability, security, networking, cost, failure modes and operations), not exhaustive low-level object-oriented design. Schedule **1-2 hours/week inside your existing 15-hour budget**, replacing supplementary video time.

### Suggested order and links

| Order | Creator / video | Where it fits | Why it helps and practical task |
|---|---|---|---|
| **1 - primary starting video** | [KodeKloud - System Design for Beginners (2026)](https://www.youtube.com/watch?v=SE2KF-vxvS0) | Month 2 | Covers requirements, scaling, load balancing, SQL/NoSQL, caching, indexes, replication and sharding; includes accompanying labs. **Task:** draw a 3-tier AWS app; add Redis and database replication and explain tradeoffs. |
| **2 - interview overview** | [freeCodeCamp - Software System Design for Beginners (Gaurav Sen)](https://www.youtube.com/watch?v=m8Icp_Cid5o) | Months 2-3 | Architecture/design approach through a streaming application. **Task:** write functional/nonfunctional requirements, components and failure modes before a diagram. |
| **3 - visual concepts** | [ByteByteGo - YouTube channel](https://www.youtube.com/@ByteByteGo) · [System Design 101 diagrams](https://github.com/ByteByteGoHq/system-design-101) | Months 2-12 | Watch by gap: load balancers, caching, replication, queues/Kafka, databases, rate limiting, URL shorteners and AI systems. **Task:** justify component choices with scale/cost/reliability constraints. |
| 4 - concrete traffic design | [ByteByteGo - Rate Limiter: Token Bucket, Leaky Bucket, Scaling](https://www.youtube.com/watch?v=YXkOdWBwqaA) | Months 4-6 | **Task:** implement API rate limits and measure fairness, burst behavior and 429 handling. |
| 5 - core proxy concepts | [Cloud X Berry - Reverse Proxy vs Load Balancer vs API Gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) | Months 2-4 | **Task:** draw an end-to-end request path through DNS, ALB/ingress, API gateway where warranted and backend services. |
| 6 - quick concepts | [Cloud X Berry - YouTube channel](https://www.youtube.com/@TheCloudXBerry) | Months 2-4 | Short concept refreshers on backend fundamentals and system design; do not substitute for the full labs. |
| 7 - deeper networking | [Hussein Nasser - Backend Engineering Show](https://www.youtube.com/@hnasr) | Months 2, 7-8 | TCP, TLS, reverse proxies, connection pooling, timeouts, database internals. **Task:** explain and reproduce a network timeout/failure. |
| **8 - interview drill** | [Hello Interview - System Design videos](https://www.youtube.com/@hello_interview/videos) · [Free written guide](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction) | Months 7-12 | Practice describing distributed schedulers, queues, rate limiters, caches, monitoring and storage with explicit tradeoffs. |
| 9 - advanced concepts | [Gaurav Sen channel](https://www.youtube.com/@gkcs) · [Arpit Bhayani](https://www.youtube.com/@ArpitBhayani) | Months 5-9 | Consistent hashing, databases, messaging, concurrency and distributed design; choose only the videos relevant to your capstone. |
| 10 - case studies | [CodeKarle](https://www.youtube.com/@codeKarle) | Months 6-9 | Draw full designs with operational concerns and compare alternatives. |
| 11 - optional deep dive | [Jordan Has No Life](https://www.youtube.com/@jordanhasnolife5163) | Months 9-12 | Deeper distributed systems; not required for the initial DevOps transition. |
| 12 - AI architecture | [ByteByteGo AI-related videos](https://www.youtube.com/@ByteByteGo/videos) · [DevOps & AI Toolkit](https://www.youtube.com/@DevOpsToolkit) | Months 10-12 | AI inference, agents, security and operational tradeoffs. **Task:** design a read-only AI incident assistant. |

> **Naming note:** Earlier questions referred to **"Code Berry"**. The closest identified channel was **Cloud X Berry**; this document does not claim they are the same creator. If you meant another channel, replace those links with the correct channel URL.

### What to design in parallel with hands-on projects

| Roadmap months | System-design question | Engineering evidence |
|---|---|---|
| 1-2 | Design a secure highly available AWS application. | VPC, AZs, IAM, DNS, TLS, ALB, threat model, cost notes. |
| 3-4 | Design a scalable delivery platform. | IaC modules, CI/CD, ECR, EKS, GitOps, canary/rollback, capacity estimates. |
| 5-6 | Design API protection and a software supply chain. | Rate limiting, authentication, isolation, signing, policy gates, blast-radius analysis. |
| 7-8 | Design observability + disaster recovery. | SLIs/SLOs, metric pipeline, tracing, RTO/RPO, failure tests, recovery notes. |
| 9 | Design a multi-team internal developer platform. | Tenant isolation, approval workflows, templates, policies, cost ownership. |
| 10-12 | Design a secure AI-powered incident assistant. | Retrieval boundaries, redaction, permission control, evaluation, latency/cost. |

### Six-week system-design mini-track (can start in Month 2)

- [ ] **Week 1:** KodeKloud System Design + basic HLD for an AWS web app.
- [ ] **Week 2:** ByteByteGo caching/replication + Redis and database scale tradeoffs.
- [ ] **Week 3:** Cloud X Berry + Hussein Nasser: DNS, TLS, proxy, load balancer, ingress and API gateway.
- [ ] **Week 4:** ByteByteGo messaging and rate-limiting: queue, retries, dead-letter queue and idempotency.
- [ ] **Week 5:** Hello Interview: architect a secure multi-team CI/CD + Kubernetes platform.
- [ ] **Week 6:** Present two 35-45 minute whiteboard designs, with requirements, estimates, tradeoffs, failure handling, security and cost.

**System-design interview structure:** clarify requirements -> estimate load and constraints -> draw components and dataflow -> explain availability/security -> explore bottlenecks and incident scenarios -> articulate alternatives, cost and operational tradeoffs.

**Optional paid courses, only after free practice:** [ByteByteGo System Design Interview](https://bytebytego.com/courses/system-design-interview), [Design Gurus Grokking System Design](https://www.designgurus.io/course/grokking-the-system-design-interview), or [AlgoExpert SystemsExpert/InfraExpert](https://www.algoexpert.io/). For your specific career goal, InfraExpert's infrastructure-oriented exercises may be more relevant than generic algorithms drills. No paid system-design subscription is required for the first pass.

---

## Additional YouTube channels

These **fill gaps**, not replace the four creators above. The links below are channel links unless a specific video is clearly marked.

| Gap | Channel / suggested video | When | What to do after watching |
|---|---|---|---|
| **Networking / DNS / routing** | [Practical Networking (channel)](https://www.youtube.com/@PracticalNetworking) · [OSI Model: A Practical Perspective (video)](https://www.youtube.com/watch?v=LkolbURrtTs) | Months 1–2 | Diagnose DNS, TLS and routing failures with `dig`, `curl`, `openssl` and `traceroute` |
| **Short IT fundamentals refreshers** | [CBT Nuggets YouTube](https://www.youtube.com/@cbtnuggets) · [Free intro-to-IT catalog](https://www.cbtnuggets.com/it-training/intro-to-it) | Months 1, 5 (optional) | Sample systems administration and cybersecurity fundamentals only if needed; full courses may require a subscription |
| **Backend internals** | [Hussein Nasser — Backend Engineering Show](https://www.youtube.com/@hnasr) | Months 1, 8 | Explain connection handling, reverse proxies, timeouts, TCP/TLS and latency |
| **Docker production practice** | [Bret Fisher — Docker and DevOps](https://www.youtube.com/@BretFisher) | Months 2–4 | Improve Dockerfile caching, image size, non-root users and multi-stage builds |
| **Cloud infrastructure end-to-end** | [DevOps Directive](https://www.youtube.com/@devopsdirective) | Months 3–4 | Compare project layout with your Terraform/Kubernetes repo |
| **Platform engineering / Crossplane** | [DevOps Toolkit — Viktor Farcic](https://www.youtube.com/@DevOpsToolkit) | Months 9–12 | Build a template and design developer self-service boundaries |
| **Cloud-native security and Kubernetes ecosystem** | [CNCF](https://www.youtube.com/@cncf) | Months 5–12 | Watch KubeCon talks about policies, Sigstore, Cilium, OpenTelemetry or KServe |
| **Secure supply chain** | [OpenSSF — Policy, Security, and the Software Supply Chain (video)](https://www.youtube.com/watch?v=pHDCwjAHJiE) | Months 5–6 | Produce SBOM, evaluate dependencies, verify image signature |
| **Observability, metrics and traces** | [Grafana channel](https://www.youtube.com/@Grafana) · [OpenTelemetry demo community call (video)](https://www.youtube.com/watch?v=cX74hkdI1zM) | Month 7 | Correlate request latency with traces, RED metrics and logs |
| **PromQL and instrumentation** | [PromLabs learning resources](https://promlabs.com/) | Month 7 | Write a useful error-rate and latency query, alert and dashboard |
| **AWS design and security** | [AWS Events channel](https://www.youtube.com/@AWSEventsChannel) | Months 2, 5, 8 | Choose AWS re:Invent deep dives on IAM, EKS, Well-Architected and incident response |
| **AI/ML operational lifecycle** | [DataTalks.Club](https://www.youtube.com/@DataTalksClub) | Months 10–11 | Create a versioned model-serving pipeline with tests and monitoring |
| **AI agents and evaluation** | [Hugging Face](https://www.youtube.com/@huggingface) | Months 11–12 | Evaluate an incident-analysis agent and bound its available tools |
| **System design / distributed systems** | [ByteByteGo](https://www.youtube.com/@ByteByteGo) · [Gaurav Sen](https://www.youtube.com/@gkcs) · [Arpit Bhayani](https://www.youtube.com/@ArpitBhayani) | Months 2–12 | Explain caches, rate limits, queues, replicas, failure domains, and validate one real architecture decision |

**Also useful outside YouTube:** [MIT Missing Semester](https://missing.csail.mit.edu/2026/), [Harvard CS50 Python](https://cs50.harvard.edu/python/), [SadServers](https://sadservers.com/scenarios), [AWS EKS Workshop](https://www.eksworkshop.com/docs/introduction/), [HashiCorp Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials), [Google SRE books](https://sre.google/books/), [OWASP GenAI Security](https://genai.owasp.org/), and [OpenTelemetry Demo](https://opentelemetry.io/docs/demo/). Use these to verify and practice what videos teach.

---

## Advanced specialist videos and practice labs — new October 2026

> **Priority:** These are *optional targeted supplements*, not another full course or a change to the 12-month plan. Select a video only for a current gap; spend at least twice the viewing time implementing and diagnosing the associated exercise. **Start with Linux performance, GitHub OIDC and OpenTelemetry.** Some videos demonstrate older tool versions; follow the **current official documentation** for production configuration.

### Six priority YouTube videos — direct links

| Priority / month | Video (direct YouTube link) | Focus and concrete evidence |
|---|---|---|
| **1 · Month 1** | [Brendan Gregg — Linux Systems Performance (USENIX LISA)](https://www.youtube.com/watch?v=fhBHvsi0Ql0) · [speaker notes](https://www.brendangregg.com/blog/2020-03-08/lisa2019-linux-systems-performance.html) | Use a systematic USE/observability approach; capture a controlled CPU, memory or disk-I/O bottleneck using `vmstat`, `mpstat`, `iostat`, `pidstat`, `perf` where available, and explain the evidence. |
| **2 · Months 5–6** | [Liz Rice — Cloud Native Superpowers with eBPF](https://www.youtube.com/watch?v=ZXDhKUeUUSs) | Understand Linux hooks, packet visibility and how eBPF helps Kubernetes networking, security and observability. Describe the datapath and limitations without assuming every cluster uses Cilium. |
| **3 · Months 5–6** | [Civo with Kunal Kushwaha — Cilium: Networking, Security & Observability](https://www.youtube.com/watch?v=yQoVOumoY5k) | Try Cilium/Hubble in an isolated disposable cluster; demonstrate default-deny and explicit allow policies, and show allowed versus rejected traffic. |
| **4 · Month 7** | [CNCF — OpenTelemetry Hands-on Tutorial](https://www.youtube.com/watch?v=8CKgAyenEjo) | Add application instrumentation and a Collector, correlate traces/logs/metrics, and write a latency root-cause note. |
| **5 · Month 6** | [DevOps Toolkit — Signing and Verifying Container Images with Sigstore Cosign and Kyverno](https://www.youtube.com/watch?v=HLb1Q086u6M) | Sign a test image and enforce trusted image admission; document a rejected unsigned image and signature trust conditions. **Use current Cosign/Kyverno policies, not 2022 commands verbatim.** |
| **6 · Month 9** | [Camille Fournier and Ian Nowland — Starting and Scaling a Platform Engineering Team](https://www.youtube.com/watch?v=9lPp-6nJ8bI) | Treat an internal platform as a product: define golden paths, user journeys, boundaries and measurable developer experience outcomes. |

### Additional practical videos and free official labs

| Month | Video, course or lab | Why it fills a gap | Deliverable |
|---|---|---|---|
| **4–5** | [GitHub Actions to AWS using OIDC (video)](https://www.youtube.com/watch?v=Sdzd4N6L5Hg) · [GitHub official OIDC → AWS documentation](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) | Replace static AWS secrets with short-lived federated credentials, using restrictive trust policy claims and least privilege. | A CI workflow that assumes a narrowly scoped AWS IAM role; proof that unauthorized repo/ref attempts are denied. |
| **6** | [Isovalent — Getting Started with Cilium lab](https://isovalent.com/labs/cilium-getting-started/) · [Cilium documentation](https://docs.cilium.io/en/stable/) | Hands-on network policy enforcement, identity and Hubble flow visibility. | Network-policy YAML, allowed/denied connectivity tests and captured flow evidence. |
| **7** | [Grafana — Getting Started with OpenTelemetry (video)](https://www.youtube.com/watch?v=Xhh9V7uRP88) · [OpenTelemetry documentation](https://opentelemetry.io/docs/) | Instrumentation and Collector configuration concepts. | Trace a request end-to-end with correlation IDs. |
| **7–8** | [OpenTelemetry Astronomy Shop Demo (free project)](https://opentelemetry.io/docs/demo/) | A maintained multi-service lab to practice observability, fault injection and debugging. | Three controlled investigations, trace screenshots, alerts and an incident write-up. |
| **9** | [TeKanAid — Backstage Crash Course (video)](https://www.youtube.com/watch?v=JbX6V9fz5QA) · [Backstage official documentation](https://backstage.io/docs/) | Prototype a service catalog and a developer self-service template; do not require a portal if a documented CLI template is more appropriate. | One self-service app template with access boundaries and resource cleanup. |
| **9** | [FinOps Foundation — Getting Started with FinOps (free learning resources)](https://www.finops.org/training-certification/recommended/new-to-finops/) · [FinOps Framework](https://www.finops.org/framework/) | Understand tagging, attribution, budgets, right-sizing and trade-offs. | A sample cost breakdown, budget alert, cleanup policy and savings proposal. |

> **Link hygiene:** Links marked *video* open specific YouTube watch pages provided in the curated recommendations; courses/labs link to the official project or publisher. A YouTube video may be renamed or removed. If a direct link no longer works, search the indicated talk title on the publisher's channel and keep the authoritative documentation as the implementation reference.

### Recommended watch/build order — without increasing study hours

1. **Linux:** Brendan Gregg → one reproducible Linux performance incident (Month 1).
2. **Pipeline security:** GitHub Actions AWS OIDC tutorial → short-lived credential workflow with constrained trust (Months 4–5).
3. **Cloud-native internals:** Liz Rice eBPF → Cilium/Kunal explanation → Isovalent network-policy lab (Months 5–6).
4. **Supply chain:** Cosign/Kyverno video → signed-image rejection test (Month 6).
5. **Observability:** CNCF OpenTelemetry → Grafana supplement only if needed → Astronomy Shop incident drills (Months 7–8).
6. **Developer platform and cost:** platform-team talk → Backstage optional → FinOps foundation (Month 9).

### Advanced track checklist

- [ ] Record a Linux resource-pressure investigation with commands, observations and a specific hypothesis.
- [ ] Authenticate GitHub Actions to AWS through OIDC, without access keys, with a restrictive role trust policy.
- [ ] Explain a pod-to-pod packet path and inspect flows using Cilium/Hubble in an isolated cluster.
- [ ] Prove that a default-deny policy blocks unexpected Kubernetes egress or ingress.
- [ ] Generate a signed test image and demonstrate rejection of an untrusted one.
- [ ] Instrument a service and correlate metrics, logs and traces while investigating latency.
- [ ] Write a reproducible incident report against the OpenTelemetry Demo, including recovery evidence.
- [ ] Deliver a self-service platform workflow with explicit permissions, budget tags and teardown.

**Keep costs and scope controlled:** Prefer `kind`/`k3d`, Isovalent's browser labs and the OpenTelemetry Demo locally. When using EKS, NAT gateways, public load balancers or observability SaaS, set budgets and tear resources down. Never copy permissive demo IAM policies into real environments.

---

## One evolving portfolio project

**Repository suggestion:** `cloud-native-devsecops-platform` (separate from this learning-guide repository).

Use [Google's Online Boutique](https://github.com/GoogleCloudPlatform/microservices-demo) or the [OpenTelemetry Astronomy Shop](https://opentelemetry.io/docs/demo/) as an application. You do **not** need to author the business application from scratch to demonstrate good platform engineering.

### Incremental build plan

| When | Build milestone | Evidence you should commit to GitHub |
|---|---|---|
| Month 1 | Bash/Python Linux diagnostics | Scripts, `pytest`, logging, example incidents |
| Month 2 | Secure AWS networking and IAM | Diagram, IAM policy design, audit and cost notes |
| Month 3 | Terraform modules and state workflows | Modules, validation, CI plan, drift investigation |
| Month 4 | Container image → CI → ECR → EKS via Argo CD | CI config, Helm/manifest repo, rollback results |
| Month 5 | Security architecture review | Threat model, least privilege, secrets plan |
| Month 6 | Security-gated build/deploy | Secret scanning, SAST/SCA, Trivy, SBOM, signing and policy test |
| Month 7 | Observability | Dashboards, metrics, traces, alerts and failure screenshot evidence |
| Month 8 | Reliability and recovery | SLOs, load tests, backup restore, incident reports |
| Month 9 | Platform self-service | Project templates, promotion policy, developer instructions |
| Months 10–12 | Read-only AI incident assistant | Sanitized inputs, evidence citations, evals, permission boundaries and costs |

### Production-style acceptance checks

- [ ] Infrastructure is reproducible with pinned Terraform/provider versions and secured remote state.
- [ ] AWS IAM uses least-privilege, short-lived credentials; no hardcoded secrets or open admin endpoints.
- [ ] Separate app CI from GitOps deployment configuration and use pull-request approvals.
- [ ] CI performs tests, secret detection, SAST/SCA, image/IaC scanning, SBOM generation and artifact verification.
- [ ] Kubernetes workloads use appropriate probes, resource limits, pod/workload security and network restrictions.
- [ ] Deployment failure, rollback, a broken dependency and backup restoration have all been tested.
- [ ] Metrics, logs and traces support documented root-cause investigations and defined SLOs.
- [ ] Cloud resources are budgeted, tagged and completely cleaned up after paid labs.
- [ ] AI components ingest sanitized telemetry, have read-only default permissions and require approval for changes.
- [ ] AI evaluations include incorrect evidence, prompt injection, unauthorized actions and hallucinated diagnoses.
- [ ] Architecture, tradeoffs, limitations, runbooks, incidents and independent contributions are documented.

> **Do not equate a good sandbox with professional production employment.** Label lab projects truthfully and seek authorized real-world CI/CD, platform, infrastructure or release-automation responsibilities at work if possible.

---

## Weekly study routine

| Activity | Hours/week | Rule |
|---|---:|---|
| Selective video instruction, including system design | **3–4** | One primary video/playlist segment per gap; reserve 1–2 hours for system design when relevant |
| Independent coding and infrastructure build | **6–7** | Recreate without blindly copying |
| Debugging / failure scenarios | **2** | SadServers, broken apps, IAM/network experiments |
| Documentation, tests and review | **2–3** | README, diagrams, runbooks, mock interview explanations |
| **Total** | **~15** | Adjust to maintain practical output |

### Video-to-project workflow

```text
1. Write down the specific skill gap.
2. Watch one selected creator's lesson.
3. Rebuild the example without copy/paste.
4. Introduce one meaningful change (security, resilience, scale or cost).
5. Break the system safely; diagnose it from logs/metrics/CLI.
6. Write tests, cleanup steps, architecture notes and an incident summary.
7. Explain the design and tradeoffs in five minutes.
```

### Interview readiness gates

- **End of Month 2:** Explain VPC routing, IAM denial, DNS, TLS, Linux failures and foundational AWS design; present one AWS HLD with reliability/cost assumptions.
- **End of Month 4:** Defend a CI/CD + Terraform + EKS deployment, with tested failure recovery; begin relevant job applications.
- **End of Month 6:** Explain secure SDLC, supply-chain scanning, signed artifacts, secret management and Kubernetes admission policies.
- **End of Month 9:** Diagnose incidents through metrics/logs/traces, discuss recovery and cost tradeoffs, demonstrate a self-service platform workflow, and complete two timed infrastructure system-design explanations.
- **End of Month 12:** Operate and evaluate a **secure, read-only** AI troubleshooting assistant; position AI as an advanced skill, not a substitute for DevOps fundamentals.

---

## Master progress tracker

### Phase 1 — Fundamentals and cloud (Months 1–2)

- [ ] Complete selected freeCodeCamp Linux Server and Bash units; skip basic terminal content already mastered.
- [ ] Complete KodeKloud System Design for Beginners and draw a secure AWS HLD.
- [ ] Review Linux, networking and Python fundamentals with selective video material.
- [ ] Solve at least six independent Linux/network scenarios.
- [ ] Complete AWS VPC/IAM/security design notes and a working sandbox deployment.
- [ ] **Advanced optional:** use the Brendan Gregg video to capture a documented Linux CPU, memory or I/O incident.

### Phase 2 — IaC and delivery (Months 3–4)

- [ ] Complete a selected portion of Piyush's **30 Days of AWS Terraform**.
- [ ] Implement and test Terraform modules, remote state and drift detection.
- [ ] Complete one Anton EKS tutorial and one Piyush or Anton GitOps implementation (not two duplicate projects).
- [ ] Use Nana's CI/CD and Argo CD videos only for gaps that remain.
- [ ] Review Vishakha's system design/project architecture and adapt your capstone.
- [ ] **Advanced optional:** replace long-lived CI/CD AWS keys with restrictive GitHub Actions OIDC.

### Phase 3 — DevSecOps (Months 5–6)

- [ ] Complete Nana's DevSecOps crash course and an OpenSSF supply-chain video.
- [ ] Implement secrets, SAST/SCA, image/IaC scanning, signing, SBOM and admission checks.
- [ ] Use Anton's EKS security lessons to audit IAM, RBAC and network controls.
- [ ] **Advanced optional:** test Cilium default-deny policy and Cosign/Kyverno trusted-image admission.

### Phase 4 — Operations and SRE (Months 7–9)

- [ ] Follow selected Piyush observability videos plus the Grafana OTel demo.
- [ ] Implement end-to-end metrics, logs, traces and tested alerts.
- [ ] Solve three Kubernetes troubleshooting incidents using Piyush/Anton methods.
- [ ] Review Anton's scaling/benchmarks and DevOps Toolkit's platform-engineering materials.
- [ ] Complete at least two infrastructure-centered system-design practice questions with diagrams and failure modes.
- [ ] Demonstrate self-service application environment creation with guardrails.
- [ ] **Advanced optional:** instrument Astronomy Shop for a trace-driven incident investigation and document developer-template cost controls.

### Phase 5 — AI and advanced engineering (Months 10–12)

- [ ] Watch Vishakha's integrated AIOps project and Piyush's AI operations demonstrations.
- [ ] Build a monitored AI inference workload or small AI-enabled service.
- [ ] Test an evidence-backed, read-only AI incident assistant against unsafe and misleading inputs.
- [ ] Publish an architecture walkthrough, security evaluation, incident demo and cost assessment.

---

## Things to check before following any YouTube video

| Check | Why it matters |
|---|---|
| **Upload date and version** | Old Kubernetes APIs, Helm charts, GitHub actions, ingress controllers and Terraform AWS providers may be outdated. |
| **Least-privilege IAM** | Tutorials often use broad permissions for speed; narrow them for your project. |
| **Secrets and credentials** | Never commit access keys or production secrets; prefer OIDC/workload identity and managed secret services. |
| **Network exposure** | Avoid unnecessary public EKS control-plane endpoints, open security groups and unauthenticated dashboards. |
| **Cloud cost** | EKS, NAT gateways, load balancers, observability SaaS and AI inference are not always free. |
| **Security gates** | A passing tutorial build is not a secure release; add tests, scans, signatures, reviews and policies. |
| **Operational quality** | Require rollback, alerting, incident runbooks, backups, recovery verification and troubleshooting. |
| **AI safety** | Treat prompts, logs and retrieved material as untrusted; prevent unreviewed infrastructure actions. |
| **Reproducibility** | Commit reusable modules, version constraints, architecture decisions, teardown and test instructions. |
| **Portfolio honesty** | Distinguish guided demos and independent lab work from actual business production ownership. |

---

## Paid specialist video companions — Pluralsight and O'Reilly (optional)

> This section is **not YouTube content**. It is included solely to show when a selected specialist paid video **replaces** overlapping videos in the 12-month plan. Keep this file as your free YouTube guide; the full course catalog, links and budget strategy live in the [master README](./README.md#e-pluralsight--optional-specialist-video-courses-and-labs-2026-update).

| Months | If a gap remains, consider this Pluralsight option | O'Reilly alternative | Do this instead of just watching |
|---|---|---|---|
| 1 | [Linux Diagnostics and Troubleshooting (EX342)](https://www.pluralsight.com/courses/red-hat-certified-specialist-in-linux-diagnostics-and-troubleshooting-ex342) | [Linux System Administration Troubleshooting](https://www.oreilly.com/videos/linux-system-administration/0642572124694/) | Troubleshoot three Linux failures independently |
| 3 | [Terraform path](https://www.pluralsight.com/paths/terraform) | [Terraform Essentials for AWS](https://www.oreilly.com/videos/terraform-essentials-for/9780135936290/) | Build reusable modules with tests and secure state |
| 4 | [GitHub Actions Deep Dive](https://www.pluralsight.com/courses/github-actions-deep-dive) | [GitHub Actions in Action](https://www.oreilly.com/videos/github-actions-in/9781633437302VE/) | CI/CD pipeline with IAM/OIDC and gated deploy |
| 4 or 8 | [Hands-On Kubernetes Troubleshooting](https://www.pluralsight.com/courses/hands-on-kubernetes-troubleshooting) | No paid course needed; use [SadServers](https://sadservers.com/scenarios) | Diagnose six K8s failures |
| 5–6 | [CKS path](https://www.pluralsight.com/paths/certified-kubernetes-security-specialist-cks) | [Kubernetes Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/) | Enforce RBAC, admission and signed-image controls |
| 7 | [Kubernetes SRE-Grade Observability](https://www.pluralsight.com/paths/kubernetes-sre-grade-observability) | [OpenTelemetry in Practice](https://www.oreilly.com/videos/opentelemetry-in-practice/9781807783334/) | Trace a failure across services using metrics/logs/traces |
| 8–9 | [Platform Engineering: The Big Picture](https://www.pluralsight.com/courses/platform-engineering-big-picture) | [SRE Essentials](https://www.oreilly.com/videos/site-reliability-engineering/9780135415016/) | SLOs, recovery test and developer platform design |
| 10–12 | [Applying GenAI to DevOps](https://www.pluralsight.com/courses/applying-genai-devops-operations) + [Agentic AI Security](https://www.pluralsight.com/courses/agentic-ai-security-tool-interfaces-least-privilege) | [LLM Lifecycle Mastery](https://www.oreilly.com/videos/llm-lifecycle-mastery/9781806696918/) | Read-only agent with evaluation and permission checks |

**Subscription decision:** First check for employer access. Do not subscribe to KodeKloud, Pluralsight and O'Reilly annually just for this roadmap. The course hyperlinks are official product pages; availability, pricing, and labs may change.

---

## Course recommendation index — non-YouTube (optional, curated)

This section is a *companion index*, not a request to purchase courses. The full curriculum lives in [README.md](./README.md). **Do not subscribe to multiple overlapping learning platforms simultaneously.** Prioritize hands-on evidence over credentials.

| Platform | Best course(s) for this roadmap | When and why |
|---|---|---|
| **Adrian Cantrill** | [AWS Solutions Architect Associate](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) | Months 2–3: primary AWS architecture foundation |
| **KodeKloud** | [DevOps learning path](https://kodekloud.com/learning-path/devops-engineer) and [learning paths catalog](https://kodekloud.com/learning-paths/) | Primary interactive labs all year |
| **Pluralsight** | [Linux Diagnostics (EX342)](https://www.pluralsight.com/courses/red-hat-certified-specialist-in-linux-diagnostics-and-troubleshooting-ex342), [Hands-On Kubernetes Troubleshooting](https://www.pluralsight.com/courses/hands-on-kubernetes-troubleshooting), [Kubernetes SRE-Grade Observability](https://www.pluralsight.com/paths/kubernetes-sre-grade-observability) | Months 1, 4–8: optional specialist fault diagnosis and telemetry labs |
| **O'Reilly video** | [Linux System Administration Troubleshooting](https://www.oreilly.com/videos/linux-system-administration/0642572124694/), [Kubernetes Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/), [OpenTelemetry in Practice](https://www.oreilly.com/videos/opentelemetry-in-practice/9781807783334/), [Site Reliability Engineering Essentials](https://www.oreilly.com/videos/site-reliability-engineering/9780135415016/) | Months 1, 6–8: selective specialist video training; alternatives to overlapping Pluralsight |
| **Udacity — best-fit** | [Site Reliability Engineer Nanodegree](https://www.udacity.com/course/site-reliability-engineer-nanodegree--nd087) | Months 7–8: optional reviewed project work; **highest-value Udacity pick** |
| **Udacity — alternatives** | [Cloud Native Application Architecture](https://www.udacity.com/course/cloud-native-architecture-nanodegree--nd064), [Cloud DevOps Engineer](https://www.udacity.com/course/cloud-dev-ops-nanodegree--nd9991) | Months 3–7: pick **one**, only if you need structured project feedback |
| **Udacity — AI specialist** | [AgentOps: Deploying, Guarding and Monitoring AI Agents](https://www.udacity.com/course/agentops-deploying-guarding-and-monitoring-ai-agents--cd15157), [AI Threat Modeling and Operational Defense](https://www.udacity.com/course/ai-threat-modeling-and-operational-defense--cd15147) | Month 12, optional |
| **Udacity — free** | [Configuring Linux Web Servers](https://www.udacity.com/course/configuring-linux-web-servers--ud299), [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123) | Month 1: optional practical refreshers |
| **CBT Nuggets** | [Free intro-to-IT courses](https://www.cbtnuggets.com/it-training/intro-to-it), [Wireshark Certified Analyst](https://www.cbtnuggets.com/it-training/networking/wca-101), [CompTIA AutoOps+](https://www.cbtnuggets.com/it-training/comptia/autoops-plus) | Free foundation where needed; paid only for diagnosed gaps |
| **System design prep** | [Hello Interview](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction), [AlgoExpert InfraExpert / SystemsExpert](https://www.algoexpert.io/), [Design Gurus Grokking](https://www.designgurus.io/course/grokking-the-system-design-interview) | Free interview practice first; optional paid framework for mock-design gaps |

**Selection rule:** Keep 1 AWS teacher + 1 lab platform + 1 optional specialist provider per phase. Reallocate time instead of expanding the ~15 hours/week plan.

---

## Source and channel directory

**Primary YouTube educators**

- [Piyush Sachdeva — official video index](https://www.piyushsachdeva.com/youtube-videos/All) · [Terraform AWS code](https://github.com/piyushsachdeva/Terraform-Full-Course-Aws).
- [Vishakha Sadhwani — channel](https://www.youtube.com/@vishakha.sadhwani) · [60DaysToCloud](https://github.com/vishakhasadhwani/60DaysToCloud) · [DevOps+AIOps introduction](https://www.youtube.com/watch?v=UBzYwNbFCKs).
- [TechWorld with Nana — channel](https://www.youtube.com/@TechWorldwithNana) · [Docker full course](https://www.youtube.com/watch?v=3c-iBn73dDE) · [DevSecOps course](https://www.youtube.com/watch?v=gLJdrXPn0ns).
- [Anton Putra — channel](https://www.youtube.com/@AntonPutra) · [tutorial repository](https://github.com/antonputra/tutorials) · [numbered catalog](https://github.com/antonputra/tutorials/blob/main/docs/contents.md).

**Linux and system-design channels**

- [freeCodeCamp](https://www.youtube.com/@freecodecamp) · [Linux Server (Shawn Powers)](https://www.youtube.com/watch?v=WMy3OzvBWc0) · [50 Linux Commands](https://www.youtube.com/watch?v=ZtqBQ68cfJc) · [Bash Scripting](https://www.youtube.com/watch?v=tK9Oc6AEnR4).
- [KodeKloud System Design for Beginners 2026](https://www.youtube.com/watch?v=SE2KF-vxvS0) · [freeCodeCamp/Gaurav Sen system design](https://www.youtube.com/watch?v=m8Icp_Cid5o).
- [ByteByteGo](https://www.youtube.com/@ByteByteGo) · [System Design 101 diagrams](https://github.com/ByteByteGoHq/system-design-101) · [Rate Limiter](https://www.youtube.com/watch?v=YXkOdWBwqaA).
- [Cloud X Berry](https://www.youtube.com/@TheCloudXBerry) · [Proxy vs LB vs API Gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) · [Hello Interview](https://www.youtube.com/@hello_interview/videos) · [Gaurav Sen](https://www.youtube.com/@gkcs) · [CodeKarle](https://www.youtube.com/@codeKarle).

**Additional creators added 16 October 2026**

- [Kunal Kushwaha](https://www.youtube.com/@KunalKushwaha) · [DevOps Bootcamp](https://www.youtube.com/playlist?list=PL9gnSGHSqcnoqBXdMwUTRod4Gi3eac2Ak) · [Networking](https://www.youtube.com/watch?v=IPvYjXCsTg8) · [Git](https://www.youtube.com/watch?v=apGV9Kg7ics) · [GitHub Actions](https://www.youtube.com/watch?v=62N8UiWUdQo) · [Argo CD](https://www.youtube.com/watch?v=8YLsQIG2Svo).
- [Ashish Pratap Singh](https://www.youtube.com/@ashishps_1) · [30 System Design Concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk) · [System Design Interview Approach](https://www.youtube.com/watch?v=l3X1t3kpmwY) · [playlist](https://www.youtube.com/playlist?list=PLCZ2MME8uzMhow9-hAsSm2-dvfF4ag6wy).
- [Cloud X Berry](https://www.youtube.com/@TheCloudXBerry) · [Networking Topics](https://www.youtube.com/watch?v=TR0RU2pmMeA) · [Linux Directories](https://www.youtube.com/watch?v=qvjRcZcW8CY) · [Backend Ecosystem](https://www.youtube.com/watch?v=mZ27vUoOEB0).

**Other YouTube channels**

- [Practical Networking](https://www.youtube.com/@PracticalNetworking), [Hussein Nasser](https://www.youtube.com/@hnasr), [Bret Fisher](https://www.youtube.com/@BretFisher), [DevOps Directive](https://www.youtube.com/@devopsdirective), [CBT Nuggets](https://www.youtube.com/@cbtnuggets).
- [DevOps Toolkit](https://www.youtube.com/@DevOpsToolkit), [CNCF](https://www.youtube.com/@cncf), [Grafana](https://www.youtube.com/@Grafana), [AWS Events](https://www.youtube.com/@AWSEventsChannel).
- [DataTalks.Club](https://www.youtube.com/@DataTalksClub), [Hugging Face](https://www.youtube.com/@huggingface), [Arpit Bhayani](https://www.youtube.com/@AsliEngineering).

**Authoritative practice references**

- [AWS EKS Best Practices](https://docs.aws.amazon.com/eks/latest/best-practices/), [AWS EKS Workshop](https://www.eksworkshop.com/docs/introduction/), [Terraform tutorials](https://developer.hashicorp.com/terraform/tutorials).
- [Google SRE](https://sre.google/books/), [OpenTelemetry Demo](https://opentelemetry.io/docs/demo/), [OpenSSF training](https://openssf.org/training/), [SLSA](https://slsa.dev/), [OWASP GenAI](https://genai.owasp.org/).

**Advanced technical talks and labs — 16 October 2026**

- [Brendan Gregg — Linux Systems Performance (video)](https://www.youtube.com/watch?v=fhBHvsi0Ql0) · [talk/slides](https://www.brendangregg.com/blog/2020-03-08/lisa2019-linux-systems-performance.html) · [Liz Rice — eBPF (video)](https://www.youtube.com/watch?v=ZXDhKUeUUSs).
- [Civo/Kunal — Cilium (video)](https://www.youtube.com/watch?v=yQoVOumoY5k) · [Isovalent interactive Cilium lab](https://isovalent.com/labs/cilium-getting-started/) · [Cilium docs](https://docs.cilium.io/en/stable/).
- [GitHub Actions AWS OIDC (video)](https://www.youtube.com/watch?v=Sdzd4N6L5Hg) · [GitHub docs](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) · [Sigstore Cosign + Kyverno (video)](https://www.youtube.com/watch?v=HLb1Q086u6M) · [Kyverno image verification docs](https://kyverno.io/docs/policy-types/cluster-policy/verify-images/sigstore/).
- [CNCF OpenTelemetry hands-on (video)](https://www.youtube.com/watch?v=8CKgAyenEjo) · [Grafana OTel intro (video)](https://www.youtube.com/watch?v=Xhh9V7uRP88) · [Astronomy Shop Demo](https://opentelemetry.io/docs/demo/).
- [Platform engineering talk (video)](https://www.youtube.com/watch?v=9lPp-6nJ8bI) · [Backstage tutorial (video)](https://www.youtube.com/watch?v=JbX6V9fz5QA) · [FinOps learning](https://www.finops.org/training-certification/recommended/new-to-finops/).

### How the video links were selected

Selected individual videos, playlists and creator-owned indexes were cross-checked against available creator catalogs, video metadata, official course pages or companion repositories through 16 October 2026. A few older links are included for stable **concept explanations**; verify commands and versions against current documentation. Where a creator's catalog is more reliable than a single moving/deleted video, the link is explicitly labeled **Catalog** or **Channel** rather than falsely implying a verified specific video.

---

**Guiding principle:** It is better to build **one independently understood, secure and observable cloud-native system** than to complete dozens of overlapping video playlists without reproducible implementation or troubleshooting evidence.
