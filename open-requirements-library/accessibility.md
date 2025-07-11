# **Open Requirements \- Section 508 Compliance for Website Maintenance and Enhancement in Public Sector Procurement**

**License & Copyright:** The materials herein are all © 2025 CivicActions

**Creative Commons License:** This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International

---

## **About the Open Requirements Library**

The purpose of the Open Requirements Library is to leverage open and emerging technology to contribute to a more equitable government marketplace—one where solicitations are more easily understood and require less time in the acquisition life cycle.

### **Key Performance Results:**

* Fewer submitted solicitation questions  
* Fewer pre-award protests  
* Faster acquisition cycles  
* Create a more inviting marketplace for new entrants  
* Reduce dependency on incumbent vendors

Read more about the [Open Requirements Library](https://github.com/civicactions/open-practice), and contribute your ideas.

---

## **How to Use the Section 508 Requirements Document**

The requirements outlined in this document provide a **comprehensive, vendor-agnostic** framework for integrating accessibility into government procurements. A contracting officer can **copy and paste** these requirements into a draft solicitation for vendor support, then **customize them** based on agency needs. This ensures a consistent and well-defined approach to accessibility requirements.

By utilizing this document, procurement officers and program managers can:
* Establish clear accessibility expectations from the outset of a project.  
* Reduce post-award disputes related to accessibility compliance.  
* Ensure compliance with **Section 508 of the Rehabilitation Act** and **WCAG 2.2 Level AA** standards.  
* Improve usability, inclusivity, and long-term sustainability of digital services.

Additionally, vendors providing digital services to the U.S. government are encouraged to **review and contribute to** these accessibility requirements, helping improve clarity and feasibility for implementation

---

## **Scope**

This document applies to the maintenance and improvement of websites and web applications that belong to federal agencies. 

---

## **Purpose of Section 508 Conformance**

[Section 508 of the Rehabilitation Act](https://www.section508.gov/manage/laws-and-policies/) (29 U.S.C. 794d), as amended in 1998, is a federal law that requires agencies to provide individuals with disabilities equal access to electronic information and data comparable to those who do not have disabilities, unless an [undue burden](https://www.section508.gov/buy/determine-ict-exceptions/#4) would be imposed on the agency. Section 508 standards set the technical requirements and criteria used to measure conformance within this law. More information on Section 508 and the associated technical standards can be found at [Section508.gov](http://Section508.gov). The Section 508 law is broad in scope, applying to all technology the federal government buys, builds, maintains, and uses. Non-compliance can result in time consuming and costly lawsuits, delayed implementation of key IT initiatives and damage to public missions or image .In addition, the Government Accountability Office (GAO) may sustain a bid protest if an agency fails to properly consider Section 508 requirements during procurement, particularly if exceptions like the “Best Meets” criteria are not adequately justified. This can force a re-competition, delaying or invalidating procurements.

---

## **Assumptions & Preconditions**

The approach below assumes an **agile, iterative** development process with accessibility embedded at every phase. Key assumptions include:

* **Agile Development Practices:** Accessibility work is integrated into the **design, development, and testing cycles** rather than being treated as an afterthought.  
* **Procurement-Driven Accessibility Planning:** Vendors are expected to submit an Accessibility Conformance Report at the proposal stage and  routinely as directed by the CO.  
* **Stakeholder Collaboration:** Decision-makers, including **accessibility subject-matter experts (SMEs)**  are actively involved.  
* **Automated and Manual Testing:** Accessibility testing is performed using open source and **automated tools** and **manual expert evaluation**.  
* **Cross-Functional Accountability:** Accessibility is a **shared responsibility** across designers, developers, content strategists, and quality assurance (QA) teams.

In addition, the contracting agency will:

* **Define accessibility standards specific to each product/service**  
  * Section 508 sets the *minimum legal standard* for government website accessibility. To ensure that a website meets and exceeds Section 508's Functional Performance Criteria (FPC), production teams should refer to the latest recommended version of the [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG22/) defined by the World Wide Web Consortium (W3C).   
  * Standards should meet *anticipated requirements over the lifespan of the project* (i.e., a website launched one year from procurement should meet the standards at time of launch). Note that Section 508 FPC are based on an early version of WCAG, version 2.0, that was published in 2008 before smartphones and responsive web design/development.   
  * Refer to the [World Wide Web Consortium (W3C)](https://www.w3.org/WAI/standards-guidelines/) for guidance on current recommendations and upcoming changes.  
  * For assistance defining which Section 508 guidelines apply to this contract, the [Accessibility Requirements Tool (ART)](https://www.section508.gov/art/#/) is an online questionnaire that determines which requirements are relevant to your product/service, with an option to copy summary language into your RFP/SOW.  
* **Define requirements for [Accessibility Conformance Reports (ACRs)](https://www.section508.gov/sell/acr/)**  
  * Which products require assessment  
  * How often an ACR should be delivered per product  
  * Which ACR template to use based on accessibility standards per product (available templates are provided with the [OpenACR Editor, on the About screen](https://acreditor.section508.gov/about))  
* **Provide access to enterprise-wide Section 508 scanning tools and associated reports, if applicable**  
  * Siteimprove  
  * LevelAccess

---

## **Project Roles in Website Accessibility Implementation**

Some roles may be combined depending on project scope and team size. 
* Project Manager  
* Accessibility Engineer / Specialist  
* User Experience (UX) Designer  
* Content Strategist / Service Designer  
* Front-End Engineer  
* Quality Assurance (QA) Engineer  
* User Research Specialist

For guidance on how to define accessibility responsibilities per role, consult the WC3's Accessibility Roles and Responsibilities Mapping (ARRM), specifically, [Roles Involved in Accessibility](https://www.w3.org/WAI/planning/arrm/roles/).

---

## **Task Requirements for Website Maintenance and Continuous Improvements**

The contractor ("Contractor") shall ensure that all task areas executed in support of the contract are compliant with Federal IT standards and requirements as defined by the contracting agency ("Agency"), and that all documents and materials delivered are Section 508 compliant. 

### **Task 1\. Project kickoff and transition-in**

1. **Kick Off Meeting.** Contractor shall schedule a kick-off meeting with the Contracting Officer's Representative (COR) within two weeks of contract award. The Contractor shall determine an agenda for the meeting and shall provide the agenda to the COR at least 48 hours in advance of the meeting. The contractor will meet with Agency stakeholders to discuss contract requirements, establish the accessibility criteria to be met by contract deliverables (Section 508 Functional Performance Criteria, and the latest WCAG recommendation), obtain necessary documentation, and meet appropriate program management staff.  
2. **Contractor Project Management Plan (CPMP).** Within 10 days of award, Contractor shall deliver a CPMP that details Contractor’s approach, timeline and tools including version designations to be used in execution of the contract. The CPMP shall be delivered in the form of both a narrative and graphic format that displays schedule, milestones, risks and resource support. CPMP shall also include how Contractor will coordinate and execute planned, routine, and ad hoc data collection reporting requests. Contractor shall update and maintain CPMP on a monthly basis throughout the Period of Performance (PoP) and, once approved by the COR, distribute final versions to the COR.  
3. **Transition plan.** The transition in period occurs at the start of this contract. The contractor shall work with the incumbent contractor, if the incumbent is not awarded the contract, to assume work during a 30-day transition-in period. At the end of the transition in period, the contractor shall deliver a transition-in status report to the COR.   
   1. Transition plan may cover, but is not limited to, handing off: ACR processes, tools, and associated accessibility evaluation results; QASP metrics and sources; and Jira ticket processes and tracking for remediation.  
4. **Quality Assurance Surveillance Plan (QASP).** See [Task 4\. Performance reporting: Quality Assurance Surveillance Plan (QASP)](#task-4.-performance-reporting:-quality-assurance-surveillance-plan-\(qasp\)).

Deliverables:
* Kickoff meeting schedule and agenda  
* Acknowledgement of Section 508 standards defined per product  
* Contractor Project Management Plan (CPMP)   
* Transition-in plan and status report  
* Quality Assurance Surveillance Plan (QASP)

### **Task 2\. Discovery and benchmarking**

1. **Performance baseline.** Within the first performance sprint (a period of time to be defined by the Agency), Contractor will establish a performance baseline:   
   1. Audit and document performance of web properties according to the Section 508 standards and guidance.  
   2. Complete an accessibility conformance report (ACR) for each digital product produced/maintained by Contractor as part of the SOW. This ACR will act as a benchmark for future reports. See ACR requirements under [Task 3\. Maintenance and continuous improvement](#task-3.-maintenance-and-continuous-improvements).  
   3. Record audit findings and ACR process in project documentation.

Deliverables:
* Benchmark ACR for each digital deliverable defined in the SOW  
* Project documentation 

### **Task 3\. Maintenance and continuous improvements** {#task-3.-maintenance-and-continuous-improvements}

1. **Design assets**  
   1. Contractor shall review and update new and edited designs to ensure conformance with accessibility standards that apply to visual and user experience (UX) features, including but not limited to color, typography, use of plain language, interactions and associated state feedback.   
2. **Website testing and code remediation.** Contractor shall:  
   1. Assign owners for responsibilities for remediation tasks, including at least one accessibility SME.  
   2. Create and document an evaluation and remediation plan to share with stakeholders that includes automated testing, manual testing, issue tracking, remediation methods, and ACR process.  
   3. Perform ongoing, regularly scheduled automated tests of pre-production code to ensure that accessibility issues and regressions are not introduced to live website code. Automated tests include but are not limited to:   
      1. Unit tests  
      2. CI pipeline testing (e.g., tests performed when code is merged to a repository/version control)  
      3. Periodic evaluations of production env  
   4. Perform manual testing with browser tools, screen reader and voice control software to ensure that accessible features in code are usable and meet expected outcomes. Manual testing must be used in conjunction with automated testing as a means of finding defects not found during automated testing and thereby providing a more robust assessment. Accessibility SMEs should define and drive this testing process, and validate others' test results. Whenever possible, disabled testers should be contracted to manually test the site for conformance and usability.  
   5. Perform both automated and manual testing on actual or simulated mobile devices to ensure that features retain accessible functionality across a variety of devices, operating systems, and viewport sizes.  
   6. Track accessibility issues by identifying and labeling Section 508 and WCAG violations in a shared, collaborative issue tracking platform like Github or Jira, and prioritize their remediation in accordance with W3C guidance.  
   7. Proactively remediate any Section 508 or WCAG violations by reviewing and editing design, and correcting code bugs as needed. Track remediation progress in the issue tracking platform.   
3. **Accessibility Conformance Reports (ACRs).** ACRs provide a standardized way to track accessibility conformance and progress against specific WCAG criteria, and should be regularly updated to reflect the current status of production (live) code.  
   1. Contractor shall produce an ACR for each product on a regular basis to be determined by the Agency (usually annually). The ACR process and report format should adhere to [ACR standards and guidelines set forth by the Section 508 office](https://www.section508.gov/sell/acr/), and utilize the [OpenACR tool](https://acreditor.section508.gov/) for creating and updating reports.  
      1. ACR results in YAML format should be stored in a secure location to be determined by the Agency, like the Agency's GitHub repository, and should be utilized and updated for creating the next round of reports.     
4. **Ad hoc reports and alerts**  
   1. Ad hoc reports may be required in response to needs of internal management or inquiries from outside requestors. Contractor shall acknowledge receipt of ad hoc inquiries in writing. During business hours, acknowledgement shall be via email within \[a period of time to be defined by the Agency\] of sending by the COR or CO; otherwise, acknowledgement shall be within three (3)  hours of the opening of the next business day (Eastern time). Contractor shall provide an Ad Hoc Report as a written response to the inquiry within three (3) business days of said inquiry.   
   2. Should the Contractor, at any time during the performance of this Contract, identify a serious risk or a requirement to deviate from the approved plans, the Contractor shall notify the COR by email using a subject line that begins with the word “ALERT:” in all capital letters. The Contractor may also telephone the COR to discuss the issue; however, the phone call (or a voicemail) shall be in addition to the ALERT email.   
      1. A serious risk would include critical accessibility barriers identified by end users, where access to content or website functionality is prohibited.

Deliverables:
* Remediation progress reports per development sprint  
* Documentation:  
  * Test plans  
  * Issue tracking and remediation methods and processes  
  * Reporting tools, methods and processes   
* Bi-weekly or monthly QASP  
* Annual ACR per product  
* Response to ad hoc reports and alerts

### **Task 4\. Performance reporting: Quality Assurance Surveillance Plan (QASP)**

A performance-based Quality Assurance Surveillance Plan (QASP) sets forth the procedures and guidance that the Agency will use in evaluating the technical performance of the contractor in accordance with the terms and conditions of the contract. The QASP will be used as a Government document to assist in monitoring contractor activities and during inspection and acceptance of contract deliverables. The Government reserves the right to make changes to this QASP during contract performance. 

The QASP describes the mechanism for documenting noteworthy accomplishments or discrepancies for work performed by the contractor. Information generated from surveillance activities will directly feed into the performance discussions with the contractor and assist CMS in its CPARS performance evaluation.

The primary goals of a QASP are to:
* Bring structure and organization to the Government’s monitoring and surveillance of key tasks/services or deliverables of contractor performance under the above contract.  
* Indicate key tasks/services or deliverables that will be assessed against established performance standards.  
* Describe the evaluation methods and processes (i.e., random sampling, etc.) that will be used by the Government during surveillance activities.  
* Document potential risk factors of concern during contract performance.  
* Guide the Government’s surveillance efforts to ensure acceptable performance by the contractor.

---

## **Resources and References**

This document aligns with federal accessibility procurement guidance, including:
* [Section 508 Standards and Assessment Criteria](https://www.section508.gov/manage/section-508-assessment/criteria-09/)  
* [Buy Accessible ICT: Section 508 Procurement](https://www.section508.gov/buy/)  
* [Government-wide Section 508 Assessment](https://www.section508.gov/manage/section-508-assessment/)  
* [Disability:INclusive Workplaces Accessible Technology Procurement Toolkit](https://disabilityin.org/procurement-toolkit/)

---

This accessibility procurement document is a **living resource** designed to evolve with best practices, legal updates, and technological advancements. Procurement officers and vendors are encouraged to **review, refine, and contribute** to ensure accessibility remains a core consideration in federal acquisitions.

For more details or to contribute, visit: **[Open Requirements Library](https://github.com/CivicActions/open-practice/)**.

