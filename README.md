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
        # optional param to check for vulnerabilities on the package-lock.json
        # in order to use that you need to have this file on your repository
        with:
          check_packages_vulnerabilities: true
```

the security ninja code scanner will automatically scan your code changes whenever you create or commit to a pull request. if it detects any security issues or secrets, it will write a comment on the pull request with a detailed report of the problem.

by default, the security ninja code scanner will scan your entire code repository for security issues and secrets. 

### output

when the security ninja code scanner detects a security issue or secret, it will write a comment on the pull request with a report of the problem. 

the report will include information about where the issue was found, such as the file name and line number, as well as a description of the issue and recommendations on how to address it.

#### the ninja dojo

you can also check the [security-ninja-code-scanner-dojo](https://github.com/agencyenterprise/security-ninja-code-scanner-dojo) repository for an example of how to use this action in practice. 

this repository includes example code that demonstrates how to configure and run various security tests with this action.

- [sample of a pull request](https://github.com/agencyenterprise/security-ninja-code-scanner-dojo/pull/1)
- [sample of action](https://github.com/agencyenterprise/security-ninja-code-scanner-dojo/actions/runs/4421055944/jobs/7751454717)
- [sample of the workflow file](https://github.com/agencyenterprise/security-ninja-code-scanner-dojo/blob/my-buggy-pr/.github/workflows/security-ninja-code-scanner.yml)

### a white belt ninja?

we take security very seriously. that's why we've enlisted the help of our trusty security ninja code scanner - our very own white belt ninja who tirelessly scans our codebase for vulnerabilities.

now, we know what you're thinking - a white belt ninja? isn't that like asking a toddler to help you with quantum mechanics? but don't let the color of our ninja's belt fool you - this little guy may be a novice, but he's got some serious moves when it comes to finding security issues.

of course, even our ninja can't catch everything, which is why we've also put together a comprehensive [security checklist guide](https://app.gitbook.com/o/-MKgZVdiD84BirEX9cXC/s/yTDqgcPmFQjEpoU9fDJt/security/application-security-checklist) to help you stay on top of your security game. so whether you're a seasoned security expert or just getting started, our ninja and our guide are here to help you keep your codebase as secure as possible.

#### do you need more?

if you're still feeling paranoid (or just want to make sure you're doing everything right), that is ok, we feel that too. that's why we've developed our own secret weapon - the [static application security testing (sast) guide](https://app.gitbook.com/o/-MKgZVdiD84BirEX9cXC/s/yTDqgcPmFQjEpoU9fDJt/security/static-application-security-testing). with our guide, you'll be able to channel your inner james bond and protect your code like it's the world's most valuable treasure.

now, we know what you're thinking - "static application security testing" sounds about as exciting as a filing cabinet. but trust us - it's a good way to keep your code safe from all kinds of attacks. with sast, you can run automated tests to check for vulnerabilities, making sure your app stays as secure as fort knox.

so, if you're ready to become a security superhero (or just want to impress your friends with your newfound security skills), check out our [static application security testing guide](https://app.gitbook.com/o/-MKgZVdiD84BirEX9cXC/s/yTDqgcPmFQjEpoU9fDJt/security/static-application-security-testing). we promise it's more fun than a night at the casino - and a lot safer, too!
