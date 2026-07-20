# [BUG-003] API Keys and Scan Progress Leak Between Accounts on Same Browser

## Metadata
- **Project**: AI-Augmented Security Scanning Platform
- **Component**: Session Isolation / Local Storage State Management
- **Type**: Bug / Session Leak / Data Isolation
- **Severity**: Critical
- **Priority**: High
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Settings page / Dashboard — cross-account session state on a single browser instance

## Steps to Reproduce
1. Authenticate as **Account A**, configure API keys in Settings, and initiate or complete one or more scans (generating progress state).
2. Log out of Account A.
3. Authenticate as **Account B** on the same PC and browser window.
4. Navigate to the **Settings** page and inspect the API key fields.
5. Navigate to the **Dashboard** and inspect scan progress charts.

## Actual Result
Account A's saved API keys and active scan progress metrics populate inside Account B's workspace. The leak is scoped to local storage and session state — specifically configuration keys and progress chart data. Execution outputs, uploaded files, and individual run test results remain correctly isolated per account.

## Expected Result
Account B's session must be fully isolated. On login, the application should purge or namespace all client-side storage (localStorage, sessionStorage, IndexedDB) on authorization transitions. API key fields should appear empty (unless separately configured for Account B), and scan history should reflect only Account B's distinct activity.

