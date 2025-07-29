# **Open Source Procurement FAQ**

This FAQ addresses common concerns procurement officers may encounter when evaluating or acquiring open source software (OSS) as part of digital government projects. It is intended to reduce confusion, debunk myths, and support compliant, confident OSS adoption.

---

## **Why does Open Source Software Matter for Procurement?**

Open source software provides procurement and contracting officers with greater flexibility, cost control, and long-term sustainability. It allows agencies to:

* **Avoid vendor lock-in:** Agencies retain full access to code and can switch vendors who fail to deliver quality services.  
* **Increase transparency:** Codebases can be independent reviewed for quality, security, and compliance with the contract.  
* **Enable reuse, rationalization and collaboration:** Common problems which are identified in one contract can be fixed in others.  
* **Strengthen market competition:** Vendors compete on service, not ownership of code.  
* **Reduce costs over time:** No licensing fees, simpler legal issues and less duplication.

These attributes align with principles of good governance, including accountability, modular design, and maximizing taxpayer value.

---

## **Can I get support for OSS?**

Yes. Open source does not mean unsupported. Many OSS projects have robust commercial ecosystems, offering support contracts, SLAs, integration services, and managed hosting. Agencies can procure OSS with support just like commercial software.

Example: Drupal, Red Hat, WordPress, GitLab, and many other vendors offer enterprise-grade support for a wide range of open source tools.

---

## **Can I mandate an OSS license?**

Yes, under specific conditions. Government agencies may require that custom-developed software produced under contract be released under an [Open Source Initiative (OSI)-approved license](https://opensource.org/licenses) (e.g., GPLv3, MIT, and Apache 2.0). This is consistent with the US [SHARE IT Act](https://dsacms.github.io/share-it-act-lp/) and [OMB M-16-21](https://obamawhitehouse.archives.gov/sites/default/files/omb/memoranda/2016/m_16_21.pdf).

However, you may not mandate that off-the-shelf software be open source, unless there's a clear and justified policy reason.

---

## **Can OSS be considered Commercial Off-the-Shelf (COTS)?**

Yes, under specific conditions. The U.S. government, including the Department of Defense, classifies commercially supported open source software as **commercial software** and is included in the definition of **COTS** (commercial off-the-shelf) when it is:

* Available to the public without custom development,  
* Offered under standard commercial terms (like OSI-approved licenses), and  
* Supported by a vendor or community.

This means that OSS can be procured just like any other commercial software, as long as it meets the functional and legal requirements of the agency. Federal Acquisition Regulation (FAR) Part [12.212](https://www.acquisition.gov/far/12.212) and [39.101](https://www.acquisition.gov/far/39.101) allow OSS to be treated as COTS software. OSS must be evaluated based on functionality, performance, security, and licensing terms—on equal footing with proprietary offerings.

---

## **What if a vendor wants to retain IP?**

Digital agencies can still require source code rights. Vendors may retain copyright (IP), but agencies can require that the software be delivered with a free and open source license that grants the government full rights to use, modify, and redistribute the software.

The key is to include license terms and deliverables in the contract, not just rely on ownership language.

---

## **Is GitHub / GitLab code safe to use?**

It depends. [GitHub](https://github.com/) and [GitLab](https://gitlab.com/) are hosting platforms, mostly for code. They are not a guarantee of quality. Before using code from an open repository:

* Check the license and confirm it's OSI-approved.  
* Review the repository’s update history, issues, community-submitted changes or problem reports. Contact your Open Source Program Office (OSPO) if you have questions.   
* Avoid using unmaintained or unaudited code in production.


For production systems, **use only actively maintained and trusted sources**, ideally through trusted source or official software registry.

---

## **How do I ensure security and patching?**

Use the same diligence as with proprietary software:

* Request a [Software Bill of Materials (SBOM)](https://www.cisa.gov/sbom) — much like a list of ingredients in a product label — listing all OSS components.  
* Ensure vendors commit to and routinely report on patching known vulnerabilities.  
* Assess community activity: more active OSS projects often patch faster than proprietary ones.  
* Align with [Critical Infrastructure Security and Resilience (CISA)](https://www.cisa.gov/) and [Open Source Security Foundation (OpenSSF)](https://openssf.org/) guidance on secure OSS consumption.  
* Good transparency leads to better security culture and maintenance of good practices.

---

**Purpose:** This FAQ should be embedded in LMS courses, linked from procurement templates, and offered in internal wikis or toolkits to empower digital acquisition teams with accurate, non-alarmist guidance on open source use.

## **Resources**

* Open Source Initiative (OSI)-approved license \- https://opensource.org/licenses  
* SHARE IT Act \- https://dsacms.github.io/share-it-act-lp  
* OMB M-16-21 \- https://obamawhitehouse.archives.gov/sites/default/files/omb/memoranda/2016/m\_16\_21.pdf  
* Federal Acquisition Regulation (FAR) Part 12.212 \- https://www.acquisition.gov/far/12.212  
* Federal Acquisition Regulation (FAR) Part 39.101 \- https://www.acquisition.gov/far/39.101  
* GitHub \- https://github.com  
* GitLab \- https://gitlab.com/  
* Critical Infrastructure Security and Resilience (CISA) \- https://www.cisa.gov  
* Open Source Security Foundation (OpenSSF) \- https://openssf.org/  
* Software Bill of Materials (SBOM) \- https://www.cisa.gov/sbom
