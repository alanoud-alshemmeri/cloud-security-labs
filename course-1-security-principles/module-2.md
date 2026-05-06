# Cloud Security Fundamentals — Module 2

**Course:** Google Cloud Cybersecurity Certificate — Course 1, Module 2  
**Topic:** Security Controls, IAM, and Shared Responsibility in the Cloud

---

## Shared Responsibility Model

Cloud security is not solely the responsibility of the CSP or the customer — it's shared between both parties.

| Model | CSP Responsible For | Customer Responsible For |
|-------|-------------------|------------------------|
| On-Premises | Nothing | Everything |
| IaaS | Physical infrastructure, hardware | OS, data, applications, access |
| PaaS | Infrastructure + OS + network security + auth | Data, access policies, deployments, web app security |
| SaaS | Almost everything | Data and access policies |

**Key models to know:**

- **Shared Responsibility Model** — The implicit and explicit agreement between the customer and the CSP regarding shared accountability for security controls.
- **Shared Fate Model** — Goes further than shared responsibility; the CSP actively participates in the customer's security journey and provides resources to help manage security at each stage.

---

## Cloud Migration Considerations

Before migrating resources to the cloud, organizations should ask:

1. **Which security controls are your responsibility?** — Catalog your assets and determine what controls are needed.
2. **Which controls does the CSP offer?** — Review CSP documentation to see what aligns with your requirements.
3. **Which controls are inherited by default?** — Some CSPs provide encryption and infrastructure-level controls automatically.
4. **What are your compliance obligations?** — Industry or government regulations may affect where and how your resources are hosted.
5. **What are the security requirements for customers and contractors?** — Migration affects access privileges and privacy disclosures for all parties involved.

**Migration strategies:**
- **Lift and Shift** — Moving workloads to the cloud with little to no modifications.
- **Landing Zone** — A modular and scalable configuration that enables organizations to adopt Google Cloud for their business needs.

---

## Platform as a Service (PaaS)

PaaS is a cloud service model where the CSP hosts and maintains the backend hardware and software, while developers use these resources to build and deploy their own applications.

**PaaS includes:**
- **Infrastructure** — Physical infrastructure like data centers and servers
- **Middleware** — Software like operating systems and code libraries that facilitates communication between services
- **User Interface** — GUI or CLI for interacting with the platform

**Why use PaaS?**
- Scalable: developers add or remove resources on demand
- Cost-efficient: organizations only pay for resources used
- Useful for hybrid cloud migrations — developers use cloud infrastructure while keeping control of their application code

---

## Identity and Access Management (IAM)

IAM controls who has access to what resources in the cloud. It is fundamental to preventing unauthorized access.

### Key IAM Concepts

| Concept | Description |
|---------|-------------|
| **Principal** | Any entity (user or application) that can be assigned permissions and roles |
| **Role** | A collection of permissions that can be applied to principals |
| **Allow Policy** | Defines what access a principal has, and sets conditions on this access |
| **Deny Policy** | A constraint that prevents principals from carrying out certain actions |

### Identity Types

- **Groups** — A collection of principals categorized together and assigned the same roles. Best practice for applying least privilege at scale. Useful when people change roles — just update group membership.
- **Service Accounts** — Represent non-human identities like applications, services, or virtual machines that need to access cloud resources.
- **Federation** — A method of granting external identities access to the cloud environment (e.g., "Sign in with Google"). Enables Single Sign-On (SSO) and allows partners/contractors to use their own credentials.

> 💡 To further secure federated identities, enforce **Multifactor Authentication (MFA)** — requiring users to verify their identity in two or more ways.

### Google Cloud Console

The Google Cloud console is a centralized web UI where users manage all their cloud resources from a single dashboard.

**Key uses:**
- Configure IAM — add users, assign roles, change permissions
- Access all Google Cloud projects and services
- Launch **Cloud Shell** — Google's command-line interface for the cloud environment
- Find documentation and how-to guides

---

## Firewalls for Network Security

Cloud networks are **software-defined** — meaning the CSP implements network devices, including firewalls, using software rather than physical hardware.

### Firewalls in the Cloud

- Monitor and filter incoming and outgoing network traffic
- Software-based and hosted by the CSP
- **CSP's responsibility:** maintain the software and physical infrastructure
- **Customer's responsibility:** configure the firewall rules that filter traffic
- **Scalable:** automatically adjust as the network grows or shrinks

### Firewall as a Service (FWaaS)

FWaaS is a service model that allows organizations to use firewall capabilities without managing physical hardware. Google's **Cloud Firewall** is an example — it protects resources from both internal and external attacks.

**FWaaS Best Practices:**
1. **Principle of Least Privilege** — Only allow traffic that is strictly necessary
2. **Hierarchical Firewall Policies** — Apply policies at the organization and folder levels for consistency across all resources
3. **Choose the right FWaaS** — If not using the CSP's built-in firewall, select a solution tailored to your CSP's environment

---

## Security Controls & Defense in Depth

**Defense in depth** is a layered approach to vulnerability management — each control plays a role in defending cloud assets.

Organizations use the **NIST Cybersecurity Framework (CSF)** as a guide. It recommends five categories of controls:

| Category | Control Type | Purpose |
|----------|-------------|---------|
| **Identify** | — | Catalog assets and rank risks to understand where gaps exist |
| **Protect** | Protective Control | Shield resources — restrict access, use firewalls, train employees |
| **Detect** | Detective Control | Monitor environments and identify suspicious activity (e.g., intrusion detection systems) |
| **Respond** | Responsive Control | Use automation to contain and mitigate incidents once detected |
| **Recover** | Recovery Control | Restore access and functionality — replicate resources across regions, maintain backups |

### Control Types Summary

| Control | Definition |
|---------|-----------|
| **Identity Control** | Authenticates a user before they access resources |
| **Network Control** | Protects access through network paths |
| **Protective Control** | Shields against malicious attacks |
| **Detective Control** | Identifies suspicious activity when it occurs |
| **Responsive Control** | Uses automation to respond to security events |
| **Recovery Control** | Restores access and functionality after failures |

---

## Glossary — Module 2

| Term | Definition |
|------|-----------|
| Allow policy | A type of access a principal has, and sets conditions on this access |
| API | A library function or system access point that communicates with other applications |
| Defense in depth | A layered approach to vulnerability management that reduces risk |
| Deny policy | A constraint that prevents principals from carrying out certain actions |
| Detective control | A measure used to identify suspicious activity if it occurs |
| Identity control | A measure that authenticates a user before they access resources |
| Lift and shift | A migration model where workloads are moved to the cloud with little to no modifications |
| Landing zone | A modular and scalable configuration that enables cloud adoption |
| Network control | A measure that protects access through network paths |
| Principals | Represent either end users or applications |
| Protective control | A measure that shields against malicious attacks |
| Recovery control | A measure that restores access and functionality after failures |
| Responsive control | An application or tool that uses automation to respond to security events |
| Roles | A collection of permissions that can be applied to principals |
| Router | A network device that connects multiple networks together |
| Service level agreement (SLA) | Quantifies the availability of services |
| Shared fate model | Emphasizes the CSP's involvement in the customer's entire security journey |
| Shared responsibility model | The agreement between customer and CSP regarding shared accountability for security |
| Switch | A device that makes connections between specific devices on a network |
| Virtual private cloud (VPC) | A private cloud hosted within a public cloud, isolated from other cloud users |
