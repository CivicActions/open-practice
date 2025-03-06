### *Open Requirements*

# Agile Migration to Drupal

## Contents

[TOC]

## About the Open Requirements Library

The purpose of the Open Requirements Library is to utilize open and emerging technology to contribute to a more equitable government marketplace—one where solicitations are more easily understood and require less time in the acquisition life cycle.

**Key performance results:**

- Fewer submitted solicitation questions
- Fewer pre-award protests
- Faster acquisition cycles
- Create a more inviting marketplace to new entrants
- Reduce dependency on input from incumbent vendors

Read more about the [Open Requirements Library](https://docs.google.com/document/d/1OYrxJp5LaZMRSFltmnwvS2BpcRwnkDY3not6ELjH2M0/edit#heading=h.hblvjympznf4), and contribute your ideas.

### How may you use the Open Requirements for a Migration to Drupal?

The requirements listed within this document are intended to be a comprehensive, yet “white-labeled,” description of actions required to complete a Drupal migration from a legacy content management system or existing website. The expectation is that a person (for example, a program office for a government agency) could copy/paste these requirements into a draft solicitation for vendor support. Then, the user could customize requirements where and how they see fit. The program office can collect and learn best practices for a Drupal migration during this process. Efficiency, integrity, and quality increase as the user doesn't have to start from scratch, ask an incumbent vendor for the content baseline, or copy/paste from a previous (potentially flawed) solicitation.

Additionally, vendors providing migration to Drupal are welcome to learn, contribute to and prepare for the best practices of Drupal migration services.

Anyone can contribute to the Open Requirements for Drupal Migration. Contributions will be reviewed for their positive impact on improving the efficiency, integrity, and quality of Drupal migration requirements.

### Assumptions

The approach below assumes an **Agile, slice-by-slice** migration of a large, public-facing website to Drupal. Key assumptions include:

1. **“The team”** refers to the technical delivery team.
2. The team operates using Agile or scrum organizing principles.
3. The product backlog is created and managed in a robust project ticketing system. Project deliverables are tracked as initiatives, epics, or user stories.
   - Deliverables are organized and prioritized in a product roadmap.
   - The roadmap allows stakeholders to agree on specific deliverables and dates and to be informed of progress or blockers.
   - Deliverables are scheduled for each two- to three-week sprint.
   - Team retrospectives are used to rapidly identify problems and improve processes.
4. Early sprints focus on **discovery** and creating the project **scaffolding** needed to deliver secure, high-quality code.
5. The new team must learn organizational details, norms, and processes for code submission and review.
   - Building production routines carefully prevents issues later in the project.
6. The team establishes and maintains a **continuous integration/continuous delivery (CI/CD) pipeline** integrating code-quality tests and functional end-to-end testing.
7. The team sets up and secures **environments**, ensuring that platform changes (permissions, security updates, etc.) don’t break the CI/CD pipeline.
8. The team assumes hosting on a secure cloud (e.g., AWS with EC2, RDS, S3), and uses GitLab, CloudFormation, Ansible, or equivalent for the CI/CD pipeline.
   - Steps are based on these assumptions and may adjust if the stack changes.
9. All stakeholders engage daily.
   - Agile is highly collaborative; decision-makers must be available to provide feedback and remove blockers quickly.
10. Everyone—including client stakeholders—participates in Quality Assurance.

   * The team tests early and often and follows “fail fast” to identify the best solution paths.

   * Methods strive to reduce “second-guessing,” which wastes development cycles.

11. System documentation is maintained in the code repository, in a documentation store, or embedded in the site.
    * No code is delivered without relevant documentation for developers and system administrators.

### Project Roles

Below is a list of typical Agile project roles for a Drupal migration. Some roles can be combined where appropriate (e.g., a Content Strategist might also conduct user research):

- Program Manager / Contract Manager
- Project Manager / Scrum Master
- Product Manager
- Technical Lead / Site Architect
- Migration Engineer
- Back-End Engineer
- Front-End Engineer
- Quality Assurance/Testing Specialist/Engineer
- Accessibility Specialist/Engineer
- User Research Specialist
- User Experience (UX) Designer
- Content Strategist / Service Designer
- Security / Compliance Officer
- DevOps Engineer
- Help/Support Specialist



## **An Agile, Slice-by-Slice Migration Approach**

Many legacy website migrations use a “big bang” or waterfall model—collecting _all_ requirements, building _everything_, then launching once. However, **best practice for larger or more complex sites** is to iteratively migrate site sections (or “slices”) while continually improving scaffolding, features, and performance. Regardless of the approach, migrations should be processed using the Drupal Core Migrate API and supporting contributed migration modules.

**In practice**, this means:

1. **Deciding on a migration strategy: how to segment/slice the site for migration. **The team should identify how to segment and prioritize slice migration. For example, the team could choose to segment by department or program, or could choose to start with low-visibility portions to test the migration process and then schedule more critical portions after more is known about migration details.
2. **Identifying a specific slice to start** (e.g., “jobs” section, “blog,” “press releases,” etc.).
3. Complete _all_ relevant activities (discovery, design, build, migration, user testing, launch) **for that slice**, using web proxy or load balancer rules to route users of that section to the new Drupal site.
4. Gather feedback, refine, address issues, and ensure stable performance.
5. Choose the next slice, repeat.

By repeating this cycle, the old system is gradually replaced, avoiding a massive single cutover. This incremental approach mitigates risk, accelerates user feedback, and can deliver immediate improvements for certain user groups earlier.

The exact order may change somewhat as the team develops agile initiatives, epics, and user stories, which are evaluated and prioritized by key stakeholders (product owners, project managers, and product managers) during each sprint cycle.

Below is a detailed breakdown of the activities, reorganized into **(1) Initial Setup & Discovery**, followed by **(2) Iterations** that are repeated slice-by-slice.



### 1. Initial Setup & Discovery (Laying the Foundation)

##### 1.1 Project Kickoff

Kickoff is where the core team is formed, roles are clarified, and communications protocols are established. Even though subsequent slices may have their own specific start-up activities, this **initial** project kickoff lays the groundwork for how everyone will collaborate and what each person is accountable for.

1.  ###### Form the Team, clarify Governance policies, and Establish Roles
  
    - Identify key participants (Scrum Master, Product Owner, DevOps Engineer, etc.).
    - Clarify responsibilities and empower people to make decisions for their domain (e.g., UI, content, infrastructure, QA) by building a Team Charter or Team Working Agreement - see below
    - Ensure the governance structure of the project is documented and accessible to team members.
2.  ###### Set Up the Collaboration Framework
  
    - Schedule regular Agile ceremonies (daily standups, sprint planning, reviews, retros) and identify a tool set for communication (Slack, Teams, email).
    - Document how the team will track and prioritize tasks (e.g., Jira, GitHub Issues, Trello).
    - Establish how design, system, workflow/decision/risk, code documentation and open source code contribution will happen, and where it will be kept.
3.  ###### Request Access and Permissions
  
    - File access requests for any existing systems, documentation, codebases, databases, issue tracker, analytics, or user research.
    - If the site is large and content owners are in multiple departments, compile a stakeholder directory.
4.  ###### Establish incident response and risk management practices
  
    - Determine how the team will respond to potential system outages, data loss, or security incidents by adopting an incident notification and response plan.
5.  ###### Establish Definitions of Done

    - **Sprint-level** definition of done: acceptance criteria, code reviews, passing tests, etc.
    - **Release-level** definition of done: user acceptance testing (UAT) passed, security scans, accessibility checks, sign-off from product owner.

6.  ###### Team Charter

    * Draft a simple statement of project goals, success metrics, roles, and timelines.
    * Include any contract deliverables or constraints, so the entire team has a shared understanding.

##### Deliverables

- Initial governance documentation created
- Roles & responsibilities within the Agile process
- Access requests completed for all team members (documentation, code, issue tracker)
- Defined issue-tracking approach (story points, acceptance criteria, etc.)
- Incident response plan is in place
- Sprint-level and release-level definitions of done
- Team charter
- Accessibility, performance and SEO baseline scans of legacy site (e.g. with Unlighthouse and/or Oobee)

#### 1.2 Initial Discovery

While **Discovery** will be repeated in smaller cycles for each slice, the **initial** discovery phase provides a high-level perspective on user needs, technical architecture, and overarching migration strategy.

1.  ###### User & Stakeholder Research

    * Conduct interviews or workshops with representative users or product owners to understand high-level pain points and immediate priorities.
    * Identify the organizational context: Are there critical deadlines? Which stakeholders have final say?

2.  ###### Preliminary Success Metrics
  
    - Define what success looks like: e.g., faster publishing workflows, improved site performance, better accessibility.
    - These metrics guide _why_ we’re migrating and _how_ to measure outcomes.
    - Capture impact and metrics in governance documentation
3.  ###### Technical Architecture Ideation
  
    - Identify major platform constraints (e.g., must be FedRAMP-approved, must integrate with existing single sign-on).
    - Consider at a high level how Drupal will be set up (traditional, decoupled, static generation, etc.).
    - Capture architecture understandings in governance documentation
4.  ###### Roadmap & Slice Strategy
  
    - Brainstorm potential “slices” (sections of the site) to migrate first—based on user impact, complexity, or content value.
    - Outline a high-level migration roadmap: the team may prioritize an easy “slice” first or one with the highest user value.
    - Plan to **revisit** this roadmap regularly, as each slice’s feedback may reprioritize the next slice.
5.  ###### Parallel or Iterative Discovery
  
    - Discovery is never finished. As soon as a slice is selected, deeper analysis occurs for that slice’s requirements (see 1.3 and 1.4 below).
    - Some tasks in initial discovery (like user research or content inventory) may proceed in parallel.

##### Deliverables

- **Project Plan (High-Level Architecture)**: An outline describing how Drupal will be structured and hosted.
- **Preliminary Migration Plan**: A top-level concept for how to move from legacy to Drupal in incremental slices.
- **Migration roadmap:** A rough order of operations for migration work to be completed
- **Story Map**: A broad set of user stories, epics, or features the new site must fulfill.
- **Candidate Backlog**: Initial backlog of tasks, which will be split into sprints or allocated to slices.
- **Foundational Technical Architecture**: Early documentation on approach to hosting, security, CI/CD strategy.

**Important Note**: The “Initial Discovery” sets a **baseline**. For each slice, the team will undertake a more focused discovery cycle to flesh out the details specific to that content or user segment.



#### 1.3 Content Discovery

Content discovery clarifies what types of content exist, who owns it, and where it lives. While you might not do a **deep** audit of every piece of content at the very start, you want enough insight to pick a good first slice and to avoid surprises.

1. ###### High-Level Content Audit
  
   - Identify broad content categories (articles, press releases, job postings, etc.).
   - Note approximate volumes, potential complexities, or special file formats.
   - Identify interactive forms or dynamic elements, including any non-content data or PII.
   - Look for legacy content or one-off projects that are distinct from the main site.
2. ###### Ownership & Storage
  
   - Document key content owners across departments.
   - Determine if content is in databases, on file servers, or scattered across multiple legacy systems.
3. ###### Initial Prioritization
  
   - Work with the product owner and stakeholders to spot any “low-hanging fruit” slices or critical content sets that can define the first migration approach.
   - Some organizations choose a less risky slice to learn or may jump to a high-value slice.

##### Deliverables

- **List of content types** and approximate volume/scope

- **Map of content owners and storage locations**

- **Potential first-slice candidates** for deeper follow-up

  

#### 1.4 Migration Discovery

With a better understanding of the content, the team can plan a **migration/cutover strategy** that minimizes user disruption. This might mean a one-time cutover for smaller projects or an **incremental** approach for large sites (recommended).

1. ###### Preliminary Migration Approach
  
   - Confirm if slices will be deployed behind an HTTP proxy so that only a certain path (like `/jobs`) points to Drupal while the rest still resides on the legacy system.
   - Outline a “rolling migration” schedule or a big-bang final cutover (depending on scale).
   - Determine if and how site navigation will change during the migration. If redirects from old locations are needed, determine how those redirects will be constructed.
   - If content needs to be reviewed and/or updated, determine how that will be accomplished (before or after migration, manually edits, automatic fixes etc)
   - Identify approaches for migrating users and any other non-content data.
2. ###### Involve Edito1rial Stakeholders
  
   - Discuss content cleanup, archiving older or irrelevant material, and ensuring only high-value content is migrated.
   - Clarify how editors will handle content updates during overlap (e.g., do they double-edit in both old and new systems for a time?).
3. ###### Document Overlap Processes
  
   - If partial slices go live in Drupal, ensure a process for user redirection or linking between new and old sites.
   - Identify how user feedback and bug reporting will be handled if portions of the site are on different systems.

##### Deliverables

- **Preliminary Migration Plan** (incremental or otherwise)

- **Defined editorial role** in migration: how content is chosen, cleaned up, moved.

- **Cutover/overlap strategy** for each slice or content set

  

#### 1.5 Repository & Code Discovery

Though some details may be clarified later when the team sets up CI/CD, you want to **inventory existing repositories** or code assets so you don’t “start from zero.”

1. ###### Locate Existing Codebases
  
   - Are there any legacy code repositories with helpful scripts, data transformations, or partial Drupal configurations?
   - Identify if the code is in GitLab, GitHub, or a private Subversion repository.
2. ###### Identify Documentation Gaps
  
   - If docs exist in Confluence, SharePoint, or PDF format, note who owns them.
   - Understand if any documentation is outdated or missing.
   - Find and review tickets relating to the legacy site to identify gaps also.
3. ###### Assess Dev Standards
  
   - Are there existing coding guidelines, style guides, or DevOps standards?
   - What languages or frameworks are used in the legacy system that might affect migrations?

##### Deliverables

- **Repository Inventory** (legacy code, scripts, etc.)

- **Documentation Source List**

- **Preliminary plan** for how new code repos will be structured

  

#### 1.6 Infrastructure Discovery

In large public-facing migrations, the hosting environment and deployment methods can significantly affect the project timeline. This step clarifies environmental constraints and opportunities.

1.  ###### FedRAMP-Approved Cloud & Security Posture

    * Confirm if you’ll use AWS, Azure, GCP or other service providers with FedRAMP compliance (for US government contexts).
    * Assess any existing Infrastructure as Code (IaC) usage (CloudFormation, Ansible, Terraform).

2.  ###### Deployment Strategy
  
    - Understand if zero-downtime or “blue-green” deployments are required.
    - Determine whether different slices can each have their own test/staging environment or if they share one.
3.  ###### Data & Backup Requirements
  
    - If the site has frequent content changes, backups must be robust and scheduled.
    - Identify compliance or retention policies for old content or logs.

##### Deliverables

- **Service Audit**: existing analytics, metrics, infrastructure details

- **Preliminary DevOps Approach**: likely CI/CD pipeline, environment setups

- **Baseline Understanding** of security, compliance, and performance requirements/ service-level-agreements (SLAs)

  

#### 1.7 User Research and Experience Discovery

While user research continues throughout each slice, the initial stage is about identifying high-level user groups and potential design goals.

1. ###### Initial Personas & Journeys
  
   - If they do not exist, create broad user persona outlines (including public users, internal staff, etc.).
   - Note the top user tasks and pain points and describe the “journeys” that users will care about. These journeys are a great input to identifying/prioritizing slices and to automated testing plans.
2. ###### High-Level UX & Design Principles
  
   - Decide if the site will adopt the USWDS (U.S. Web Design System) or another well maintained, accessible design library.
   - Identify any brand or accessibility mandates. Is there an accessibility statement?
   - Determine the approach to content discoverability: site navigation and search integration.
3. ###### Future Testing Strategy
  
   - Plan how to incorporate user feedback: e.g., quick usability tests, surveys, or pilot groups.
   - Identify which user segments to recruit for testing each slice.

##### Deliverables

- **Preliminary user research findings** (who, what they need)

- **Design Concepts/Wireframes** for overarching site look and feel

- **Initial plan** for ongoing UX validation (through user testing in future sprints)

  

#### 1.8 Publishing Workflow Discovery

Before building or customizing Drupal’s editorial workflow, it helps to understand how content is published in the **current** system and what might need to change.

1. ###### Current Workflow Analysis
  
   - Identify roles (author, editor, publisher) and any multi-level approval processes.
   - Determine which processes are mandated by policy vs. which are simply habits.
2. ###### Future Workflow Options
  
   - Decide if the new site will store content in Drupal but publish it as static HTML, or if it will be fully dynamic.
   - Confirm if you need scheduled publishing, editorial reviews, or version control for compliance.
3. ###### Implications for Architecture
  
   - If a static approach is chosen, the team must plan for content rendering and distribution via CDN or some other means.
   - If fully dynamic, pay close attention to performance, caching, and security.
4. ###### Testing & Automation
  
   - Incorporate workflow testing into the backlog.
   - Plan to use automated tests or manual QA to verify that new editorial flows match user expectations.

##### Deliverables

- **Documented “As-Is” and “To-Be”** publishing workflow

- **Proposed approach** (static vs. fully dynamic, or a hybrid)

- **Draft workflow** to be refined in subsequent slices

  

## 2. Iterative Slices: Repeat for Each Section of the Site

This section focuses on how to set up the **technical foundation** and **operational scaffolding** needed to build and launch each slice of the new Drupal site. While many of these activities will initially be addressed before work on the _first_ slice, each subsequent slice may prompt **refinements** to the environments, repositories, testing frameworks, or CI/CD pipeline. In other words, scaffolding is neither a purely “one-and-done” step nor entirely sequential; rather, it **evolves** to meet the needs of each new slice.



### 2.1 Establish Code, Infrastructure, and Documentation Repositories

Before building the first slice (and for each subsequent slice if needed), the team must confirm that all **repositories** are properly created and structured:

1. ###### Infrastructure Repository
  
   - Stores “infrastructure as code” (e.g., CloudFormation, Ansible, Terraform scripts) and any associated configuration to spin up or modify environments reliably.
   - Defines how servers, networks, and storage are provisioned, secured, and scaled.
   - Makes environment changes traceable and reviewable via pull requests or merge requests.
2. ###### Application (Drupal) Code Repository
  
   - References the Drupal core code, contributed modules, and houses custom modules, theme files, and any front-end assets.
   - Allows for separate branches for each feature, bug fix, or slice-specific enhancement.
   - May also include relevant build scripts (e.g., Drush commands, composer.json).
3. ###### Documentation Repository
  
   - Contains system documentation, developer onboarding guides, architecture diagrams, team charters, security plans, and any compliance paperwork (e.g., for an Authority To Operate).
   - Ensures team knowledge is centralized and version-controlled.
   - Facilitates ongoing updates as the site evolves through multiple slices.

**Iterative Consideration**: In future slices, the team might add new sub-repositories (e.g., specialized microservices or unique front-end frameworks for a specific slice) or reorganize documentation if the project scope grows.

##### Deliverables

- Version-controlled infrastructure repository (including environment code)
- Drupal/application code repository (with branch and tagging strategy defined)
- Documentation repository (with structure for architecture, user guides, and system security artifacts)



### 2.2 Establish Hosting and Development Scaffolding

Using the Discovery findings, the team **implements or refines** the hosting environment and local development approach. This scaffolding often evolves in parallel with the first slice, but may continue to expand for subsequent slices if new requirements emerge (e.g., multilingual sub-sites or specialized hardware needs).



#### 2.2.1 Hosting Environment(s)

1. ###### FedRAMP-approved Cloud (or equivalent secure hosting)
  
   - Typically AWS, Azure, GCP or Acquia for high-visibility government sites.
   - Must meet scalability, reliability, and security/compliance standards (e.g., 24x7x365 availability, 99.8% uptime).
2. ###### **Continuous Availability**
  
   - Incident response playbooks ensure rapid recovery.
   - Redundant architecture to minimize single points of failure.

**Refining Over Time: **Early slices might require a smaller environment or minimal redundancy; later slices or increased traffic may lead to scaling or additional load-balancing features.



#### 2.2.2 Local (Developer) Sandboxes

1. ###### Docker-based or VM-based Environments:
  
   - Tools like DDEV or Lando can create local containers mirroring Production (same PHP versions, DB engines, etc.).
   - Ensures code works “the same” locally and in the server environment.
2. ###### Automated Setup
  
   - Scripts (e.g., Bash, Ansible) to bootstrap local dev quickly.
   - Encourages consistent testing across the team.

**Refining Over Time:** Each new slice may add new dependencies (modules, libraries) that require updates to the local environment definitions or container images.



#### 2.2.3 Backup and Disaster Recovery

1. ###### Frequent Snapshots
  
   - Example: Hourly snapshots retained for one month, nightly for a year (adjust per requirements).
2. ###### **Geographic Redundancy**
  
   - Data stored in multiple regions to protect from localized outages.
3. ###### Rollback Procedures
  
   - Ability to revert if a slice deployment breaks something or if content migration fails.

**Refining Over Time:** Additional backup schedules or more granular backups may be added if a new slice holds mission-critical data or large media assets.

**Deliverables**

- Fully configured hosting environment (initial size may be modest, can scale later)

- Local development environments with automated setup scripts

- Backup and DR plan (hourly/daily snapshots, tested restore process)

  

### 2.3 Build and Maintain CI/CD Pipeline(s)

Once the repositories and basic environments exist, the team sets up a **continuous integration/continuous delivery** (CI/CD) pipeline to streamline:

- **Code Quality Checks**: Linting, coding standards, and static analysis.

- **Automated Testing**: Unit, functional, end-to-end, accessibility, visual regression, security scans, etc.

- **Automated On-demand Pull Request Environments:** For more rapid QA and stakeholder engagement.

- **Automated Deployments**: Triggered merges or tags that push code to dev, staging, or production environments.

  

#### 2.3.1 Typical Pipeline Workflows

1. ###### Infrastructure Pipeline
  
   - Watches for changes in the infrastructure repository.
   - Uses CloudFormation, Ansible, or Terraform to build and configure environments (development, staging, production).
   - Automates patching, user management, and environment versioning.
2. ###### Drupal/Application Pipeline
  
   - Watches for commits/merge requests in the application code repository.
     1. Runs tests (unit, functional, accessibility, etc.) on a build server or container.
     2. Builds an environment visible to QA personnel and stakeholders.
   - Upon merge, packages the build for deployment or triggers an environment update (blue-green or rolling).
   - Automates database updates (e.g., `drush updb`) and config imports for deployment.
3. ###### Documentation Pipeline
  
   - Might generate static docs for developer onboarding or compliance (Markdown → HTML/PDF, for example).
   - Ensures that all updates to documentation are versioned and automatically published (e.g., a docs site).

**Iterative Consideration:** Early slices might only require a minimal pipeline, but as more content types or complex integrations come into play, the team can extend the pipeline for deeper security scans, performance testing, or specialized regression checks.



#### 2.3.2 Pipeline Configuration Details

1. ###### **Branch & Tag Triggers**
  
   - For example, merging into `main` or tagging a commit with `v1.0` might automatically deploy to staging.
2. ###### **Static Site Regeneration** (if decoupled)
  
   - Re-rendering static pages (e.g., Gatsby) as part of the pipeline.
3. ###### **Smoke Tests & Rollback**
  
   - Automatic checks for environment health and immediate rollback if a deployment fails.

##### Deliverables

- CI/CD pipelines for infrastructure and application code

- Automated tests integrated into each pipeline stage

- Tag/branch strategy for environment deployments

- Smoke-testing and rollback strategy

  

### 2.4 Establish an Integrated Testing Framework

As part of the CI/CD setup, the team implements a **testing framework** that covers both **platform-level** and **application-level** tests. This ensures that each slice’s features are robust, secure, and accessible.



#### 2.4.1 Platform Tests

- **Baseline & STIG Compliance**: Tools like OpenSCAP, ZAP, or similar.

- **Load & Performance Tests**: Confirm the environment can handle anticipated traffic.

- **Security Vulnerability Scans**: Regularly check for OS, server, or library vulnerabilities.

  

#### 2.4.2 Application Tests

- **Unit Tests**: Validate Drupal modules, custom code, or transformations.
- **Functional Tests**: Ensure that user-facing forms, workflows, and permissions behave correctly.
- **End-to-End (E2E) Tests**: Tools like Cypress, Behat, or Selenium to simulate real user journeys (e.g., searching, editing, logging in).
- **Visual Regression Tests**: Tools like Backstop.js to catch unexpected UI changes.
- **Accessibility Tests**: Automated scans (pa11y, axe) plus manual checks to verify 508/WCAG compliance.

**Refining Over Time:** Each new slice might introduce new content types, user flows, or specialized integrations requiring additional test coverage (e.g., new form fields, advanced search facets, or more complex data transformations).

##### Deliverables

- Documented test strategy covering platform and application

- Automated test suites running in CI/CD for each commit or merge

- Accessibility baseline tests (WCAG 2.x, etc.)

- Defined approach for manual regression and acceptance testing

  

### 2.5 Ongoing Security and Compliance

**Security** is a continuous process, especially for high-visibility government websites. Once the first slice is under development, relevant security and compliance workflows should be in place.

- **Security Controls Documentation**: Identify which NIST or other controls are relevant (e.g., FedRAMP moderate).
- **Vulnerability Management**: Ongoing scans for new threats, patching schedules for OS/PHP/Drupal modules, continuous monitoring.
- **Incident Response**: Clear runbooks describing steps if an intrusion or outage is detected.
- **Provisional Authority to Operate (ATO)**: For government agencies, begin drafting or updating the ATO package in parallel with development.
- **Role-Based Access Controls**: Align with the user management scheme for editors, admins, and dev team members.

**Refining Over Time:** Each additional slice might add new data classifications or require distinct access restrictions, prompting updates to the security documentation or additional approval steps for compliance (e.g., revising the ATO scope).

---

### 2.6 Slice-by-Slice Scaffolding Refinement

Although the above steps describe a “foundational setup,” in practice the scaffolding is **iterative** and may evolve as each new slice is tackled. For instance:

1. **Second Slice** might introduce a unique migration pipeline, requiring additional automation scripts.
2. **Third Slice** might handle secure user submissions, prompting new end-to-end encryption or form testing.
3. **Fourth Slice** might require an additional subdomain or separate environment, refining the infrastructure code.

At each iteration, the **DevOps, QA, and Security** practices above are revisited and enhanced.



### 2.7 Deliverables Summary (Section 2)

By the time the _first_ slice is ready to begin detailed feature development, you should have:

1. ###### Repositories
  
   - Infrastructure (with environment definitions)
   - Application (Drupal code + front-end assets)
   - Documentation (system design, security, ATO)
2. ###### Hosting & Dev Environment
  
   - FedRAMP-approved cloud or equivalent
   - Local dev sandboxes (Docker or VM-based)
   - Backup, snapshot, DR processes
3. ###### CI/CD Pipelines
  
   - Automated On-demand Pull Request environments
   - Automatic build, test, deploy for each code push
   - Infrastructure pipeline for environment updates
   - Documentation pipeline if needed
4. ###### Integrated Testing Framework
  
   - Automated tests (unit, functional, accessibility, performance)
   - Security/vulnerability scans
   - Rollback procedures and smoke tests
5. ###### Security & Compliance Setup
  
   - Security controls & scanning schedule
   - Role-based access architecture
   - Early ATO or compliance documentation (if relevant)

These core **scaffolding elements** ensure that each _incremental slice of site functionality_ (whether it is a new content type, a complex form, or a new department’s section) can be developed, tested, and deployed **quickly and reliably** without compromising quality or security.



## Continuous and Overarching Activities

Although the migration proceeds in **iterative slices**, certain activities must be conducted **continuously** and **across all slices** to ensure that quality, security, accessibility, and user needs are addressed throughout the entire project life cycle. These activities include:

### 1. Security and Compliance

1. ###### Security Scanning & Hardening
  
   - Each slice follows the same baseline security scanning before being deployed.
   - Software Bill of Materials (SBOM) scanners (e.g. Syft or Trivy), web application scanners (e.g. OWASP ZAP), automated Security Technical Implementation Guideline (STIG) checks identify vulnerabilities early.
   - The team updates the environment’s Ansible/CloudFormation scripts to apply necessary patches.
2. ###### Authority to Operate (ATO) Process
  
   - For U.S. government sites, a Provisional Authority to Operate (P-ATO) may be pursued early, and refined into a full ATO as slices approach production quality.
   - Security documentation (System Security Plan, contingency plans, etc.) is updated incrementally as new functionality is introduced with each slice.
3. ###### Access Controls & Permissions
  
   - As new slices bring in new user roles or content workflows, permission structures are continuously audited to maintain **least privilege** principles and ensure compliance (e.g., FedRAMP, FISMA).
4. ###### Data Protection & Backups
  
   - Regular backups (hourly or daily snapshots) are maintained in secure, redundant storage.
   - Disaster recovery playbooks are updated to reflect the newly integrated slices.
   - Incident response procedures are documented, practiced and reviewed.

### 2. Ongoing User Research & Experience Design

1. ###### User Testing and Feedback
  
   - For each new slice, user research specialists and UX designers conduct interviews, usability tests, and gather analytics on real usage.
   - Feedback loops are short: design changes or new features are prototyped in the next sprint.
2. ###### Accessibility Reviews
  
   - Including accessibility review and testing in the design process (e.g. Figma, Storybook/PatternLab) so that errors are caught earlier in the design phase.
3. ###### Information Architecture (IA) and Content Strategy
  
   - With each new slice, content strategists refine navigational structures, taxonomies, and cross-links to ensure a cohesive experience and a forward-looking information architecture.
   - The team continually looks for ways to optimize SEO, site performance, and user workflows.
4. ###### Design Libraries and Theming
  
   - Reusable design patterns (e.g., USWDS components) and style guides are updated in real time, ensuring the site evolves consistently across slices.
   - If a design library (PatternLab, Storybook) is used, new slice-specific components are added there for consistency and future reuse.

### 3. Continuous Quality Assurance and Automated Testing

1. ###### Automated Testing Framework
  
   - Unit, functional, end-to-end (E2E), accessibility, visual regression, and performance tests run on every merge or pull request.
   - For each new slice, test suites expand to include newly created content types, configurations, or workflows.
   - Automated accessibility tests (e.g., Axe) are built into the CI/CD pipeline, supplemented by manual testing from an accessibility specialist.
2. ###### Regression Testing
  
   - As new functionality is introduced, the QA team verifies no regression in previously launched slices.
   - Smoke tests ensure critical features (e.g., authentication, main navigation, search) remain stable.
3. ###### Performance and Load Testing
  
   - Periodically, the team conducts load tests or stress tests to verify that newly introduced slices maintain expected performance.
   - Any necessary optimizations (e.g., caching, database indexing) are made proactively.
   - Monitoring front-end performance (e.g. using Unlighthouse)
4. ###### Continuous Integration / Continuous Delivery (CI/CD)
  
   - The DevSecOps pipeline remains central to how code is built, tested, scanned, and deployed.
   - If new infrastructure or modules are required by a slice, the pipeline is updated so that future slices automatically benefit from the refinements.

### 4. Documentation and Knowledge Transfer

1. ###### Developer & Admin Documentation
  
   - Each slice introduces or modifies code. Corresponding developer docs are updated in the repository.
   - Infrastructure-as-code scripts (CloudFormation, Ansible, Terraform) are documented so onboarding new DevOps engineers is straightforward.
   - Contributions to relevant open source communities, e.g. Drupal.org.
2. ###### Site Editor Training Materials
  
   - As new slices add content types or editorial workflows, training materials and style guides are updated to help content editors adopt new features.
   - Help systems embedded in Drupal (e.g., contextual help, user guides) grow with each slice’s launch.
3. ###### Change Logs and Release Notes
  
   - Every sprint or release cycle includes a summary of changes, known issues, and instructions for stakeholders.
   - This transparency ensures that product owners and other agency stakeholders remain informed about progress and potential impacts.

### 5. Continuous Feedback and Planning for Next Slices

1. ###### Stakeholder Collaboration
  
   - Stakeholders (including product owners, content owners, security teams) participate in sprint reviews for each slice, providing feedback to guide prioritization.
   
2. ###### Backlog Grooming
  
   - Newly discovered requirements or improvement ideas from the ongoing slices are documented, estimated, and put into the product backlog for future slices.
   
3. ###### Retrospectives and tracking lessons learned
  
   - The team meets regularly to discuss what went well, what can be improved, and how to adjust the approach in upcoming iterations.
   
   - The team maintains a record of project-specific lessons learned as well as documenting findings that may lead to new best practices.
   
     

## Final Full Launch and Decommissioning Legacy Systems

Because this migration is approached **slice-by-slice**, the “final launch” is less of a single event and more of a culmination of partial (and overlapping) cutovers. However, once **all major content slices** are successfully running on Drupal and the old site has little or no content remaining, the team can orchestrate the final cutover and full decommissioning:

1. ###### Confirm Completion of All High-Priority Slices
  
   - The team and stakeholders verify that all required content types and site sections have been migrated through a formal content acceptance testing process.
   - Any non-critical or archival content still on the legacy site is either migrated, archived, or intentionally retired.
   
2. ###### Plan the Final Cutover
  
   - While many slices may already be live in production, a formal “all-systems go” sign-off ensures no mission-critical content remains on the old site.
   - DNS or proxy rules that partially directed traffic to the old site are removed or reconfigured, funneling all users to the new Drupal system.
   
3. ###### Schedule a “Last Synch”
  
   - If there is still a need for content synchronization (e.g., editorial changes in the old site), the team schedules a final migration run.
   - This ensures the latest updates are present in the new environment before the old environment is taken down.
   
4. ###### Decommission the Legacy Site
  
   - The old site may remain accessible in a read-only or private capacity for several weeks/months to ensure no critical data is lost.
   - Eventually, the old infrastructure is fully deprovisioned (servers shut down, hosting accounts closed) once it is confirmed that all content and functionality exist on the new platform.
   
5. ###### Post-Cutover Validation
  
   - The team conducts thorough smoke tests and automated scans to confirm the site is stable, secure, and fully functional.
   - They monitor user feedback closely, as real users may uncover hidden legacy references or unexpected data issues.
   - A comparative performance, accessibility, SEO review is completed (e.g. with Unlighthouse and/or Oobee) to verify that performance in these areas has been sustained or improved relative to the legacy site..
   
6. ###### Finalize ATO and Compliance Documentation
  
   - If a Provisional ATO was in place, the final environment with all slices is documented for a full ATO.
   - Security checklists, vulnerability scans, and compliance attestations are updated one last time to reflect the final production state.
   
7. ###### Celebrate and Move into Operations & Maintenance
  
   - Once the entire site is considered stable, the project transitions to a maintenance or sustainment phase.
   
   - Any future enhancements or new features are planned using the same Agile approach, but the large “migration project” is declared complete.
   
     

## Quality Assurance Surveillance Plan / Schedule of Deliverables

The **Quality Assurance Surveillance Plan (QASP)** outlines how deliverables are tracked, validated, and approved across **all slices** of the Drupal migration project. Below is a **high-level schedule** and **checklist** that can be adapted to each iteration:

1. ###### Initial Setup & Discovery Deliverables
  
   - **Project Scaffolding including: Governance, Team Charter, Roles/Responsibilities artifacts**
   - **Access and Environment Setup**
   - **Preliminary Roadmap** for slices
   - **Discovery Artifacts** (initial content inventory, user research findings, infrastructure discovery)
   
2. ###### Slice Deliverables
  
   - **Slice-Level Discovery**
     - Refined backlog items (user stories, acceptance criteria)
     - Updated design comps, wireframes, or prototypes
     - Security and compliance considerations for that slice
   - **Slice Development**
     - Updated Drupal configurations (content types, workflows)
     - Theming and UI components (USWDS integration)
     - Automation scripts for any new or changed infrastructure
     - Updated QA tests (unit, functional, accessibility, performance)
   - **Slice Migration and Testing**
     - Slice migration and dependency migrations created.
     - Data mapping, sample migration runs, and validated import results on lower environments.
     - Accessibility compliance checks (manual + automated)
     - Performance checks (load tests if relevant for that slice)
     - Security scans (ZAP, OpenSCAP)
     - Editorial team performs any post migration content cleanup.
   - **Slice Beta Launch**
     - UAT feedback from stakeholders and end-users
     - Resolved critical and high-priority defects
     - Updates to user guides or editorial documentation
     - Partial cutover (web proxy or load balancer rules for that slice/path)
   - **Slice Acceptance**
     - Sign-off from product owners and relevant stakeholders
     - Slice is fully operational in Production
     - Retrospective on lessons learned, improvements for next slice
   
3. ###### Overarching Deliverables (Continuous & Incremental)
  
   - **CI/CD Pipeline** Setup and Refinement
   - **Security & Compliance** Documentation (SSP, STIG reports, etc.)
   - **System Backups & DR Strategy** Confirmation
   - **Ongoing Accessibility Testing** and Remediation Reports
   - **Analytics & Metrics** dashboards, usage reports
   
4. ###### Final Cutover and Decommissioning Deliverables
  
   - **Cutover Checklists** (covering final proxy/balancer updates, final synchronization, user communication)
   
   - **Decommissioning Plan** for the legacy system (timeline, rollback procedures if needed)
   
   - **Final ATO or Full Security Authorization** for the new site environment
   
   - **Project Close-Out** (lessons learned, final documentation, archived content logs)
   
     

### QASP Methods and Metrics

1. ###### Performance Standards
  
   - **Timeliness**: Each slice completes within the agreed-upon sprint or release cadence, unless blocked or reprioritized with stakeholder approval.
   - **Quality**: User stories meet acceptance criteria; no _high-severity_ defects remain open.
   - **Compliance**: All code merges pass security scans, accessibility tests, and automated test suites.
   
2. ###### Monitoring & Inspection
  
   - **Sprint Reviews** and **Retrospectives** track progress, surface risks, and gather stakeholder feedback.
   - **Automated CI/CD Reports** highlight coverage metrics and test pass/fail states.
   - **Issue Tracking and Burn-Down Charts** show backlog progress.
   
3. ###### Acceptance Criteria
  
   - Defined per user story, ensuring clarity for each feature or content type.
   
   - Formal sign-off from product owners on each slice once acceptance tests are passed.
   
     

## Summary

Using an **Agile, slice-by-slice** methodology allows teams to deliver immediate value, gather real-world user feedback, and iteratively build a robust Drupal solution. Each slice undergoes its own discovery, build, and release cycle, leveraging and improving shared scaffolding. Over time, the entire legacy site is replaced with minimal disruption and continuous improvement.

All the technical details—from code repositories, CI/CD automation, theming with USWDS, rigorous testing for Section 508/WCAG compliance, content modeling, to final environment cutover—remain essential, but are **applied repeatedly in smaller increments** rather than in a singular, monolithic waterfall.

This approach is **flexible, reduces risk, and aligns with modern digital service best practices** for large-scale Drupal migrations.