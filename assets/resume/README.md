# Nitish Hurduke - Resume Draft and Review

Status: working draft based on supplied information and the existing profile, updated November 12, 2026. Not yet application-ready: education, earlier-role ownership, and several impact claims need confirmation. No metrics, credentials, or customer counts have been invented.

Primary positioning: senior software developer with backend architecture and applied AI responsibilities. Software architect is a long-term direction, not a current job title. The draft uses official employment titles and does not imply staff-level or organization-wide architecture ownership.

## Files and Build

- [Compiled PDF](./nitish-hurduke-resume.pdf): one-page working draft.
- [LaTeX source](./nitish-hurduke-resume.tex): single-column A4 resume with standard headings, selectable text, visible contact links, and no tables, icons, or skill ratings.
- This document contains the readable resume content, review, tailoring guidance, and unanswered questions. Review notes are not part of the application resume.

Verified with Tectonic 0.15.0: compilation succeeds, the PDF extracts as one page, and expected headings and literal keywords (including MLflow) are preserved in UTF-8 text. The XeTeX font configuration disables common ligatures for keyword extraction. The compiler emits a non-fatal Fontconfig warning on this Windows environment; explicit font files allow the build to complete. The pdfLaTeX branch has not been executed here.

Compile with Tectonic:

```sh
tectonic --outdir assets/resume assets/resume/nitish-hurduke-resume.tex
pdftotext -enc UTF-8 -layout assets/resume/nitish-hurduke-resume.pdf -
```

Alternatively, compile with a TeX Live or MiKTeX installation containing the listed packages:

```sh
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=assets/resume assets/resume/nitish-hurduke-resume.tex
pdftotext -enc UTF-8 -layout assets/resume/nitish-hurduke-resume.pdf -
```

Check page count, font embedding, clipping, and extracted reading order after compilation. A one-page layout is the initial target; consider two pages only if confirmed architecture achievements and relevant education or projects justify the space. Do not shrink the text excessively to force one page.

## Resume Content

### Nitish Hurduke

**Senior Software Developer | Backend Architecture & AI Integration**

Pune, Maharashtra, India | +91 8983214817 | nitishhurduke@gmail.com  
LinkedIn: https://www.linkedin.com/in/nitishhurduke/  
GitHub: https://github.com/nitishhurduke  
Portfolio: https://portfolio.nitishhurduke.workers.dev/  
Blog: https://medium.com/@nitishhurduke

### Professional Summary

Senior software developer with 7+ years of experience in enterprise web applications, Java/Spring Boot backends, and Angular interfaces. Delivered production AI integration for Windchill PLM, including a shared LLM layer for three agents, benchmark evaluation, and CI security checks. Owns user and license validation across three MCP servers.

### Technical Skills

- **Languages:** Java 21, TypeScript, Python, SQL
- **Backend & Data:** Spring Boot, Spring Web MVC, REST APIs, PostgreSQL
- **AI Engineering:** LLM integration, Spring AI, Model Context Protocol (MCP), MCP Java SDK, MLflow, Databricks
- **Frontend & Enterprise:** Angular, RxJS, Windchill PLM, Windchill REST Services (WRS), ThingWorx
- **Delivery & Security:** Gradle, Docker, GitHub, CI, Checkmarx SAST, Black Duck, Jira

### Professional Experience

**PTC | Senior Software Specialist | November 2024 - Present**

- Implemented a shared LLM communication and response-processing layer using Spring Boot across three production Change AI agents, supporting Problem Report drafting and human-reviewed validation; report drafting takes approximately 10-30 seconds.
- Built an Angular LLM configuration interface and investigated Windchill REST Services APIs to align enterprise data integration with extension requirements.
- Integrated Checkmarx static application security testing and Black Duck dependency security checks into CI to surface code and dependency risks during delivery.
- Implemented agent benchmark evaluation and usage/behavior report generation using Python, MLflow, and Databricks to support agent assessment.
- Owned periodic user information and license validation across three Java/Spring AI MCP servers containing 11 registered tools for Parts, Documents, and Change Management.

**PTC | Software Specialist | May 2022 - November 2024**

- Contributed to Windchill Navigate Extension development on ThingWorx, connecting enterprise PLM data and functionality to a lightweight application experience.
- Supported custom Navigate applications through reusable components and Windchill API integration.

