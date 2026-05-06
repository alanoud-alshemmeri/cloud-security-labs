# Cloud Security Ecosystem & Career Readiness — Module 4

**Course:** Google Cloud Cybersecurity Certificate — Course 1, Module 4  
**Topic:** Cloud Security Roles, Tools, VPCs, AI in Security, and Career Preparation

---

## The Cloud Security Ecosystem

The **cloud cybersecurity ecosystem** is the network of people, processes, and technologies that work together to keep the cloud secure.

### Key Roles in Cloud Security

| Role | What They Do |
|------|-------------|
| **Cloud Security Analyst** | Monitors, detects, and responds to security incidents; uses tools to track assets and misconfigurations |
| **Cloud Security Engineer** | Implements and manages secure cloud workloads and infrastructure |
| **Cloud Security Architect** | Designs and develops security controls and measures within an organization's cloud infrastructure |
| **Compliance Team** | Ensures processes comply with laws, regulations, and standards |
| **SOC (Security Operations Center)** | Detects and responds to cybersecurity incidents |

---

## Cloud Security Analyst Responsibilities

### Core Responsibilities

1. **Map security concepts to cloud products** — Identify attack vectors for compute, network, and storage products and know how to protect them
2. **Use tools** — Work with Linux, Terraform, Google Cloud tools, and IDS to check VMs, containers, and networks for misconfigurations and threats
3. **Communicate security** — Prepare status reports, convey info to technical and non-technical audiences, avoid jargon
4. **Monitor and respond to incidents** — Use threat detection and compliance reports, cloud logging tools, and escalate incidents
5. **Test new security products** — Evaluate whether new tools are suitable and don't introduce new risks
6. **Stay current** — Follow security blogs, journals, and resources like the OWASP Top 10

---

## Cloud Security Stakeholders

A **stakeholder** is a person or organization who can affect or be affected by a system.

| Stakeholder Type | How Analysts Engage |
|-----------------|-------------------|
| **Leadership (CEO, CFO, CTO, CISO)** | Status reports, team meetings |
| **Other employees** | Simplify technical info during breaches (e.g., company-wide phishing alerts) |
| **Compliance teams** | Internal audit reports, identify controls impacting legal requirements |
| **End users** | Provide context to PR teams who communicate incidents to users |

> 💡 The **CISO** (Chief Information Security Officer) is the leader in charge of security governance.

---

## Google Cloud Tools

| Tool | Type | Purpose |
|------|------|---------|
| **Google Cloud Console** | GUI (Web UI) | Centralized dashboard to manage resources, access tools, find documentation |
| **Cloud Shell** | CLI | Enter commands, develop shell scripts, debug apps, view credentials |
| **Cloud Functions** | Serverless | Execute small pieces of code in response to event triggers (e.g., security alerts) |
| **Google Workspace** | Collaboration | Gmail, Drive, Docs, Calendar — collaborate with DevSecOps teams |
| **Cloud Identity** | IDaaS | Manage IAM, enable SSO & MFA, enforce policies from the admin console |
| **Compute Engine** | Compute | Create and deploy VMs on Google's infrastructure; monitor for suspicious activity |

---

## Virtual Private Cloud (VPC)

A **VPC** is a private cloud hosted within a public cloud, enabling organizations to use public cloud resources while being completely isolated from other users.

### Key VPC Concepts

- VPC networks and their components (routes, firewall rules) are **global** resources — accessible by any resource in any zone within the same project
- A VPC consists of **regional subnets** connected by a global WAN
- **Subnets** divide a network into logical groups with specific IP address ranges; they are **regional** resources

### VPC Modes

| Mode | Behavior |
|------|---------|
| **Auto mode** | Automatically creates a subnet in each region with predefined IPv4 ranges |
| **Custom mode** | You manually create and configure subnets with IPv4/IPv6 addresses |

### Useful gcloud Commands

