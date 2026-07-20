# [BUG-005] Inconsistent Stochastic Responses on Identical Queries

## Metadata
- **Project**: AI-Powered E-commerce Search & Chatbot Platform
- **Component**: Chatbot Widget / LLM Orchestration
- **Type**: Bug / Reliability / Stochastic Behavior
- **Severity**: High
- **Priority**: Medium
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Storefront Chatbot Widget

## Preconditions
The user has launched the storefront chatbot modal.

## Steps to Reproduce
1. Trigger the chatbot widget.
2. Send the exact query string: `"Show me products below $25"` (or regional equivalent: `"Show me products below 50 GEL"`).
3. Clear the session context or initialize a new parallel chat thread.
4. Repeat the exact query sequence 5 consecutive times across independent sessions.

## Actual Result
The platform exhibits highly volatile stochastic divergence on deterministic data. Across 5 identical runs, results randomly rotate between three distinct states:
1. *State A (Defect):* Returns an ungrounded, hallucinated product card.
2. *State B (Defect):* Returns an empty "No items found" message despite matching items existing in the inventory.
3. *State C (Expected):* Correctly calls the catalog API and renders valid matching items.

## Expected Result
System behavior must be deterministic for structural inventory queries. The temperature parameter of the underlying LLM orchestrator should be configured close to `0.0` for search/inventory queries, forcing the agent to rely strictly on structured JSON data returned from live catalog database calls.
