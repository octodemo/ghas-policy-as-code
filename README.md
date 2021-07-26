# Demo GHAS 

Code Scanning Alerts & Dependency Alerts on non-default Branches

#### WebGoat 8: A deliberately insecure Web Application

This is a copy of WebGoatm, a deliberately insecure web application maintained by [OWASP](http://www.owasp.org/) designed to teach web
application security lessons.

#### :rotating_light: Do not use it to demo features not related to GHAS Code Scanning and Vulnerabilities alerts on non-default branches

This program is a demonstration of common server-side application flaws. The
exercises are intended to be used by people to learn about application security and
penetration testing techniques.

**WARNING 1:** *While running this program your machine will be extremely
vulnerable to attack. You should disconnect from the Internet while using
this program.*  WebGoat's default configuration binds to localhost to minimize
the exposure.

**WARNING 2:** *This program is for educational purposes only. If you attempt
these techniques without authorization, you are very likely to get caught. If
you are caught engaging in unauthorized hacking, most companies will fire you.
Claiming that you were doing security research will not work as that is the
first thing that all hackers claim.*

## How to use it
In order to install and run it, check out the [original demo](https://github.com/octodemo/WebGoat) created by @bas

#### `codeql.yml`
Workflow with the CodeQL analysis. Runs at 0:00 UTC on Sunday.

You can check the results of its runs on the [Security Tab](https://github.com/octodemo/demo-vulnerabilities-ghas/security/code-scanning).

#### `dependencies.yml`
Workflow that checks every new PR that changes dependencies files. If the PR introduces dependencies with known vulnerabilities, it fails. PRs that don't change dependencies are not checked.

Uses [this Action](https://github.com/marketplace/actions/scan-a-pr-for-vulnerable-dependencies) to perform the analysis on non-default branches. The Action uses GitHub's [SecurityVulnerability API](https://developer.github.com/v4/object/securityvulnerability/)