```bash
# Create a custom mode VPC
gcloud compute networks create example-vpc --subnet-mode=custom

# List all networks
gcloud compute networks list

# Create a subnet
gcloud compute networks subnets create example-vpc-sub \
    --network example-vpc \
    --region us-west1 \
    --range 10.0.0.0/28

# List subnets for a specific network
gcloud compute networks subnets list --network=example-vpc
```

### Create a VPC via Console

1. Navigation menu → **VPC network** → **VPC networks**
2. Click **+ Create VPC Network**
3. Specify subnets, firewall rules, and configurations
4. Click **Create**

> 💡 Pro tip: The **"Equivalent command line"** link at the bottom generates the Cloud Shell commands matching your console selections.

---

## Artificial Intelligence in Cloud Security

**AI** is the theory and development of computer systems that perform tasks normally requiring human intelligence.

### AI Hierarchy

| Level | Description |
|-------|-------------|
| **AI** | Broad field — systems performing human-like tasks |
| **Machine Learning (ML)** | Uses algorithms to train data and make predictions without explicit programming |
| **Deep Learning** | Subset of ML using multiple layers of neural networks for complex problems |
| **Large Language Models (LLMs)** | Subset of deep learning for language tasks (answering questions, summarizing, generating text) |
| **Generative AI (GenAI)** | Subset of deep learning that creates new content (text, images, audio, video) |

### ML Training Methods

| Method | Description |
|--------|-------------|
| **Supervised learning** | Uses labeled data with tags (name, type, number) |
| **Unsupervised learning** | Uses unlabeled data; the model learns to categorize on its own |
| **Semisupervised learning** | Small amount of labeled data + large amount of unlabeled data |

### GenAI Model Types

| Type | What It Does |
|------|-------------|
| Text-to-text | Produces text from text (e.g., translation) |
| Text-to-image | Generates images from descriptions |
| Text-to-video/3D | Creates video or 3D objects from scripts |
| Text-to-task | Performs actions from text input (e.g., updating a document) |
| Foundation model | Adapts to different tasks; can be fine-tuned for specific domains |
| Multimodal | Converts one input type to a different output type |

### GenAI in Security — Use Cases

- Generate shell scripts to monitor system resources
- Analyze large volumes of vulnerability and threat data
- Identify patterns in network traffic during incidents
- Interpret and summarize security data

> ⚠️ Always **verify and modify** GenAI output to meet your organization's specific requirements.

---

## Entry-Level Cloud Security Job Titles

- SOC Analyst: Tier 1
- Incident Responder
- Jr. Cloud Security Analyst
- Jr. Cybersecurity Specialist
- Information Security Analyst
- Cybersecurity Analyst
- SOC Security Engineer
- Cloud Security Specialist
- DevSecOps Engineer

---

## Interview Tips

- **Show your thought process** — Focus on *how* and *why* you solved a problem, not just the result
- Practice with Google's **Interview Warmup** tool (select Cloud Cybersecurity)
- Each session: 2 background questions, 1 behavioral, 2 technical (~10 min)

---

## Glossary — Module 4

| Term | Definition |
|------|-----------|
| Cloud cybersecurity ecosystem | The network of people, processes, and technologies that keep the cloud secure |
| Cloud security architect | Designs and develops security controls within cloud infrastructure |
| Cloud security controls | Controls that safeguard cloud environments and minimize attack effects |
| Cloud security engineer | Implements and manages secure cloud workloads and infrastructure |
| Cloud security posture management | Monitoring and configuring cloud assets for security and compliance |
| Compliance team | Ensures processes comply with laws, regulations, and standards |
| Information risk management | Identifying, assessing, and minimizing threats to information assets |
| Security operations center (SOC) | Detects and responds to cybersecurity incidents |
| Stakeholder | A person or organization who can affect or be affected by a system |
| Threat intelligence | The collection, analysis, and evaluation of cyber threat information |
