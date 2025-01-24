Vulnerability Detection Tool
A comprehensive tool designed for detecting common vulnerabilities like SQL Injection, Cross-Site Scripting (XSS), and more. This tool aims to assist in bug bounty hunting and security testing by providing automated checks for these vulnerabilities.

Features
     !SQL Injection Detection: Identifies potential SQL injection vulnerabilities by testing input fields and URL parameters.
     
     !XSS Detection: Scans for Cross-Site Scripting (XSS) vulnerabilities in web applications by detecting input handling flaws.
     
     !Customizable Scan: You can extend the tool to add additional vulnerability checks as required.
     
Installation
Follow the steps below to install and run the tool.

Prerequisites
Python 3.6 or higher
pip (Python package installer)
pip install requests

Usage
To use the Cyber_Prasanna tool, run the following command:

bash
Copy
Edit
python scanner.py --url <target_url> --scan <scan_types> --params <params> --headers <headers>
Arguments:
--url <target_url>: The target URL to test for vulnerabilities (e.g., http://example.com).
--scan <scan_types>: A comma-separated list of scan types to run. Available options: xss, sqli. For example, xss,sqli.
--params <params>: Optional. Parameters to test in the format key=value. For example, id=1 for testing URL parameters.
--headers <headers>: Optional. Custom headers to include in the request, in the format key=value.
Example Usage:
Scanning for XSS and SQLi on http://example.com with parameters id=1 and name=test:

bash
Copy
Edit
python scanner.py --url http://example.com --scan xss,sqli --params id=1 name=test
Scanning for only XSS on http://example.com with custom headers:

bash
Copy
Edit
python scanner.py --url http://example.com --scan xss --params id=1 --headers User-Agen
