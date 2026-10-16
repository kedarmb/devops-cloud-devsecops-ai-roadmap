# Structured DevOps & Cloud Engineering Upskilling + Interview Roadmap

> **Repository note:** This is the shorter interview sprint companion; the [complete 48-week roadmap](./COMPLETE_DEVOPS_UPSKILLING_AND_INTERVIEW_ROADMAP.md) is the primary execution guide. The separate `devops-youtube-roadmap/README.md` has been superseded.

> **Version:** 1.0 — 16 October 2026  
> **Designed for:** Experienced IT professional transitioning back to hands-on DevOps/Cloud Engineering; background in QA and earlier DevOps work; CKA/CKAD-qualified.  
> **Target:** Product-company DevOps Engineer / Cloud Engineer / Cloud Automation Engineer; subsequently DevSecOps, SRE, and Platform Engineering.  
> **Time budget:** **15 hours/week** (about **240 hours over 16 weeks**; about **720 hours across 48 active weeks**).  
> **Core stack:** Linux, networking, Bash/Python, Git, AWS, Terraform, GitHub Actions, Docker, EKS, Helm, Argo CD, security, OpenTelemetry, Prometheus, Grafana.  
> **Companion documents:** [Master roadmap](./README.md) · [YouTube and course links](./YOUTUBE_LEARNING_RESOURCES.md).

**Read this first:** Your goal is not to finish every course. Your goal is to **independently build, operate, secure, recover, and explain a cloud-native service**. Prioritize practical competence, realistic incidents, and interview evidence. Do not describe lab work as employer production experience.

---

## Contents

