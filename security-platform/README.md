# Project 5 — AI-Augmented Security Scanning Platform

## Overview
A web-based cybersecurity platform integrating multi-provider LLM analysis (Claude, Grok, Groq, Gemini, OpenAI) with automated security scanning workflows. The system supports configurable scan team approaches (Blue Team / Red Team), AI-powered vulnerability analysis, real-time AI chat, and multi-language localization.

## Scope
- **Platform**: Web (PC)
- **Testing Type**: Manual QA (API integration, session isolation, i18n coverage)
- **Bugs Found on First Pass**: 4 (3 Critical, 1 Low)

## Technical Risk Areas
- Multi-provider LLM API payload serialization and authentication handshake
- Client-side session state isolation across authentication transitions
- Local storage namespace pollution between user accounts
- Internationalization (i18n) resource bundle coverage completeness

## Bug Reports

| Bug ID | Component | Summary | Severity |
|---|---|---|---|
| BUG-001 | AI Analysis Pipeline | HTTP 400 / "Failed to Fetch" on Blue Team scan AI analysis |  Critical |
| BUG-002 | AI Chat / API Gateway | Chat fails across all LLM providers despite valid API keys |  Critical |
| BUG-003 | Session Isolation | API keys and scan progress leak between accounts on same browser |  Critical |
| BUG-004 | i18n / Localization | Scan type descriptions remain in English under Georgian locale |  Low |

See individual `bug-report-*.md` files in this folder.
