# [BUG-001] AI Analysis Fails with HTTP 400 / "Failed to Fetch" on Blue Team Scan Completion

## Metadata
- **Project**: AI-Augmented Security Scanning Platform
- **Component**: AI Analysis Pipeline / Scan Results Handler
- **Type**: Bug / API Integration
- **Severity**: Critical
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Security Scan page — Blue Team scan with Claude selected as AI model

## Preconditions
The user is authenticated and has valid AI provider API keys saved in Settings.

## Steps to Reproduce
1. Log in and navigate to the **Security Scan** page.
2. Enter a valid website URL in the target field (e.g., `http://demo.testfire.net`).
3. Select **"Blue Team"** as the team approach.
4. Select **"Claude"** in the AI Analysis dropdown.
5. Click **"Run Blue Team Scan."**
6. Wait for the scan to complete and observe the AI Analysis panel.

## Actual Result
The scan phase completes successfully, but the subsequent AI Analysis request triggers an **HTTP 400 Bad Request** in the background. The AI Analysis field renders the message: **"failed to fetch"** — indicating the outgoing payload to the Claude API endpoint is malformed or incorrectly structured.

## Expected Result
Upon scan completion, the application should serialize the collected network response data into a correctly formatted request payload conforming to the Claude API contract, dispatch it successfully, and render the full vulnerability analysis returned by the model inside the AI Analysis panel.

