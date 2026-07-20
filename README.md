# Portfolio — Saba Davitashvili

### About me 👋
Hi, my name is Saba. I am a QA Manual Engineer passionate about software quality, precision testing, and system stability. I specialize in identifying critical edge cases, structural race conditions, cache leaks, and API discrepancies. My goal is to ensure that software is not only functional but highly resilient and secure. In this portfolio, I share my technical skills, tools of choice, and showcase real-world QA testing samples from my workspaces.

[My LinkedIn profile](https://linkedin.com)

---

### Tools 🔧
* **Jira / Trello** - Agile project management and bug tracking
* **Confluence** - Test documentation and knowledge sharing
* **Postman** - REST API manual testing and parameter validation
* **Maestro** - Mobile user journey flow automation
* **Chrome DevTools** - Inspector, network payload analysis, cookies/session auditing, and debugging
* **Git & GitHub** - Version control and collaborative repository management
* **Markdown** - Writing structured test plans and detailed bug logs
* **Slack / MS Teams** - Seamless communication within cross-functional teams

---

### Tech skills 💻
* **Manual Testing Practices:** Smoke testing, regression testing, UAT, exploratory testing, security validation, and boundary value analysis.
* **API Testing:** JSON payload verification, response code validation (2xx, 4xx, 5xx), header and session cookie auditing.
* **Mobile & Web Testing:** Cross-platform validation (Android & iOS tracks), viewport reload handling, and history state verification.
* **RAG & AI Testing:** Evaluating LLM grounding, RAG catalog validation, and testing stochastic model behavior for consistency.

---

### Soft skills 📁
* **Precision & Analytical Thinking** - Isolating root causes of intermittent or race-condition bugs.
* **Clear Technical Writing** - Writing developer-friendly steps to reproduce with expected vs. actual outcomes.
* **Assertiveness & Collaboration** - Constructively reporting defects and working closely with developers.
* **Empathy** - Always testing from the end-user's perspective to ensure maximum accessibility and usability.

---

### Certifications & Courses 📓
* **ISTQB Certified Tester** - Foundation Level (Syllabus Knowledge)
* **API Testing Masterclass** - Handshake validation, request methods, and session management
* **Mobile Automation Fundamentals** - Building end-to-end user flows in Maestro

---

### Samples 🔬

#### **1. Social Travel & Booking Platform**
A full-featured social platform combining a content feed, real-time messaging, interactive map, and hotel/restaurant/tour booking — tested across both mobile (Android) and web platforms.
* [Test Plan & Strategy](travel-app/README.md)
* [83 Comprehensive Test Cases Index](travel-app/README.md#feature-modules)

  **Mobile (Android) — 18 Defect Reports:**
  * [BUG-007: Verification Code Spam & Token Failures](travel-app/mobile/bug-report-007-multiple-otp-dispatch-failure.md)
  * [BUG-008: UI Freeze During Registration Submit](travel-app/mobile/bug-report-008-ui-freeze-on-registration-submit.md)
  * [BUG-012: Group Chat UI Navigation Deadlock](travel-app/mobile/bug-report-012-group-chat-ui-deadlock.md)
  * [BUG-018: Image Lightbox Full UI Freeze Thread Lock](travel-app/mobile/bug-report-018-chat-image-view-freeze-deadlock.md)
  * [Read full list →](travel-app/README.md#bug-reports--18-defects)

  **Web — 11 Defect Reports:**
  * [BUG-002: Block Profile Action Unresponsive from "Not Interested" Menu](travel-app/web/bug-report-002-block-profile-action-unresponsive.md)
  * [BUG-005: Follow Button Triggers 403 Forbidden Network Error](travel-app/web/bug-report-005-follow-button-403-error.md)
  * [BUG-010: @Mention Click Opens Post Instead of Profile](travel-app/web/bug-report-010-tagged-user-opens-post-instead-of-profile.md)
  * [Read full list →](travel-app/README.md#bug-reports--11-defects)

#### **2. AI-Powered E-commerce Search & Chatbot Platform**
An e-commerce storefront integration utilizing elasticsearch queries and a generative AI chatbot widget based on Retrieval-Augmented Generation (RAG).
* [Master Testing Scope](ai-ecommerce-chatbot/README.md)
* **5 Detailed Defect Reports:**
  * [BUG-001: Chatbot WebSocket Failure on Apex Domain](ai-ecommerce-chatbot/bug-report-001-websocket-apex-domain.md)
  * [BUG-002: DOM Freeze on Rapid Interactive Refreshes](ai-ecommerce-chatbot/bug-report-002-dom-freeze-rapid-refreshes.md)
  * [BUG-003: Elasticsearch Parameter Filter Overwrite](ai-ecommerce-chatbot/bug-report-003-search-filter-overwrite.md)
  * [BUG-004: Chatbot Fabricated Product/Inventory RAG Hallucination](ai-ecommerce-chatbot/bug-report-004-rag-hallucination.md)
  * [BUG-005: Non-Deterministic / Stochastic Response Divergence](ai-ecommerce-chatbot/bug-report-005-stochastic-response-divergence.md)

#### **3. Gardening & Landscaping Service Platform**
A comprehensive web and mobile platform connecting residential and commercial clients with professional gardeners.
* [Test Plan & Strategy](gardening-services-platform/README.md)
* **22 Detailed Defect Reports:**
  * [BUG-001: Service Request Submission Fails When Authenticated via Google Sign-In](gardening-services-platform/bug-report-001-google-sign-in-unresponsive.md)
  * [BUG-002: Additional Urgent Service Fee Excluded from Final Price Calculation](gardening-services-platform/bug-report-002-urgent-fee-missing-calculation.md)
  * [BUG-005: Decimal Price Values Rounded Up Erroneously After 1.25x Multiplier](gardening-services-platform/bug-report-005-incorrect-rounding-multiplier.md)
  * [Read full list →](gardening-services-platform/README.md)

#### **4. Professional Occupational Safety & Risk Management Platform**
A B2B cloud-native platform providing professional occupational health and safety (OHS) services — including work environment assessments, risk management, and compliance recommendations via a lead intake engine.
* [Test Plan & Strategy](occupational-safety-portal/README.md)
* **6 Detailed Defect Reports:**
  * [BUG-001: Alphanumeric clipboard paste bypasses numeric filter in phone input](occupational-safety-portal/bug-report-019-scientific-notation-input-bypass.md)
  * [BUG-003: Missing string length constraint allows uncapped data injection](occupational-safety-portal/bug-report-021-missing-input-length-constraint.md)
  * [BUG-004: Dot/period dividers bypass format checks on phone fields](occupational-safety-portal/bug-report-022-insufficient-input-sanitization.md)
  * [Read full list →](occupational-safety-portal/README.md)

#### **5. AI-Augmented Security Scanning Platform**
A web-based cybersecurity platform integrating multi-provider LLM analysis (Claude, Grok, Groq, Gemini, OpenAI) with automated security scanning workflows, AI-powered vulnerability analysis, and multi-language localization.
* [Test Plan & Strategy](security-platform/README.md)
* **4 Detailed Defect Reports:**
  * [BUG-001: AI Analysis HTTP 400 / "Failed to Fetch" on Blue Team Scan](security-platform/bug-report-001-ai-analysis-http400-scan-failure.md)
  * [BUG-002: AI Chat Fails Across All LLM Providers Despite Valid Keys](security-platform/bug-report-002-ai-chat-all-providers-auth-failure.md)
  * [BUG-003: API Keys & Scan Progress Leak Between Accounts](security-platform/bug-report-003-cross-account-session-state-leak.md)
  * [Read full list →](security-platform/README.md#bug-reports)
