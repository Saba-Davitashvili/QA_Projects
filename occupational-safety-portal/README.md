# Project 4 — Professional Occupational Safety & Risk Management Platform

## Overview
A cloud-native multi-tenant B2B portal offering professional occupational health and safety (OHS) services. The platform enables businesses to request work environment assessments, manage operational risks, and receive practical compliance recommendations via an onboarding and lead intake engine.

## Scope
- **Platform**: Web (B2B SaaS)
- **Testing Type**: Manual QA (BVA, input type sanitization, navigation routing)
- **Test Cases Written**: 6
- **Bugs Found on First Pass**: 6 (1 High, 3 Medium, 2 Low)

## Technical Risk Areas
- Form input validation boundaries (numeric clipboard sanitization)
- Parameter formatting for external mapping integrations
- Length constraints and buffer bounds handling on input submissions
- Layout navigation consistency across global footer templates
- Cross-component data integrity and information sync

## Bug Reports

| Bug ID | Component | Summary | Severity |
|---|---|---|---|
| BUG-001 | Form Validation | Alphanumeric clipboard paste bypasses numeric filter in phone input |  Medium |
| BUG-002 | Routing / Maps | Address routing parameters zoom out to broad regional view |  Low |
| BUG-003 | Data Security | Missing string length constraint allows uncapped data injection |  Critical |
| BUG-004 | Input Sanitization | Dot/period dividers bypass format checks on phone fields |  Medium |
| BUG-005 | UI / Footer | Dead/Empty social media hyperlink anchors in global footer |  Low |
| BUG-006 | Data Consistency | Footer location data does not match the detailed contact page address |  Low |

See individual `bug-report-*.md` files in this folder.
