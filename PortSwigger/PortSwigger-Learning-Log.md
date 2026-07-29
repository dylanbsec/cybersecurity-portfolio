# PortSwigger Learning Log

This file tracks my progress through the PortSwigger Web Security Academy, including topics studied, labs completed and practical skills developed using Burp Suite.

---

## Entry 001 - Burp Suite Basics

**Date:** 30 June 2026  
**Focus:** Intercepting HTTP requests using Burp Suite

### What I Learned

I learned how to use Burp Suite's built-in browser and Proxy tool to intercept HTTP requests between the browser and a web application.

I practised:

- Opening Burp Suite's embedded browser
- Enabling and disabling Intercept
- Capturing HTTP requests
- Viewing request methods, paths and headers
- Forwarding intercepted requests to the server

### Reflection

This helped me understand the basic workflow of using Burp Suite as an interception proxy. I can now capture a request before it reaches the server and inspect the information being sent by the browser.

---

## Entry 002 - Path Traversal

**Date:** 8 July 2026  
**Focus:** Understanding path traversal vulnerabilities

### What I Learned

Path traversal, also known as directory traversal, is a vulnerability that can allow an attacker to access files outside of the directory intended by a web application.

A vulnerable application may take user-controlled input, such as a filename, and append it to a directory path on the server.

For example:

```text
/loadImage?filename=218.png
```

---

## Entry 003 - Access Control Fundamentals

**Date:** 13 July 2026

**Focus:** Understanding access control and vertical privilege escalation.

### Topics Covered

- Access control
- Authentication
- Session management
- Vertical privilege escalation
- Unprotected functionality
- robots.txt information disclosure

### Reflection

I learned that access control determines whether an authenticated user is authorised to perform a specific action or access a resource. Effective access control relies on authentication to verify a user's identity and session management to maintain that identity across requests.

I also learned about **vertical privilege escalation**, where a user gains access to functionality intended for users with higher privileges, such as an administrator.

To reinforce these concepts, I completed the **Unprotected Admin Functionality** lab. The lab demonstrated how sensitive administrative pages can sometimes be exposed due to missing access controls. By reviewing the application's `robots.txt` file, I discovered the hidden administrator panel and successfully accessed it to delete the user **carlos**, completing the exercise.

This highlighted that hiding functionality is not the same as securing it. Sensitive pages must be protected by proper access control rather than relying on obscure URLs.

### Next Steps

- Continue the Access Control learning path.
- Learn additional privilege escalation techniques.
- Explore common access control vulnerabilities and how to identify them.

---

## Entry 004 - Access Control: Unprotected Functionality & Parameter-Based Access Control

**Date:** 15 July 2026

**Focus:** Identifying hidden administrative functionality and exploiting insecure access control mechanisms.

### Topics Covered

- Security through obscurity
- Unprotected admin functionality
- Inspecting page source
- JavaScript information disclosure
- Parameter-based access control
- Cookie-based privilege escalation

### Reflection

I continued studying access control vulnerabilities through the PortSwigger Web Security Academy and completed two practical labs.

The first lab demonstrated that hiding sensitive functionality behind an unpredictable URL is not an effective security measure. By inspecting the page source, I found JavaScript containing the hidden administrator panel URL and used it to access the admin interface and delete the user **carlos**.

The second lab explored parameter-based access control. After logging in as a normal user, I intercepted the server's response using Burp Suite and identified a cookie (`Admin=false`) used to determine administrative privileges. By modifying the cookie to `Admin=true`, I successfully gained access to the admin panel and completed the lab by deleting **carlos**.

These exercises reinforced that client-side values such as JavaScript, cookies and request parameters should never be trusted for enforcing access control, as they can be viewed and modified by an attacker.

### Next Steps

- Continue the Access Control learning path.
- Explore horizontal privilege escalation techniques.
- Gain more experience identifying insecure client-side access control mechanisms.

---

## Entry 005 - Access Control: Horizontal Privilege Escalation

**Date:** 29 July 2026

**Focus:** Exploiting horizontal privilege escalation vulnerabilities and understanding how they can lead to administrative compromise.

### Topics Covered

- Horizontal privilege escalation
- Insecure Direct Object References (IDOR)
- GUID-based identifiers
- Parameter tampering
- Password disclosure
- Horizontal to vertical privilege escalation

### Reflection

I continued the Access Control learning path in PortSwigger Web Security Academy and completed two practical labs covering horizontal privilege escalation.

The first lab demonstrated an IDOR vulnerability where user accounts were identified using GUIDs instead of sequential IDs. Rather than following the walkthrough exactly, I inspected the page source to discover Carlos' GUID before modifying the `id` parameter to access his account and retrieve his API key. This was the first PortSwigger lab I completed entirely on my own, which gave me confidence that I am beginning to recognise vulnerabilities independently.

The second lab demonstrated how horizontal privilege escalation can lead to vertical privilege escalation. By modifying the `id` parameter to reference the administrator's account, I was able to obtain the administrator's password from the page source, log in as the administrator and delete the user **carlos**.

These labs reinforced that using GUIDs alone does not provide effective access control, and that sensitive information should never be exposed to users simply because a request parameter has been modified.

### Next Steps

- Continue the Access Control learning path.
- Gain more experience identifying IDOR vulnerabilities.
- Improve my use of Burp Suite alongside browser developer tools when analysing requests and responses.
