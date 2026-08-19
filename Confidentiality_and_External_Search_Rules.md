**Confidentiality and External Search Rules**

Governance document for Innovation Partner Discovery Agent

Version 0.1 | 05/06/2026 | For internal pilot use

# 1\. Purpose

This document defines how the agent and users must handle confidential innovation disclosures, unpublished inventions, patent drafts, software/data descriptions and technical documents when producing commercialisation exploration reports.

# 2\. Core rule

All input disclosure forms, unpublished technology descriptions, draft patents, draft papers, datasets, diagrams, performance data and inventor-supplied technical details are confidential by default unless the user explicitly states that the material is public or approved for external use.

# 3\. What the agent may use for external searching

- Non-confidential technology title or generic description.
- Broad technical field and application area.
- Generic problem-solution wording.
- General keywords that do not reveal enabling details.
- Public patent/publication numbers or public links supplied by the user.
- Public company names supplied by the user.

# 4\. What the agent must not use externally without approval

- Unpublished enabling details, precise formulations, algorithms, source code, datasets, experimental conditions, prototype designs or performance data.
- Confidential project names, internal reference numbers, grant numbers or agreement details.
- Inventor names or research group names where disclosure could reveal unpublished IP.
- Draft patent claims, unpublished manuscript text, confidential figures or diagrams.
- Commercially sensitive sponsor, collaborator or agreement details.

# 5\. Required workflow

1. Extract disclosure content internally.
2. Create a non-confidential summary and safe keyword set.
3. Ask the user to confirm if any borderline terms are approved for external search.
4. Perform external research only using the safe keyword set.
5. Record the search terms used in the report appendix.
6. Flag any uncertain confidentiality decision for human review.

# 6\. User warning text

Suggested wording for the agent: "I will treat this disclosure as confidential. I will first create a non-confidential search set and will avoid using unpublished enabling details externally. Please confirm if any specific details are already public."

# 7\. Exceptions

The agent may use more specific terms only where the user confirms that the information is already public, published, patented, disclosed externally or authorised for external search. The report must record this confirmation as an assumption or note.

# 8\. Audit checklist

| **Check**                                                            | **Pass/Fail** | **Notes** |
| -------------------------------------------------------------------- | ------------- | --------- |
| Was a non-confidential summary generated before searching?           |               |           |
| Were confidential implementation details excluded from search terms? |               |           |
| Were search terms listed in the report appendix?                     |               |           |
| Were public-only assumptions clearly marked?                         |               |           |
| Were any borderline disclosures flagged for human review?            |               |           |