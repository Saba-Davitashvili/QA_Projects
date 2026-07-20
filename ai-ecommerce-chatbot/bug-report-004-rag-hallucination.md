# [BUG-004] Generative AI Fabricated Inventory Output (RAG Hallucination)

## Metadata
- **Project**: AI-Powered E-commerce Search & Chatbot Platform
- **Component**: Chatbot Widget / RAG Integration
- **Type**: Bug / Data Integrity / LLM Hallucination
- **Severity**: Critical
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Storefront Chatbot Widget

## Preconditions
The user has launched the storefront chatbot modal.

## Steps to Reproduce
1. Open the storefront chatbot modal.
2. Enter a bounded parameter query: `"Show me products below $25"` (or regional equivalent: `"Show me products below 50 GEL"`).
3. Cross-reference the items returned in the chatbot's product cards against the live database inventory.

## Actual Result
The AI model outputs a clean, well-formatted, but entirely fabricated product card. The returned product, its pricing, and stock details do not exist in the live database catalog. The chatbot hallucinates mock data instead of calling or parsing the real catalog API.

## Expected Result
The LLM orchestration layer must be strictly grounded to the database catalog API. If no products match the specified parameters, it must return a standardized fallback message (e.g., *"No items found matching that price criteria."*) instead of fabricating non-existent inventory objects.