1. [Strategy and success definition](#1-strategy-and-success-definition)
2. [Your fixed 15-hour weekly study routine](#2-your-fixed-15-hour-weekly-study-routine)
3. [First 16 weeks: job-readiness sprint](#3-first-16-weeks-job-readiness-sprint)
4. [Weeks 17–48: deeper engineering and specialization](#4-weeks-1748-deeper-engineering-and-specialization)
5. [Recommended courses and videos: one primary source per topic](#5-recommended-courses-and-videos-one-primary-source-per-topic)
6. [Flagship portfolio project: build and prove it](#6-flagship-portfolio-project-build-and-prove-it)
7. [Interview preparation: domain checklists and practice questions](#7-interview-preparation-domain-checklists-and-practice-questions)
8. [Mock interviews, applications, and 30/60/90-day cadence](#8-mock-interviews-applications-and-306090-day-cadence)
9. [Practical assessments and readiness gates](#9-practical-assessments-and-readiness-gates)
10. [Progress trackers, templates, and first seven days](#10-progress-trackers-templates-and-first-seven-days)

---

## 1. Strategy and success definition

### Where you are and where you're going

| Dimension | Plan implication |
|---|---|
| 10+ years total IT experience | Prepare for experienced-level architecture, troubleshooting, collaboration, and ownership questions, while being candid about role-specific hands-on depth. |
| Recent manual QA experience | Reuse strengths in quality gates, release risk, API testing, incident reproduction, and test automation. |
| Prior DevOps-designated experience, limited recent practical ownership | Rebuild confidence through independent implementations and failure drills, not another beginner bootcamp. |
| CKA / CKAD | **Test your Kubernetes proficiency first.** Skip introductory content that you can already perform without guidance. |
| Existing 12-month learning guides | Use the present document to **execute** them; don't stack every resource into an impossible schedule. |

### Priorities in order

| Priority | What matters | Evidence that proves it |
|---|---|---|
| **P0 — Employability (Weeks 1–16)** | Linux troubleshooting, TCP/IP, AWS/IAM/VPC, Terraform, CI/CD, EKS/GitOps, basic security, articulate system design | Working AWS/EKS project; CI tests; diagrams; 6+ incidents; timed mock interviews |
| **P1 — Strong operations (Weeks 17–32)** | Cloud/cluster security, supply-chain controls, OTel, SLOs, alerts, on-call practices, recovery | Security policy enforcement; traces/logs/metrics; SLO report; restore drill; postmortem |
| **P2 — Differentiation (Weeks 33–48)** | Platform engineering, FinOps, advanced AWS, safe AI/AIOps and production-oriented system design | Self-service template; cost report; read-only, tested AI incident assistant |

### A practical job-search rule

**Begin selective applications around Weeks 13–16**, once you can demonstrate Terraform-managed AWS infrastructure, a CI/CD deployment to Kubernetes, and at least three independent troubleshooting stories. Do **not** postpone applications until the entire 12-month plan is finished. Apply earlier to suitable QA automation / release-engineering / CI-CD bridge roles if they make better use of your real experience.

**Potential titles:** DevOps Engineer, Cloud Engineer, Cloud Automation Engineer, Infrastructure Automation Engineer, CI/CD Engineer, Release Engineer; later SRE, Platform Engineer, DevSecOps Engineer. Seniority depends on actual production depth and the employer's expectations, not total years alone.

### Weekly definition of success

Every week should produce **all four**:

- [ ] **Learn:** Explain the week's fundamental concepts without reading notes.
- [ ] **Build:** Implement something independently; commit the working changes.
- [ ] **Break & fix:** Create or diagnose at least one safe failure; record symptoms → hypotheses → commands → fix → prevention.
- [ ] **Communicate:** Answer three interview questions aloud, update one diagram or README, and write one STAR/CAR story when relevant.

---

## 2. Your fixed 15-hour weekly study routine

| Activity | Hours/week | Standard of work |
|---|---:|---|
| One selected course / documentation / targeted video | **3.0** | Take minimal notes; avoid multiple teachers on the same topic. |
| Independent build + labs | **6.0** | Type code/configuration yourself; commit reproducible work. |
| Troubleshooting and failure injection | **2.0** | Work without copying a solution; measure the root cause. |
| Interview prep (conceptual, scripting, system design, mock) | **2.0** | Timed, spoken answers; keep an error log. |
| Documentation / portfolio / application work | **2.0** | README, diagrams, cost cleanup, resume, selected applications. |
| **Total** | **15.0** | Adjust within the same total, never pile on optional courses. |

**Suggested five-session schedule:** 2h × 3 weekdays + 4.5h Saturday + 4.5h Sunday. Keep at least one rest day. For a demanding week, preserve 1) independent lab, 2) one failure drill, and 3) interview questions; postpone passive video watching.

**Repeatable 4-week monthly cycle:** Week A = learn and design; Week B = implement; Week C = secure, break and recover; Week D = demonstrate, document, mock interview and review.

### Course-selection discipline

- **Primary AWS:** [Adrian Cantrill AWS SAA](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) + [official AWS workshops](https://workshops.aws/).
- **Primary labs:** [KodeKloud learning paths](https://kodekloud.com/learning-paths/) + [SadServers](https://sadservers.com/scenarios) for Linux incidents.
- **Primary AWS/Terraform implementation references:** [Piyush Terraform playlist](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp), [Anton Putra Terraform playlist](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA), and [HashiCorp tutorials](https://developer.hashicorp.com/terraform/tutorials). Pick **one** video series at a time.
- **Primary system design:** [ByteByteGo](https://www.youtube.com/@ByteByteGo) + [Hello Interview](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction), not a new paid system-design bundle immediately.
- **Advanced reading/videos:** O'Reilly, Pluralsight, Udacity, CBT Nuggets, InfraExpert/SystemsExpert **only when** a measurable skill gap justifies them. Do not run overlapping paid subscriptions by default.

---

## 3. First 16 weeks: job-readiness sprint

**Target by Week 16:** Deploy a secure containerized application to EKS from a GitHub Actions pipeline using AWS OIDC, Terraform and Argo CD; show actionable monitoring, a documented rollback, three or more fault investigations, and credible answers to common infrastructure interviews.

> For cost control: start with local Docker/Kubernetes (`kind` or `minikube`) and use a short-lived AWS sandbox for cloud demonstrations. **EKS control planes, NAT gateways, load balancers, log storage and data transfer may incur meaningful costs**; create AWS budgets and destroy idle infrastructure. Never put AWS credentials into Git or logs.

### Month 1 — Linux, networking, Git, Bash/Python and diagnosis

| Week | Main learning target | Independent deliverable | Exit test / interview question |
|---|---|---|---|
| **1** | Linux filesystem, permissions, users/groups, processes, `systemd`, packages, journals | Ubuntu/RHEL-compatible disposable VM; service health-check Bash script; README of ≥12 commands | Diagnose a failing service from `journalctl`, permissions and resource state, without watching the solution. |
| **2** | DNS, TCP/UDP, CIDR, routing, NAT, HTTP(S)/TLS, proxies; Git workflows | Network troubleshooting playbook with `dig`, `ss`, `curl`, `openssl`, `ip`, `tcpdump`/Wireshark samples; branch/PR demonstration | Explain a client-to-server request from DNS lookup to TLS handshake and HTTP response; reproduce and isolate one DNS fault. |
| **3** | Bash reliability and Python automation: args, JSON, APIs, errors, logging, tests | `ops-healthcheck` Python CLI with tests, clear exit codes, JSON output and failure handling | Write a script to find services that are down, parse health data and generate a nonzero exit code when unhealthy. |
| **4** | Performance tools and systematic root-cause analysis | ≥6 documented Linux/network incidents, 1 short performance investigation, README + sample logs | Given slow response, distinguish CPU pressure vs disk I/O vs DNS/TCP latency using evidence. **Gate A.** |

**Best resources:** [freeCodeCamp Linux Server](https://www.youtube.com/watch?v=WMy3OzvBWc0) · [Kunal Networking](https://www.youtube.com/watch?v=IPvYjXCsTg8) · [Kunal Git/GitHub](https://www.youtube.com/watch?v=apGV9Kg7ics) · [MIT Missing Semester](https://missing.csail.mit.edu/2026/) · [CS50 Python](https://cs50.harvard.edu/python/) · [Brendan Gregg Linux performance](https://www.youtube.com/watch?v=fhBHvsi0Ql0) · [SadServers](https://sadservers.com/scenarios).

### Month 2 — AWS architecture, secure networking and infrastructure design

| Week | Main learning target | Independent deliverable | Exit test / interview question |
|---|---|---|---|
| **5** | IAM/STS, roles, least privilege, account guardrails, CloudTrail/CloudWatch, billing | Cost alerts, MFA/roles, basic audit trail; IAM policy that grants only required sandbox access | Troubleshoot an AWS `AccessDenied` incident and explain identity vs resource-based policies. |
| **6** | VPC, subnets, routing, SG/NACL, internet/NAT, DNS and private access | VPC diagram with public/private tiers, routing tables and explicitly allowed network paths | Explain private subnet egress, VPC endpoints, SG statefulness vs NACL behavior. |
| **7** | ALB, EC2/Auto Scaling, S3/EBS/RDS concepts, KMS, backups, HA | Deploy an app behind a load balancer; document scaling, encryption and recovery choices | Trace 502/503 errors and explain how an unhealthy backend impacts request routing. |
| **8** | AWS Well-Architected; 3-tier system design and threat thinking | Versioned AWS high-level design (HLD), request flow, approximate cost and 1 recovery drill; tear down unused AWS resources | Present your AWS design for 15 minutes; defend HA, IAM, cost, latency and failure trade-offs. **Gate B.** |

**Best resources:** [Adrian Cantrill Technical Fundamentals](https://learn.cantrill.io/p/tech-fundamentals) · [Adrian AWS SAA](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) · [AWS Well-Architected](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) · [Cloud X Berry proxy/LB/gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI) · [Ashish Pratap Singh 30 system-design concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk).

### Month 3 — Terraform and secure infrastructure delivery

| Week | Main learning target | Independent deliverable | Exit test / interview question |
|---|---|---|---|
| **9** | Terraform core workflow, resources, data, variable types, outputs | AWS VPC/compute converted from manual steps into version-controlled Terraform | Run clean `fmt`, `validate`, `plan`, `apply` and `destroy` on a disposable environment. |
| **10** | Reusable modules, dependencies, environment boundaries, remote state and locking | Reusable `network`, `iam`, `compute` modules; protected state backend and environment variables | Explain why Terraform state is sensitive and how you prevent concurrent applies. |
| **11** | Terraform testing, IaC scanning, drift, import/move; Ansible optionally | CI for IaC lint/validation/scan; documented drift scenario, safe planned repair | Diagnose a manual cloud change without recklessly applying or deleting resources. |
| **12** | IaC peer-review simulation and cloud architecture trade-offs | Versioned architecture, cost estimate, full `terraform destroy` evidence and reusable module documentation | Conduct a 30-minute Terraform deep dive and live troubleshooting session. **Gate C.** |

**Best resources:** [KodeKloud Terraform](https://kodekloud.com/learning-paths/) · [HashiCorp tutorials](https://developer.hashicorp.com/terraform/tutorials) · [Piyush 30 Days of AWS Terraform](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp) · [Terraform drift tutorial](https://www.youtube.com/watch?v=nRgNIy-SDEw) · [Anton tutorials index](https://github.com/antonputra/tutorials/blob/main/docs/contents.md).

### Month 4 — CI/CD, containers, EKS and GitOps; begin applications

| Week | Main learning target | Independent deliverable | Exit test / interview question |
|---|---|---|---|
| **13** | Docker, image layering, non-root runtime, tests, registries; GitHub Actions basics | Containerize flagship app; build/test/scan workflow, branch protection and pull request checks | Explain image vs container, container runtime, caching and a failed build diagnosis. |
| **14** | AWS GitHub Actions OIDC, IAM trust policy, artifact security; ECR | Keyless GitHub→AWS authentication scoped by repository, branch/environment; ECR push pipeline | Explain why static access keys are unsafe and demonstrate scoped OIDC session access. |
| **15** | EKS / Kubernetes revision, Helm, ingress/service networking, GitOps with Argo CD | Versioned local Kubernetes proof, followed by short-lived EKS deployment; Argo CD sync of Helm/Kustomize configs | Debug an `ImagePullBackOff`, `CrashLoopBackOff` or wrong-Service-selector incident independently. |
| **16** | Rollback, health probes, deployment strategies, end-to-end demonstration | 15-minute demo; failed-deployment rollback test; design diagram; 3 incident writeups; GitHub README | Conduct AWS/Terraform/CI/CD/EKS mock interview; **submit targeted applications if Gate D is met**. |

**Best resources:** [TechWorld with Nana Docker](https://www.youtube.com/watch?v=3c-iBn73dDE) · [Kunal GitHub Actions](https://www.youtube.com/watch?v=62N8UiWUdQo) · [GitHub OIDC AWS guide](https://docs.github.com/en/actions/how-tos/secure-your-work/security-harden-deployments/oidc-in-aws) · [Kunal Argo CD](https://www.youtube.com/watch?v=8YLsQIG2Svo) · [Piyush GitOps/EKS](https://www.youtube.com/watch?v=c_a5e2Dnxkk) · [Anton EKS series](https://www.youtube.com/playlist?list=PLiMWaCMwGJXnKY6XmeifEpjIfkWRo9v2l) · [EKS workshop](https://www.eksworkshop.com/).

### At the end of Week 16, you should have

- [ ] One **public, sanitized project** with infrastructure, app deployment and operational runbooks (never expose account IDs unnecessarily, passwords, secrets or private logs).
- [ ] Terraform modules and verifiable IaC checks in CI.
- [ ] GitHub Actions → AWS (OIDC) → ECR → EKS/Argo CD delivery sequence.
- [ ] Minimum three validated failures and documented rollback/recovery.
- [ ] A 15-minute architecture walkthrough, 30-minute live diagnostic ability and truthful resume stories.
- [ ] First set of tailored job applications **if** the core readiness gate is passed (Section 9).

---

## 4. Weeks 17–48: deeper engineering and specialization

You can pursue these weeks **while actively interviewing or after moving into a DevOps role**. The core employability track remains more important than completing every specialization.

### Month 5 — AWS security and threat modeling (Weeks 17–20)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **17** | Harden AWS IAM/STS, service identity, secrets and encryption | Least-privilege policies, deny-case tests, no long-lived credentials in CI |
| **18** | CloudTrail/CloudWatch, configuration/audit, secure VPC endpoints, runtime access | Trace one authorization denial and one suspicious API request |
| **19** | Model threats to VPC, CI/CD, artifact registry and Kubernetes | Threat model, security boundaries and mitigations linked to tests |
| **20** | Run a red-team-style configuration review in an isolated lab | Security posture checklist, remediations, 30-minute security mock |

**Resources:** [AWS Security](https://docs.aws.amazon.com/security/) · [OpenSSF training](https://openssf.org/training/) · optional [O'Reilly Kubernetes Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/).

### Month 6 — DevSecOps and software supply chain (Weeks 21–24)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **21** | Add SAST/SCA, IaC scan and container scanning to CI | Intentionally vulnerable test dependency fails policy gate |
| **22** | Generate SBOM; sign container with Cosign; verify provenance | Signed artifact and verification evidence |
| **23** | Harden Kubernetes with RBAC, namespace network policies, admission enforcement | Rejected unsigned workload; allowed signed workload; blocked network path |
| **24** | Threat scenario and security incident review | Security pipeline demo and remediation report |

**Resources:** [Nana DevSecOps](https://www.youtube.com/watch?v=gLJdrXPn0ns) · [Cosign/Kyverno video](https://www.youtube.com/watch?v=HLb1Q086u6M) · [Kubernetes Goat](https://github.com/madhuakula/kubernetes-goat) · [Liz Rice eBPF](https://www.youtube.com/watch?v=ZXDhKUeUUSs) · [Cilium/Hubble](https://www.youtube.com/watch?v=yQoVOumoY5k) · [Isovalent Cilium labs](https://isovalent.com/labs/cilium-getting-started/).

### Month 7 — Observability instrumentation (Weeks 25–28)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **25** | Instrument service with RED/USE-style metrics and Prometheus | Grafana dashboard; correct request/error/latency interpretation |
| **26** | Centralize structured logs; deploy OpenTelemetry Collector | Correlated trace IDs in logs with consistent attributes |
| **27** | Enable distributed tracing and exemplars/service map where feasible | Find slow downstream dependency from a trace |
| **28** | Perform an observable incident exercise; tune alerts | Dashboards, alert rules and a reproducible root-cause report |

**Resources:** [Piyush Observability playlist](https://www.youtube.com/playlist?list=PLl4APkPHzsUWC89lwHRGxk1GDtS7dkUsE) · [CNCF OpenTelemetry hands-on](https://www.youtube.com/watch?v=8CKgAyenEjo) · [OpenTelemetry Demo](https://opentelemetry.io/docs/demo/) · [Grafana](https://www.youtube.com/@Grafana) · optional [Pluralsight SRE-Grade Observability](https://www.pluralsight.com/paths/kubernetes-sre-grade-observability).

### Month 8 — SRE, incident response and disaster recovery (Weeks 29–32)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **29** | Define SLIs, SLOs and error budget for one user-facing operation | Written SLO spec and error-budget calculation |
| **30** | Inject pod/node/dependency failures; identify alerting gaps | At least three independent incident reports with time-to-detect/recover |
| **31** | Test restore, rollback, backups and a region/AZ-loss design scenario | Measured recovery time, data-loss assumptions and evidence |
| **32** | Write a blameless postmortem and reduce one piece of toil | On-call runbook, postmortem and SRE interview mock |

**Resources:** [Google SRE books](https://sre.google/books/) · [Piyush Kubernetes troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc) · optional [Udacity SRE Nanodegree](https://www.udacity.com/course/site-reliability-engineer-nanodegree--nd087) **instead of** other paid SRE courses · optional [O'Reilly SRE Essentials](https://www.oreilly.com/videos/site-reliability-engineering/9780135415016/).

### Month 9 — Internal developer platform and FinOps (Weeks 33–36)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **33** | Define self-service platform interface and golden path | Platform user journey, constraints and ownership model |
| **34** | Create a service scaffold / GitOps template | New sample service deployed from a repeatable template |
| **35** | Add multi-environment promotions, access control, policy checks | Demonstrate isolated namespaces/environments and approval gates |
| **36** | Establish cost visibility, tags and right-sizing review | Per-environment cost analysis and improvement recommendations |

**Resources:** [DevOps Toolkit](https://www.youtube.com/@DevOpsToolkit) · [Backstage crash course](https://www.youtube.com/watch?v=JbX6V9fz5QA) · [Platform-team talk](https://www.youtube.com/watch?v=9lPp-6nJ8bI) · [FinOps Foundation](https://www.finops.org/training-certification/recommended/new-to-finops/).

### Month 10 — Advanced AWS operations and AI-assisted workflows (Weeks 37–40)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **37** | Review advanced IAM, service quotas, resiliency and deployment patterns | Document cross-account trust and two failure-mode trade-offs |
| **38** | Improve infrastructure delivery with policy checks, drift detection and progressive rollout | Automated policy failure and successful controlled rollout |
| **39** | Prototype read-only AI assistance over sample logs/metrics | Agent only retrieves approved synthetic/sanitized operational data |
| **40** | Evaluate false conclusions, bad citations and unsafe-action recommendations | Adversarial test set, failure log and guardrail documentation |

**Resources:** [Vishakha DevOps/AIOps overview](https://www.youtube.com/watch?v=UBzYwNbFCKs) · [Piyush AI operations video](https://www.youtube.com/watch?v=hULkzJMHf7U) · [AWS Well-Architected](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html).

### Month 11 — AI workload delivery and LLMOps fundamentals (Weeks 41–44)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **41** | Package a small inference/API workload in a container | Local reproducibility and baseline performance numbers |
| **42** | Deliver via pipeline with model/application versioning | Versioned deployment and successful rollback |
| **43** | Instrument latency, errors, usage and cost | Dashboard and load-test evidence; constrained resource use |
| **44** | Assess data protection, evaluation and operations | Model-service runbook and failure evaluation results |

**Resources:** [DataTalks MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp) · [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction) · optional [Udacity AI Ops Engineer](https://www.udacity.com/course/ai-ops-engineer-nanodegree--nd907).

### Month 12 — Secure read-only incident assistant and final interview portfolio (Weeks 45–48)

| Week | Implementation milestone | Evidence/acceptance test |
|---|---|---|
| **45** | Connect sanitized telemetry to read-only incident-analysis tools | Enforced read-only API permissions and audit logs |
| **46** | Add source attribution, retrieval constraints, redaction, human approval barrier | Prompt-injection test; no unauthorized actions or secret exfiltration |
| **47** | Evaluate diagnosis quality, hallucinations, missing evidence and replay | Repeatable test set with success/failure analysis |
| **48** | Consolidate demos, runbooks, diagrams, interview stories and targeted role applications | Full end-to-end portfolio demo + multi-round mock panel |

**Resources:** [OWASP GenAI Security](https://genai.owasp.org/) · [Hugging Face Agents](https://huggingface.co/learn/agents-course/en/unit0/introduction) · optional [Udacity AgentOps](https://www.udacity.com/course/agentops-deploying-guarding-and-monitoring-ai-agents--cd15157) · optional [Udacity AI Threat Modeling](https://www.udacity.com/course/ai-threat-modeling-and-operational-defense--cd15147).

---

## 5. Recommended courses and videos: one primary source per topic

**How to choose:** Start with the **primary** source; use the **targeted free video** only for unclear concepts; take a **paid alternative** if a lab or mock exposes a repeatable weakness. Direct links below originate from the companion resource guides; availability or titles may change over time.

| Skill | Primary learning material | Free targeted video / lab | Optional specialized paid course |
|---|---|---|---|
| Linux administration | [freeCodeCamp Linux Server](https://www.youtube.com/watch?v=WMy3OzvBWc0), [KodeKloud](https://kodekloud.com/learning-paths/) | [Kunal Linux](https://www.youtube.com/watch?v=iwolPf6kN-k), [SadServers](https://sadservers.com/scenarios) | [Pluralsight Linux Diagnostics EX342](https://www.pluralsight.com/courses/red-hat-certified-specialist-in-linux-diagnostics-and-troubleshooting-ex342) **or** [ZTM Linux Sysadmin](https://zerotomastery.io/courses/devops-bootcamp/) (alternative foundation) |
| Linux performance | [MIT Missing Semester](https://missing.csail.mit.edu/2026/) and your own profiling lab | [Brendan Gregg performance](https://www.youtube.com/watch?v=fhBHvsi0Ql0) | [O'Reilly Linux Troubleshooting](https://www.oreilly.com/videos/linux-system-administration/0642572124694/) |
| Network and TCP/IP | [Practical Networking](https://www.youtube.com/@PracticalNetworking) | [Kunal Networking](https://www.youtube.com/watch?v=IPvYjXCsTg8), [Cloud X Berry networking](https://www.youtube.com/watch?v=TR0RU2pmMeA) | [CBT Nuggets Wireshark WCA](https://www.cbtnuggets.com/it-training/networking/wca-101) |
| Python and Bash | [CS50P](https://cs50.harvard.edu/python/) + scripts you author | [freeCodeCamp Bash](https://www.youtube.com/watch?v=tK9Oc6AEnR4) | [ZTM Bash Scripting](https://zerotomastery.io/courses/learn-bash-scripting/) **first if Bash needs structure**, or [ZTM Python Automation](https://zerotomastery.io/courses/learn-python-automation/) for a Python gap |
| Git/GitHub | [GitHub Skills](https://skills.github.com/) | [Kunal Git](https://www.youtube.com/watch?v=apGV9Kg7ics) | Not needed initially |
| AWS architecture/IAM/VPC | [Adrian Cantrill AWS SAA](https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c03) | [Cloud X Berry LB/API gateway](https://www.youtube.com/watch?v=ywrlEV6g_jI), [AWS workshops](https://workshops.aws/) | [Udacity AWS Cloud Architect](https://www.udacity.com/course/aws-cloud-architect-nanodegree--nd063) if reviewed projects are needed |
| Terraform | [HashiCorp tutorials](https://developer.hashicorp.com/terraform/tutorials) + [KodeKloud](https://kodekloud.com/learning-paths/) | [Piyush Terraform](https://www.youtube.com/playlist?list=PLl4APkPHzsUXcfBSJDExYR-a4fQiZGmMp), [Anton Terraform](https://www.youtube.com/playlist?list=PLiMWaCMwGJXkGuVPyM2hTQumcaqnXEgHA) | [ZTM Terraform](https://zerotomastery.io/courses/learn-terraform-certification/) **or** [O'Reilly Terraform Essentials AWS](https://www.oreilly.com/videos/terraform-essentials-for/9780135936290/) (not both) |
| Docker and CI/CD | [KodeKloud DevOps](https://kodekloud.com/learning-paths/) | [Nana Docker](https://www.youtube.com/watch?v=3c-iBn73dDE), [Kunal GitHub Actions](https://www.youtube.com/watch?v=62N8UiWUdQo) | [Pluralsight GitHub Actions Deep Dive](https://www.pluralsight.com/courses/github-actions-deep-dive) |
| GitOps/EKS | [EKS Workshop](https://www.eksworkshop.com/) + [Argo CD docs](https://argo-cd.readthedocs.io/en/stable/) | [Piyush EKS GitOps](https://www.youtube.com/watch?v=c_a5e2Dnxkk), [Kunal Argo CD](https://www.youtube.com/watch?v=8YLsQIG2Svo) | [Udacity Cloud Native Architecture](https://www.udacity.com/course/cloud-native-architecture-nanodegree--nd064) (optional) |
| Kubernetes troubleshooting | Your own failure drills + [Kubernetes docs](https://kubernetes.io/docs/) | [Piyush troubleshooting](https://www.youtube.com/watch?v=6hqXrYlf5qc) | [Pluralsight Hands-On K8s Troubleshooting](https://www.pluralsight.com/courses/hands-on-kubernetes-troubleshooting) |
| DevSecOps / image signing | [OpenSSF](https://openssf.org/training/) + [Kubernetes Goat](https://github.com/madhuakula/kubernetes-goat) | [Nana DevSecOps](https://www.youtube.com/watch?v=gLJdrXPn0ns), [Cosign + Kyverno](https://www.youtube.com/watch?v=HLb1Q086u6M) | [O'Reilly K8s Security Essentials](https://www.oreilly.com/videos/kubernetes-security-essentials/9780135485361/) |
| eBPF, Cilium and K8s network policy | [Isovalent Cilium labs](https://isovalent.com/labs/cilium-getting-started/) | [Liz Rice eBPF](https://www.youtube.com/watch?v=ZXDhKUeUUSs), [Kunal/Civo Cilium](https://www.youtube.com/watch?v=yQoVOumoY5k) | Not required |
| Observability | [OpenTelemetry Demo](https://opentelemetry.io/docs/demo/), [PromLabs](https://promlabs.com/) | [CNCF OTel workshop](https://www.youtube.com/watch?v=8CKgAyenEjo), [Piyush series](https://www.youtube.com/playlist?list=PLl4APkPHzsUWC89lwHRGxk1GDtS7dkUsE) | **Choose one:** [Pluralsight Observability](https://www.pluralsight.com/paths/kubernetes-sre-grade-observability) **or** [O'Reilly OTel](https://www.oreilly.com/videos/opentelemetry-in-practice/9781807783334/) |
| SRE and incident response | [Google SRE books](https://sre.google/books/) + incident labs | [Hussein Nasser](https://www.youtube.com/@hnasr), [Brendan Gregg](https://www.youtube.com/watch?v=fhBHvsi0Ql0) | [Udacity SRE Nanodegree](https://www.udacity.com/course/site-reliability-engineer-nanodegree--nd087) if you will use project feedback |
| Infrastructure system design | [Hello Interview](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction), [ByteByteGo](https://www.youtube.com/@ByteByteGo) | [Ashish Pratap Singh 30 concepts](https://www.youtube.com/watch?v=s9Qh9fWeOAk), [KodeKloud system design](https://www.youtube.com/watch?v=SE2KF-vxvS0) | [InfraExpert](https://www.algoexpert.io/) / [SystemsExpert](https://www.algoexpert.io/) only after mock gaps |
| Platform Engineering | Self-service GitOps implementation | [Backstage tutorial](https://www.youtube.com/watch?v=JbX6V9fz5QA), [Platform team talk](https://www.youtube.com/watch?v=9lPp-6nJ8bI) | [O'Reilly Effective Platform Engineering](https://www.oreilly.com/videos/effective-platform-engineering/9781633436497VE/) |
| FinOps | [FinOps Foundation](https://www.finops.org/training-certification/recommended/new-to-finops/) | AWS cost dashboards and budget lab | Not required |
| AI operations and security | [Hugging Face Agents](https://huggingface.co/learn/agents-course/en/unit0/introduction), [OWASP GenAI](https://genai.owasp.org/) | [Vishakha AIOps](https://www.youtube.com/watch?v=UBzYwNbFCKs) | [ZTM AWS Bedrock](https://zerotomastery.io/courses/learn-aws-bedrock/) **or** [ZTM AI Agents](https://zerotomastery.io/courses/ai-agents-bootcamp/) **or** [Udacity AgentOps](https://www.udacity.com/course/agentops-deploying-guarding-and-monitoring-ai-agents--cd15157) (choose one) |

### Zero To Mastery selection — optional course overlay

[ZTM](https://zerotomastery.io/) is **not** required for the 16-week interview sprint. Its paid courses are alternatives, not additions. Prioritize the selected free source and labs; subscribe only if a gap persists after attempting independent exercises.

- **Weeks 1–4:** [ZTM Bash Scripting](https://zerotomastery.io/courses/learn-bash-scripting/) is the best immediate optional course if shell scripting is weak. The [Linux Bootcamp](https://zerotomastery.io/courses/devops-bootcamp/) substitutes for freeCodeCamp/KodeKloud introductory Linux content. [Python Automation](https://zerotomastery.io/courses/learn-python-automation/) is less urgent than CS50P plus real log-parsing scripts.
- **Weeks 9–12:** [ZTM Terraform](https://zerotomastery.io/courses/learn-terraform-certification/) is only an alternative to current Terraform classes. Preserve the CI plan, state security and testing milestones.
- **Weeks 33–40:** [ZTM System Design](https://zerotomastery.io/courses/system-design/) is low priority; continue ByteByteGo, Hello Interview and timed HLD practice.
- **Weeks 41–48:** [ZTM AWS Bedrock](https://zerotomastery.io/courses/learn-aws-bedrock/) or [ZTM AI Agents](https://zerotomastery.io/courses/ai-agents-bootcamp/) could support the read-only incident assistant. Use one if needed, with tool least privilege, evaluation gates and explicit cloud/model cost limits.

**Buying gate:** Check [current membership and free previews](https://zerotomastery.io/academy/). A course that offers preview lessons is not necessarily free. ZTM does not replace KodeKloud/NextWork labs or guarantee interviews/jobs. Never raise the 15-hour weekly commitment just to finish a subscription.

- [ ] Optional: I identified a measurable gap before deciding to buy ZTM.
- [ ] Optional: I replaced—not duplicated—my existing study material.
- [ ] Optional: I can show independent code, tests, failure reports and interview explanations from the selected course.

**Preferred content format for each topic:** 1 video/course chapter → 1 self-built lab → 1 deliberately introduced failure → 1 written explanation → 3 spoken interview answers. If two providers cover the same skill, select one; **more subscriptions do not mean faster progress**.

**Creator selection:** Ashish Pratap Singh's System Design content is retained. Analogies Cloud is optional for AI/cloud concepts and is not needed for the core path.

---

## 6. Flagship portfolio project: build and prove it

### Project title: Secure, Observable AWS Cloud-Native Delivery Platform

Use one realistic microservice demo, preferably the [OpenTelemetry Demo (Astronomy Shop)](https://opentelemetry.io/docs/demo/) or [Google Cloud Online Boutique](https://github.com/GoogleCloudPlatform/microservices-demo). Keep a small deployment footprint. The demo application is a learning workload—not a claim that it served real customers.

### Target high-level architecture

```text
Developer PR -> GitHub Actions (lint/test/SAST/SCA/IaC scan)
             -> GitHub OIDC -> short-lived AWS role
             -> Build container -> SBOM/scan/sign -> Amazon ECR
             -> GitOps config PR -> Argo CD -> EKS / Helm workload
                                       |-- ingress / ALB
                                       |-- NetworkPolicy / RBAC / secrets
                                       |-- health probes / HPA / rollout
                                       +-- OTel -> collector -> metrics/logs/traces

Terraform -> VPC, IAM, ECR, EKS, cluster add-ons, budgets/tags
Operations -> Grafana + alerts -> incident runbooks -> restore/rollback
Optional later -> read-only AI incident assistant (no autonomous changes)
```

### Incremental repository layout

```text
cloud-native-devsecops-platform/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── threat-model.md
│   ├── adr/                  # Architecture decision records
│   ├── cost-and-cleanup.md
│   └── incidents/            # Symptom -> evidence -> resolution
├── app/
├── tests/
├── scripts/                   # Linux/Python/diagnostics
├── infra/terraform/
│   ├── modules/
│   └── environments/
├── .github/workflows/
├── deploy/helm/
├── deploy/argocd/
├── security/
├── observability/
├── runbooks/
└── demo/                      # Sanitized outputs and reproducible steps
```

### Production-style definition of done (portfolio, not production claim)

- [ ] A fresh reader can understand setup, design decisions, prerequisites, cloud costs and teardown.
- [ ] No passwords, private keys, AWS tokens, sensitive identifiers or real customer data are checked into Git.
- [ ] All IaC, applications and scripts are reproducible; GitHub Actions CI passes.
- [ ] Least-privilege access and short-lived CI credentials are documented and demonstrated.
- [ ] Image is scanned and (later) signed; policy failures block release.
- [ ] Workload has readiness/liveness probes, resource requests/limits and meaningful rollback instructions.
- [ ] Metrics, logs and traces are correlated; alerts link to actionable runbooks.
- [ ] At least one **documented restore** and three incident recovery procedures work.
- [ ] Security controls and intended failure scenarios have **repeatable tests**.
- [ ] Diagram explains trade-offs: HA vs cost, self-managed vs managed services, blast radius, secret management, and state integrity.
- [ ] Environment can be destroyed, with resource inspection and cost monitoring after teardown.

### Evidence pack to present in interviews

1. **2-minute demo** — what was built, who it serves, design summary.
2. **10-minute deep dive** — VPC/IAM, Terraform, GitHub OIDC, CI/CD, EKS/Argo CD, telemetry.
3. **5-minute failure story** — one incident, competing hypotheses, evidence, fix, prevention.
4. **Design alternatives** — why ALB vs API Gateway, EKS vs ECS, managed database choices, operational cost.
5. **Security evidence** — an intentionally blocked unauthorized action or unsigned deployment.
6. **Written caveat** — this is a controlled portfolio lab, not professional ownership of a customer-production service.

---

## 7. Interview preparation: domain checklists and practice questions

Practice **out loud** and without reading reference material. Every correct conceptual answer should include at least one real command, diagram, AWS/Kubernetes setting, failure mode, or test that you personally performed.

### A. Linux and networking (Weeks 1–16; revise throughout)

- [ ] Diagnose high CPU, memory pressure, disk exhaustion, high load average and disk I/O bottlenecks.
- [ ] Explain `systemctl`, `journalctl`, file permissions/ACL, user/groups, process signals and OOM kills.
- [ ] Trace DNS resolution, TCP handshake, TLS handshake, reverse proxy and HTTP request routing.
- [ ] Use `ss`, `dig`, `curl -v`, `ip route`, `tcpdump`, `top`, `vmstat`, `iostat` correctly.

**Questions:**
1. Service is active but clients receive connection refused. What do you check in order?
2. DNS resolves internally but fails from a Kubernetes pod. How do you isolate the issue?
3. CPU is low but application latency is high. What are your hypotheses?
4. Disk usage says 100% despite deleting files. What might be happening?
5. Explain NAT gateway vs reverse proxy vs ALB vs API Gateway.

### B. AWS, IAM and networking (Weeks 5–16)

- [ ] Walk through VPC, SG, NACL, routing, NAT, VPC endpoints, ALB, Auto Scaling, DNS and IAM.
- [ ] Explain IAM roles, STS, policy evaluation, session credentials, KMS and CloudTrail.
- [ ] Defend a Multi-AZ/backup architecture against both failures and excessive cost.

**Questions:**
6. EC2 in a private subnet cannot reach the internet—how do you troubleshoot it?
7. Why does an EKS pod get `AccessDenied` for S3 while its node has access?
8. Your target group is unhealthy although the app process is running. What do you test?
9. How does GitHub Actions authenticate to AWS without storing access keys?
10. How would you design secure cross-account CI/CD deployments?

### C. Terraform / configuration management (Weeks 9–16)

- [ ] Explain state storage, remote locking, state sensitivity, modules, drift, import, lifecycle and tests.
- [ ] Demonstrate `fmt`, `validate`, `plan`, safe apply, policy checks and teardown.

**Questions:**
11. A teammate manually changes a security group managed by Terraform. What do you do?
12. Two pipelines attempt a simultaneous Terraform apply. What stops corruption?
13. How would you migrate a resource into a module without recreating it?
14. Terraform plan wants to replace a critical resource. How do you respond?
15. Where do you keep secrets and how do you prevent state from leaking them?

### D. CI/CD, Docker, EKS and GitOps (Weeks 13–24)

- [ ] Build/scan/sign/promote an image; use OIDC and environment approvals.
- [ ] Explain ingress vs service, pod vs deployment, Helm, Argo CD reconciliation and rollout.
- [ ] Debug scheduling, image pulls, probes, DNS, RBAC, resource and network issues.

**Questions:**
16. A CI job passes tests but security scanning fails. What should deployment do?
17. New deployment is crashing. How do you triage and roll back safely?
18. Why is `ImagePullBackOff` occurring with an apparently valid image tag?
19. How does Argo CD handle manual cluster drift? What happens during a failed sync?
20. Explain progressive rollout, rollback triggers and secrets management.

### E. DevSecOps, observability and SRE (Weeks 17–32)

- [ ] Distinguish SAST, SCA, secret scanning, IaC scanning, SBOM, signatures, admission policies.
- [ ] Define an SLI/SLO and calculate an error budget using real monitoring data.
- [ ] Correlate metrics/logs/traces to isolate a failed downstream request.
- [ ] Describe incident roles, severity, mitigation, rollback, RTO/RPO and postmortem process.

**Questions:**
21. How do you stop an unsigned or critically vulnerable container from reaching production?
22. A service has 99.9% monthly availability SLO. What does its monthly downtime budget imply?
23. Latency increases while CPU and memory look normal. How do traces help?
24. An alert fires every few minutes and no incident occurs. How do you reduce noise?
25. What does a good blameless postmortem contain?

### F. Infrastructure and system design (Weeks 5–48)

For each case, use: **requirements → capacity assumptions → HLD → critical flows → failures → security → observability → cost → trade-offs**.

- [ ] Secure, highly available web service on AWS: ALB, autoscaling, DB, private networking.
- [ ] Enterprise CI/CD platform: multi-account deployment, identities, artifact provenance, approvals.
- [ ] Kubernetes multi-team platform: namespaces, GitOps, network policy, policies, templates.
- [ ] Monitoring stack: ingestion, cardinality, retention, alerting, sampling and scale.
- [ ] Disaster recovery: backup frequency, RPO/RTO, failover procedures, test evidence.
- [ ] Rate limiter / async event processor: scaling, queuing, idempotency, retry/DLQ.

**Free prep:** [ByteByteGo System Design 101](https://github.com/ByteByteGoHq/system-design-101) · [Hello Interview](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction) · [Ashish Pratap Singh playlist](https://www.youtube.com/playlist?list=PLCZ2MME8uzMhow9-hAsSm2-dvfF4ag6wy) · [Gaurav Sen introduction](https://www.youtube.com/watch?v=quLrc3PbuIw) · [Cloud X Berry backend overview](https://www.youtube.com/watch?v=mZ27vUoOEB0).

### G. Scripting and coding interviews (2 problems per week initially)

Use Python for operational problems; prioritize arrays, dictionaries, strings, files, recursion basics, API calls, time complexity and robust error handling. Only add advanced algorithms if target jobs clearly require them.

- [ ] Parse JSON application logs; count failed requests per endpoint and 5-minute window.
- [ ] Inspect a list of servers/services and produce an availability report with retries/timeouts.
- [ ] Read YAML config, validate required fields and fail with actionable diagnostics.
- [ ] Compare two infrastructure inventories and output added/removed/modified resources.
- [ ] Implement a simple rate limiter or exponential backoff with jitter.
- [ ] Write tests for malformed input, empty results, network failures, duplicate records and permission denial.

### H. Behavioral and experience interviews

Prepare **eight truthful STAR/CAR narratives**: Situation/Context, Task/Challenge, Action you personally took, Result (measurable when possible), Lessons.

- [ ] Release-quality improvement or finding a critical defect.
- [ ] Collaboration across QA, development, SRE and release teams.
- [ ] Investigating a difficult failure with incomplete information.
- [ ] Learning an unfamiliar system quickly and safely.
- [ ] Preventing recurrence via automation or quality control.
- [ ] Handling conflicting priorities or deployment risk.
- [ ] Leading without authority / communicating during an incident.
- [ ] Explaining the shift from recent QA work toward cloud operations **without overstating hands-on DevOps tenure**.

**Interview positioning sample (adapt to the truth):** “My background combines software quality and previous DevOps-oriented responsibilities. I hold CKA/CKAD and have recently built and independently tested AWS/Terraform/CI/CD/EKS projects to deepen my hands-on infrastructure skills. My QA experience helps me design reliable quality gates and investigate failures systematically. I'm targeting roles where I can contribute to cloud automation, delivery and operations.”

---

## 8. Mock interviews, applications, and 30/60/90-day cadence

### Start interview preparation in Week 1, not after courses

| Timing | Practice/market action | Evidence |
|---|---|---|
| Every week | 3 spoken technical answers, 2 small Python tasks, 1 failure investigation | Video/audio self-review optional; notes with corrected answers |
| Every 2 weeks from Week 5 | 30-min AWS/networking or Terraform technical mock | Scores and missed concepts |
| Week 8 | 30-min architecture presentation | Diagram and peer/self feedback |
| Week 12 | Terraform + live diagnosis mock | No-notes demo, blockers list |
| **Week 16** | Full 60–90-min DevOps mock; resume/project review | **Go / improve / defer** decision for applications |
| Weeks 17 onward | Alternate Linux/AWS, Kubernetes/CI-CD, security/SRE and system design mocks | Written interview-error backlog |
| Weeks 25 onward | One 45-min design + 30-min ops exercise monthly | Clear architecture + debugging approach |

### 30 / 60 / 90 days of execution

| Period | Learning outcome | Career action |
|---|---|---|
| **Days 1–30** | Linux/networking/Python tool + 6 incident writeups | Collect 20–30 relevant JDs; identify shared requirements; draft a truthful base resume. |
| **Days 31–60** | Secure AWS VPC/IAM architecture + one HLD presentation | Identify skill gaps by role; connect portfolio topics to job requirements; practice intro/STAR. |
| **Days 61–90** | Reusable Terraform modules + policy checks; working CI foundation | Tailor resume; schedule mock interviews; shortlist bridge and direct DevOps roles. |
| **Days 91–120** | End-to-end AWS/Terraform/GitHub Actions/EKS/GitOps demonstration | Begin targeted applications once Gate D is passed; iterate based on actual interview feedback. |

### Applying intentionally (avoid arbitrary application quotas)

- Keep a shortlist of **10–20 relevant employers/roles**, refreshed periodically; verify active openings directly.
- Prefer jobs matching AWS/Linux/IaC/CI-CD/automation and where QA/release expertise adds value.
- Tailor 3–5 resume bullets to **real work** and add separate project bullets for your lab.
- Save each job description, date, requirements, recruiter screen observations and weaknesses exposed.
- After every interview, update: *question → my answer → correct/stronger answer → proof from a lab → next action*.
- Do not claim exact salaries, placement outcomes or professional production experience on the basis of coursework. Negotiate against role scope, current CTC, and validated market opportunities.

### Mock scorecard (score each dimension 0–4)

| Dimension | 0–1 (not yet ready) | 2 (developing) | 3 (interview ready) | 4 (strong) |
|---|---|---|---|---|
| Linux/network diagnostics | Guesses, few commands | Some guided diagnosis | Structured evidence-led diagnosis | Fast root-cause isolation and prevention |
| AWS architecture/IAM | Can't justify design | Understands typical patterns | Defends services, routing and identity | Handles constraints and unusual failures |
| Terraform/automation | Tutorial-only | Modifies working examples | Independently implements/tests modules | Explains state, drift, safety and design |
| CI/CD/EKS | Can recite tool names | Limited working pipeline | Demonstrates working pipeline + rollback | Recovers failures and explains trade-offs |
| Security/operations | Omits risks | Basic awareness | Built controls, alerts, runbooks | Trade-off-aware defense in depth |
| System design/communication | Disorganized answers | Reasonable diagram, weak trade-offs | Structured HLD with failure/cost/security | Concise, prioritized and adaptable |

**Week-16 decision:** Target **≥3/4 in Linux, AWS, Terraform, CI/CD/EKS, and communication**, with no unresolved critical safety mistakes; security/observability depth can continue through Weeks 17–32. This is a self-assessment heuristic, **not a universal employer hiring threshold**.

---

## 9. Practical assessments and readiness gates

| Gate | Timing | Pass criteria | If not yet passing |
|---|---|---|---|
| **A — Engineer's fundamentals** | Week 4 | Linux + DNS failure diagnosed without help, tested Python health-check, ≥6 incident notes | Repeat failure drills before advanced AWS work; study only the weak subtopics. |
| **B — AWS HLD** | Week 8 | Correct VPC/IAM/ALB explanation, cost/HA/security trade-offs, demo and cleanup | Revisit routing/IAM and rebuild a smaller secure environment. |
| **C — IaC owner** | Week 12 | Apply/modify/destroy Terraform safely, protect state, detect drift, discuss plan impact | Fix state/design/testing problems before wiring production-style pipelines. |
| **D — Apply-ready core** | **Week 16** | CI→ECR→EKS via OIDC/GitOps, rollback, tests, no secrets, ≥3 incidents, project walkthrough, key mock scores ≥3 | Continue interviews for bridge roles; dedicate 2–4 weeks to the weakest practical gate. |
| **E — Security/SRE credible** | Week 32 | Signed-image gate, telemetry, SLO, recovery drill, useful postmortem | Re-run a realistic failure scenario and document how controls change the outcome. |
| **F — Platform/AI specialist** | Week 48 | Self-service template, cost review, constrained AI incident assistant with adversarial tests | Treat as elective; not a prerequisite for Core DevOps applications. |

### Scenario drills to run and document

- [ ] Deliberately misconfigure service port / health endpoint; isolate 502 and restore.
- [ ] Create a bad DNS resolver entry / blocked firewall rule in a sandbox; distinguish failure layer.
- [ ] Introduce restrictive IAM policy and inspect `AccessDenied` with least-privilege remediation.
- [ ] Create Terraform drift; compare state and plan; repair safely through code.
- [ ] Deploy a broken image tag and failed readiness probe; inspect events and rollback.
- [ ] Block egress via Kubernetes NetworkPolicy; identify blocked destination using flow visibility.
- [ ] Fail a dependency or overload a service; use traces and metrics to identify the culprit.
- [ ] Restore a database/data snapshot into a test environment and measure recovery time.

---

## 10. Progress trackers, templates, and first seven days

### Phase tracker

- [ ] **Weeks 1–4:** Linux/networking/automation Gate A.
- [ ] **Weeks 5–8:** Secure AWS architecture Gate B.
- [ ] **Weeks 9–12:** Tested Terraform Gate C.
- [ ] **Weeks 13–16:** Secure delivery, Kubernetes recovery and Gate D; interview applications begin.
- [ ] **Weeks 17–24:** Security controls and supply-chain integrity.
- [ ] **Weeks 25–32:** Tracing, SLOs, incidents, disaster recovery and Gate E.
- [ ] **Weeks 33–40:** Developer platform, FinOps, advanced AWS and safe AI prototype.
- [ ] **Weeks 41–48:** AI workload operations, secure incident assistant and Gate F.

### Weekly study log — copy into `docs/progress/YYYY-WW.md`

```markdown
# Week XX — YYYY-MM-DD to YYYY-MM-DD

## Outcome this week
- [ ] Explain the core concepts without notes
- [ ] Build a working independent implementation
- [ ] Investigate and document at least one failure
- [ ] Answer three interview questions aloud
- [ ] Publish sanitized evidence and clean up cloud costs

## Time allocation (target = 15 hours)
- Courses/documentation: __ / 3h
- Build/labs: __ / 6h
- Break/fix: __ / 2h
- Interview practice: __ / 2h
- Documentation/applications: __ / 2h

## Artifact and evidence
- Repo/PR/commit:
- Architecture diagram / screenshot:
- Test results:
- Incident (symptoms, hypotheses, evidence, root cause, fix, prevention):
- AWS cost + teardown confirmation:

## Interview error log
| Question | My weak point | Improved answer + lab proof | Re-test date |
|---|---|---|---|

## Next week: top two priorities
1.
2.
```

### Interview tracker — copy into `docs/interview-tracker.md` (do not publish personally sensitive notes)

```markdown
| Company / Role | Date | Skill fit | Stage | Interview gap | Follow-up |
|---|---|---|---|---|---|
| Example / Cloud Engineer | YYYY-MM-DD | AWS, IaC, Linux | Screening | Explain VPC endpoints | Build/test private S3 access |
```

### Your first seven days — start here

- [ ] **Day 1:** Read this file, set up a private/public GitHub plan, create local Linux sandbox, confirm 15-hour calendar slots.
- [ ] **Day 2:** Watch selected [freeCodeCamp Linux Server](https://www.youtube.com/watch?v=WMy3OzvBWc0) chapters on services, processes, permissions; reproduce commands.
- [ ] **Day 3:** Create a systemd service and deliberately break its configuration; restore it using journal evidence.
- [ ] **Day 4:** Practice `ss`, `ip`, `dig`, `curl` and one [Kunal Networking](https://www.youtube.com/watch?v=IPvYjXCsTg8) section; document the network request flow.
- [ ] **Day 5:** Implement a Bash service-check script and add argument validation and exit codes.
- [ ] **Day 6:** Solve one or two [SadServers](https://sadservers.com/scenarios) exercises without viewing solutions; write root-cause notes.
- [ ] **Day 7:** Push README + script + sanitized outputs, answer three Linux interview questions aloud, review progress and next week's networking plan.

---

## Final execution rules

1. **Stop collecting course recommendations.** Follow this schedule unless an actual interview reveals a specific gap.
2. **Do not learn three providers for one skill.** One primary + one optional explanatory video is enough.
3. **Build before watching the next module.** Reconstruct the lab without copying from the instructor.
4. **Practice failure recovery every week.** Interview credibility comes from diagnosis, not tool-name recall.
5. **Test before claiming readiness.** Use gates and timed mocks; keep a written mistake backlog.
6. **Protect data and costs.** Use sandboxes, no real customer data, no credentials in repos, and prompt teardown of AWS resources.
7. **Be accurate about your experience.** Certifications and labs demonstrate learning but are not substitutes for employer production ownership.
8. **Apply before Month 12.** Seek relevant opportunities after Gate D; develop deeper SRE/platform/AI work in parallel.

**Start with Week 1 now. At the end of Week 4 you should have a working Linux automation toolkit and evidence from six incident investigations. At the end of Week 16 you should be able to present a working AWS/Terraform/CI/CD/EKS delivery platform and begin serious technical interviews.**
