# Security Policy

Security reports are taken seriously in binkru.

This policy describes what should be reported as a security issue and how security concerns are distinguished from issues with the Engineering Operating Model itself.

## Scope

binkru currently consists primarily of the Engineering Operating Model, its specifications, documentation, and related repository material.

The project may also include supporting software, automation, examples, generated artifacts, or other implementation components over time.

This security policy applies to vulnerabilities in repository content or implementation components where disclosure could create a meaningful security risk to users, contributors, adopters, or their environments.

## What to report

Examples of issues that should be reported as security vulnerabilities include:

- vulnerabilities in software or automation distributed by binkru;
- unsafe execution behavior that could permit unintended code execution or privilege use;
- handling of credentials, secrets, tokens, or other sensitive information that could expose them;
- vulnerabilities in generated or supplied configuration that could create an exploitable security condition;
- dependency or supply-chain issues that materially affect components distributed by the project; and
- other defects where public disclosure before remediation could create a meaningful security risk.

If you are uncertain whether an issue has security implications, reporting it privately is preferable to disclosing a potentially exploitable vulnerability publicly.

## Engineering model issues

Not every issue involving security, authority, governance, or trust in the Engineering Operating Model is a security vulnerability.

Examples that should normally be raised through the project's regular contribution or issue process include:

- ambiguity or inconsistency in an Engineering specification;
- disagreement with an architectural decision;
- missing or insufficiently defined governance semantics;
- proposed changes to authority, responsibility, lifecycle, or provenance semantics;
- terminology issues;
- conformance questions; and
- improvements to security-related architectural guidance that do not expose an exploitable vulnerability.

These may be important architectural concerns, but they should not use the private security-reporting process unless disclosure itself could create a meaningful security risk.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for guidance on proposing changes to the Engineering Operating Model.

## Reporting a vulnerability

Do not disclose a suspected vulnerability through a public issue, pull request, discussion, or other public project channel before it has been assessed.

To report a vulnerability privately:

Use GitHub's private vulnerability reporting for this repository. From the repository, open **Security and quality**, select **Advisories**, and choose **Report a vulnerability**.

Please include, where possible:

- a description of the vulnerability;
- the affected component, file, version, or revision;
- steps required to reproduce or demonstrate the issue;
- the potential security impact;
- any known conditions required for exploitation; and
- any suggested remediation, if available.

Do not include sensitive credentials, personal information, or unrelated confidential material in a report.

## What to expect

Security reports will be reviewed to determine their applicability, impact, and appropriate handling.

Where a reported issue is confirmed as a vulnerability, the project will determine an appropriate remediation and disclosure approach based on the nature and severity of the issue.

Where a report is determined to be an architectural, documentation, conformance, or other non-security issue, it may be redirected to the normal project contribution process.

No specific response or remediation timeframe is guaranteed by this policy.

## Supported versions

binkru does not currently maintain multiple supported release lines.

Security fixes, when applicable, will target the version or revision of the project that is actively maintained at the time the issue is addressed.

This section may be revised if binkru establishes versioned releases with explicit support periods.

## Disclosure

Please allow reasonable time for a reported vulnerability to be assessed and, where necessary, remediated before public disclosure.

Coordinated disclosure helps protect users and adopters while a security issue is being addressed.
