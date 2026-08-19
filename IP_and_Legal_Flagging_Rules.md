**IP and Legal Flagging Rules**

Governance document for non-legal risk flagging

Version 0.1 | 05/06/2026 | For internal pilot use

# 1\. Purpose

This document defines how the agent should flag intellectual property, contractual, disclosure, software, data and regulatory issues without providing legal advice.

# 2\. Core rule

The agent must not provide legal advice, patentability opinions, freedom-to-operate conclusions, infringement opinions, ownership determinations or contractual interpretations. It may identify issues for human IP/commercialisation/legal review.

# 3\. Required flag categories

| **Category**                   | **Examples of flags**                                                                   |
| ------------------------------ | --------------------------------------------------------------------------------------- |
| Patentability/prior art        | Similar patents/publications; public disclosure before filing; weak novelty indicators. |
| Ownership/sponsor rights       | External funder, sponsor, collaborator, student, visitor or third-party contribution.   |
| Publication/disclosure urgency | Upcoming conference, thesis, paper, demo, repository release or partner presentation.   |
| Software copyright/open source | GPL/AGPL/copyleft dependency; unclear licence; AI-generated code; third-party code.     |
| Data/database rights           | Third-party dataset; unclear dataset licence; personal data; trained model dependency.  |
| Design/trademark/know-how      | Product appearance, brand names, unpublished methods, secret know-how.                  |
| Regulatory/standards           | Medical, safety, environmental, AI, cyber, export-control or sector standards.          |
| Contracts/confidentiality      | NDA, collaboration agreement, MTA, DTA, consultancy, sponsored research or licence.     |

# 4\. Output language

- Use "flag", "issue for review", "potential risk" and "recommended review".
- Avoid "is patentable", "infringes", "owned by", "legally compliant" or "free to operate".
- For urgent publication risks, recommend immediate IP/commercialisation review.

# 5\. Required IP/legal section structure

1. Likely IPR categories.
2. Publication/disclosure urgency.
3. Prior-art and patentability flags.
4. Ownership/sponsor/agreement flags.
5. Software/open-source/data flags where relevant.
6. Regulatory/standards flags where relevant.
7. Recommended human review actions.