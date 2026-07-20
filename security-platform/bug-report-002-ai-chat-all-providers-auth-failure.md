# [BUG-002] AI Chat Fails Across All LLM Providers Despite Valid API Keys

## Metadata
- **Project**: AI-Augmented Security Scanning Platform
- **Component**: AI Chat Interface / Multi-Provider API Gateway
- **Type**: Bug / API Authentication
- **Severity**: Critical
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: AI Chat interface — all available LLM providers

## Preconditions
The user is authenticated with valid API keys saved in Settings for all supported models (Claude, Grok, Groq, Gemini, OpenAI).

## Steps to Reproduce
1. Log in with valid API keys configured for all models (Claude, Grok, Groq, Gemini, OpenAI).
2. Open the **AI Chat** interface and select an active model (e.g., Claude).
3. Type a message (e.g., `"Hello"`) and send it.
4. Repeat by cycling through each remaining model (Grok, Groq, Gemini, OpenAI).

## Actual Result
No model returns a valid response. Provider-specific error behavior:
- **Claude**: Displays a localized error string — *"Error invoking the API. Check the API key in Settings"* (Georgian: *"შეცდომა API-ის გამოძახებისას. API key-ი შეამოწმე Settings-ში."*).
- **Grok / Gemini / OpenAI / Groq**: A generic `"error"` message is returned without additional diagnostic context.

## Expected Result
The application should authenticate successfully against each provider's API using the persisted keys, process the chat request, and stream or display the model's text response inside the chat window. Error messages, if any, should include actionable diagnostic detail (e.g., HTTP status codes, provider error codes) rather than generic labels.

