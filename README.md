[Innovation Partner Discovery Agent - User Guide.md](https://github.com/user-attachments/files/31219231/Innovation.Partner.Discovery.Agent.-.User.Guide.md)
This agent analyses innovation disclosure forms, patent text, publication abstracts or technology descriptions and produces a commercialisation exploration report.

Inputs:

\- completed innovation disclosure form;

\- pasted technology description;

\- patent text;

\- publication abstract.

Outputs:

\- executive summary;

\- technology overview;

\- value proposition;

\- market applications;

\- prior art and competitor landscape;

\- company matching;

\- contact-role recommendations;

\- outreach pack;

\- development roadmap;

\- commercialisation route recommendation;

\- IP and legal flags;

\- risk register;

\- next actions;

\- references.

Rules:

\- Treat all disclosure forms as confidential.

\- Do not disclose confidential details externally.

\- Do not invent sources.

\- Mark uncertain findings as assumptions.

\- Do not give legal advice.

# A practical "manual flow"

Paste each of the following prompts into the agent in sequence. Swap the chosen model from auto to the latest 'think deeper' version (currently 5.5)

# Prompt 1 – Extract

Create a new Innovation Commercialisation Exploration Report.

Use your knowledge source templates, including the Innovation Commercialisation Report Template, the disclosure form templates, the output schema, the figure/table standards, the source reliability rubric, and the confidentiality/external search rules.

Treat the information below as confidential.

First:

1\. Extract the key information from the disclosure.

2\. Classify the opportunity as physical product/process, software/data/hardware, mixed, patent, publication, free-text or unclear.

3\. Identify missing critical information.

4\. Identify confidentiality, publication, IP, software/data, ownership, agreement and development-stage flags.

5\. Create a non-confidential summary and search keyword set that can be safely used for external research.

Do not start external searching until you have produced the safe non-confidential search set.

Here is the disclosure or technology description:

\[ATTACH OR PASTE DISCLOSURE TEXT OR TECHNOLOGY DESCRIPTION HERE\]

# Prompt 2 – Perform External Research

Now perform the external research stage using only the non-confidential search terms you created.

Use the Approved Source List and Source Reliability Rubric from your knowledge source.

Research the following areas:

1\. Market applications and use cases

2\. Market trends, drivers and barriers

3\. Patent and prior-art landscape

4\. Academic publication and research landscape

5\. Competing products, services, open-source projects or substitute technologies

6\. Potential companies, licensees, research sponsors, co-development partners, users or funders

7\. Public contact roles or named public contacts where sourceable and appropriate

8\. Funding routes and development support

9\. Standards, regulation, policy or adoption constraints

For each finding, provide:

\- claim or insight;

\- source title;

\- publisher/organisation;

\- URL if available;

\- date or date accessed if available;

\- relevance to the innovation;

\- confidence level: high, medium or low.

Rules:

\- Do not use confidential implementation details in searches.

\- Do not invent sources or facts.

\- If web search is unavailable or insufficient, say so clearly and provide the exact manual searches that should be run.

\- If a source is weak or secondary, mark it as such.


# Prompt 5 - Tech Assessments (repeat as necessary for each Evaluator)

(For this prompt, users should  use the '+' icon to add content to their prompt, searching 'Evaluator' and selecting one of the categories.)

Perform an assessment based on the attached requirements.

# Prompt 4 – Build the company, contact and route strategy

Using the extracted disclosure information and the external research findings, create the company matching, contact strategy and commercialisation route assessment.

Produce:

1\. Ranked company-matching table with 15–25 organisations where possible:

\- rank;

\- company/organisation;

\- country/region;

\- sector;

\- evidence of fit;

\- source;

\- suggested engagement route;

\- priority score out of 100;

\- confidence;

\- recommended first approach.

2\. Shortlists:

\- top 5 highest-priority companies;

\- top 5 easiest-to-approach organisations;

\- top 5 strategic long-term targets;

\- top 5 UK or regional opportunities if relevant.

3\. Contact strategy:

\- target roles;

\- relevant business units;

\- named public contacts and contact information (e.g. email addresses) only if sourceable and appropriate;

\- source URL for named contacts;

\- contact-compliance notes;

\- no invented private email addresses.

4\. Commercialisation route assessment:

\- licence;

\- sponsored research;

\- KTP;

\- consultancy;

\- services rendered;

\- spin-out;

\- core facility access;

\- monitor/fundamental research.

5\. Recommended primary route, secondary routes and rationale.

# Prompt 5 – Generate figures and report-ready tables

Now create the report-ready figures and tables using the Figure and Table Standards in your knowledge source.

Use only extracted disclosure information and sourced external research findings. Where evidence is incomplete, use qualitative scoring and clearly mark assumptions.

Create the following tables:

1\. Extracted innovation profile

2\. Missing information and assumptions

3\. Market applications

4\. Market evidence and source table

5\. Prior art and competing technologies

6\. Company matching

7\. Contact strategy

8\. Development roadmap

9\. Commercialisation route assessment

10\. IP/legal and software/data flags

11\. Risk register

12\. Recommended next actions

13\. References

Create figure-ready outputs for:

Figure 1: Technology-to-market map

Figure 2: Market attractiveness matrix

Figure 3: Competitive positioning matrix

Figure 4: Company relevance vs ease-of-engagement chart

Figure 5: Development roadmap

Figure 6: Commercialisation route decision tree

For each figure provide:

\- figure title;

\- purpose;

\- data table;

\- scoring explanation;

\- caption;

\- assumptions;

\- instructions for recreating the figure in Word, Excel or PowerPoint.

Do not create decorative figures. Only include figures that help the commercialisation decision.

# Prompt 6 – Final Report

Draft the final Innovation Commercialisation Exploration Report into a word document.

Use:

\- the extracted disclosure profile;

\- the non-confidential summary;

\- the external research findings;

\- the company and contact strategy;

\- the commercialisation route assessment;

\- the figures and tables pack;

\- the report template in your knowledge source.

Requirements:

\- Mark the report CONFIDENTIAL.

\- Use UK English.

\- Use DD/MM/YYYY date format.

\- Follow the full Innovation Commercialisation Report Template structure.

\- Include source citations or source notes for all factual claims.

\- Mark unsupported claims as assumptions.

\- Include all report-ready tables.

\- Include figure titles, captions and figure-ready data tables.

\- Include an outreach pack with licensing, sponsored research and exploratory collaboration messages.

\- Include IP/legal issues as flags for human review, not legal advice.

\- Include GDPR/PECR/contact-compliance cautions.

\- Include a references section.

\- Include an appendix of search terms used and follow-up searches needed.

Before the final report, include a short quality-control checklist showing:

1\. Whether the report structure is complete.

2\. Whether all external claims are sourced.

3\. Whether unsupported claims are marked as assumptions.

4\. Whether confidential information has been protected.

5\. Whether contact recommendations are compliant and sourceable.

6\. Whether next actions are clear.

# Promt 7 (optional) - Refresh

Review the report and identify the weakest sections based on evidence quality, missing sources or low-confidence assumptions.

Then perform a targeted refresh for the weak sections only.

Focus on:

1\. Additional market evidence

2\. Additional prior-art or publication evidence

3\. Stronger company matches

4\. Better public contact-role evidence

5\. Funding and development opportunities

6\. Standards or regulatory constraints

Use only non-confidential search terms. Add new findings with sources, confidence levels and a short explanation of how they change the recommendations.
