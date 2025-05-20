### _Open Requirements_

# Consolidating Web Properties with AI into Drupal

_License & Copyright: The materials herein are all © 2025 CivicActions_

_Creative Commons License:_ _This work is licensed under a_ _Creative_ _Commons_ [_Attribution-ShareAlike 4.0 International_](https://creativecommons.org/licenses/by-sa/4.0/deed.en)

## About the Open Requirements Library

The purpose of the Open Requirements Library is to utilize open and emerging technology to contribute to a more equitable government marketplace—one where solicitations are more easily understood and require less time in the acquisition life cycle.

**Key performance results:**

- Fewer submitted solicitation questions
- Fewer pre-award protests
- Faster acquisition cycles
- Create a more inviting marketplace to new entrants
- Reduce dependency on input from incumbent vendors

Read more about the [Open Requirements Library](https://docs.google.com/document/d/1OYrxJp5LaZMRSFltmnwvS2BpcRwnkDY3not6ELjH2M0/edit#heading=h.hblvjympznf4), and contribute your ideas.

### How may you use the Open Requirements for Consolidating Web Properties with AI into Drupal?

The requirements listed within this document are intended to be a comprehensive, yet “white-labeled,” description of actions required to  _multiple_ sites across the enterprise into a single Drupal site. The expectation is that a person (for example, a program office for a government agency) could copy/paste these requirements into a draft solicitation for vendor support. Then, the user could customize requirements where and how they see fit. The program office can collect and learn best practices for web-consolidation initiatives during this process. Efficiency, integrity, and quality increase as the user doesn't have to start from scratch, ask an incumbent vendor for the content baseline, or copy/paste from a previous (potentially flawed) solicitation.

Additionally, vendors providing web consolidation services are welcome to learn, contribute to and prepare for best practices.

Anyone can contribute to the Open Requirements for Consolidating Web Properties with AI into Drupal. Contributions will be reviewed for their positive impact on improving the efficiency, integrity, and quality of requirements.

## 1 Purpose & Scope

This requirements template supports solicitations aimed at merging _multiple_ sites across the enterprise into a **single, already‑live Drupal instance**. The purpose of this is typically **cost savings** through decommissioning and efficiencies gained from a **streamlined enterprise-wide content management platform**. The focus is on **efficient content discovery and migration**—not on building a new site. Key outcomes include:

- Comprehensive inventory of every retiring site’s information architecture.
- AI‑assisted identification of Drupal content‑types, fields and metadata.
- Programmatic import of pages and page assets from a source site as **draft content** for editorial review.
- Consolidation of dynamic digital service front-ends onto the central Drupal platform where feasible.
- Incremental, low‑risk delivery using an **Agile slice‑by‑slice approach** (one source site per slice).

## 2 How to Use this Document

- **Copy/Paste Ready** – Sections may be inserted directly into an RFP, SOW or internal charter.
- **Tailor Variables** – Replace placeholders for agency name, timelines, approval gates, and security posture.
- **Keep Outcomes Front‑of‑Mind** – Requirements emphasize _what_ must be achieved, leaving vendors flexibility in _how_ they deliver.
- **Technical Implementation Reference** (Section 10) provides one example of tools and commands; agencies may accept or substitute equivalents.

## 3 Assumptions & Preconditions

1. The destination Drupal site is operational with standard CI/CD, theming and editorial workflow.
2. Source websites run on varied platforms (static HTML, WordPress, SharePoint, custom CMS, etc.).
3. Initial migration prioritizes moving content to the destination Drupal site with minimal changes to structure or presentation. Major visual redesign or significant information architecture overhaul is typically out of scope for the initial migration but can be addressed iteratively post-consolidation.
4. Work is delivered in two‑week sprints under an Agile framework.
5. The contracting agency permits the use of artificial‑intelligence tooling, subject to privacy and security review.
6. Drupal’s core migration APIs (or equivalent, industry‑standard migration framework) will be used to import content.
7. Existing DevSecOps and hosting baselines remain in force. Migration code integrates with—not replaces—those controls.

## 4 Project Roles (Minimum)

- **Program Manager / Contract Manager**
- **Project Manager / Scrum Master**
- **Product Manager**
- **Technical Lead / Site Architect**
- **Back-End / Migration Engineer**
- **Front-End Engineer**
- **Quality‑Assurance & Accessibility Engineer**
- **Content Strategist / Service Designer**
- **DevOps Engineer**

## 5 Best‑Practice Agile Consolidation Methodology

### Overview

Migrations are made agile by migrating in **slices** \- each slice is a distinct website, sub‑site or discrete set of content (depending on size) that progresses through six phases over the course of one or more agile sprints. Completion of a slice results in the source site/section being decommissioned or redirected to Drupal, yielding immediate cost savings and governance simplification. While each migration should maintain or improve the editorial and user experience, the emphasis is on moving first, then following up with ongoing iterative UX/design enhancements.

### 5.1 Inception (Project‑Wide – once)

- **Proof of Concept Crawl**: Perform a small‑scale automated crawl on one source site to demonstrate ability to inventory pages, media assets and link structure.
- **Proof of Concept AI Mapping**: Feed crawl results into a large‑language model to generate a proposed set of Drupal content‑types and field structures.
- **AI Governance Framework**: Detail the planned AI usage, including data masking procedures, confidence measurement methods, and mandatory human-in-the-loop checkpoints. Explicitly define human oversight at every AI stage, from initial audits and content mapping to transformation and QA, ensuring stakeholder validation and adherence to editorial and accessibility standards.
- **Baseline Documentation**: Establish a single source of truth for content models, migration guidelines and acceptance criteria.

### 5.2 Slice Discovery (Repeated per Source Site)

**Outcome of this phase — a definitive list of migration _slices_ for the source site**:

- For **large or complex** source websites, discovery typically breaks the site into several logical slices (for example, program areas, content archetypes, or high‑level URL paths). **Each slice will then progress independently through AI‑Enabled Migration (5.4) and Quality Assurance & Launch (5.5)** in its own sprint or set of sprints.
- For **small or uncomplicated** sites, the discovery effort may conclude that the entire site can be migrated in a single slice, allowing steps 5.4 and 5.5 to be executed once without further subdivision.

The contractor shall perform the following discovery activities and deliverables for every source site:

1. **Comprehensive Automated Crawl**: Produce a full inventory of URLs, metadata and internal link structure for the source site.
2. **Data Refinement**: Remove duplicate URLs, filter out irrelevant file types, and prioritise pages by traffic or business value.
3. **AI‑Assisted Content Mapping**: Use language‑model analysis to group pages into logical archetypes (e.g., articles, press releases, event listings) and to suggest corresponding Drupal content‑types and field lists, as well as to identify potential patterns, content relationships, and areas with potentially complex or dynamic content requiring special attention.
4. **Human Review Workshop**: Content strategists and stakeholders validate or adjust the AI recommendations, ensuring alignment with user, agency, policy and regulatory needs, editorial standards and information architecture.
5. **Signed‑Off Mapping Package**: Produce an approved content‑type mapping, redirect plan, and backlog of user stories for each resulting slice.

### 5.3 Destination Configuration (Per Slice)

- **Content‑Type & Field Updates**: Add any missing fields, taxonomies, or view modes to the existing Drupal site while maintaining backward compatibility.
- **Navigation & URL Strategy**: Pre‑configure menu links and SEO‑friendly path patterns for incoming content.
- **Redirect Framework**: Prepare a mapping of source URLs to their future Drupal locations to ensure uninterrupted user journeys and search‑engine ranking.
- **Editor Training & Feedback**: Train editors on the new editorial experience for operational readiness post-migration and gather feedback for minor content structure refinements (field descriptions, order, etc.).

### 5.4 AI‑Enabled Migration (Per Slice)

- **Extract**: Obtain source content through available export mechanisms or automated scraping when no export exists.
- **Transform**: Apply AI models to convert raw HTML or data exports into structured records that match the approved content‑type schema, enriching metadata (e.g., alt‑text, tags) and initial HTML cleanup where feasible.
- **Load**: Import structured records into Drupal as **draft** items, tagged with metadata indicating their origin for traceability.
- **Review Environment**: Deploy an isolated preview of the imported content so editors and stakeholders can perform acceptance testing without impacting production.

### 5.5 Quality Assurance & Launch (Per Slice)

- **Automated Validation**: Run a suite of tests covering broken links, accessibility, performance, and security.
- **Editorial Spot‑Checks**: Human reviewers compare a sample of migrated pages against the source to confirm fidelity of content and layout.
- **Acceptance Gate**: The slice passes when agreed‑upon quality thresholds are met (see QASP), and editorial sign‑off is obtained.
- **Go‑Live Activities**: Activate redirects, clear caches/CDN, and monitor error logs and analytics for anomalies during the first 48 hours.
- **Decommissioning:** Decommissioning support for the old site can include redirects to avoid unintentional usage, generating agency and NARA-compliant archives and progressively winding down infrastructure/services.

### 5.6 Retrospective & Continuous Improvement

- Capture lessons learned, update AI prompts and migration playbooks, and adjust velocity forecasts before commencing the next slice.

## 6 Continuous Cross‑Slice Activities

- **Security & Compliance**: Ongoing vulnerability scans, least‑privilege reviews, and updates to Authority‑to‑Operate (ATO) documentation.
- **Accessibility**: Continuous automated and manual WCAG testing; AI‑generated alt‑text reviewed by accessibility specialists.
- **Analytics & SEO**: Track redirect coverage and search‑traffic trends to ensure no degradation.
- **Knowledge Management**: Maintain a living playbook of migration standards, AI prompt templates and editorial guidelines.
- **Continuous Migration:** Migration activities themselves will be continuous to reflect content updates.

## 7 Ongoing Incremental Improvement

This will depend on the needs of each site:

- At a minimum there needs to be defined channels for tracking bug reports from editors and users, responding to issues identified as part of operations (log issues) and keeping up with standard security and framework updates.
- There is also potential for more comprehensive user research leading to content structure and design improvements where warranted. This can be accomplished in-situ after the site is migrated, for example by using the [Beta Site](https://www.drupal.org/project/betasite) module.

## 8 Quality Assurance Surveillance Plan / Schedule of Deliverables

The **Quality Assurance Surveillance Plan (QASP)** details deliverable tracking, validation, and approval for **all slices** of the AI-assisted Drupal consolidation. This **high-level schedule** and **checklist** adapt to each iteration:

1. ###### **Project Inception & Foundation Deliverables**

   - **Proof of Concept (Crawl & AI Mapping) Reports**
   - **AI Governance Framework** (detailing AI usage, data masking, human oversight, validation)
   - **Baseline Documentation** (Content Models, Migration Guidelines, Initial Acceptance Criteria)

2. ###### **Per-Slice Deliverables**

   - **Slice Discovery & Planning**
     - **Source Site Inventory & Prioritized Migration Scope**
     - **Validated AI Content Mapping Proposal** (AI suggestions refined by human review)
     - **Signed-Off Mapping Package** (Approved Mappings, Redirect Plan, User Stories)
   - **Slice Destination Configuration**
     - **Drupal Destination Configuration** (Content Types, Fields, Taxonomies, URLs, Redirects)
     - **Editor Training Materials & Feedback Summary**
   - **Slice AI-Enabled Migration & Review**
     - **Transformed Content Records** (AI-converted, structured content as Drupal drafts)
     - **Deployed Review Environment** with migrated slice content
   - **Slice Quality Assurance & Launch**
     - **QA Test Results** (Automated: links, accessibility, performance, security; Manual: editorial spot-checks)
     - **Slice Acceptance Sign-Off** (Product Owner & Stakeholders)
     - **Go-Live Confirmation** & initial monitoring summary

3. ###### **Continuous & Overarching Deliverables**

   - **Updated Security, Compliance & Accessibility Documentation/Reports**
   - **Analytics & SEO Monitoring Reports**
   - **Knowledge Management Playbook Updates** (Standards, AI Prompts)
   - **Retrospective Summaries & Action Items**; Issue Resolution Logs

### QASP Methods and Metrics

1. ###### **Performance Standards**

   - **Timeliness**: Slices adhere to agreed sprint cadence; project roadmap milestones met.
   - **Quality**: Content fidelity confirmed; user stories meet acceptance criteria; no critical/high defects at launch; AI outputs validated by humans per **AI Governance Framework**.
   - **Compliance**: Adherence to **AI Governance Framework**, DevSecOps baselines, and WCAG 2.1 AA.

2. ###### **Monitoring & Inspection**

   - **Agile Ceremonies**: Sprint reviews/retrospectives for progress tracking and feedback.
   - **AI Governance Checkpoints**: Mandatory human review of AI-generated outputs.
   - **Automated & Manual Testing**: CI/CD test suites and human QA (editorial, accessibility) in review environments.
   - **Issue Tracking**: Centralized logging and monitoring of defects and tasks.
   - **Post-Launch Monitoring**: Initial 48-hour monitoring post-slice go-live.

3. ###### **Acceptance Criteria**

   - Defined per user story in the **Signed-Off Mapping Package**.
   - Successful completion of all automated and manual QA tests meeting defined thresholds.
   - Formal sign-off on each slice by Product Owner and key stakeholders.
   - Confirmation of operational slice in production with correct redirects.

## 9 Glossary (Selected)

- **Slice**: A discrete source website, sub‑site or section of content migrated as a unit.
- **AI Mapping**: The process of using language models to propose how source site pages translate into Drupal content‑types.
- **ETL**: Extract, Transform, Load workflow that moves content from source site systems into Drupal.
- **Draft Node**: An unpublished Drupal content item awaiting editorial approval.
- **Review Environment**: A temporary site clone where imported content can be tested safely.

## 10 Technical Implementation Reference

_(Informative – vendors may propose equivalent toolsets. Remove or replace if not required in the solicitation.)_

The following pages consolidate detailed examples of tooling, command‑line sequences, AI prompt templates, and file‑naming conventions that a vendor **might** use to satisfy the outcomes described above. Use of these specific technologies is **not mandatory** but illustrates one proven approach.

### 10.1 Sample Toolchain Overview

- Interactive web crawlers (e.g., Screaming Frog with API access for AI processing) for interactive site auditing and prompt iteration.
- Automated crawler capable of exporting URL inventories in CSV or JSON.
- Scripting language (e.g., Python) for data cleanup and orchestration.
- Large‑language model (commercial or open‑source) accessible via API for classification and transformation tasks.
- Drupal migration framework (core Migrate API plus AI integration & mapping configuration).
- Continuous‑integration system that can stand up disposable review environments, execute tests, and deploy content.

### 10.2 Excerpt: AI Prompt Template (Information‑Architecture Classification)

```
SYSTEM: You are an information‑architecture analyst. For each input URL provide: {url, archetype, recommended_content_type, suggested_fields[], confidence_score}.
```

### 10.3 Excerpt: AI Prompt Template (HTML to Structured Record)

```
SYSTEM: Convert the supplied HTML into JSON that matches the approved content‑type schema. Provide values for title, body, media, tags, publication_date.
```

### 10.4 Basic Drupal Migration Module Stack

- [Migrate](https://www.drupal.org/docs/core-modules-and-themes/core-modules/migrate-module): This core module provides a framework for migrating content into Drupal from various sources.
- [Migrate Plus](https://www.drupal.org/project/migrate_plus): Extends the core Migrate module with additional functionality, including support for more complex migration scenarios involving fetching data from files or HTTP and parsing XML/JSON data.
- [Migrate Source CSV](https://www.drupal.org/project/migrate_source_csv): Allows migration from CSV files. Useful for importing data from spreadsheets.
- [Migration Tools](https://www.drupal.org/project/migration_tools): Developer toolkit for custom migration classes to make migrations easier and more reliable. (Maintained by CivicActions).
- Custom development, as needed, for complex migrations using Drupal’s [Migrate API](https://www.drupal.org/docs/drupal-apis/migrate-api): Provides APIs for developers to write custom migrations and integrate with different data sources.
- [Migrate Tools](https://www.drupal.org/project/migrate_tools): Offers a user interface and Drush commands to manage migrations, making it easier to execute and control the migration process.
- [Drupal AI](https://www.drupal.org/project/ai): A set of modules and submodules providing content type creation, content creation, revision, and translation to assist in site migration efficiency and post-migration content support.

### 10.5 Illustrative Acceptance‑Test Suite

- Link checker ensures zero broken internal links.
- Accessibility scanner covering WCAG 2.1 AA success criteria that can be machine tested.
- Automated performance audit verifying page‑load benchmarks.
