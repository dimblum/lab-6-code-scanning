# Answers to Part 3

Add your answers to the questions in Part 3, Step 2 below. 

## Vulernability Remediation:
### Vulnerability 1: 
1. Which package or library are you addressing?
pkg:pypi/pyyaml@5.1
2. Which CVE is linked to this vulnerability?
CVE-2020-14343
3. What remediation steps do you suggest?
Upgrade PyYAML to version 5.4 or higher, since versions <5.4 are affected. In addition, replace calls to `yaml.load()` with `yaml.safe_load()` when parsing YAML input to avoid arbitrary code execution.

https://pyyaml.org/wiki/PyYAMLDocumentation
https://nvd.nist.gov/vuln/detail/CVE-2020-14343

### Vulnerability 2:
1. Which vulnerability are you addressing?
Pillow (pkg:pypi/pillow@9.4.0)

3. Which CVE is linked to this vulnerability?
CVE-2023-50447

5. What remediation steps do you suggest? 
Upgrade Pillow to version 10.2.0 or higher in `requirements.txt` and redeploy the application.
This removes the vulnerable code paths that allow malicious image files to trigger arbitrary code execution.

https://nvd.nist.gov/vuln/detail/CVE-2023-50447
https://pillow.readthedocs.io/en/stable/releasenotes/10.2.0.html