**IP Tech System | Software Engineer | January 2019 - May 2022**

- Developed a document verification module for a furniture-financing application, integrating government API information to support clerk-led KYC and loan-document review.
- Implemented verification state tracking and disbursement gating so that loan processing advanced only after verification was complete and all required documents were approved.

### Selected Project

**Sorting Algorithm Visualizer | Angular, TypeScript, Angular Signals**

- Built an interactive visualizer for six sorting algorithms using generator-driven execution, configurable inputs, and operation counters for comparisons, swaps, auxiliary writes, and array accesses.

## Evidence and Wording Decisions

| Item | Treatment |
| :--- | :-------- |
| Experience | January 2019 to November 2026 is approximately 7 years 10 months; use conservative 7+ years on the resume. |
| MCP scope | 11 registered tools: Parts 5, Documents 3, Change Management 3. This is system scope, not sole authorship. |
| MCP ownership | Periodic user information and license validation is explicitly confirmed. Other implementation and architecture ownership needs examples. |
| AI scope | Contributions to Draft and Validator agents; common communication/response layer serves all three agents. Do not equate this with building every agent. |
| Release status | Change AI is production-released. MCP release status has not been supplied. |
| Drafting duration | User-reported 10-30 seconds, not a verified benchmark or a percentage reduction. Confirm timing boundaries, environment, sample size, and manual baseline. |
| Validation | Human review remains required. Completeness and potential-duplicate analysis are capabilities, not proven accuracy improvements. |
| Versions and models | Supplied versions and model aliases are not independently verified. Omit exact Spring/MCP and model versions from the resume until clarified. Confirm whether OpenCode is a client, gateway, or provider in this architecture. |
| Security architecture | Inbound trust, Streamable HTTP, and outbound mutual TLS describe the implementation. Do not claim personal ownership of the entire security design without confirmation. Management API keys are not MCP-client authentication. |
| Scale and impact | "Major contributions" to users, deployments, latency, and reliability is not measurable evidence. Do not add adoption, cost, performance, or revenue figures without examples and a basis. |
| Older roles and project | Based on existing profile material; exact implementation ownership and impact still need confirmation. |
| Phone | Formatted with India's +91 prefix; confirm this is the desired public resume number. Phone is not added to the main profile README. |
| Education and credentials | Omitted until supplied, rather than represented by invented qualifications or empty placeholders. |

## Recruiter, Manager, and ATS Review

### Large Technology Company Recruiter

The strongest signal is production enterprise AI work grounded in Java backend experience. The official PTC progression also shows career growth. Current weaknesses are limited scale evidence, no education information, and generic earlier-role bullets. The resume does not yet demonstrate the breadth or decision-making authority needed to market the candidate as a software architect.

### Engineering Manager

The shared LLM layer, evaluation tooling, and periodic MCP validation are useful ownership signals. Follow-up interviews will need architectural trade-offs, failure handling, test strategy, security behavior, and evidence that evaluations affected release decisions. Project/Jira tracking alone does not establish technical leadership. Replace "Contributed" and "Supported" in the Navigate bullets with specific shipped changes once confirmed, rather than upgrading ownership through wording alone.

### ATS Review

The source is designed for straightforward extraction: one column, standard section names, visible links, chronological dates, Unicode mappings, and no graphical contact information. Relevant keywords are supported by the supplied work rather than keyword stuffing. The compiled PDF passes a one-page UTF-8 extraction check with expected keywords intact. Education is absent and exact job-description alignment is unknown; no commercial ATS parser has been tested.

**Provisional editorial readiness estimate: 65/100. This is not a score from an ATS, a hiring probability, or a validated job-match score.** Transparent rubric: structure 18/20, supported role keywords 17/20, evidence of impact 11/25, completeness 9/20, targeting 10/15. The final estimate should be revisited after the missing details, a target job description, and PDF extraction checks are available. Different employers and ATS products use different rules; no universal ATS score exists.

## Role-Specific Versions

These are tailoring directions, not five copies with unsupported claims. Preserve official titles and facts in every version.

