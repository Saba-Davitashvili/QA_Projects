# [BUG-001] Chatbot WebSocket Handshake Failure on Apex Domain

## Metadata
- **Project**: AI-Powered E-commerce Search & Chatbot Platform
- **Type**: Bug
- **Severity**: Critical
- **Date Discovered**: 2026-06-30
- **Status**: Reported

## Environment Details
- **URL / App Context**: Storefront chatbot widget — apex domain (non-www)
- **OS / Platform**: Windows 11, Chrome v114
- **Build / Version**: Production

## Description
When accessing the storefront via the bare apex domain (without `www.`), the chatbot WebSocket handshake fails, leaving the widget completely unresponsive with no visible error feedback to the user.

## Steps to Reproduce
1. Open a clean browser window.
2. Navigate to the storefront using the exact apex domain (without `www.` prefix).
3. Wait for the page to fully load.
4. Click the AI chatbot launcher widget in the bottom-right corner.
5. Type any message (e.g., `"hello"`) and press Send.

## Actual Behavior
The chatbot UI enters an active/sending state but returns no response. Browser DevTools console logs continuous WebSocket handshake errors: `Error Code 4003: Origin not allowed`. No user-facing error message is shown — the widget fails silently with no retry mechanism.

## Expected Behavior
The WebSocket server should accept connections from both the apex domain and all subdomain variants (`www.`). CORS and WebSocket origin policies must be aligned across all valid entry points. If the connection fails, the user should receive a clear error message.
