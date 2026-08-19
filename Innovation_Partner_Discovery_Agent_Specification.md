**Innovation Partner Discovery Agent**

Implementation Specification for M365 Copilot / Copilot Studio

Version 0.1 | 05/06/2026 | Confidential design draft

# 1\. Purpose

This specification defines an internal University innovation-commercialisation agent that accepts an innovation disclosure form, patent text, publication abstract or free-text technology description and produces a single commercialisation exploration report. The agent is intended to replicate the core functional pattern of a partnership discovery platform: technical summarisation, market exploration, prior-art and competitor scan, partner matching, contact-role discovery, outreach material generation, development roadmap and commercialisation-route recommendation.

# 2\. Primary Inputs

- Innovation Disclosure Form – Physical Product and Process: title, contributors, ownership/funding context, external disclosures, agreements, value proposition, summary, detailed description, development stage, next steps, interested companies and prior art.
- Innovation Disclosure Form – Software, Related Hardware and Data: all of the above plus programming language, AI-written code, software/hardware/data format, update needs, third-party/open-source elements, datasets used for training, licence terms and duplicability.
- Patent text, publication abstract, invention summary, draft manuscript, slide deck or pasted technology description.

# 3\. Recommended Microsoft Architecture

Build as a Copilot Studio agent with generative orchestration enabled, grounded in SharePoint/OneDrive and connected to approved tools through Power Automate, Graph connectors and/or MCP-enabled connectors where available.

- Copilot Studio Agent: front-door conversational and report-generation agent.
- SharePoint: controlled store for disclosure forms, generated reports, approved guidance and reusable templates.
- Power Automate: document ingestion, structured extraction, report assembly, approval routing and archive workflow.
- Dataverse or SharePoint Lists: opportunity records, company matches, contact recommendations, run metadata and risk registers.
- Approved external data connectors: patents, publications, companies, market reports and contact data only where licensed/lawful.
- Human approval gates: before outreach, before CRM creation and before sharing reports externally.

# 4\. Agent Components

| **Component**                           | **Purpose**                                                                              | **Key Outputs**                                                                                    |
| --------------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Front-door Agent                        | Accepts input, classifies technology type, coordinates specialist actions.               | Run plan, missing information questions, final report request.                                     |
| Intake & Extraction Agent               | Parses disclosure form and creates a structured opportunity profile.                     | Extracted fields, missing data checklist, confidentiality and publication-risk flags.              |
| Technical Summarisation Agent           | Converts technical disclosure into non-confidential, market-facing language.             | Plain-English summary, technical summary, executive statement, key advantages, value propositions. |
| Market Discovery Agent                  | Finds applications, sectors, use cases, drivers, barriers and market signals.            | Market map, sector ranking, trend notes, market source references.                                 |
| Prior Art & Competitive Landscape Agent | Searches patents, publications, products and similar software/tools.                     | Prior-art table, competitor list, differentiation matrix, novelty risk flags.                      |
| Company Matching Agent                  | Ranks companies likely to license, fund, co-develop, validate or adopt the technology.   | Company longlist, priority ranking, rationale, evidence, engagement route.                         |
| Contact Discovery Agent                 | Finds relevant public contacts or, where unavailable, role-based contact targets.        | Named/public contacts, target role categories, source URLs, GDPR/PECR notes.                       |
| Funding & Development Roadmap Agent     | Identifies validation gaps, next projects and funding routes.                            | TRL estimate, roadmap, funding options, milestone plan.                                            |
| Commercialisation Route Agent           | Recommends licence, spin-out, KTP, consultancy, services, sponsored research or monitor. | Route recommendation, rationale, risk register, next actions.                                      |
| Report Generation Agent                 | Compiles all outputs into Word/PDF and appendices.                                       | Report, company/contact appendix, reference list, figures.                                         |

# 5\. Required Tools and Actions

