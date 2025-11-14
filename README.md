# security-header-checker
A lightweight Python tool for quick AppSec checks. It scans a target URL for essential HTTP security headers like CSP, HSTS, and X-Frame-Options, helping identify missing protections and weak configurations during web application security reviews.

How to Use

Clone the repository:

git clone https://github.com/yourusername/security-header-checker.git
cd security-header-checker

Install the required dependency:
pip install requests

Run the script:
python header_checker.py

Enter the target URL when prompted (e.g., https://example.com).

The tool will scan the site and report which critical security headers are present or missing, helping you quickly validate web application security configurations during assessments, audits, or AppSec workflows.
