# Project 2 — AI-Powered E-commerce Search & Chatbot Platform

## Overview
A Shopify-integrated storefront with NLP-driven product search, deep attribute filtering, and a context-aware AI chatbot powered by a RAG (Retrieval-Augmented Generation) pipeline.

## Scope
- **Platform**: Web
- **Testing Type**: Manual QA
- **Test Cases Written**: 5
- **Bugs Found on First Pass**: 5 (3 Critical, 2 High)

## Technical Risk Areas
- WebSocket origin configuration across apex and subdomain variants
- Client-side DOM stability under rapid repeated interactions
- Elasticsearch lexical scoring and parameter weight management
- RAG pipeline data grounding — preventing LLM hallucinations
- Stochastic response variance from identical prompt inputs

## Bug Reports

| Bug ID | Title | Severity |
|---|---|:---:|
| BUG-001 | Chatbot WebSocket Handshake Failure on Apex Domain | 🔴 Critical |
| BUG-002 | Memory Leak / DOM Freeze on Rapid Interactive Refreshes | 🔴 Critical |
| BUG-003 | Search Parameter Filtering Overwrite | 🟠 High |
| BUG-004 | Generative AI Fabricated Inventory Output | 🔴 Critical |
| BUG-005 | Inconsistent Stochastic Responses on Identical Queries | 🟠 High |

See individual `bug-report-*.md` files in this folder.
