**Contact Discovery and Outreach Compliance Rules**

Governance document for contact recommendations

Version 0.1 | 05/06/2026 | For internal pilot use

# 1\. Purpose

This document defines how the agent should recommend company contacts and outreach routes while avoiding unsupported or non-compliant use of personal data.

# 2\. Core principles

- Prefer role-based target recommendations where named contacts are not clearly public, relevant and sourceable.
- Named contacts may be included only if they appear on public, sourceable pages or approved internal/licensed sources.
- Do not invent, guess, derive or pattern-match private email addresses.
- Do not imply that outreach has been sent. The agent may draft messages only.
- All contact recommendations are for human review before use.

# 3\. Permitted contact sources

| **Source**                            | **Permitted use**                        | **Notes**                                      |
| ------------------------------------- | ---------------------------------------- | ---------------------------------------------- |
| Company leadership/team pages         | Named contact or target role.            | Record URL.                                    |
| Press releases/news pages             | Named contact or relevant business unit. | Confirm recency and relevance.                 |
| Public professional profiles          | Role validation and public profile link. | Avoid scraping or private details.             |
| Existing CRM records supplied by user | Named contact if user has lawful access. | Record CRM/source note.                        |
| Licensed contact database             | Only if approved by institution.         | Record provider and lawful-basis note.         |
| Generic role target                   | Always permitted.                        | Use where no named public contact is suitable. |

# 4\. Contact output fields

| **Field**                                              | **Requirement**                                                                         |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| Company                                                | Required.                                                                               |
| Target role or named contact, including email address. | Named only if sourceable; otherwise role-based.                                         |
| Reason for contact                                     | Must link to technology fit or engagement route.                                        |
| Source URL                                             | Required for named public contacts.                                                     |
| Recommended route                                      | Website form, public profile, CRM contact, existing relationship, or role-based target. |
| Compliance notes                                       | GDPR/PECR caution and human approval requirement.                                       |
| Confidence                                             | High, medium or low.                                                                    |

# 5\. Prohibited behaviours

- No private email guessing.
- No collection of personal data from sources that prohibit such use.
- No automatic outreach.
- No adding contacts to CRM without approval.
- No presenting a named contact as definitely interested unless source evidence supports that claim.

# 6\. Standard disclaimer

Suggested report note: "Contact recommendations are based on public or user-supplied information and are provided for human review. Outreach should follow institutional data-protection, PECR and CRM policies."