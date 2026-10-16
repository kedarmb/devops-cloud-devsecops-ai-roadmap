# Complete DevOps, Cloud, SRE, DevSecOps, Platform Engineering & AI Upskilling + Interview Roadmap

> **Updated:** 16 October 2026  |  **Plan:** 48 focused weeks / 12 study months  |  **Pace:** 15 hours/week  |  **Early interview milestone:** Week 16
>
> **Audience:** Experienced IT professional moving from recent manual QA responsibilities back into hands-on DevOps/Cloud Engineering; earlier DevOps exposure and CKA/CKAD credentials. Adapt tasks to actual prior experience.  **Primary stack:** Linux · Python/Bash · Git · AWS · Terraform · Docker · GitHub Actions · Kubernetes/EKS · Helm · Argo CD · Security · OpenTelemetry · Prometheus/Grafana.

**Repository note:** The recommended download contains exactly four root-level Markdown files and only one `README.md`; the older standalone YouTube README has been retired from this package.

**Use this document as the execution guide.** Existing companion references: [Master technical roadmap](./README.md), [YouTube and course video library](./YOUTUBE_LEARNING_RESOURCES.md), and [Earlier interview roadmap](./STRUCTURED_UPSKILLING_INTERVIEW_ROADMAP.md). The companion files are optional background; this file includes the *primary links and decisions needed to start*.

## Navigation

