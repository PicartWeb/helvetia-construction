# Security Policy

## Supported Project

This repository is a static portfolio website demo. It does not include a backend, database, authentication system, payment flow, or server-side form handling.

## Reporting a Vulnerability

If you find a security issue related to this repository, please contact Picart Web privately:

```text
info@picartweb.com
```

Please include:

- A clear description of the issue
- Steps to reproduce
- Affected file or URL
- Suggested fix, if available

Please do not open public issues for sensitive vulnerabilities.

## Scope

In scope:

- Static HTML/CSS/JavaScript security issues
- Unsafe external links or embeds
- Incorrect security headers
- Deployment configuration problems

Out of scope:

- Vulnerabilities in third-party platforms not controlled by Picart Web
- Browser extension behavior
- Issues caused by modified forks
- Server misconfiguration outside this repository's `.htaccess`

## Deployment Notes

The included `.htaccess` adds baseline security headers and disables directory listing. Production server configuration should still be reviewed by the hosting provider or site owner.
