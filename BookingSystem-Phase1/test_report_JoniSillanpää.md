# 1️⃣ Introduction

**Tester(s):**  
- Name: Joni Sillanpää 

**Purpose:**  
- Describe the purpose of this test (e.g., identify vulnerabilities in registration and authentication flows).

**Scope:**  
- Tested components:  
- Exclusions:  
- Test approach: Gray-box / Black-box / White-box

**Test environment & dates:**  
- Start:  21:02
- End:  21:03
- Test environment details (OS, runtime, DB, browsers):

**Assumptions & constraints:**  
- e.g., credentials provided, limited time, etc.

---

# 2️⃣ Executive Summary

**Short summary (1-2 sentences):**  

**Overall risk level:** (Low / Medium / High / Critical)

**Top 5 immediate actions:**  
1.  Implement unpredictable CSRF per session tokens
2.  Set Content Security Policy (CSP) Header
3.  Deny the usage of iframe
4.  Replace detailed error messages with generic ones
5.  Use nosniff on all responses

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|     🟠 **Medium**    | Absence of Anti-CSRF Tokens.                                                                                                 | *Immediate fix required*         |
|     🟠 **Medium**    | Content Security Policy (CSP) Header Not Set.                                                                                | *Fix ASAP*                       |
|     🟠 **Medium**    | Missing Anti-Clickjacking Header.                                                                                            | *Fix soon*                       |
|     🟡 **Low**       | Application Error Disclosure.                                                                                                | *Monitor and fix in maintenance* |
|     🟡 **Low**       | X-Content-Type-Options Header Missing.                                                                                       | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🟠 Medium | Absence of Anti-CSRF Tokens | No Anti-CSRF tokens were found in a HTML submission form | <form action="/register" method="POST"> |
| F-02 | 🟠 Medium | Content Security Policy (CSP) Header Not Set | Not safe against XSS and data injection attacks |  |
| F-03 | 🟠 Medium | Missing Anti-clickjacking Header | The response does not protect against 'ClickJacking' attacks |  |
| F-04 | 🟡 Low | Application Error Disclosure | This page contains an error/warning message that may disclose sensitive information | HTTP/1.1 500 Internal Server Error |
| F-05 | 🟡 Low | X-Content-Type-Options Header Missing | The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff' |  |

---

> [!NOTE]
> Include up to 5 findings total.   
> Keep each description short and clear.

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).

---

**Instructions:**
1. Check lecture recordings
2. Save the report as `zap_report_round1.md` and link it below.

---
> [!NOTE]
> 📁 **Attach full report:** → `check itslearning` → **Add a link here**

---
