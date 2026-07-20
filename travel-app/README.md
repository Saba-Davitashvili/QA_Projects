# Project 1 — Social Travel & Booking Platform

## Overview
A full-featured social platform combining a content feed, real-time messaging, interactive map, and hotel/restaurant/tour booking — tested across both mobile (Android) and web platforms, backed by a mix of live and mock APIs.

## Scope
- **Platforms**: Android (Mobile) · Web
- **Testing Type**: Manual QA
- **Test Cases Written**: 83 (Mobile)
- **Feature Modules**: Login/Registration · Feed · Profile · Messenger & Notifications · Explore & Bookings · Hotel Listings · Stories · Settings

## Technical Risk Areas
- Token persistence across dual logout mechanisms (menu logout vs. settings logout)
- WebSocket connection lifecycle and reconnect behavior
- Dual-phase feed pagination (Following → For You)
- Mixed real/mock API modules in the same app
- Video autoplay state control on scroll
- Photo lightbox event propagation and profile navigation routing
- Client-side state synchronization on delete operations
- Cross-field validation on booking restriction forms

---

## Mobile (Android)

### Feature Modules

| Module | Test Cases | Focus Areas |
|---|:---:|---|
| Login & Registration | 16 | OTP, rate limiting, deep links, session cleanup |
| Feed Flow | 18 | Pagination, autoplay, stories, post CRUD, map, search |
| Profile Flow | 18 | Dual logout, edit profile, security, 2FA, lists |
| Messenger & Notifications | 20 | WebSocket, voice notes, real-time updates |
| Explore & Bookings | 11 | Hotel search, booking checkout, cancellation |

### Bug Reports — 18 Defects

| Bug ID | Component | Summary | Severity |
|---|---|---|---|
| BUG-001 | Authentication | Missing UI validation on forgot password submission |  Medium |
| BUG-002 | Registration | False validation highlight on duplicate email |  Medium |
| BUG-003 | Profile / Security | Email change allowed without verification | Medium |
| BUG-004 | Authentication | Generic offline login error surfaced |  Medium |
| BUG-005 | Authentication | Technical error code shown to end user |  Medium |
| BUG-006 | Registration | Missing age limit registration check |  Medium |
| BUG-007 | Authentication / OTP | Verification code spam and token failures |  High |
| BUG-008 | Registration | UI freeze during registration submit |  High |
| BUG-009 | Authentication | Forgot password back button navigation loop |  Medium |
| BUG-010 | Authentication | Symbol requirement regex mismatch |  Medium |
| BUG-011 | Map / Permissions | Map location permission bypass |  Medium |
| BUG-012 | Messenger | Group chat UI navigation deadlock |  High |
| BUG-013 | Explore / Search | Tour search results sorting failure |  Medium |
| BUG-014 | Feed / Post Actions | Post context menu ellipsis unresponsive |  Medium |
| BUG-015 | Explore / Bookings | Booking stays CTA navigation failure |  Medium |
| BUG-016 | Messenger / Media | Chat media bubble preview caching error |  Medium |
| BUG-017 | Messenger / Media | Shared media video playback unresponsive |  Medium |
| BUG-018 | Messenger / Media | Image lightbox full UI freeze thread lock |  High |

See individual files in the `mobile/` folder.

---

## Web

### Bug Reports — 11 Defects

| Bug ID | Component | Summary | Severity |
|---|---|---|---|
| BUG-001 | Hotel Listing / Validation | Max stay accepted below min stay without validation |  Medium |
| BUG-002 | Feed / Block Pipeline | Block Profile action unresponsive from "Not Interested" menu |  High |
| BUG-003 | Stories / State Sync | Deleted story remains visible until manual page refresh | 🟠 Medium |
| BUG-004 | Chat / Navigation | "Visit Profile" from chat menu fails to navigate |  Medium |
| BUG-005 | Profile / Follow API | Follow button triggers 403 Forbidden network error |  High |
| BUG-006 | Profile / Social Graph | Followers and Following buttons unresponsive |  Medium |
| BUG-007 | Feed / Photo Lightbox | Post author navigation blocked in full-screen photo view |  Medium |
| BUG-008 | Feed / Photo Lightbox | Comment author navigation blocked in full-screen photo view |  Medium |
| BUG-009 | Feed / Photo Lightbox | Tagged user navigation blocked in full-screen photo view |  Medium |
| BUG-010 | Feed / Tag Routing | @mention click opens post instead of profile (event propagation) |  Medium |
| BUG-011 | Settings / Dropdown UI | Time zone and date format dropdown options visually overlap |  Low |

See individual files in the `web/` folder.