- [1. Objectives, course selection and baseline](#1-objectives-course-selection-and-baseline)
- [2. Weekly timetable and evidence rule](#2-weekly-timetable-and-evidence-rule)
- [3. Month-by-month, week-by-week learning plan](#3-month-by-month-week-by-week-learning-plan)
- [4. Sixteen-week interview acceleration plan](#4-sixteen-week-interview-acceleration-plan)
- [5. Flagship portfolio: architecture, repo and acceptance tests](#5-flagship-portfolio-architecture-repo-and-acceptance-tests)
- [6. Interview preparation, mock questions and coding](#6-interview-preparation-mock-questions-and-coding)
- [7. Readiness gates and application strategy](#7-readiness-gates-and-application-strategy)
- [8. Complete curated learning materials and direct links](#8-complete-curated-learning-materials-and-direct-links)
- [9. Paid course choices and spending discipline](#9-paid-course-choices-and-spending-discipline)
- [10. First seven days: start immediately](#10-first-seven-days-start-immediately)
- [11. Progress templates and master checklist](#11-progress-templates-and-master-checklist)
- [12. NextWork.ai — guided projects and independent portfolio extensions](#12-nextworkai--guided-projects-and-independent-portfolio-extensions)
- [13. Zero To Mastery — optional paid course overlays](#13-zero-to-mastery--optional-paid-course-overlays)

---

## 1. Objectives, course selection and baseline
**The primary objective is job readiness in 16 weeks, not finishing every course.** Continue advanced specializations during applications or after entering an engineering role. At the end of Week 16, show a self-built cloud-native delivery path and explain it under interview questioning. At the end of the full plan, extend that platform with measurable security, reliability, cost, and safe AI-operations controls.

| Priority | Timing | Competencies | Proof |
|---|---|---|---|
| **P0: Core employability** | Weeks 1–16 | Linux, networking, Bash/Python, Git, AWS, Terraform, Docker, GitHub Actions, EKS and GitOps | Working project, automated tests, 3+ incident stories, technical interviews |
| **P1: Operations maturity** | Weeks 17–32 | IAM, cluster security, supply chain, Cilium, OpenTelemetry, SRE and recovery | Security tests, alerts, traces, SLOs, restore drills and postmortems |
| **P2: Senior-level differentiation** | Weeks 33–48 | Platform engineering, FinOps, distributed systems, AI/AgentOps | Golden path, cost report and read-only, evaluated AI incident assistant |

**Skill assessment before starting (1 hour):** without notes, (a) troubleshoot one failed Linux service, (b) explain DNS → TCP → TLS → HTTP, (c) write a 30-line Python script and test it, (d) explain IAM role assumption, (e) explain Terraform state, (f) fix a broken Kubernetes Deployment. Rate each **0 = cannot**, **1 = guided**, **2 = independent**, **3 = can teach and debug**. Fast-forward on subjects already rated 3 and redirect that time into troubleshooting.
**Learning selection rule:** For each topic, use **one primary teacher + official docs + one hands-on exercise**. [Zero To Mastery](https://zerotomastery.io/) is a paid **alternative** for targeted Linux/Bash/Terraform or late AWS AI/agent gaps, never an additional mandatory track; see [Section 13](#13-zero-to-mastery--optional-paid-course-overlays). [NextWork.ai](https://nextwork.ai/) is an optional source of guided implementation projects: use it to replace an overlapping lab, never as an additional required course. Items marked *optional* are substitutes or gap-fillers, **not** mandatory additions. Avoid a new certification unless job postings or a demonstrable gap justify it.

## 2. Weekly timetable and evidence rule

| Activity | Hours/week | Outcome |
|---|---:|---|
| Targeted course/video or documentation | 3 | Explain concepts without notes |
| Building infrastructure and writing automation | 6 | Git commits + independently executed lab |
| Injecting and diagnosing controlled faults | 2 | Failure report with commands and root cause |
| Interview drills (voice + code + system design) | 2 | Recorded answers or timed mock scorecard |
| Portfolio, cleanup, resume and applications | 2 | Readable evidence or tailored application |
| **Total** | **15** | **No mandatory extra subscriptions or video hours** |

**Every week:** [ ] learn one core concept [ ] build a reproducible artifact [ ] deliberately break and recover something safe [ ] answer 3 interview questions aloud [ ] commit a README/runbook [ ] clean up cloud resources.
**Nonnegotiable safeguards:** work in disposable accounts/clusters; enable budgets *before* provisioning; use short-lived IAM credentials; never upload access keys or unredacted internal data; document teardown and verify bills. EKS control planes, NAT gateways, load balancers, storage and logs are not free by default. Never run policy-bypass or failure-injection tests in employer or shared production environments.

## 3. Month-by-month, week-by-week learning plan
The weeks below are **active study weeks**, not necessarily consecutive calendar weeks. If life interrupts the schedule, resume at the next incomplete deliverable. Each month closes with a gate: demonstrate the artifact independently and explain the design and failure modes.

### Month 1 — Linux, networking, scripting and diagnostic habits
**Outcome:** Linux diagnostics toolkit, six failure writeups, a tested Python CLI.  **Monthly gate:** Linux and network incident lab; at least one performance investigation.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **1** | Linux CLI, users, filesystem, permissions, services, systemd and journald | Build VM + Bash service inspector with tests; document systemd failure | A service fails after reboot: how do you isolate it? |
| **2** | TCP/IP, subnetting, DNS, NAT, TLS, HTTP, curl, ss, dig, tcpdump; Git workflows | Network diagnostic runbook + intentional DNS break + PR/merge/revert | Trace a browser request and distinguish DNS/TCP/TLS failures |
| **3** | Bash safety; Python argparse, JSON, HTTP, exceptions, logging and pytest | Tested Python health-check CLI and Bash backup checker | Parse logs and report top error categories in Python |
| **4** | Linux performance: CPU, memory, IO; hypothesis-based investigations | Six reproducible incidents and one performance report with commands | How do you distinguish CPU pressure from IO wait? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [freeCodeCamp — Linux Server Administration (Shawn Powers)](https://www.youtube.com/watch?v=WMy3OzvBWc0) · [MIT — The Missing Semester](https://missing.csail.mit.edu/) · [SadServers — Troubleshooting Scenarios](https://sadservers.com/scenarios) · [Kunal Kushwaha — Computer Networking Full Course](https://www.youtube.com/watch?v=IPvYjXCsTg8) · [Kunal Kushwaha — Git and GitHub Full Tutorial](https://www.youtube.com/watch?v=apGV9Kg7ics) · [Practical Networking — YouTube](https://www.youtube.com/@PracticalNetworking) · [Harvard CS50 — Introduction to Programming with Python](https://cs50.harvard.edu/python/).
- **Choose when needed:** [freeCodeCamp — Bash Scripting Tutorial](https://www.youtube.com/watch?v=tK9Oc6AEnR4) · [pytest documentation](https://docs.pytest.org/en/stable/) · [Brendan Gregg — Linux Systems Performance](https://www.youtube.com/watch?v=fhBHvsi0Ql0) · [ShellCheck](https://www.shellcheck.net/).
- **Optional paid substitute (not extra hours):** [ZTM Bash Scripting](https://zerotomastery.io/courses/learn-bash-scripting/) for Weeks 3–4 **if your Bash diagnostic fails**, or [ZTM Linux Sysadmin Bootcamp](https://zerotomastery.io/courses/devops-bootcamp/) *instead of* freeCodeCamp Linux plus beginner labs. [ZTM Python Automation](https://zerotomastery.io/courses/learn-python-automation/) only if CS50P plus self-built scripts are insufficient.

- [ ] **Month 1 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional project accelerator (Week 1–2):** [NextWork — Linux Service Health Monitor](https://nextwork.ai/projects/5d8df751-6459-473f-ae86-d8ee7ad4ccc3). Use the guided project *instead of* a duplicate Linux service lab, then independently introduce a failing service, validate restart limits, collect `journalctl` evidence and document recovery. [Full NextWork project map](#12-nextworkai--guided-projects-and-independent-portfolio-extensions).

### Month 2 — AWS core architecture and operational fundamentals
**Outcome:** Cost-controlled AWS design and working application behind ALB.  **Monthly gate:** HLD review defending IAM, VPC, HA, recovery, cost and teardown.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **5** | AWS accounts, MFA, IAM/STS, policies, budgets, CloudTrail | Sandbox guardrails, spend alerts, scoped IAM role + denial proof | Debug AccessDenied in an assumed role |
| **6** | VPC CIDR, subnets, routes, NAT, endpoints, SG vs NACL, Route 53 | Public/private VPC design and traffic-flow diagram | How does an EC2 host in a private subnet reach S3? |
| **7** | EC2, ALB, Auto Scaling, S3, EBS/RDS, KMS and backups | App behind ALB with health checks, failure test and cleanup | Investigate an ALB 502/503 and explain failure isolation |
| **8** | HA, DR, operational excellence and introductory HLD | 20-minute HLD review, threat and cost trade-offs, recovery test | Why multi-AZ? What are RTO/RPO and an SLO? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [Adrian Cantrill — AWS Solutions Architect Associate](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) · [AWS IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) · [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) · [AWS Workshops](https://workshops.aws/) · [Cloud X Berry — Reverse Proxy vs Load Balancer vs API Gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) · [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) · [Ashish Pratap Singh — 30 System Design Concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk).
- **Choose when needed:** [Hello Interview — System Design in a Hurry](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction).

- [ ] **Month 2 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

### Month 3 — Terraform and repeatable infrastructure
**Outcome:** Reusable Terraform modules, safe state and CI validation.  **Monthly gate:** Independent clean-room apply, review, drift and destroy.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **9** | Terraform provider, resources, variables, outputs, workspaces basics | Terraform creates/destroys versioned sandbox infrastructure | Explain lifecycle and what plan does not guarantee |
| **10** | Modules, state sensitivity, remote backend, locks and identity | Reusable modules, remote state, access controls, env isolation | What if state is lost, leaked or locked? |
| **11** | Validation, fmt, tflint/scan, CI checks, drift and import | Terraform PR checks + documented drift discovery & review | What would you do when console changes drift from IaC? |
| **12** | Infrastructure design review and safe lifecycle | Clean-room apply/destroy; architecture ADR and cost/cleanup proof | Defend module boundaries, blast radius and promotion workflow |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [HashiCorp — Terraform Tutorials](https://developer.hashicorp.com/terraform/tutorials) · [Piyush Sachdeva — 30 Days of Terraform on AWS](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp) · [KodeKloud — Learning Paths](https://kodekloud.com/learning-paths/) · [Piyush Sachdeva — Terraform Drift](https://www.youtube.com/watch?v=nRgNIy-SDEw) · [Anton Putra — Terraform Playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA) · [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html).

- [ ] **Month 3 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional project accelerator (Weeks 10–12):** [NextWork — Terraform GitOps Foundation on AWS](https://nextwork.ai/projects/7f66d30f-cafc-46d8-b106-f48321581f37). Run the guided IaC + GitHub Actions/OIDC flow, then rebuild IAM trust, plan approvals and Terraform state protections independently. Treat guided work as a replacement for an overlapping Terraform lab, not an extra requirement.

### Month 4 — CI/CD, containers, Kubernetes and GitOps
**Outcome:** Pipeline: GitHub Actions OIDC → ECR → EKS / Argo CD.  **Monthly gate:** 15-minute demo, controlled rollback and 3+ infrastructure incidents; start targeted applications.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **13** | Dockerfiles, containers, image security and CI basics | Containerize app; unit test, image build and vulnerability scan | Why does a container exit? How do you debug a failed build? |
| **14** | GitHub Actions jobs, OIDC, least-privilege IAM and ECR | Keyless GitHub Actions -> AWS ECR image push, scoped trust | Why federated OIDC instead of long-lived CI credentials? |
| **15** | EKS architecture, Helm, ingress, Argo CD sync and troubleshooting | Local kind GitOps then short-lived EKS deploy using IaC | Debug ImagePullBackOff, 503, Pending pods and wrong selectors |
| **16** | Release safety, readiness/liveness, progressive rollout and rollback | End-to-end demo, bad-release rollback, 3 incident stories | Design a reliable deployment pipeline under outage conditions |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [TechWorld with Nana — Docker Full Course](https://www.youtube.com/watch?v=3c-iBn73dDE) · [Kunal Kushwaha — GitHub Actions CI/CD](https://www.youtube.com/watch?v=62N8UiWUdQo) · [Trivy Documentation](https://trivy.dev/latest/docs/) · [GitHub — Configure OIDC in AWS](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) · [GitHub Actions to AWS Using OIDC — Video](https://www.youtube.com/watch?v=Sdzd4N6L5Hg) · [Amazon EKS Workshop](https://www.eksworkshop.com/) · [Kunal Kushwaha — Argo CD / GitOps](https://www.youtube.com/watch?v=8YLsQIG2Svo).
- **Choose when needed:** [Piyush Sachdeva — GitOps on EKS](https://www.youtube.com/watch?v=c_a5e2Dnxkk) · [Argo CD Documentation](https://argo-cd.readthedocs.io/en/stable/) · [TechWorld with Nana — Argo CD](https://www.youtube.com/watch?v=MeU5_k9ssrs) · [Piyush Sachdeva — Kubernetes Troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc).

- [ ] **Month 4 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

> **Week 16 job-search checkpoint:** Begin selective applications when the build and troubleshooting criteria below are met; do not postpone applications until advanced Months 5–12. Bridge roles such as release engineering, CI/CD engineering and cloud automation may legitimately leverage your recent QA experience.

**Optional project accelerators (Weeks 13–16):** [NextWork — Terraform EKS with GitHub Actions CI/CD](https://nextwork.ai/projects/d40c742f-9bac-40c1-b651-52ae96e6ba30) and [NextWork — End-to-End GitOps Pipeline](https://nextwork.ai/projects/2757d4a2-0371-4c1c-8389-4e52c53dac6b). Prefer **the local GitOps project first** to minimize AWS charges; use the EKS lab only after enabling budgets and reviewing its estimated costs. Extend the chosen lab with image scanning, approval gates, failure drills and rollback proof.

### Month 5 — Cloud IAM, network security and threat modeling
**Outcome:** Threat model, IAM denial tests and Kubernetes security context.  **Monthly gate:** Security review with exploit path → control → verification.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **17** | IAM trust boundaries, resource policies, IRSA/pod identity | Compare federated identities, negative IAM tests and security review | Explain role assumption, privilege escalation and identity scoping |
| **18** | KMS, encryption, secrets and cloud audit trails | Secrets lifecycle diagram, alertable audit event, encrypted data flow | How do you rotate a compromised credential? |
| **19** | Threat modeling: CI runner, artifact registry, VPC, Kubernetes, supply chain | Threat model with data flows, abuse cases, mitigations and tests | Where are the trust boundaries in your CI/CD path? |
| **20** | Kubernetes cluster isolation, RBAC, pod hardening | Run negative RBAC tests, security context, admission proofs | Why does least-privilege Pod identity matter? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [AWS Security Documentation](https://docs.aws.amazon.com/security/) · [AWS IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) · [Amazon EKS Workshop](https://www.eksworkshop.com/) · [AWS Workshops](https://workshops.aws/) · [OpenSSF Training](https://openssf.org/training/) · [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) · [O’Reilly — Kubernetes Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/).
- **Choose when needed:** [Kubernetes Documentation](https://kubernetes.io/docs/).

- [ ] **Month 5 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

### Month 6 — DevSecOps, Kubernetes networking and provenance
**Outcome:** SAST/SCA/scan gates, signed image and Kubernetes policy enforcement.  **Monthly gate:** Unsigned-image rejection and denied network flow demonstrated.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **21** | SAST/SCA, IaC analysis, Trivy, CVE triage and exceptions | Build scan gates and documented risk exception policy | How do you reduce false positives without ignoring risk? |
| **22** | SBOM, signing, Cosign, admission policy, provenance | Produce SBOM; sign good image; block unsigned image | How would you prevent a tampered container from deploying? |
| **23** | CNI, eBPF, Cilium, Hubble and default-deny policy | Default-deny and explicit allow traffic matrix with packet evidence | Service fails with NetworkPolicy enabled: how do you debug? |
| **24** | Secure deployment gate, image/policy failure drills | Security runbook + simulated policy bypass attempt and resolution | Discuss defense in depth across build, registry and cluster |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [Trivy Documentation](https://trivy.dev/latest/docs/) · [OpenSSF Training](https://openssf.org/training/) · [TechWorld with Nana — DevSecOps / Docker Scout](https://www.youtube.com/watch?v=gLJdrXPn0ns) · [Sigstore Cosign](https://docs.sigstore.dev/cosign/overview/) · [DevOps Toolkit — Sign/Verify Images with Cosign and Kyverno](https://www.youtube.com/watch?v=HLb1Q086u6M) · [Kyverno — Verify Images](https://kyverno.io/docs/policy-types/cluster-policy/verify-images/sigstore/) · [Liz Rice — Cloud Native Superpowers with eBPF](https://www.youtube.com/watch?v=ZXDhKUeUUSs).
- **Choose when needed:** [Civo / Kunal Kushwaha — Cilium Networking, Security & Observability](https://www.youtube.com/watch?v=yQoVOumoY5k) · [Isovalent — Cilium Getting Started Labs](https://isovalent.com/labs/cilium-getting-started/) · [Kubernetes Goat](https://madhuakula.com/kubernetes-goat/).

- [ ] **Month 6 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

### Month 7 — Metrics, logs, traces and operational diagnostics
**Outcome:** Metrics, traces, logs and runbooks for a distributed app.  **Monthly gate:** Diagnose an injected p99 latency incident from correlated telemetry.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **25** | Prometheus metrics, labels, cardinality, basic PromQL | Golden-signal dashboard and custom instrumented metric | What metrics reveal saturation vs elevated error rate? |
| **26** | OpenTelemetry SDK, collector, context propagation | Traced request through 2+ services in OpenTelemetry demo | How do you find latency across microservices? |
| **27** | Central logs, Grafana, alert rules, noise and correlation | Alert rule -> runbook; correlate logs, traces and metrics | What does a useful production alert look like? |
| **28** | Observability cost, missing telemetry, investigation drill | Latency incident report: signal -> hypothesis -> mitigation | How do you investigate a slow p99 with normal CPU? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/) · [Grafana Documentation](https://grafana.com/docs/) · [Piyush Sachdeva — Observability Playlist](https://www.youtube.com/playlist?list=PLl4APkPHzsUWC89lwHRGxk1GDtS7dkUsE) · [CNCF — OpenTelemetry Hands-on Tutorial](https://www.youtube.com/watch?v=8CKgAyenEjo) · [OpenTelemetry Demo / Astronomy Shop](https://opentelemetry.io/docs/demo/) · [OpenTelemetry Documentation](https://opentelemetry.io/docs/) · [Grafana — Getting Started with OpenTelemetry](https://www.youtube.com/watch?v=Xhh9V7uRP88).
- **Choose when needed:** [Google — Site Reliability Engineering Books](https://sre.google/books/).

- [ ] **Month 7 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional guided SRE project (Weeks 27–29):** [NextWork — Observability and SLOs on Kubernetes](https://nextwork.ai/projects/0a918f05-9085-4ff0-a825-7c1000d13108). Run it when your Prometheus/OpenTelemetry environment is ready; independently inject latency or errors, validate burn-rate alerts and attach an incident report.

### Month 8 — SRE, incident response and disaster recovery
**Outcome:** SLOs, alerts, incident procedure, verified restoration.  **Monthly gate:** Timed recovery with actual RTO/RPO evidence and postmortem.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **29** | SLIs, SLOs, error budget burn and service ownership | Define availability/latency SLOs and alert burn rates | Why should an SLO target be less than 100%? |
| **30** | On-call runbooks, severity, incident command, retrospectives | SEV drill with comms timeline and blameless postmortem | How do you communicate impact under uncertainty? |
| **31** | Backup/restore, RTO/RPO, AZ failure, IaC recovery | Restore database/service in test env and measure RTO | How do backups differ from DR? |
| **32** | Capacity, load testing, Kubernetes failure analysis | Load test + six K8s troubleshooting reproductions | Investigate OOMKilled versus CrashLoopBackOff |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [Google — Site Reliability Engineering Books](https://sre.google/books/) · [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/) · [O’Reilly — SRE Essentials](https://www.oreilly.com/videos/site-reliability-engineering/9780135415016/) · [SadServers — Troubleshooting Scenarios](https://sadservers.com/scenarios) · [Pluralsight — Hands-On Kubernetes Troubleshooting](https://www.pluralsight.com/courses/hands-on-kubernetes-troubleshooting) · [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) · [AWS Workshops](https://workshops.aws/).
- **Choose when needed:** [Piyush Sachdeva — Kubernetes Troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc) · [OpenTelemetry Demo / Astronomy Shop](https://opentelemetry.io/docs/demo/).

- [ ] **Month 8 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional SRE deployment drill (Weeks 30–32):** [NextWork — GitOps Canary Deployments with Argo](https://nextwork.ai/projects/df2b6349-a5e8-4448-b807-7564d6a3c015). Run on a disposable local Kubernetes cluster, define a meaningful rollout-analysis metric and prove that a deliberately bad release aborts automatically.

### Month 9 — Platform engineering, golden paths and FinOps
**Outcome:** Internal developer golden path and cloud cost accountability.  **Monthly gate:** A new service scaffold deploys under scoped permissions and can be torn down.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **33** | Platform-as-product, developer personas, paved roads and ownership | Platform product brief and internal developer workflow | What does a platform team provide versus app teams? |
| **34** | Backstage catalog/templates, service bootstrap, guardrails | Bootstrap template that scaffolds repo + CI + GitOps app | How do you design self-service safely? |
| **35** | GitOps tenancy, namespace boundaries, policy, permissions | Multi-team demo, RBAC, template restrictions, isolated environment | How do you prevent team A from modifying team B workloads? |
| **36** | Tagging, usage, budgets, idle-resource cleanup and cost trade-offs | Cost dashboard/report and teardown automation | Compare EKS, ECS, EC2 for a small team |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [CNCF — Starting and Scaling a Platform Engineering Team](https://www.youtube.com/watch?v=9lPp-6nJ8bI) · [DevOps Toolkit — YouTube](https://www.youtube.com/@DevOpsToolkit) · [Backstage Documentation](https://backstage.io/docs/) · [TeKanAid — Backstage Crash Course](https://www.youtube.com/watch?v=JbX6V9fz5QA) · [Argo CD Documentation](https://argo-cd.readthedocs.io/en/stable/) · [Kubernetes Documentation](https://kubernetes.io/docs/) · [Isovalent — Cilium Getting Started Labs](https://isovalent.com/labs/cilium-getting-started/).
- **Choose when needed:** [FinOps Foundation — Start Here](https://www.finops.org/training-certification/recommended/new-to-finops/) · [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) · [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html).

- [ ] **Month 9 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional platform lab (Weeks 34–35):** [NextWork — GitOps Across Clusters with Argo CD](https://nextwork.ai/projects/41b34a8d-255a-4b89-876d-4ec34e9c5184). Independently demonstrate controlled promotion, sync drift and recovery across isolated environments; explain blast radius and team access.

### Month 10 — Advanced AWS, resilience and safe AI-assisted operations
**Outcome:** Advanced AWS operational design and safe AI-assisted diagnostics.  **Monthly gate:** 10-case read-only recommendation comparison against verified runbooks.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **37** | Advanced release design, environments, accounts and identity | Document staging->production separation and deployment approvals | How do you control blast radius in multi-account AWS? |
| **38** | Advanced EKS networking and performance diagnosis | Simulate an intermittent network fault, document packets and flow | How do you isolate CNI vs DNS vs service endpoint issues? |
| **39** | Reliability automation and policy-driven response with guardrails | Read-only automation to gather diagnostics, with permissions test | Which incident actions are safe to automate? |
| **40** | AI-assisted troubleshooting evaluation baseline | Compare AI suggestions with verified runbooks on 10 fixed incidents | What happens if an AI diagnosis is confident but wrong? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [Adrian Cantrill — AWS Solutions Architect Associate](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) · [GitHub — Configure OIDC in AWS](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) · [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) · [Anton Putra — EKS Playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXnKY6XmeifEpjIfkWRo9v2l) · [Isovalent — Cilium Getting Started Labs](https://isovalent.com/labs/cilium-getting-started/) · [Hussein Nasser — Backend Engineering](https://www.youtube.com/@hnasr) · [Google — Site Reliability Engineering Books](https://sre.google/books/).
- **Choose when needed:** [Pluralsight — Applying GenAI to DevOps](https://www.pluralsight.com/courses/applying-genai-devops-operations) · [AWS Security Documentation](https://docs.aws.amazon.com/security/) · [Vishakha Sadhwani — DevOps / AIOps Intro](https://www.youtube.com/watch?v=UBzYwNbFCKs) · [OWASP — Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/).

- [ ] **Month 10 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

### Month 11 — AI workload delivery, model observability and LLMOps
**Outcome:** Versioned AI/ML delivery, instrumentation and rollback.  **Monthly gate:** Monitored inference service with workload and cost evidence.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **41** | MLOps lifecycle: versions, data drift, reproducible deployments | Version small model/service with testable promotion criteria | What must be versioned beyond a container image? |
| **42** | Inference serving patterns, scaling, rate limiting and cost | Containerized inference API with load test and budget note | How does autoscaling inference differ from web traffic? |
| **43** | LLM application telemetry, prompt/version tracing, evals | Evaluate latency, cost, errors and prompt-response quality | Which failure modes make token-level monitoring insufficient? |
| **44** | Secure model deploy, release rollback and fallback | Deployment runbook + controlled failure/fallback demo | How do you release a new model safely? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [DataTalks.Club — MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp) · [DataTalks.Club — YouTube](https://www.youtube.com/@DataTalksClub) · [KServe Documentation](https://kserve.github.io/website/) · [Amazon Bedrock Documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html) · [ByteByteGo — Rate Limiter Design](https://www.youtube.com/watch?v=YXkOdWBwqaA) · [OpenTelemetry Documentation](https://opentelemetry.io/docs/) · [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction).
- **Choose when needed:** [OWASP — Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) · [Udacity — AI Ops Engineer Nanodegree](https://www.udacity.com/course/ai-ops-engineer-nanodegree--nd907) · [Google — Site Reliability Engineering Books](https://sre.google/books/) · optional substitute [ZTM AWS Bedrock](https://zerotomastery.io/courses/learn-aws-bedrock/) for managed AI/RAG/inference.

- [ ] **Month 11 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional AI release lab (Weeks 43–44):** [NextWork — GitOps Canary Deployments for LLM Services](https://nextwork.ai/projects/4834f07a-60e6-46b6-9666-56d37a132984). Measure latency, error rates and rollback quality; use small local inference workloads or safe test fixtures when possible.

### Month 12 — Secure read-only AIOps incident assistant and interview packaging
**Outcome:** Secure, read-only incident assistant and job-ready portfolio package.  **Monthly gate:** 20-case evaluation, prompt injection and permission-denial tests; full mock panel.

| Week | Concepts to learn | Hands-on / portfolio deliverable | Interview check |
|---|---|---|---|
| **45** | Tool-scoped read-only architecture, RBAC and request auditing | Read-only diagnostics endpoint; explicit deny mutation actions | How is least privilege enforced for a tool-using agent? |
| **46** | Prompt injection, untrusted logs, redaction and threat modeling | Malicious log fixtures and tests; no secrets in outputs | How do you stop log content from overriding instructions? |
| **47** | Evaluation, hallucination detection, reliability and failure handling | 20-case benchmark, citations to telemetry, uncertainty handling | What evidence validates an AI-generated incident hypothesis? |
| **48** | Portfolio handoff, interview simulation, job-search refresh | Record demo; present architecture, incidents, trade-offs and learnings | Can you explain one real challenge you solved personally? |

**Recommended materials (start with the first links; alternatives are for targeted gaps):**
- **Primary/core:** [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction) · [Udacity — AgentOps: Deploying, Guarding, Monitoring AI Agents](https://www.udacity.com/course/agentops-deploying-guarding-and-monitoring-ai-agents--cd15157) · [OWASP — Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) · [Udacity — AI Threat Modeling and Operational Defense](https://www.udacity.com/course/ai-threat-modeling-and-operational-defense--cd15147) · [AWS Security Documentation](https://docs.aws.amazon.com/security/) · [OpenTelemetry Demo / Astronomy Shop](https://opentelemetry.io/docs/demo/) · [Google — Site Reliability Engineering Books](https://sre.google/books/).
- **Choose when needed:** [Hello Interview — System Design in a Hurry](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction) · [Tech Interview Handbook](https://www.techinterviewhandbook.org/) · [Designing Data-Intensive Applications — O’Reilly](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781098119058/) · optional alternative [ZTM AI Agents](https://zerotomastery.io/courses/ai-agents-bootcamp/) to learn tool constraints and approvals.

- [ ] **Month 12 gate passed:** artifact works independently, at least one deliberately failed scenario is diagnosed, diagram/runbook is committed, and interview reasoning is demonstrated.

**Optional final-project accelerators (Weeks 45–48):** [NextWork — AI Infrastructure Operations Copilot](https://nextwork.ai/projects/45e74930-c12e-41f4-83bf-ec7fe145c598) and [NextWork — Kubernetes Agent with kagent](https://nextwork.ai/projects/6b73937a-3f61-43fb-9299-928344892504). Start with a **read-only** tool allowlist. Do not deploy mutation/repair capabilities to shared or production infrastructure; any proposed write action must remain disabled or require explicit approval within a disposable sandbox. Test malicious telemetry, denied permissions and factual grounding.

---

## 4. Sixteen-week interview acceleration plan
Practice interviews **from Week 1**, in parallel with labs. The advanced roadmap is not a reason to delay job applications.

| Period | Interview focus | Minimum output |
|---|---|---|
| Weeks **1–4** | Linux, networking, Git, Bash, Python | 2 short scripts, 6 documented incidents, 1 timed troubleshooting mock |
| Weeks **5–8** | AWS IAM, VPC, HA, AWS design | 2 HLD whiteboards, `AccessDenied` mock, AWS project walkthrough |
| Weeks **9–12** | Terraform, state, testing, security | 2 Terraform failure explanations, live IaC plan review and PR review simulation |
| Weeks **13–16** | CI/CD, Docker, EKS/GitOps, system design | 1 end-to-end project demo, 1 break/fix interview, 2 mocks, tailored resume |
| Weeks **17+** | SRE/DevSecOps/platform depth while applying | Weekly mock, targeted gap repair and deeper portfolio evidence |

**Interview practice cadence:**
- **Monday/Tuesday:** 20–30 minutes each, explain 3 concepts aloud with a diagram or terminal command.
- **Thursday:** 30–45 minutes of Python automation or shell coding; two questions/week (one practical ops coding, one data-structure/problem-solving).
- **Weekend:** 30–45 minutes of system design *or* a troubleshooting simulation; alternate each week. Every fourth week, do a full 45–60-minute mock.
- **After Week 12:** refresh resume/portfolio, target roles matched to real experience, and start selective applications when Gate D is passed. Maintain an interview error log, not just a question list.
**System-design study mini-sequence (six sessions, ~2 hours/session spread across Months 2–8):**
1. HLD framework and requirements — [freeCodeCamp / Gaurav Sen — System Design for Beginners](https://www.youtube.com/watch?v=m8Icp_Cid5o) and [Hello Interview — System Design in a Hurry](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction); design a 3-tier AWS application.
2. Caching and horizontal scaling — [ByteByteGo — YouTube](https://www.youtube.com/@ByteByteGo) and [ByteByteGo — System Design 101](https://github.com/ByteByteGoHq/system-design-101); design read replica + Redis + autoscaling trade-offs.
3. Gateways, proxies, routing, rate limiting — [Cloud X Berry — Reverse Proxy vs Load Balancer vs API Gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) and [ByteByteGo — Rate Limiter Design](https://www.youtube.com/watch?v=YXkOdWBwqaA); explain ALB vs API Gateway vs ingress.
4. Queues, retry, backpressure and idempotency — [Ashish Pratap Singh — 30 System Design Concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk); design a resilient async job worker.
5. CI/CD platform and observability system — [Hello Interview — System Design in a Hurry](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction); design secrets handling, versioned artifacts, alert cardinality and storage retention.
6. Timed mock: multi-AZ e-commerce on EKS with security and recovery; defend SLOs, costs, blast radius and trade-offs.

## 5. Flagship portfolio: architecture, repo and acceptance tests
**Project:** `cloud-native-devsecops-platform` — one evolving platform rather than 12 unrelated tutorials. Use [OpenTelemetry Astronomy Shop](https://opentelemetry.io/docs/demo/) or a small independently created API/worker system. Prefer a small app early, adding complexity only when it creates a useful operational test.
**High-level architecture:**
```text
Developer -> PR -> tests/linters/security scans -> GitHub Actions
       |                    |
       |                    +-- OIDC trust -> scoped AWS IAM role
       v                                     |
   GitOps config repo                  Signed image -> ECR
       |                                     |
       +-- Argo CD -> Helm/Kustomize -> EKS workload in AWS VPC
                                             |
User -> Route 53 -> ALB/Ingress -> Service -> API -> (RDS/queue/cache)
                                             |
                              OTel Collector -> metrics/logs/traces
                                             |
                           Grafana / alerts / SLO dashboards

Terraform -> VPC, IAM, ECR, EKS, endpoints, tagged resources, budgets
Security  -> least-privilege identity + image signature policy + policies
Operations-> incident runbooks, rollback, backup and restore tests
Optional -> read-only AI triage tool, scoped to diagnostics only
```
**Suggested repository:**
```text
cloud-native-devsecops-platform/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── decisions/
│   ├── threat-model.md
│   ├── cost-and-teardown.md
│   └── incidents/
├── app/
├── tests/
├── scripts/
├── infra/terraform/{modules,environments}/
├── .github/workflows/
├── deploy/{helm,argocd}/
├── security/{policies,sbom,attestations}/
├── observability/{dashboards,alerts,collectors}/
├── platform/{templates,docs}/
├── ai-incident-assistant/
└── runbooks/
```
**Portfolio definition of done (testable, not aspirational):**
- [ ] For any [NextWork](https://nextwork.ai/) guided lab used, rebuild a meaningful subsystem **without following the steps**, explain each design choice, add a negative/failure test and attribute tutorial origins in the README.
- [ ] Include at least one before/after engineering improvement over a guided baseline (e.g., narrower OIDC permissions, safe rollout gate, useful SLO or trace-based root cause).
- [ ] Fresh clone reproduces local build and a safe cloud deployment with documented pre-requisites.
- [ ] Cloud budgets/alerts exist and short-lived environments can be destroyed; post-destroy inventory is clean.
- [ ] Git history shows personally authored Terraform modules, app changes, scripts and CI workflows.
- [ ] Terraform validation, scans, plan review, state controls and least-privilege IAM checks are in place.
- [ ] GitHub Actions uses AWS OIDC; no long-lived AWS keys in repo, CI variables or demo footage.
- [ ] Containers run non-root where practical, with health probes, resource requests/limits and no baked-in secrets.
- [ ] Argo CD has a known rollback path; intentionally broken release is diagnosed and rolled back.
- [ ] One denied IAM action, one failed image trust policy and one rejected network flow are demonstrated.
- [ ] Observability links user-visible degradation with logs, metrics and distributed traces.
- [ ] An alert fires on a defined symptom and links to a usable runbook (not just a dashboard).
- [ ] At least six safe lab incidents have root causes, commands, fix evidence and prevention steps.
- [ ] Backup restore is tested and measured (RTO/RPO); failures are recoverable without hidden tutorial state.
- [ ] One architecture diagram, two ADRs, threat model and cost/performance/security trade-offs are documented.
- [ ] A 2-minute demo, 15-minute deep dive and 30-minute troubleshooting defense can be performed without prompts.
- [ ] The portfolio is labeled an independent educational/lab environment, not employer production experience.

**Proof-pack for interviews:** `docs/architecture.md`, screenshots or sanitized terminal outputs, PR/check run links, at least three memorable break/fix stories, one measured restore, one security denial, one cost/cleanup report and the architectural trade-offs. Record commands and outcomes, not sensitive account information.

## 6. Interview preparation, mock questions and coding

### Linux and networking
- [ ] Explain the order of investigation for high CPU, high load average, OOMKilled and high IO wait.
- [ ] A service cannot start. Which systemd, journald, permission and port checks do you run?
- [ ] Walk through DNS, TCP handshake, TLS handshake and HTTP request/response; identify failure boundaries.
- [ ] Difference between reverse proxy, ALB, API gateway, ingress, and L4/L7 balancing.
- [ ] How do you prove whether a connectivity issue is routing, firewall, DNS or application-level?

### AWS
- [ ] Explain IAM policies, resource policies, permission boundaries, SCPs and role trust policies.
- [ ] Design multi-AZ web hosting with private compute, ALB, RDS and secure egress.
- [ ] Explain SG/NACL rules, NAT gateway vs VPC endpoint, and private subnet access.
- [ ] Diagnose AccessDenied, unhealthy ALB targets, unexpected bill growth, and failed autoscaling.
- [ ] Compare EKS/ECS/EC2 for security, cost, developer velocity and operations.

### Terraform
- [ ] What is Terraform state, why is it sensitive, and how do you lock and protect it?
- [ ] Design Terraform modules and environment separation without copy-paste sprawl.
- [ ] Explain drift, import, `moved` blocks, dependency ordering and plan-review safety.
- [ ] How would you keep cloud secrets out of Terraform state and CI logs?
- [ ] How do you prevent an accidental `terraform destroy` on production?

### CI/CD, Kubernetes and GitOps
- [ ] Contrast CI, CD, image registry, Helm release and GitOps desired-state reconciliation.
- [ ] Design GitHub OIDC trust, approval boundaries, least privilege and artifact promotion.
- [ ] Debug CrashLoopBackOff, ImagePullBackOff, Pending pods and Service selector mismatches.
- [ ] How do readiness/liveness/startup probes differ? Why might they cause an outage?
- [ ] How do you perform a safe rollback with Argo CD? What if the database schema changes?

### DevSecOps, networking and SRE
- [ ] What are SBOM, provenance, signed images and admission policy? Where are the limitations?
- [ ] Debug a default-deny Cilium policy using DNS and observed flows.
- [ ] What is an SLI, SLO, SLA and error budget? Give an alerting example.
- [ ] How do you correlate logs, metrics and traces to isolate high p99 latency?
- [ ] Explain a real-like lab incident: impact, diagnosis, mitigation, root cause, follow-up and measurable recovery.

### Architecture and platform
- [ ] Design a highly available AWS application with RTO/RPO and an affordable recovery strategy.
- [ ] Design a multi-team CI/CD platform with role isolation and artifact security.
- [ ] Design a monitoring pipeline: ingestion, cardinality, retention, query and alert fan-out.
- [ ] Design a Backstage golden path that cannot escalate privileges or create unlimited cost.
- [ ] Explain caching, replication, sharding, idempotency, retries, rate limiting and eventual consistency.

### AI/AIOps safety
- [ ] How would you constrain a diagnostic agent to read-only Kubernetes/AWS API operations?
- [ ] How can an attacker inject instructions through untrusted logs or tool responses?
- [ ] What quantitative measures show whether the AI triage assistant is reliable?
- [ ] How do you avoid sending secrets/PII to an external model during incident analysis?

**Coding/automation target (2 problems/week):** log parser with counts/percentiles; retry with exponential backoff and jitter; process health monitor; JSON/YAML config validator; duplicate-alert suppression; CIDR membership; pagination over an API; checksum/digest verifier; parse and group Kubernetes events; small data-structure exercises (arrays/strings/hash maps/stacks/graphs). Test each script with happy-path and failure cases; explain time and space complexity. Use [Harvard CS50 — Introduction to Programming with Python](https://cs50.harvard.edu/python/), [pytest documentation](https://docs.pytest.org/en/stable/) and (only as needed) [Tech Interview Handbook](https://www.techinterviewhandbook.org/).
**Behavioral story bank (STAR/CAR, fully truthful):** describe a release-quality decision, a test failure you reproduced, a scripting improvement, a defect triage with stakeholders, a time you identified an operational risk, a disagreement, a missed expectation and your response, and an independent cloud lab showing growth. State clearly whether an event was professional experience or a home lab.
**Mock interview scorecard (0–4 each; revisit scores weekly):** correctness; troubleshooting process; design trade-offs; communication; security; production/cost awareness; programming/test quality. Target **≥3** in core categories before broadening to senior-level interviews; no single aggregate score guarantees hiring.

## 7. Readiness gates and application strategy

| Gate | When | Must independently demonstrate |
|---|---|---|
| **A — Linux/operator fluency** | Week 4 | Diagnose a Linux failure and a DNS/network failure; Python tool with tests; six written incident examples |
| **B — Cloud fluency** | Week 8 | Secure AWS design, role debugging, routing explanation, 15-minute architecture walkthrough and teardown |
| **C — IaC fluency** | Week 12 | Reproducible Terraform modules, protected state, CI validation, detected drift and safe destroy |
| **D — Initial interview readiness** | Week 16 | CI through OIDC/ECR/EKS/GitOps, rollback, ≥3 independently solved faults, diagram, truthful project explanation, 2 timed mocks |
| **E — Strong SRE/DevSecOps depth** | Week 32 | Security policy tests, correlated observability, quantified SLOs and a measured restore |
| **F — Advanced differentiation** | Week 48 | Golden path, cost controls and evaluated read-only AI diagnostic assistant |

**Application strategy:** Use Weeks 1–12 to assemble evidence and shortlist suitable roles; start selective applications around Weeks 13–16 **only after** core artifacts are demonstrable. Progress from Cloud/DevOps/CI-CD engineering roles into roles with greater platform and SRE ownership. Look at individual job descriptions rather than assuming that 10+ years overall means 10+ years of professional DevOps ownership. Tailor the resume to actual duties, demonstrate lab work separately, and use your QA background as a differentiator in testing, release safety and reliability.
**Interview pipeline:** for each application track date, company/role, specific stack, recruiter screen, coding, troubleshooting, system design, behavioral, open gaps and next action. Keep private data in a local document, not a public repo. After rejections, log the missing skill and address it with one targeted lab, not another full course.

## 8. Complete curated learning materials and direct links
This is the **comprehensive index** referenced by the 48-week tables. You do **not** have to complete everything. **P0** means core suggested material where needed, **Gap-only** means use for a weakness, **Alternative** means choose one, and **Optional** means advanced/subscription/specialization. The link is to an actual video, playlist, course page, lab or documentation; channel links deliberately serve as discovery references when a suitable exact lesson is not established. Verify content and version against current official documentation.

### Linux, networking, shell and Python

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [freeCodeCamp — Linux Server Administration (Shawn Powers)](https://www.youtube.com/watch?v=WMy3OzvBWc0) | YouTube | P0 | Linux administration: users, storage, packages, systemd, networking, troubleshooting. |
| [freeCodeCamp — 50 Linux / Terminal Commands](https://www.youtube.com/watch?v=ZtqBQ68cfJc) | YouTube | Gap-only | Refresh core commands if shell navigation and pipelines are slow. |
| [freeCodeCamp — Introduction to Linux](https://www.youtube.com/watch?v=sWbUDq4S6Y8) | YouTube | Alternative | Replace, not stack with, the Linux Server course for an introductory pathway. |
| [freeCodeCamp — Bash Scripting Tutorial](https://www.youtube.com/watch?v=tK9Oc6AEnR4) | YouTube | P0 | Shell scripting entry point; supplement with ShellCheck and self-written scripts. |
| [MIT — The Missing Semester](https://missing.csail.mit.edu/) | Free course | P0 | Shell, version control, data wrangling, debugging, environment and tooling. |
| [Harvard CS50 — Introduction to Programming with Python](https://cs50.harvard.edu/python/) | Free course | P0 | Python fundamentals, testing, I/O, exceptions and automation. |
| [Kunal Kushwaha — Computer Networking Full Course](https://www.youtube.com/watch?v=IPvYjXCsTg8) | YouTube | P0 | OSI/TCP-IP, routing, practical networking and application troubleshooting. |
| [Kunal Kushwaha — Git and GitHub Full Tutorial](https://www.youtube.com/watch?v=apGV9Kg7ics) | YouTube | P0 | Branching, merging, pull requests and source-control workflows. |
| [Kunal Kushwaha — Linux / Terminal Commands](https://www.youtube.com/watch?v=iwolPf6kN-k) | YouTube | Optional | Faster Linux basics refresher. |
| [Practical Networking — YouTube](https://www.youtube.com/@PracticalNetworking) | YouTube channel | Alternative | Visual TCP/IP, subnetting and packet behavior. |
| [Cloud X Berry — 20 Networking Topics](https://www.youtube.com/watch?v=TR0RU2pmMeA) | YouTube | Optional | Short overview of application-networking components. |
| [Cloud X Berry — Reverse Proxy vs Load Balancer vs API Gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) | YouTube | P0 | Map edge and request-routing components onto AWS designs. |
| [Cloud X Berry — Backend Ecosystem Explained](https://www.youtube.com/watch?v=mZ27vUoOEB0) | YouTube | Optional | Trace applications through services, data stores, CI/CD and observability. |
| [Cloud X Berry — Linux Filesystem Directories](https://www.youtube.com/watch?v=qvjRcZcW8CY) | YouTube | Optional | Quick orientation to Linux layout. |
| [Brendan Gregg — Linux Systems Performance](https://www.youtube.com/watch?v=fhBHvsi0Ql0) | YouTube | P0 | Performance investigation methodology, CPU, memory and disk bottlenecks. |
| [SadServers — Troubleshooting Scenarios](https://sadservers.com/scenarios) | Interactive lab | P0 | Independent broken-server diagnosis under controlled conditions. |
| [ShellCheck](https://www.shellcheck.net/) | Official tool | P0 | Static checks for reliable Bash scripts. |
| [pytest documentation](https://docs.pytest.org/en/stable/) | Official documentation | P0 | Automated tests for CLI and operational Python tooling. |
| [Udacity — Configuring Linux Web Servers](https://www.udacity.com/course/configuring-linux-web-servers--ud299) | Free course | Optional | Linux server practice; examples may be old. |
| [Udacity — Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123) | Free course | Optional | Alternative Git fundamentals. |

### AWS architecture and cloud operations

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [Adrian Cantrill — AWS Solutions Architect Associate](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) | Paid course | P0 (if accessible) | Detailed AWS fundamentals, networking, identity, storage and architecture. |
| [Adrian Cantrill — Technical Fundamentals](https://learn.cantrill.io/p/tech-fundamentals) | Course | Gap-only | Optional prerequisite if core networking and infrastructure remain weak. |
| [AWS Workshops](https://workshops.aws/) | Free official labs | P0 | AWS hands-on reference workshops. |
| [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) | Official documentation | P0 | Operational, reliability, security, performance, cost and sustainability trade-offs. |
| [AWS IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) | Official documentation | P0 | IAM, temporary credentials, least privilege and security guardrails. |
| [AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) | Official documentation | P0 | Set alerts and limits before cloud labs. |
| [Amazon EKS Workshop](https://www.eksworkshop.com/) | Official hands-on labs | P0 | Hands-on AWS EKS operating patterns. |
| [AWS Security Documentation](https://docs.aws.amazon.com/security/) | Official documentation | P0 | Cloud IAM, audit, network security and threat reduction. |

### Terraform and CI/CD

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [Ansible — Getting Started](https://docs.ansible.com/ansible/latest/getting_started/index.html) | Official documentation | Optional | Configuration-management basics after Terraform; not required for Week 16. |
| [TechWorld with Nana — Jenkins Pipeline Tutorial](https://www.youtube.com/watch?v=7KCS70sCoK0) | YouTube | Optional | Jenkinsfiles, pipelines and CI/CD comparison with GitHub Actions. |
| [HashiCorp — Terraform Tutorials](https://developer.hashicorp.com/terraform/tutorials) | Official hands-on tutorials | P0 | Terraform state, modules, plan, apply, tests and IaC practices. |
| [Piyush Sachdeva — 30 Days of Terraform on AWS](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp) | YouTube playlist | P0 | End-to-end Terraform/AWS implementation; choose this or Anton as guide. |
| [Piyush Sachdeva — Terraform Drift](https://www.youtube.com/watch?v=nRgNIy-SDEw) | YouTube | P0 | Understand safe drift remediation. |
| [Anton Putra — Terraform Playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA) | YouTube playlist | Alternative | Detailed IaC demos; choose if Piyush presentation does not suit you. |
| [Anton Putra — Full Tutorials Index](https://github.com/antonputra/tutorials/blob/main/docs/contents.md) | GitHub index | Optional | Find exact infrastructure lesson and source code. |
| [KodeKloud — Learning Paths](https://kodekloud.com/learning-paths/) | Courses + labs | P0 (if subscribed) | Primary interactive DevOps lab platform. |
| [KodeKloud — DevOps Engineer Learning Path](https://kodekloud.com/learning-path/devops-engineer) | Courses + labs | Alternative | Structured labs and guided projects when a roadmap is desired. |
| [TechWorld with Nana — Docker Full Course](https://www.youtube.com/watch?v=3c-iBn73dDE) | YouTube | P0 | Container fundamentals and working applications. |
| [TechWorld with Nana — GitHub Actions](https://www.youtube.com/watch?v=R8_veQiYBjI) | YouTube | Alternative | CI/CD workflows and automation introduction. |
| [Kunal Kushwaha — GitHub Actions CI/CD](https://www.youtube.com/watch?v=62N8UiWUdQo) | YouTube | P0 | Practical pipeline walkthrough with checks. |
| [GitHub — Configure OIDC in AWS](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) | Official documentation | P0 | Workload identity and short-lived AWS tokens in CI/CD. |
| [GitHub Actions to AWS Using OIDC — Video](https://www.youtube.com/watch?v=Sdzd4N6L5Hg) | YouTube | P0 | Guided OIDC trust setup; compare against current docs. |
| [Trivy Documentation](https://trivy.dev/latest/docs/) | Official documentation | P0 | Image, dependency, filesystem and IaC vulnerability scanning. |

### Kubernetes, EKS, GitOps and networking

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [TechWorld with Nana — Kubernetes Full Course](https://www.youtube.com/watch?v=X48VuDVv0do) | YouTube | Gap-only | Kubernetes refresh; skip mastered CKA/CKAD content. |
| [TechWorld with Nana — Argo CD](https://www.youtube.com/watch?v=MeU5_k9ssrs) | YouTube | Alternative | GitOps explanation and demonstration. |
| [Kunal Kushwaha — Argo CD / GitOps](https://www.youtube.com/watch?v=8YLsQIG2Svo) | YouTube | P0 | GitOps deployment fundamentals. |
| [Piyush Sachdeva — GitOps on EKS](https://www.youtube.com/watch?v=c_a5e2Dnxkk) | YouTube | P0 | AWS/EKS GitOps walkthrough. |
| [Anton Putra — EKS Playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXnKY6XmeifEpjIfkWRo9v2l) | YouTube playlist | Alternative | Deeper AWS/EKS configuration and troubleshooting. |
| [Anton Putra — Argo CD Playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkktZoHhmL6sbg7ELNjv9Xw) | YouTube playlist | Optional | Advanced GitOps workflows. |
| [Argo CD Documentation](https://argo-cd.readthedocs.io/en/stable/) | Official documentation | P0 | GitOps app sync, health, rollback and policies. |
| [Helm Documentation](https://helm.sh/docs/) | Official documentation | P0 | Kubernetes templating and charts. |
| [kind — Kubernetes in Docker](https://kind.sigs.k8s.io/) | Free local lab | P0 | Affordable local Kubernetes experimentation. |
| [Kubernetes Documentation](https://kubernetes.io/docs/) | Official documentation | P0 | Current API behaviors and debugging references. |
| [Piyush Sachdeva — Kubernetes Troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc) | YouTube | P0 | Failure diagnosis and kubectl debugging. |
| [Liz Rice — Cloud Native Superpowers with eBPF](https://www.youtube.com/watch?v=ZXDhKUeUUSs) | YouTube | P0 | Understand datapath, observability and kernel capabilities. |
| [Civo / Kunal Kushwaha — Cilium Networking, Security & Observability](https://www.youtube.com/watch?v=yQoVOumoY5k) | YouTube | P0 | Apply network policies and analyze Hubble flows. |
| [Isovalent — Cilium Getting Started Labs](https://isovalent.com/labs/cilium-getting-started/) | Free interactive lab | P0 | Network-policy exercises without expensive cloud infrastructure. |

### DevSecOps and supply-chain security

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [OpenSSF Training](https://openssf.org/training/) | Free security training | P0 | Secure supply chain and software development. |
| [TechWorld with Nana — DevSecOps / Docker Scout](https://www.youtube.com/watch?v=gLJdrXPn0ns) | YouTube | Optional | Introduce security gates in delivery pipelines. |
| [Sigstore Cosign](https://docs.sigstore.dev/cosign/overview/) | Official documentation | P0 | Image signatures and provenance concepts. |
| [Kyverno — Verify Images](https://kyverno.io/docs/policy-types/cluster-policy/verify-images/sigstore/) | Official documentation | P0 | Kubernetes policy enforcement for trusted artifacts. |
| [DevOps Toolkit — Sign/Verify Images with Cosign and Kyverno](https://www.youtube.com/watch?v=HLb1Q086u6M) | YouTube | P0 | Video security enforcement demo; validate current syntax. |
| [Kubernetes Goat](https://madhuakula.com/kubernetes-goat/) | Free security lab | Alternative | Intentionally vulnerable Kubernetes exercises in a safe sandbox. |

### Observability, incident response and SRE

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [TechWorld with Nana — Prometheus Monitoring](https://www.youtube.com/watch?v=h4Sl21AKiDg) | YouTube | Optional | Intro to Prometheus data and architecture before full OTel projects. |
| [CNCF — OpenTelemetry Hands-on Tutorial](https://www.youtube.com/watch?v=8CKgAyenEjo) | YouTube | P0 | Instrument services and configure telemetry collection. |
| [OpenTelemetry Demo / Astronomy Shop](https://opentelemetry.io/docs/demo/) | Free demo application | P0 | Complex traced distributed application for SRE drills. |
| [OpenTelemetry Documentation](https://opentelemetry.io/docs/) | Official documentation | P0 | Current SDK, collector and signal practices. |
| [Grafana — Getting Started with OpenTelemetry](https://www.youtube.com/watch?v=Xhh9V7uRP88) | YouTube | Alternative | Observability ecosystem overview. |
| [Piyush Sachdeva — Observability Playlist](https://www.youtube.com/playlist?list=PLl4APkPHzsUWC89lwHRGxk1GDtS7dkUsE) | YouTube playlist | Alternative | Cloud monitoring and telemetry implementation. |
| [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/) | Official documentation | P0 | Time series, queries, alerts, service monitoring. |
| [Grafana Documentation](https://grafana.com/docs/) | Official documentation | P0 | Dashboards, alerting and visualization. |
| [Google — Site Reliability Engineering Books](https://sre.google/books/) | Free books | P0 | SLI/SLOs, incidents, toil, error budgets and production practices. |

### System design, backend architecture and platform engineering

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [CNCF — Starting and Scaling a Platform Engineering Team](https://www.youtube.com/watch?v=9lPp-6nJ8bI) | YouTube | P0 | Platform as product, golden paths and team-level strategy. |
| [TeKanAid — Backstage Crash Course](https://www.youtube.com/watch?v=JbX6V9fz5QA) | YouTube | Optional | Self-service software catalog and developer portal. |
| [Backstage Documentation](https://backstage.io/docs/) | Official documentation | P0 | Developer portal templates and permissions. |
| [FinOps Foundation — Start Here](https://www.finops.org/training-certification/recommended/new-to-finops/) | Free learning | P0 | Cost allocation, optimization and accountability. |
| [ByteByteGo — YouTube](https://www.youtube.com/@ByteByteGo) | YouTube channel | P0 | Visual system design foundations. |
| [ByteByteGo — System Design 101](https://github.com/ByteByteGoHq/system-design-101) | Free reference | P0 | System design reference diagrams and concepts. |
| [ByteByteGo — Rate Limiter Design](https://www.youtube.com/watch?v=YXkOdWBwqaA) | YouTube | P0 | Traffic shaping, throttling, distributed rate limiting. |
| [Ashish Pratap Singh — 30 System Design Concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk) | YouTube | P0 | Fundamentals for HLD and scalability discussions. |
| [Ashish Pratap Singh — System Design Interview Preparation](https://www.youtube.com/watch?v=l3X1t3kpmwY) | YouTube | Optional | Interview strategy and communication. |
| [Ashish Pratap Singh — System Design Playlist](https://www.youtube.com/playlist?list=PLCZ2MME8uzMhow9-hAsSm2-dvfF4ag6wy) | YouTube playlist | Optional | More system design case studies. |
| [Hello Interview — System Design in a Hurry](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction) | Free guide + premium options | P0 | Structured interview framework and design problems. |
| [freeCodeCamp / Gaurav Sen — System Design for Beginners](https://www.youtube.com/watch?v=m8Icp_Cid5o) | YouTube | P0 | Structured system design exercise. |
| [KodeKloud — System Design for Beginners](https://www.youtube.com/watch?v=SE2KF-vxvS0) | YouTube | Alternative | System design plus related practice labs. |
| [Hussein Nasser — Backend Engineering](https://www.youtube.com/@hnasr) | YouTube channel | P0 | Backend/networking internals and production troubleshooting. |
| [Arpit Bhayani — YouTube](https://www.youtube.com/@ArpitBhayani) | YouTube channel | Optional | Distributed systems and databases deep dives. |
| [Designing Data-Intensive Applications — O’Reilly](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781098119058/) | Paid book | Optional | Distributed systems architecture and trade-offs. |

### AI, AIOps, LLMOps and AI security

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [Vishakha Sadhwani — AWS Bedrock AIOps Part 4](https://www.youtube.com/watch?v=WyLWj5MjzCE) | YouTube | Optional | AI-assisted operations architecture; assess permission, grounding and cost gaps. |
| [DataTalks.Club — YouTube](https://www.youtube.com/@DataTalksClub) | YouTube channel | Optional | MLOps Zoomcamp and data/ML production workflows. |
| [DataTalks.Club — MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp) | Free course | Optional | ML lifecycle, experiment tracking and productionization. |
| [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction) | Free course | P0 (AI phase) | Agent concepts and integration. |
| [OWASP — Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) | Free guidance | P0 (AI phase) | LLM/agent threat and defensive design ideas. |
| [Amazon Bedrock Documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html) | Official documentation | Optional | Managed AI model integration reference. |
| [KServe Documentation](https://kserve.github.io/website/) | Official documentation | Optional | Kubernetes model serving architecture. |
| [Vishakha Sadhwani — DevOps / AIOps Intro](https://www.youtube.com/watch?v=UBzYwNbFCKs) | YouTube | Optional | Project architecture and AI ops learning orientation. |
| [Vishakha Sadhwani — Project Implementation](https://www.youtube.com/watch?v=abkv1MSk1lU) | YouTube | Optional | Step-by-step project supplement. |

### Zero To Mastery (ZTM) — optional paid alternatives to existing courses

**Do not add these to the mandatory 48-week curriculum.** [ZTM](https://zerotomastery.io/) provides recorded lessons and project exercises. Sample its previews, then substitute **one** course only if the stated skill gap is confirmed. Course lengths are catalog estimates, and independent tests/failure drills remain mandatory. [Detailed selection rules and assignments](#13-zero-to-mastery--optional-paid-course-overlays).

| Direct course link | Week(s) | Decision | Evidence |
|---|---|---|---|
| [Bash Scripting](https://zerotomastery.io/courses/learn-bash-scripting/) | 3–4 | **Best immediate ZTM candidate** if Bash is weak | ShellCheck, safe exit codes, tested service health scripts |
| [Linux & Sysadmin Bootcamp](https://zerotomastery.io/courses/devops-bootcamp/) | 1–4 | Alternative to freeCodeCamp Linux introductory learning | Systemd/permissions recovery without guidance |
| [Python Automation](https://zerotomastery.io/courses/learn-python-automation/) | 3–4 | Only if CS50P is insufficient | Python CLI, pytest, robust exceptions |
| [Terraform Bootcamp](https://zerotomastery.io/courses/learn-terraform-certification/) | 9–12 | Alternative to beginner Terraform tutorials | Tested Terraform modules, remote state and CI plan |
| [System Design + Architecture](https://zerotomastery.io/courses/system-design/) | 33–40 | Low priority after ByteByteGo/Hello Interview | Two timed cloud HLD mocks |
| [AWS Bedrock Bootcamp](https://zerotomastery.io/courses/learn-aws-bedrock/) | 41–44 | Strong **optional** advanced AI alternative | Grounded, measured, cost-capped AI application |
| [AI Agents Bootcamp](https://zerotomastery.io/courses/ai-agents-bootcamp/) | 45–48 | Optional agent integration alternative | Read-only tools, citations, audit, injection evaluation |

### NextWork.ai — optional hands-on project library

[NextWork.ai](https://nextwork.ai/) provides guided technical projects. **Use one project per identified skill gap, then extend it independently**; do not complete the entire catalog. Platform access and project availability can change, and AWS services can incur charges regardless of any free learning access.

| Project and direct link | Suggested week | Purpose and independent acceptance evidence |
|---|---|---|
| [Linux Service Health Monitor](https://nextwork.ai/projects/5d8df751-6459-473f-ae86-d8ee7ad4ccc3) | 1–2 | systemd diagnosis; service failure + recovery log and runbook. |
| [Terraform GitOps Foundation on AWS](https://nextwork.ai/projects/7f66d30f-cafc-46d8-b106-f48321581f37) | 10–12 | Terraform modules, AWS OIDC, PR-based plan and secure state. |
| [Terraform EKS with GitHub Actions CI/CD](https://nextwork.ai/projects/d40c742f-9bac-40c1-b651-52ae96e6ba30) | 13–15 | IaC-provisioned EKS; signed off architecture, scoped roles, teardown. |
| [End-to-End GitOps Pipeline](https://nextwork.ai/projects/2757d4a2-0371-4c1c-8389-4e52c53dac6b) | 15–16 | Local cluster, GitHub Actions, Argo CD, bad-release recovery. |
| [Observability and SLOs on Kubernetes](https://nextwork.ai/projects/0a918f05-9085-4ff0-a825-7c1000d13108) | 27–29 | Prometheus, SLI/SLOs, burn-rate alert test and incident report. |
| [GitOps Canary Deployments with Argo](https://nextwork.ai/projects/df2b6349-a5e8-4448-b807-7564d6a3c015) | 30–32 | Metric-gated rollout; failed canary abort and evidence. |
| [GitOps Across Clusters with Argo CD](https://nextwork.ai/projects/41b34a8d-255a-4b89-876d-4ec34e9c5184) | 34–35 | Environment promotion, drift recovery and tenancy limits. |
| [GitOps Canary Deployments for LLM Services](https://nextwork.ai/projects/4834f07a-60e6-46b6-9666-56d37a132984) | 43–44 | AI release health checks, metric-gated rollback and inference cost. |
| [AI Infrastructure Operations Copilot](https://nextwork.ai/projects/45e74930-c12e-41f4-83bf-ec7fe145c598) | 45–48 | Read-only incident analysis; runbook references and 20-case evaluation. |
| [Kubernetes Agent with kagent](https://nextwork.ai/projects/6b73937a-3f61-43fb-9299-928344892504) | 45–48 | Optional advanced agent lab; deny write tools and test approval boundaries. |

See [Section 12](#12-nextworkai--guided-projects-and-independent-portfolio-extensions) for sequencing, cost controls and completion gates.

### Creator indexes and YouTube channels

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [Cloud X Berry — YouTube](https://www.youtube.com/@TheCloudXBerry) | YouTube channel | Optional | Fast networking, Linux and backend concept refreshers. |
| [Piyush Sachdeva — YouTube](https://www.youtube.com/@TechTutorialswithPiyush) | YouTube channel | P0 | Hands-on AWS/Terraform/GitOps/observability videos. |
| [Vishakha Sadhwani — YouTube](https://www.youtube.com/@vishakha.sadhwani) | YouTube channel | Optional | Integrated DevOps and AI-assisted operations projects. |
| [TechWorld with Nana — YouTube](https://www.youtube.com/@TechWorldwithNana) | YouTube channel | P0 | DevOps conceptual teaching and demonstrations. |
| [Anton Putra — YouTube](https://www.youtube.com/@AntonPutra) | YouTube channel | Alternative | Advanced infrastructure walkthroughs and benchmarks. |
| [Kunal Kushwaha — YouTube](https://www.youtube.com/@KunalKushwaha) | YouTube channel | P0 | Networking, Git, GitOps and collaborative workflows. |
| [Kunal Kushwaha — DevOps Bootcamp Playlist](https://www.youtube.com/playlist?list=PL9gnSGHSqcnoqBXdMwUTRod4Gi3eac2Ak) | YouTube playlist | Optional | Full course if modular explanations are insufficient. |
| [DevOps Toolkit — YouTube](https://www.youtube.com/@DevOpsToolkit) | YouTube channel | P0 | GitOps, policy, platform engineering and cloud-native operations. |
| [CNCF — YouTube](https://www.youtube.com/@cncf) | YouTube channel | Optional | Expert talks about cloud-native operations. |

### Optional paid specialist courses (compare; do not stack)

| Resource | Format | Priority | Why/when to use |
|---|---|---|---|
| [O’Reilly — Linux System Administration Troubleshooting](https://www.oreilly.com/videos/linux-system-administration/0642572124694/) | Paid video | Optional | Diagnose Linux operational problems. |
| [O’Reilly — GitHub Actions in Action, Video Edition](https://www.oreilly.com/videos/github-actions-in/9781633437302VE/) | Paid narrated book | Optional | Detailed pipeline patterns; narrated-book format. |
| [O’Reilly — Kubernetes Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/) | Paid video | Optional | Deeper cluster hardening and security. |
| [O’Reilly — OpenTelemetry in Practice](https://www.oreilly.com/videos/opentelemetry-in-practice/9781807783334/) | Paid video | Optional | Specialist observability course. |
| [O’Reilly — SRE Essentials](https://www.oreilly.com/videos/site-reliability-engineering/9780135415016/) | Paid video | Optional | Structured SRE introduction. |
| [O’Reilly — Software Architecture Fundamentals](https://www.oreilly.com/videos/software-architecture-fundamentals/0642572016094/) | Paid video | Optional | Architecture patterns and decisions. |
| [Pluralsight — Linux Diagnostics and Troubleshooting](https://www.pluralsight.com/courses/red-hat-certified-specialist-in-linux-diagnostics-and-troubleshooting-ex342) | Paid course | Optional | Advanced Linux diagnostics path. |
| [Pluralsight — Hands-On Kubernetes Troubleshooting](https://www.pluralsight.com/courses/hands-on-kubernetes-troubleshooting) | Paid course | Optional | Practice diagnostic scenarios beyond CKA/CKAD. |
| [Pluralsight — Kubernetes SRE-Grade Observability](https://www.pluralsight.com/paths/kubernetes-sre-grade-observability) | Paid path | Optional | Prometheus, Grafana, Loki, Tempo, OpenTelemetry labs. |
| [Pluralsight — Terraform Path](https://www.pluralsight.com/paths/terraform) | Paid path | Optional | Terraform depth and testing after initial basics. |
| [Pluralsight — GitHub Actions Deep Dive](https://www.pluralsight.com/courses/github-actions-deep-dive) | Paid video | Optional | Deepen GitHub Actions knowledge. |
| [Pluralsight — Applying GenAI to DevOps](https://www.pluralsight.com/courses/applying-genai-devops-operations) | Paid video | Optional | AI tools for operations; evaluate recommendations carefully. |
| [Udacity — Site Reliability Engineer Nanodegree](https://www.udacity.com/course/site-reliability-engineer-nanodegree--nd087) | Paid Nanodegree | Optional | Reviewed project-oriented reliability curriculum. |
| [Udacity — Cloud Native Application Architecture Nanodegree](https://www.udacity.com/course/cloud-native-architecture-nanodegree--nd064) | Paid Nanodegree | Optional | Cloud-native apps, platform architecture and delivery. |
| [Udacity — Cloud DevOps Engineer Nanodegree](https://www.udacity.com/course/cloud-dev-ops-nanodegree--nd9991) | Paid Nanodegree | Optional | Project-heavy CI/CD and cloud fundamentals. |
| [Udacity — AI Ops Engineer Nanodegree](https://www.udacity.com/course/ai-ops-engineer-nanodegree--nd907) | Paid Nanodegree | Optional | ML/LLM operational engineering after core cloud skills. |
| [Udacity — AgentOps: Deploying, Guarding, Monitoring AI Agents](https://www.udacity.com/course/agentops-deploying-guarding-and-monitoring-ai-agents--cd15157) | Paid course | Optional | Agent monitoring, RBAC, guardrails and deployment. |
| [Udacity — AI Threat Modeling and Operational Defense](https://www.udacity.com/course/ai-threat-modeling-and-operational-defense--cd15147) | Paid course | Optional | AI attack surfaces and authorization controls. |
| [CBT Nuggets — Free Introduction to IT](https://www.cbtnuggets.com/it-training/intro-to-it) | Free lessons | Optional | Short sysadmin and cybersecurity refreshers. |
| [CBT Nuggets — Wireshark Certified Analyst Course](https://www.cbtnuggets.com/it-training/networking/wca-101) | Paid course | Optional | Packet analysis specialization. |
| [CBT Nuggets — CompTIA AutoOps+](https://www.cbtnuggets.com/it-training/comptia/autoops-plus) | Paid course | Optional | Automation breadth, overlaps KodeKloud. |
| [AlgoExpert — InfraExpert](https://www.algoexpert.io/) | Paid interview training | Optional | Infrastructure design and troubleshooting drills. |
| [AlgoExpert — SystemsExpert](https://www.algoexpert.io/) | Paid interview training | Optional | System design cases and distributed systems topics. |
| [Design Gurus — Grokking System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview) | Paid course | Optional | System-design interview structure if free preparation insufficient. |
| [Tech Interview Handbook](https://www.techinterviewhandbook.org/) | Free reference | Optional | Coding interview study and behavioral structure. |

## 9. Paid course choices and spending discipline
**Preferred spending order:** 1. Free/official materials and local labs; ZTM is optional after a tested gap, never a default purchase; 2. KodeKloud for repeatable exercises **if useful**; 3. Adrian Cantrill for AWS depth **if not already owned**; 4. one specialist course subscription for a proven shortfall. Check for employer access first; pricing, access, trial entitlements and course availability vary.

| Identified bottleneck | Start with free / existing | Paid **option only** | Purchase test |
|---|---|---|---|
| Linux troubleshooting | [freeCodeCamp — Linux Server Administration (Shawn Powers)](https://www.youtube.com/watch?v=WMy3OzvBWc0), [SadServers — Troubleshooting Scenarios](https://sadservers.com/scenarios) | [Pluralsight — Linux Diagnostics and Troubleshooting](https://www.pluralsight.com/courses/red-hat-certified-specialist-in-linux-diagnostics-and-troubleshooting-ex342) **or** [O’Reilly — Linux System Administration Troubleshooting](https://www.oreilly.com/videos/linux-system-administration/0642572124694/) | Can you solve realistic incidents independently after the free labs? |
| AWS depth | [AWS Workshops](https://workshops.aws/), [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) | [Adrian Cantrill — AWS Solutions Architect Associate](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) | Are VPC/IAM/system-design mistakes slowing you down? |
| IaC and CI/CD | [HashiCorp — Terraform Tutorials](https://developer.hashicorp.com/terraform/tutorials), [Piyush Sachdeva — 30 Days of Terraform on AWS](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp) | [Pluralsight — Terraform Path](https://www.pluralsight.com/paths/terraform) **or** [O’Reilly — GitHub Actions in Action, Video Edition](https://www.oreilly.com/videos/github-actions-in/9781633437302VE/) | Have you exhausted guided practice? |
| K8s troubleshooting | [Amazon EKS Workshop](https://www.eksworkshop.com/), [Piyush Sachdeva — Kubernetes Troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc) | [Pluralsight — Hands-On Kubernetes Troubleshooting](https://www.pluralsight.com/courses/hands-on-kubernetes-troubleshooting) | Can you independently resolve four common Kubernetes failures? |
| Kubernetes security | [OpenSSF Training](https://openssf.org/training/), [Kyverno — Verify Images](https://kyverno.io/docs/policy-types/cluster-policy/verify-images/sigstore/) | [O’Reilly — Kubernetes Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/) | Is secure policy implementation still weak? |
| Observability/SRE | [OpenTelemetry Demo / Astronomy Shop](https://opentelemetry.io/docs/demo/), [Google — Site Reliability Engineering Books](https://sre.google/books/) | [Pluralsight — Kubernetes SRE-Grade Observability](https://www.pluralsight.com/paths/kubernetes-sre-grade-observability) **or** [O’Reilly — OpenTelemetry in Practice](https://www.oreilly.com/videos/opentelemetry-in-practice/9781807783334/) **or** [Udacity — Site Reliability Engineer Nanodegree](https://www.udacity.com/course/site-reliability-engineer-nanodegree--nd087) | Need structured labs, specialist instruction or reviewed projects? Pick one. |
| Interview system design | [ByteByteGo — System Design 101](https://github.com/ByteByteGoHq/system-design-101), [Hello Interview — System Design in a Hurry](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction) | [AlgoExpert — InfraExpert](https://www.algoexpert.io/) **or** [AlgoExpert — SystemsExpert](https://www.algoexpert.io/) **or** [Design Gurus — Grokking System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview) | Only if timed mocks expose a repeatable reasoning gap. |
| AI operations specialization | [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction), [OWASP — Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) | [Udacity — AgentOps: Deploying, Guarding, Monitoring AI Agents](https://www.udacity.com/course/agentops-deploying-guarding-and-monitoring-ai-agents--cd15157) **or** [Udacity — AI Threat Modeling and Operational Defense](https://www.udacity.com/course/ai-threat-modeling-and-operational-defense--cd15147) | Only after you have a working, evaluated read-only prototype. |

**Udacity decision:** [Udacity — Site Reliability Engineer Nanodegree](https://www.udacity.com/course/site-reliability-engineer-nanodegree--nd087) offers structured project work if you need guided reviews; [Udacity — Cloud Native Application Architecture Nanodegree](https://www.udacity.com/course/cloud-native-architecture-nanodegree--nd064) and [Udacity — Cloud DevOps Engineer Nanodegree](https://www.udacity.com/course/cloud-dev-ops-nanodegree--nd9991) overlap your core path. **CBT Nuggets:** [CBT Nuggets — Free Introduction to IT](https://www.cbtnuggets.com/it-training/intro-to-it) is optional foundation material; [CBT Nuggets — Wireshark Certified Analyst Course](https://www.cbtnuggets.com/it-training/networking/wca-101) is only worth paying for when packet capture is a genuine gap. **O’Reilly:** prioritize advanced technical depth, not basic videos duplicated elsewhere. **Pluralsight:** troubleshoot and observe rather than re-certifying Kubernetes basics. Avoid maintaining several overlapping annual subscriptions.

## 10. First seven days: start immediately
- [ ] **Day 1 — 2h:** Review baseline without notes; set local Ubuntu VM or safe Linux sandbox; create GitHub repository and `docs/` folders.
- [ ] **Day 2 — 2h:** Watch targeted chapters of [freeCodeCamp — Linux Server Administration (Shawn Powers)](https://www.youtube.com/watch?v=WMy3OzvBWc0); inspect `/etc`, `/var/log`, `/proc`, users, permissions and systemd.
- [ ] **Day 3 — 2h:** Intentionally stop a disposable service; diagnose with `systemctl`, `journalctl`, `ss` and logs; write failure report.
- [ ] **Day 4 — 2h:** Study [Kunal Kushwaha — Computer Networking Full Course](https://www.youtube.com/watch?v=IPvYjXCsTg8); practice `dig`, `curl -v`, `ss`, `openssl s_client`, `ip route` and DNS failures.
- [ ] **Day 5 — 2h:** Review [Kunal Kushwaha — Git and GitHub Full Tutorial](https://www.youtube.com/watch?v=apGV9Kg7ics); create branch, commit Bash health check, open PR and merge; run [ShellCheck](https://www.shellcheck.net/).
- [ ] **Day 6 — 3h:** Write Python script with `argparse`, `json`, logging, exit codes and 3 [pytest documentation](https://docs.pytest.org/en/stable/) tests.
- [ ] **Day 7 — 2h:** Run one [SadServers — Troubleshooting Scenarios](https://sadservers.com/scenarios) exercise, record symptoms-to-resolution, rehearse five questions, plan Week 2.

**End-of-week evidence:** one Bash script, one tested Python script, one service incident, one network case, one merged pull request, and one 2-minute verbal explanation of a troubleshooting decision. **Optional:** [NextWork — Linux Service Health Monitor](https://nextwork.ai/projects/5d8df751-6459-473f-ae86-d8ee7ad4ccc3) can replace the service exercise once you independently reproduce and debug its failure. If you cannot produce this, reduce video consumption and repeat the build/diagnostic portions.

## 11. Progress templates and master checklist

### Twelve-month checkpoint tracker
- [ ] **Month 1:** Linux, networking, scripting and diagnostic habits.
- [ ] **Month 2:** AWS core architecture and operational fundamentals.
- [ ] **Month 3:** Terraform and repeatable infrastructure.
- [ ] **Month 4:** CI/CD, containers, Kubernetes and GitOps.
- [ ] **Month 5:** Cloud IAM, network security and threat modeling.
- [ ] **Month 6:** DevSecOps, Kubernetes networking and provenance.
- [ ] **Month 7:** Metrics, logs, traces and operational diagnostics.
- [ ] **Month 8:** SRE, incident response and disaster recovery.
- [ ] **Month 9:** Platform engineering, golden paths and FinOps.
- [ ] **Month 10:** Advanced AWS, resilience and safe AI-assisted operations.
- [ ] **Month 11:** AI workload delivery, model observability and LLMOps.
- [ ] **Month 12:** Secure read-only AIOps incident assistant and interview packaging.

### Interview and portfolio checkpoints
- [ ] Gate A — Linux/networking diagnostic demonstration
- [ ] Gate B — secure AWS design walkthrough and teardown
- [ ] Gate C — Terraform modules, CI and drift recovery
- [ ] Gate D — working OIDC/ECR/EKS/GitOps pipeline plus rollback; targeted applications
- [ ] Gate E — signed images, observability, SLO, restore and postmortem
- [ ] Gate F — platform golden path, FinOps evidence and read-only AI evaluation
- [ ] Two full 45-minute mocks and a 15-minute architecture narrative
- [ ] Private application tracker and truthful resume updates

### Weekly log template (copy into `docs/progress/YYYY-WW.md`)
```markdown
# Week NN — Focus

## Study time (target 15 hours)
- Learning/docs: __/3h
- Build/lab: __/6h
- Break/fix: __/2h
- Interview practice: __/2h
- Portfolio/career: __/2h

## What I implemented
- Commit / PR link:
- Architecture decisions:
- Reproduction steps:

## Failure investigation
- Symptoms / user impact:
- Hypotheses and evidence:
- Root cause and fix:
- Prevention / alert or test:

## Interview questions answered out loud
1.
2.
3.

## Gaps, cloud bill and clean-up
- Skill gap to address:
- Resources still running:
- Teardown / budget evidence:

## Next week (top two goals)
-
-
```

### Resume and interview storytelling rules
- Demonstrate what **you actually built or owned**; clearly label personal/cloud labs as independent projects.
- Translate manual QA experience into concrete strengths—test design, release risk identification, incident reproduction, and quality gates—without relabeling the role as DevOps.
- For each claimed skill, prepare a proof artifact and at least one *why this design?* answer.
- Mention cost controls, security limitations and what you would change in a genuine multi-team production deployment.
- Retire old resource versions or commands that no longer work; favor current official documentation over dated video demos.

---
**Bottom line:** Study fundamental topics deeply enough to troubleshoot; build one secure cloud-native deployment by Week 16 and begin suitable applications; use Months 5–12 to strengthen security, operations, system design, platform engineering, and carefully constrained AI operations. **One independently operated project plus convincing incident evidence beats completion badges from ten overlapping courses.**


## 12. NextWork.ai — guided projects and independent portfolio extensions

**Decision:** Add [NextWork.ai](https://nextwork.ai/) as a **high-value, optional, project-based supplement**. The goal is not project certificates or completion counts. Use a project to start, then independently adapt it until it meets the interview-ready acceptance criteria already defined in [Section 5](#5-flagship-portfolio-architecture-repo-and-acceptance-tests). **Do not add hours**: replace an overlapping KodeKloud, video-follow-along or existing practice lab within the 15-hour weekly budget.

### Recommended sequence, with tangible proof

| Step | Timing | Project | Required independent extension | Interview talking point |
|---|---|---|---|---|
| 1 | Week 1–2 | [Linux Service Health Monitor](https://nextwork.ai/projects/5d8df751-6459-473f-ae86-d8ee7ad4ccc3) | Break a unit configuration or service; collect `journalctl` evidence, use safe restart limits and write a runbook. | Diagnose failed Linux services systematically. |
| 2 | Weeks 10–12 | [Terraform GitOps Foundation on AWS](https://nextwork.ai/projects/7f66d30f-cafc-46d8-b106-f48321581f37) | Narrow GitHub OIDC trust, protect backend state and reject an unsafe PR plan. | Explain federation, state security and IaC lifecycle. |
| 3 | Weeks 13–15 | [Terraform EKS with GitHub Actions CI/CD](https://nextwork.ai/projects/d40c742f-9bac-40c1-b651-52ae96e6ba30) | Add a budget and teardown check; reason about private networking, RBAC and health checks. | Defend AWS/EKS design and operating costs. |
| 4 | Weeks 15–16 | [End-to-End GitOps Pipeline](https://nextwork.ai/projects/2757d4a2-0371-4c1c-8389-4e52c53dac6b) | Demonstrate Argo CD sync, deliberately broken deployment and rollback from Git. | Explain CI vs CD vs GitOps and release recovery. |
| 5 | Weeks 27–29 | [Observability and SLOs on Kubernetes](https://nextwork.ai/projects/0a918f05-9085-4ff0-a825-7c1000d13108) | Inject bad latency/errors; capture an alert, dashboard, root cause and SLO impact. | Explain error budgets and useful incident alerts. |
| 6 | Weeks 30–32 | [GitOps Canary Deployments with Argo](https://nextwork.ai/projects/df2b6349-a5e8-4448-b807-7564d6a3c015) | Break a canary; prove metric-driven automatic abort and safe rollback. | Compare canary, blue-green and rolling deployments. |
| 7 | Weeks 34–35 | [GitOps Across Clusters with Argo CD](https://nextwork.ai/projects/41b34a8d-255a-4b89-876d-4ec34e9c5184) | Enforce team/environment separation and demonstrate drift recovery. | Platform engineering tenancy and blast-radius control. |
| 8 | Weeks 43–44 | [GitOps Canary Deployments for LLM Services](https://nextwork.ai/projects/4834f07a-60e6-46b6-9666-56d37a132984) | Define inference latency/error objectives, canary rejection and cost controls. | Explain reliable AI service rollouts. |
| 9 | Weeks 45–48 | [AI Infrastructure Operations Copilot](https://nextwork.ai/projects/45e74930-c12e-41f4-83bf-ec7fe145c598) | Run read-only log/metrics/runbook tools, evaluate 20 incident cases and show rejected unauthorized operations. | Defend AI incident response accuracy and security. |
| 10 | Weeks 45–48, **optional** | [Kubernetes Agent with kagent](https://nextwork.ai/projects/6b73937a-3f61-43fb-9299-928344892504) | Keep write tools disabled or approval-gated in disposable labs; red-team untrusted log inputs. | Least privilege, human oversight and prompt injection. |

**Selection guidance:** If you only have time for **four** NextWork projects, choose Linux Service Health Monitor, Terraform GitOps Foundation, End-to-End GitOps Pipeline and Observability/SLOs. The paid-cloud EKS project is optional if your existing EKS flagship already proves the same skills. Projects 7–10 are advanced specialization, not prerequisites for the Week 16 job search.

### Required completion protocol for each guided project

- [ ] **Guided baseline:** Follow the tutorial once in a disposable account or local cluster. Note every dependency, cost-bearing resource and assumption.
- [ ] **Independent rebuild:** Close the guide and reproduce a critical component from your own notes; change a meaningful design parameter or implementation choice.
- [ ] **Fault injection:** Introduce one safe, reversible failure (DNS, IAM deny, unhealthy pod, invalid rollout or missing metric) and document hypothesis → diagnostic commands → verified fix.
- [ ] **Security and cost checks:** Verify least privilege, secret handling, log redaction, infrastructure limits and teardown. Avoid persistent EKS/NAT/LB resources for short labs.
- [ ] **Portfolio evidence:** Commit original configuration, test commands, relevant sanitized outputs, an architecture diagram, ADR, runbook and a candid statement that the work began as a guided lab.
- [ ] **Interview rehearsal:** Explain the design in 5 minutes, then answer 3 questions about trade-offs, operating cost, failure scenarios and production-hardening gaps without video prompts.

### Spending and technical-accuracy safeguards

NextWork has advertised free learning access, but **verify current platform and project access terms** before starting; “free project” does **not** mean free AWS infrastructure. EKS, NAT gateways, load balancers, storage, endpoints and logs may incur charges. Create an AWS Budget, prefer local **kind** clusters for GitOps/rollout exercises, use disposable credentials, destroy cloud resources immediately after collecting evidence and verify nothing remains. For Terraform backends, IAM/OIDC, Kubernetes and Argo CD, prefer current [HashiCorp](https://developer.hashicorp.com/terraform/), [AWS](https://docs.aws.amazon.com/), [GitHub OIDC](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) and [Argo CD](https://argo-cd.readthedocs.io/en/stable/) documentation over older guide commands.

**Production-readiness caveat:** Completing a guided project shows practice, not professional production ownership. Distinguish lab experience from employment experience on resumes and in interviews. For AI agents, never expose production write credentials to untrusted model output; enforce permissions in the tool layer and test denial paths.

---
**Next action:** Start with the Linux service project during Week 1–2 only if it replaces an overlapping lab. Move to Terraform GitOps after your AWS foundations are ready, and keep the 16-week interview milestone unchanged.


---

## 13. Zero To Mastery — optional paid course overlays

**Decision:** [Zero To Mastery](https://zerotomastery.io/) is a **selective paid alternative**, *not* a new mandatory learning track. First exhaust your existing freeCodeCamp, MIT, CS50P, KodeKloud, HashiCorp and NextWork materials. Sample free course previews, check employer-funded access and compare the current regional checkout and refund terms before paying. **Do not extend the 15-hour/week study allocation or delay the Week 16 interview milestone.**

| ZTM course (official link) | Estimated course length | When | Priority and substitution | Independent acceptance evidence |
|---|---:|---|---|---|
| [Bash Scripting: Learn Shell Scripting](https://zerotomastery.io/courses/learn-bash-scripting/) | 10h | Weeks 3–4 | **Most useful immediate ZTM option**, *only if* Bash is a real gap; **replace** overlapping Bash lectures. | Write tested service-check/backup scripts with argument validation, meaningful exit codes, logs, ShellCheck and failure handling. |
| [DevOps Bootcamp: Linux & System Administration](https://zerotomastery.io/courses/devops-bootcamp/) | 25h | Weeks 1–4 | Alternative to **freeCodeCamp Linux Server + an introductory lab path**; do **not** complete both. | Diagnose systemd, permissions, SSH and disk incidents without instructor hints; publish runbook and recovery evidence. |
| [Python Automation Bootcamp](https://zerotomastery.io/courses/learn-python-automation/) | 22.5h | Weeks 3–4, optional | Only if a diagnostic Python assignment exposes a deficit; CS50P/your own operations scripts are sufficient otherwise. | Build a pytest-tested CLI that parses log files/JSON and implements timeouts, API errors and structured logging. |
| [DevOps Bootcamp: Terraform](https://zerotomastery.io/courses/learn-terraform-certification/) | 8h | Weeks 9–12 | Alternative to KodeKloud/Piyush beginner Terraform tutorials; **not additive**. | Provision tested AWS modules with protected remote state, OIDC CI plans and destruction/cleanup evidence. |
| [AWS Bootcamp: Build AI Apps with AWS Bedrock](https://zerotomastery.io/courses/learn-aws-bedrock/) | 15.5h | Weeks 41–44 | **Strong later-stage specialization** if choosing managed AWS foundation models; replace overlapping AI videos. | Integrate an opt-in, cost-limited Bedrock evaluation or RAG component; record latency, cost, grounding and guardrail tests. |
| [AI Agents Bootcamp](https://zerotomastery.io/courses/ai-agents-bootcamp/) | 7h | Weeks 45–48 | Optional to understand LangGraph/CrewAI/MCP/tool approvals; use **read-only** tools for your incident assistant. | Demonstrate least-privilege tool access, untrusted-input handling, source attribution, 20 test cases and no unauthorized writes. |
| [System Design + Architecture](https://zerotomastery.io/courses/system-design/) | 4h | Weeks 33–40 | **Low priority**; ByteByteGo, Hello Interview and Ashish Pratap Singh already cover this. | Prefer two timed infrastructure HLD mocks over course completion. |

**Practical decision:** If you pay for only one ZTM topic now, prioritize **Bash Scripting**, and only if you cannot already automate Linux administration confidently. For Months 10–12, **AWS Bedrock** or **AI Agents** may provide incremental value; choose at most one before considering a second. The course pages are paid products with selected preview lessons—not free full YouTube courses. The platform does not guarantee employment and costs of AWS/LLM APIs are separate. [Review membership options](https://zerotomastery.io/academy/).

- [ ] Gap-check Bash and decide whether a paid ZTM course is necessary.
- [ ] If selected, **replace** a duplicate lesson block; keep the same weekly schedule.
- [ ] Rebuild the related project independently with fault injection and a recorded design explanation.
- [ ] Add only original code, sanitized evidence, tests, runbooks and cost/teardown instructions to GitHub.

