# Security Testing Report

## 🛡️ Target: Sample Web Application (e.g., DVWA)

---

## 🔍 Vulnerabilities Identified

### 1. SQL Injection
- **Location**: Login form (`/login`)
- **Payload**: `' OR '1'='1`
- **Impact**: Bypasses authentication
- **Mitigation**:
  - Use parameterized queries (e.g., prepared statements)
  - Sanitize user inputs

### 2. Cross-Site Scripting (XSS)
- **Location**: Search box (`/search`)
- **Payload**: `<script>alert("XSS")</script>`
- **Impact**: Executes arbitrary JavaScript
- **Mitigation**:
  - Encode output before rendering to the browser
  - Use Content Security Policy (CSP)

---

## ✅ Recommendations
- Regularly test input fields for injection vulnerabilities.
- Use security linters and automatic scanners.
- Train developers on secure coding practices.

---

**Tools Used**:
- Burp Suite
- OWASP ZAP
- Manual testing with browser developer tools