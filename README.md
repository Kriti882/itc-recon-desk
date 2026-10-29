# ITC Recon Desk

A business analysis case study on GST Input Tax Credit reconciliation for small Indian businesses, with a working prototype.

**Live demo:** https://YOUR-GITHUB-USERNAME.github.io/itc-recon-desk/

## The problem

A business can only claim tax credit on purchase invoices its suppliers have reported in GSTR-2B. Most small businesses check this by hand in Excel. Invoice numbers are written differently on each side, GSTINs get mistyped, and vendors file late. Mismatches often surface only after GSTR-3B is filed.

## What's inside

| Area | What I did |
|---|---|
| Research | GST rules (Section 16(2)(aa), Rule 36(4), IMS), hypotheses, interview guide |
| Users | Proto-personas and a stakeholder map |
| Process | AS-IS and TO-BE flowcharts |
| BRD | Objectives, scope, 10 business rules, assumptions, constraints |
| FRD | 12 functional and 4 non-functional requirements (MoSCoW) |
| Backlog | 6 user stories with Given/When/Then acceptance criteria |
| Traceability | Objective → requirement → rule → story → test |
| UAT | 11 test cases that run live against the matching engine |
| Prototype | Matching engine with 8 exception types, ITC-at-risk summary, vendor follow-up ranking, CSV upload |

## How the matching works

1. Normalise invoice numbers (`INV/26-27/0045` and `INV-26-27-45` become the same key).
2. Match on GSTIN + invoice number.
3. Classify each row: Matched, Period mismatch, Probable match, Value mismatch, GSTIN mismatch, Missing in 2B, Duplicate in books, or Missing in books.
4. Validate GSTIN check digits.
5. Add up ITC at risk and rank vendors by it.

## Tools

HTML, CSS and plain JavaScript. No backend. Data never leaves the browser.

## Data note

All vendors, GSTINs and invoices are synthetic and generated in the browser. This is a personal portfolio project, not client work and not tax advice.

## About me

Kriti Sharma, Business Analyst (PGDM, Research & Business Analytics and Finance).
LinkedIn: https://www.linkedin.com/in/kriti-sharma-7h25k
