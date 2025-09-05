# CivicActions DRAFT GitHub Use Policy

This is a DRAFT policy outlines when work should go into the CivicActions corporate GitHub repository versus a personal repository, and how to attribute CivicActions support when experimenting on paid time. All projects should have an appropriate license. CivicActions default license should be the [AGPL v3](https://opensource.org/license/agpl-v3), but other [OSI-approved licneses](https://opensource.org/licenses) can also be appropriate. 

---

## 1. Governance: Corporate vs. Personal Repositories

CivicActions wants to track Practices (org-wide methods, standards, shared tools), Projects (client or internal initiatives) and Products (open-source tools we want to sustain). We do not want to restrict creativity and experimentation of our team, but we do want to be able to maintain our corporate repositories. 

### Corporate GitHub Repository (use when…)
- The work is **intended to be maintained** beyond the original author’s involvement.  
- The project aligns with **client delivery, internal tooling, or CivicActions strategy**.  
- The code is itended to be **reused, extended, or depended on** by others in the company.  
- The work touches on **governance, compliance, or accessibility** standards where CivicActions must show accountability.
- The code is intended to be **shared widely** and is tied to our practices, projects or products.
- Documentation, issue tracking, or contribution from other staff will be needed.
- Build to align with our Check My Repo https://github.com/CivicActions/check-my-repo
- Security, licensing, and support responsibilities fall to CivicActions.  

### Personal or Private Repositories (use when…)
- The work is **exploratory, throw-away, or highly experimental**, and may never be maintained.  
- The work is part of **personal learning or prototyping** that doesn’t yet meet company governance standards.  
- The project is tied to **individual interests or experiments** that may or may not align with client work.  
- The author wants to test or draft ideas before proposing them for company adoption.  

**Rule of thumb:** If CivicActions or its clients will **depend** on it, it belongs in the corporate repo. If it’s **personal exploration**, keep it in a personal repo unless and until it becomes company-backed.

---

## 2. Attribution of CivicActions-Supported Work

When staff experiment during CivicActions-paid time, they should acknowledge CivicActions’ support while respecting personal repositories. Anyone at CivicActions should feel free to fork a project into the CivicActions repository if it is relevent to practices, projects or products we are working on. With personal projects of staff, it is good to reach out.

- Include a statement in the README of personal repos created on CivicActions time:  
  > “This work was initiated with support from CivicActions.”  
- If the project later becomes useful to CivicActions or its clients, it should be **migrated into the corporate GitHub** and maintained under CivicActions governance.  
- Staff are encouraged to **flag experiments** in weekly updates or Slack so others are aware of the exploration, even if it stays in a private repo.  
- When in doubt, **err on the side of attribution**. This protects both the individual and the company and demonstrates CivicActions’ commitment to open knowledge and stewardship.

---

## 3. Decision Tree

```mermaid
flowchart TD
    A[Do you expect others at CivicActions to use or depend on this work?] -->|Yes| B[Put it in the Corporate GitHub Repo]
    A -->|No| C[Is this just personal learning or an experiment?]

    C -->|Yes| D[Keep it in a Personal Repo<br/>Add note: 'Supported in part by CivicActions']
    C -->|No| E[Does it align with client delivery or CivicActions strategy?]

    E -->|Yes| B
    E -->|No| D

    B --> F[Add docs & follow CivicActions governance]
