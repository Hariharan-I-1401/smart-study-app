# Security Policy

We take the security and privacy of our users seriously. Since this Smart Learning App processes live camera data (eye-tracking) and document uploads, maintaining a secure ecosystem is our top priority.

## Supported Versions

Only the latest version of the application currently receives active security updates and patches.


| Version | Supported          |
| ------- | ------------------ |
| Main    | ✅ Yes             |
| < Main  | ❌ No              |

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.** 

If you discover a security vulnerability (such as data leaks, camera feed exploits, file upload bypasses, or injection flaws), please report it responsibly by following these steps:

1. **Email the Maintainer**: Send a detailed report to **hariharani1401@gmail.com**.
2. **Include Details**: To help us verify and fix the issue quickly, please provide:
   * A clear description of the vulnerability.
   * Step-by-step instructions or a Proof of Concept (PoC) script to reproduce it.
   * The potential impact (e.g., unauthorized data access, server crash).
3. **Wait for Resolution**: Please allow us reasonable time to investigate, address, and patch the issue before making any information public.

## Security Practices for Contributors

If you are contributing code to this repository, please keep the following security principles in mind:
* **Local Data Handling**: Ensure that all face and eye-tracking metrics calculated from the live video feed are processed safely and do not expose raw video frames to unauthorized endpoints.
* **Input Sanitization**: Always sanitize and validate files uploaded to the `uploads/` directory to prevent malicious file executions or path traversal attacks via `PyPDF2`.
* **Database Security**: Ensure that the SQLite database engine utilizes parameterized queries (via Pydantic/SQLAlchemy) to protect against SQL Injection vulnerabilities.
