# security ninja code scanner

this github action performs a security scan on your code repository and detects any potential security vulnerabilities or secrets that may be present. the security ninja code scanner uses a variety of techniques to identify and report potential issues, helping you to keep your codebase secure and your secrets safe

### how to use
to use the Security Ninja Code Scanner action in your gitHub actions workflow, you can add the following step to your workflow yaml file (`.github/workflows/security-ninja-code-scanner.yml`):

```yaml
name: security ninja code scanner
on:
  pull_request:
    types:
      - opened
      - synchronize
      - reopened

permissions:
  contents: read
  id-token: write
  issues: write
  pull-requests: write
  checks: write

jobs:
  katana-check:
    runs-on: ubuntu-latest

    steps:
      - name: start blade dance
        uses: agencyenterprise/security-ninja-code-scanner@v2
```

the security ninja code scanner will automatically scan your code changes whenever you create or commit to a pull request. if it detects any security issues or secrets, it will write a comment on the pull request with a detailed report of the problem.

by default, the security ninja code scanner will scan your entire code repository for security issues and secrets. 

### output

when the security ninja code scanner detects a security issue or secret, it will write a comment on the pull request with a report of the problem. 

the report will include information about where the issue was found, such as the file name and line number, as well as a description of the issue and recommendations on how to address it.