| **Tool / Action**       | **Type**                           | **Description**                                                                 | **Approval Needed**                       |
| ----------------------- | ---------------------------------- | ------------------------------------------------------------------------------- | ----------------------------------------- |
| ExtractDisclosureFields | Power Automate / document AI       | Reads Word/PDF inputs and maps answers into the JSON schema.                    | No                                        |
| SearchWeb               | Connector / grounded search        | Searches public web for companies, markets, products, standards and references. | No, if using non-confidential query terms |
| SearchPatents           | Connector/API/manual tool          | Searches patent data using non-confidential technical keywords.                 | No, if using non-confidential query terms |
| SearchPublications      | Connector/API/manual tool          | Searches publications, grants and academic experts.                             | No, if using non-confidential query terms |
| SearchCompanies         | Connector/API/manual tool          | Finds companies, sectors, recent activity and R&D signals.                      | No                                        |
| FindContacts            | Connector/API/manual tool          | Finds public named contacts or role-based contact targets.                      | Yes if using licensed contact databases   |
| GenerateFigures         | Code/Power Automate/Azure Function | Creates market maps, matrices and roadmap figures from structured JSON.         | No                                        |
| GenerateReport          | Word template automation           | Populates report template and exports Word/PDF.                                 | No                                        |
| RequestHumanApproval    | Power Automate approvals           | Routes report/outreach for IP or KE approval.                                   | Yes                                       |

# 6\. Governance Controls

- Treat every disclosure form and uploaded technical document as confidential by default.
- Use only non-confidential search queries unless a named authorised user explicitly approves broader disclosure.
- Do not send outreach automatically. Generate drafts only, then route to human approval.
- Do not provide legal advice. Flag issues for IP/commercialisation review.
- Do not invent market sizes, contacts, company facts, patent references or publication references.
- Every factual claim in the report must include a source, confidence level or explicit assumption statement.
- For software/data opportunities, always assess open-source licences, third-party code, AI-generated code, training data, dataset rights, future updates and duplicability.
- For physical product/process opportunities, always assess manufacturability, scale-up, validation stage, standards/regulation and patent/prior-art risk.
- Named contacts must be sourced from public pages, approved CRM records or licensed contact-data providers with lawful basis and retention controls.

# 7\. Standard Operating Workflow

1. User uploads a completed disclosure form or pastes a technology description.
2. Agent classifies the innovation type and extracts structured fields.
3. Agent asks targeted follow-up questions only if critical information is missing.
4. Agent creates a non-confidential summary and search keyword set.
5. Agent runs market, prior-art, publication, company and contact-role discovery.
6. Agent ranks markets and companies using relevance, evidence strength, opportunity size, fit and engagement feasibility.
7. Agent drafts outreach messages and recommended first engagement route.
8. Agent generates figures and compiles the final report.
9. Agent routes the report to IP/KE human review before any external use.
10. Approved report and structured data are stored against the disclosure record.

# 8\. Scoring Models

Company priority score should be calculated from transparent sub-scores. Suggested formula:

Priority = 0.30 × technical fit + 0.20 × market access + 0.15 × evidence strength + 0.15 × partnership likelihood + 0.10 × UK/strategic relevance + 0.10 × speed-to-engage

Market attractiveness score should be similarly transparent:

Attractiveness = 0.25 × problem urgency + 0.20 × market growth + 0.20 × adoption fit + 0.15 × competitive whitespace + 0.10 × regulatory feasibility + 0.10 × fundability

# 9\. Build Backlog

| **Phase** | **Deliverable**                        | **Acceptance Criteria**                                                                                   |
| --------- | -------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Phase 1   | Disclosure intake and report generator | Takes a completed disclosure form and outputs a referenced Word report with figures and company longlist. |
| Phase 1   | JSON extraction schema                 | All required template fields map to structured data with missing-field flags.                             |
| Phase 1   | Human review workflow                  | Report can be approved/rejected with comments before sharing.                                             |
| Phase 2   | Partner/contact discovery              | Produces ranked companies and public or approved contacts with sources and compliance notes.              |
| Phase 2   | CRM/SharePoint opportunity store       | Structured results saved against internal reference number.                                               |
| Phase 3   | Monitoring and refresh                 | Agent can re-run market/company monitoring and update report sections.                                    |
| Phase 3   | Licensed data integration              | Approved contact/company/patent databases integrated under data protection controls.                      |

# 10\. Testing Plan

- Test with one physical product disclosure, one software/data disclosure and one free-text patent abstract.
- Validate extraction accuracy against manually completed field checklist.
- Check all factual claims for citations and all low-confidence claims for caveats.
- Review for accidental disclosure of confidential material in external search queries.
- Ask IP/commercialisation reviewers to score usefulness, risk flags and company matching quality.
- Run red-team prompts attempting to force legal advice, private email scraping or unapproved external disclosure.

# 11\. Report Output Package

- Word report: main deliverable for the IP/KE team.
- PDF report: shareable static version after approval.
- Excel/CSV appendix: company and contact-role longlist.
- JSON file: structured run output for audit/re-use.
- PowerPoint summary: optional pitch/committee briefing version.