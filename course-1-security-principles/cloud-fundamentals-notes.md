# Cloud Computing Fundamentals — Study Notes
**Course:** Google Cloud Cybersecurity Certificate — Course 1, Module 1  
**Topic:** Introduction to Cloud Computing  

---

## What is Cloud Computing?

Cloud computing is the delivery of on-demand computing resources over the internet. Instead of owning physical servers, organizations rent compute, storage, and networking from a Cloud Service Provider (CSP) like Google Cloud.

**Key cloud models:**
| Model | Description | Example Use Case |
|-------|-------------|-----------------|
| Public Cloud | Shared infrastructure over the internet | Startups, web apps |
| Private Cloud | Dedicated to one organization | Government, banks |
| Hybrid Cloud | Mix of public + private | Cymbal Bank's strategy |
| Multicloud | Multiple CSPs | Avoiding vendor lock-in |

---

## Core Cloud Concepts

### Virtualization
Creates virtual versions of physical hardware (servers, storage, networks), enabling multiple workloads to run on one physical machine via a **hypervisor**.

### Containers vs Virtual Machines
- **VM**: Full OS per instance, heavier but isolated
- **Container**: Shares OS kernel, lightweight, ephemeral — ideal for microservices

### Serverless Computing
- **BaaS** (Backend as a Service): CSP manages all backend infrastructure
- **FaaS** (Function as a Service): Short-lived functions triggered by events (e.g., Google Cloud Functions)
- Security benefit: Short function lifespan limits attack windows

---

## Google Cloud Storage Classes

| Class | Access Frequency | Use Case |
|-------|-----------------|----------|
| Standard | Frequent (daily) | Active apps, medical records |
| Nearline | ~Once/month | Backups |
| Coldline | ~Once/quarter | Archived records |
| Archival | ~Once/year | Disaster recovery |

> **Security Note:** Classifying data correctly reduces exposure — less frequently accessed data should have stricter access controls.

---

## Google's Trusted Infrastructure — 5 Security Layers

1. **Secure Low-Level Infrastructure** — Physical data center security (biometrics, cameras, unique server IDs)
2. **Secure Service Deployment** — Zero-trust model: every user/device must authenticate before access
3. **Secure Data Storage** — Encryption at rest; scheduled deletion to prevent accidental loss
4. **Secure Internet Communication** — Private IP address space, isolated from public internet
5. **Operational Security** — MFA for employees, verified code libraries, dedicated threat monitoring team

---

## Cloud Benefits vs Limitations

| Benefits | Limitations |
|----------|-------------|
| Faster time to market | Loss of physical infrastructure control |
| Improved collaboration | Data privacy concerns |
| Built-in data security (encryption) | Complex migration process |
| Durability & redundancy | Dependency on CSP's security measures |

---

## Key Terminology

| Term | Definition |
|------|-----------|
| Redundancy | Multiple data copies across locations to avoid single point of failure |
| Resiliency | Ability to recover from disruptions |
| Ephemerality | Resources that exist only temporarily |
| Immutability | Objects that cannot be changed after creation |
| Latency | Time for data to travel between locations |
| Zone | Collective data centers in an area |
| Region | Group of zones |

---

## Real-World Connection: Cymbal Bank

Cymbal Bank chose a **hybrid cloud** model for their digital transformation — keeping sensitive customer data in a private environment while leveraging Google Cloud's public infrastructure for scalability. As a junior cloud security analyst, understanding these fundamentals is the foundation for securing their cloud environment.

---

*Part of the [cloud-security-labs](https://github.com/alanoud-alshemmeri/cloud-security-labs) portfolio*
