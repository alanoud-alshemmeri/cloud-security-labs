# DevSecOps & Software Supply Chain Security — Module 3

**Course:** Google Cloud Cybersecurity Certificate — Course 1, Module 3  
**Topic:** DevSecOps, CI/CD Pipelines, IaC, and Securing the Software Supply Chain

---

## DevSecOps Culture

**DevSecOps** is a collaborative culture supported by guidelines, best practices, and tools that **development**, **operation**, and **security** teams use to work together.

It supports a **"security first"** culture by **shifting left** — meaning security is incorporated at the **beginning** of the development process, not at the end.

### The DevSecOps Lifecycle (7 Phases)

| Phase | What Happens | Security Role |
|-------|-------------|---------------|
| **1. Plan** | Outline scope, assets, and templates | Threat analysis, assign IAM roles, plan security tools |
| **2. Code** | Translate plans into source code | Safe coding practices, code reviews, automated bug/policy plugins |
| **3. Build** | Source code becomes artifacts and services | Automated vulnerability checks and security scans |
| **4. Test** | Manual + automated testing | Verify build integrity, security & compliance requirements |
| **5. Release** | Final review before production | Automated security checks, source code sign-offs |
| **6. Deploy** | Application goes live 🚀 | Automated push to production |
| **7. Operate** | Monitor live software | Continuous feedback loop, patch vulnerabilities |

> 💡 The **DevSecOps infinity loop** is the common visual — security wraps around the entire Dev → Ops cycle.

---

## Software Pipelines

A **software pipeline** is a process that uses automation and tools to facilitate movement through each phase of the software development lifecycle.

**Why pipelines matter:**
- Developers can release changes quickly
- Work on small pieces of code without interrupting other parts
- Automation ensures consistency and reduces human error
- Testing happens **throughout** the lifecycle, not just at the end (shift left)

### CI/CD Pipelines

The most common type of software pipeline.

| Term | Meaning |
|------|---------|
| **CI — Continuous Integration** | Developers continuously create and update code uploaded to a shared repository |
| **CD — Continuous Delivery** | Continuously releases software builds into a **testing** environment |
| **CD — Continuous Deployment** | Extension of delivery — automatically deploys builds into **production** in real time |

### Security in a CI/CD Pipeline (Example Flow)

1. Source code uploaded to shared repository → triggers a **build**
2. Build becomes an **image** → automated scans check for vulnerabilities & policy violations
3. If passed → image moves to the **artifact repository** (where images are stored)
4. **IAM permissions** ensure only authorized users can access the image
5. Automated vulnerability scans → if a vulnerability is found, automation triggers a **patch and redeploy**
6. Only privileged **service accounts** access deployed builds (less human error)

---

## Google's Cloud Build

**Cloud Build** is a Google **serverless** service that helps build and protect software.

**What it does:**
- Integrates code from cloud repositories or storage
- Creates builds → produces artifacts like container images
- Scans container images for **vulnerabilities** and **compliance**
- Provides insights into build health to identify bugs and errors
- Fully automated → improves consistency, reduces human error

---

## Infrastructure as Code (IaC)

**IaC** is the practice of provisioning and managing infrastructure using **reusable scripts**.

**Why it matters for security:**
- Automation reinforces security posture by adding security checks early
- Ensures developers across teams use the **same source code** for VMs and apps
- Reduces **configuration drift** (when a resource's configuration alters from its expected state)
- Catches invalid code inputs before they cause issues

### Terraform (IaC Tool)

- Used to write configuration files that define infrastructure
- Each **resource block** in the file describes what to create (network, VM, etc.)
- A single file can create networks + Google Compute Engine instances at once
- Reviewing Terraform files **before deployment** is a key security analyst task

### Related: Policy as Code (PaC)

The use of code to define, manage, and automate policies, rules, and conditions using a high-level programming language.

### Related: GitOps

A framework that applies version control, collaboration, compliance, and CI/CD best practices to **automate cloud infrastructure**.

---

## Software Supply Chain

The **software supply chain** includes the **people**, **processes**, and **tools** involved in software development.

### Key Concepts

| Term | Definition |
|------|-----------|
| **Artifact** | A digital object (file, image) used in the SDLC |
| **Provenance** | A description of the processes and tools used to build an artifact |
| **SBOM (Software Bill of Materials)** | A machine-readable list of every piece of software and its components in the supply chain |
| **SLSA** | Supply chain Levels for Software Artifacts — standards that enhance artifact integrity |
| **Security Hardening** | Strengthening a system to reduce vulnerabilities and attack surface |

---

## Google's Software Delivery Shield (SDS)

**SDS** is a fully managed Google Cloud solution that strengthens software supply chain security across **every stage** of the SDLC.

### What SDS Combines

- Google's best practices for securing software development
- Dashboards in the Google Cloud console showing security health of resources
- Comparison of your supply chain security against **SLSA guidelines**

### Key SDS Features

| Feature | Purpose |
|---------|---------|
| **Cloud Workstations** | Securely access development environments from a browser; reduces locally-stored code risks |
| **Automatic SBOM generation** | Provides a full overview of software components and compliance |
| **Assured Open Source Software (OSS)** | Same OSS Google uses internally — trusted, regularly scanned packages |

### How SDS Supports Shift Left

- Secures CI/CD pipelines with suggested IAM policies
- VPC guidance for network protection
- Cloud-native development environments
- Aligns with SLSA guidance for artifact security

---

## Glossary — Module 3

| Term | Definition |
|------|-----------|
| Artifact | A digital object (file, image) used in the SDLC |
| Commit | The specific change made to a file |
| Configuration drift | When a resource's configuration alters from its original or expected state |
| Continuous delivery | Continuous release of software builds to a testing environment |
| Continuous deployment | Deploys builds into a production environment in real time |
| Continuous integration | Developers continuously create/update code uploaded to a shared repository |
| CI/CD | A process DevSecOps teams use to create software and automate updates |
| DevSecOps | A culture of guidelines, practices, and tools for dev, ops, and security collaboration |
| GitOps | Framework applying version control, collaboration, and CI/CD to automate cloud infrastructure |
| Infrastructure as Code (IaC) | Automating and managing infrastructure using reusable scripts |
| Policy as Code (PaC) | Using code to define, manage, and automate policies and rules |
| Provenance | Description of processes and tools used to build an artifact |
| Security hardening | Strengthening a system to reduce vulnerabilities and attack surface |
| Shift left | Implementing security checks at the beginning and throughout the SDLC |
| Software Bill of Materials (SBOM) | Machine-readable list of software and its components in the supply chain |
| Software development lifecycle | A process for developing, testing, and monitoring software |
| Software pipeline | Process using automation and tools to move through each SDLC phase |
| Software supply chain | The people, processes, and tools that play a part in software development |