| Target | Suggested Headline | Prioritize | Evidence Still Needed |
| :----- | :----------------- | :--------- | :-------------------- |
| Software Engineer | Software Engineer - Java, Spring Boot, Angular | End-to-end feature delivery, APIs, document workflows, tests | Features shipped and quality outcomes |
| Senior Software Engineer | Senior Software Engineer - Backend and Applied AI | Shared LLM layer, cross-agent reuse, production delivery, MCP validation | Architecture decisions, mentoring, cross-team influence |
| AI Engineer | AI Engineer - Enterprise LLM Applications | Agent integration, MLflow/Databricks evaluation, human review | Evaluation dataset, scoring, regressions detected, latency/cost; do not imply model-training expertise |
| Backend Engineer | Backend Engineer - Java and Enterprise Integration | Java 21, Spring MVC, WRS APIs, MCP transport, validation | API scale, data design, resilience, concurrency, observability |
| Cloud Engineer | Software Engineer - Cloud-Integrated Applications | Only confirmed cloud deployment and operations work | Actual AWS/Azure/GCP services, IAM, IaC, operations, incidents; Foundry development usage alone does not establish cloud engineering expertise |

The senior backend/applied-AI version currently has the strongest evidence. A cloud-first application should wait for verified operational experience.

## Ten Profile Improvements

1. Establish a before/after drafting benchmark, including sample size and timing boundaries, before claiming time savings.
2. Record agent evaluation dataset size, scoring criteria, and at least one regression or release decision informed by MLflow results.
3. Document an architecture decision you owned, alternatives considered, and the resulting engineering benefit.
4. Quantify MCP validation scope and behavior: frequency, invalid/expired licenses, outages, cache behavior, and relevant latency.
5. Add concrete Navigate features and verified usability, performance, reliability, or delivery outcomes.
6. Confirm the finance application's stack, transaction volume, personal ownership, and document-processing outcomes.
7. Substantiate leadership through engineers mentored, design reviews led, migrations owned, or training delivered.
8. Add degree details and only completed, verifiable certifications or awards that support the target role.
9. Link one reproducible public backend or AI project with tests, architecture documentation, and evaluation results; do not present conceptual showcases as deployed systems.
10. Tailor the final resume to a real job description and add relevant publications, patents, external contributions, or technical talks when supported.

## Round 2: Questions to Finalize

Answer in rough notes; use "none" or "unknown" where appropriate. Estimates are acceptable when explicitly labeled and defensible. Use only material you are permitted to share.

1. **Education:** degree, discipline, institution/university, graduation year, and optionally strong GPA or relevant coursework?
2. **Target and skills:** preferred companies, industries, locations, and work arrangement? Share a target job posting. Which listed skills are production experience versus personal projects? Any confirmed AWS/Azure/GCP, CI platform, testing, OAuth/SSO/SAML, Kubernetes, or infrastructure-as-code experience?
3. **Hardest AI problem:** what failed, what did you decide, what alternatives did you reject, and how did you validate the fix? What does the common LLM layer own: provider routing, timeouts, retries, structured responses, errors, or telemetry? Confirm the exact model IDs and OpenCode's role.
4. **AI results:** how was the 10-30 second duration measured, and what was the manual baseline? How many reports, test cases, customers, or users? Which evaluation metrics, scores, release gates, and regressions? Any measured security findings or remediation outcomes from CI?
5. **MCP ownership and outcomes:** which tools did you personally implement? Is it released? What is the revalidation interval, failure behavior, test coverage, and any measured deployment, latency, reliability, or integration result?
6. **Earlier roles:** name two specific Navigate features you delivered and the finance application's actual stack, your implementation boundaries, scale, and outcomes.
7. **Leadership and recognition:** engineers mentored, architecture decisions, critical feature ownership, migrations, training, conference talks, awards, or hackathons? Include dates and concrete examples. Any completed AWS, Azure, GCP, Kubernetes, OCI, AI, or security certifications?
8. **Public work:** confirm the sorting project's repository and personal ownership. Any additional AI/LLM, agentic, MCP, RAG, cloud, enterprise, or open-source projects? For the best one, provide purpose, stack, architecture, scale, challenge, outcome, and repository. Any external contributions, stars/forks, community work, technical articles, papers, whitepapers, or patents with links/status?

Finalization will reconcile these answers, strengthen weak bullets, add relevant missing sections, and rerun layout and extraction checks. Optional sections should earn their space; do not add empty certifications, awards, or publications sections.