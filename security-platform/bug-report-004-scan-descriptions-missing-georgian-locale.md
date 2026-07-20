# [BUG-004] Scan Type Descriptions Remain Hardcoded in English Under Georgian Locale

## Metadata
- **Project**:  AI-Augmented Security Scanning Platform
- **Component**: Internationalization (i18n) / Scan Configuration UI
- **Type**: Bug / Localization
- **Severity**: Low
- **Priority**: Low
- **Status**: Open

## Environment Details
- **Platform**: Web
- **App Context**: Security Scan configuration and results page under Georgian language setting

## Steps to Reproduce
1. Set the application interface language to **Georgian**.
2. Navigate to the **Security Scan** page.
3. Observe the informational text blocks and scan type description strings (e.g., explanatory subtitles describing what each scan type does).

## Actual Result
Core navigation buttons, labels, and interface framework elements are correctly translated into Georgian. However, the descriptive content strings explaining individual scan actions and scan type behaviors remain **hardcoded in English** — bypassing the localization layer entirely.

## Expected Result
All user-facing text — including placeholder strings, instructional guides, scan type descriptions, and explanatory subtitles — must be routed through the application's i18n resource bundle and fully localized into Georgian to maintain linguistic consistency across the interface.

