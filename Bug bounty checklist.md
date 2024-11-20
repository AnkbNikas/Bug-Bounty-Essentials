# Information gathering:
Enumerate subdomains and directories
Identify web technologies used (e.g., JavaScript libraries, CMS, server software)
Look for default installations, test pages, and exposed sensitive files (e.g., backup files, Git directories, logs)
Review public resources (e.g., documentation, GitHub repositories, support forums)

# Authentication and authorization:
Test for weak credentials, password reuse, and password reset vulnerabilities
Check for authentication bypass and session management issues
Test role-based access control and vertical/horizontal privilege escalation
Verify proper enforcement of CORS policies

# Input validation and output encoding:
Test for Cross-site Scripting (XSS), both reflected and stored
Test for SQL Injection (SQLi) and other injection vulnerabilities (e.g., command, LDAP, XPath)
Test for XML External Entity (XXE) attacks
Check for Open Redirect vulnerabilities
Test for insecure deserialization vulnerabilities

# Business logic vulnerabilities:
Test for Insecure Direct Object Reference (IDOR) issues
Check for rate limiting and brute force protection
Examine multi-step processes for logic flaws (e.g., shopping carts, registration)
Test for data leakage through cache and history poisoning

# Server-side vulnerabilities:
Test for server-side vulnerabilities like remote code execution (RCE), local file inclusion (LFI), and remote file inclusion (RFI)
Test for Server-Side Request Forgery (SSRF) vulnerabilities
Check for server misconfigurations, including weak TLS/SSL cipher suites, insecure HTTP headers, and exposed error messages
Test for path traversal vulnerabilities

# Client-side vulnerabilities:
Test for Cross-Site Request Forgery (CSRF) vulnerabilities
Examine JavaScript code for vulnerabilities (e.g., client-side validation, DOM-based XSS)
Check for Clickjacking and other UI redressing attacks
Test for HTML5 postMessage vulnerabilities

# Web APIs:
Enumerate API endpoints and methods
Test for authentication, authorization, and rate limiting issues
Check for parameter tampering and injection vulnerabilities
Test for improper handling of data formats (e.g., JSON, XML)

# Third-party components and integrations:
Check for vulnerabilities in third-party libraries, plugins, or themes
Test for OAuth misconfigurations and other issues related to Single Sign-On (SSO)
Review APIs and other integrations for proper security configurations

# Mobile application components:
Test for insecure communication between mobile apps and web servers
Check for mobile-specific issues such as insecure storage of sensitive data
Assess mobile app-specific vulnerabilities, like deep linking or WebView issues
