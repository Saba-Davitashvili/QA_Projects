# Project 3 — On-Demand Gardening & Landscaping Service Platform

## Overview
A comprehensive web and mobile platform connecting residential and commercial clients with professional gardeners. The platform manages multi-step service requests, gardener bidding list matches, real-time client-gardener chat, automated pricing calculations, and localized notifications.

## Scope
- **Platform**: Web / Mobile (iOS & Android)
- **Testing Type**: Manual QA, UI/UX Verification, Localization Auditing, Edge Case Testing
- **Test Cases Written**: 74
- **Feature Modules**: Authentication · Request Creation & Matching · Billing & Invoice Invoicing · Support Chatbot · Gardener Portal

## Technical Risk Areas
- Float-rounding and precision loss on dynamic invoice calculations with 1.25x platform multipliers
- Session preservation and state synchronization when converting Guest users to registered accounts mid-booking
- Localization and language fallback consistency in Georgian/English UI sections (month formatting, date parsing)
- Element overlapping and layout responsiveness on small viewports for floating chatbot widgets
- Real-time event notifications routing to details pages for authenticated users

## Feature Modules

| Module | Focus Areas |
|---|---|
| **Authentication** | Google Sign-In token validation, guest mode account conversion |
| **Request & Matching** | Multi-step request wizard (steps 1–6), page state history tracking |
| **Billing & Calculations** | Linear pricing scaling, 1.25x platform fee breakdowns, decimal rounding |
| **Gardener Portal** | Price settings validation, gardener profile paths, pricing updates |
| **Support & Messaging** | Support chatbot widget, upload button debouncing, notification click routing |

## Bug Reports

Below is the index of the 22 detailed defect reports identified and resolved for this platform:

* [[BUG-001] Service Request Submission Fails When Authenticated via Google Sign-In](bug-report-001-google-sign-in-unresponsive.md)
* [[BUG-002] Additional Urgent Service Fee Excluded from Final Price Calculation](bug-report-002-urgent-fee-missing-calculation.md)
* [[BUG-003] Back Navigation from Gardener Profile Redirects to Step 1 Instead of Step 6](bug-report-003-back-navigation-state-loss.md)
* [[BUG-004] Price Discrepancy Displayed Between Customer Request and Gardener Offer Interfaces](bug-report-004-price-discrepancy-user-gardener-view-9.md)
* [[BUG-005] Decimal Price Values Rounded Up Erroneously After 1.25x Multiplier](bug-report-005-incorrect-rounding-multiplier.md)
* [[BUG-006] Gardener Base Service Rate Omitted from Price Breakdown Screen](bug-report-006-base-rate-missing-breakdown.md)
* [[BUG-007] Request a Service Button Becomes Unresponsive Post-Submission](bug-report-007-request-service-unresponsive-submit.md)
* [[BUG-008] View Request Button Unresponsive After Returning from Gardener Profile](bug-report-008-view-request-unresponsive-back-navigation.md)
* [[BUG-009] Service Price Input Accepts Alphabetic Characters and Falsely Indicates Success](bug-report-009-input-field-silent-save-failure.md)
* [[BUG-010] Spamming Send Button in Chatbot Widget Dispatches Duplicate Image Attachments](bug-report-010-chatbot-spam-send-duplicate-image.md)
* [[BUG-011] Gardener Profile Button Leads to Page Not Found Error Page](bug-report-011-gardener-profile-not-found.md)
* [[BUG-012] Raw Localization Key "common.profile" Rendered on Gardener List Card](bug-report-012-untranslated-card-button-label.md)
* [[BUG-013] Connect Button Unresponsive in Gardener List for Guest-Created Requests](bug-report-013-guest-mode-connect-button-unresponsive.md)
* [[BUG-014] Chatbot Widget Icon Overlaps Profile Navigation Button on Mobile Viewports](bug-report-014-chatbot-widget-overlaps-profile-mobile.md)
* [[BUG-015] English Month Names Displayed in Georgian UI on Requests Page](bug-report-015-month-localization-my-requests.md)
* [[BUG-016] Mixed-Language Registration Date Displayed in Georgian UI](bug-report-016-profile-registration-date-mixed-localization.md)
* [[BUG-017] Non-Linear Pricing Logic Deviation After Selecting Soil Preparation Service](bug-report-017-soil-preparation-pricing-calculation-threshold.md)
* [[BUG-018] Clicking Service Request Notification Redirects Gardener to Page Not Found Screen](bug-report-018-notification-redirects-page-not-found.md)
* [[BUG-019] Suggestion to Include 1.25x Platform Fee in Initial Quote Stage to Prevent User Trust Issues](bug-report-019-estimated-price-multiplier-quotes.md)
* [[BUG-020] Suggestion to Support Drag and Drop Interactions for Photo Uploads](bug-report-020-drag-drop-photo-upload-suggestion.md)
* [[BUG-021] Platform Commission Fee Omitted from Price Breakdown Screen](bug-report-021-platform-commission-fee-omitted-breakdown.md)
* [[BUG-022] Price Discrepancy Between Customer View and Gardener Offer View](bug-report-022-price-discrepancy-user-gardener-view-95.md)
