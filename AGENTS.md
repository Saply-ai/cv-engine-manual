# cv-engine-manual

HTML user manual for CV Engine, the email-based service that formats, translates, tailors, and anonymizes CVs into chosen templates. GitHub repo in the `Saply-ai` org.

## GitHub

- Org: `Saply-ai`, Repo: `cv-engine-manual`
- PR URL pattern: `https://github.com/Saply-ai/cv-engine-manual/pull/{id}`
- Branch naming: `{type}/description` (`{type}/[issue-id]-description` when issue-linked)
- If `.mcp.json` is present, use its MCP tools for PRs and issues.

## Stack

Static HTML, a single self-contained `index.html` with inline CSS. No build tooling, package manifest, or dependencies.

## Manual content

`index.html` documents how end users drive CV Engine over email (send to `engine@saply.ai`):

- Template: put a template name (e.g. `bnp`) in the email subject.
- Translation: add `french`, `dutch`, `english`, `spanish`, or `portuguese` in the subject.
- Anonymization: add `anonymize` in the subject to redact personal data.
- Tailor ("pimp") mode: add `pimp` in the subject and paste the vacancy description in the email body.
- Vacancy matching: paste a vacancy description in the email body.
- Subject keywords can be combined and order does not matter (e.g. `bnp dutch`).
- Batch: multiple attached CVs are all processed with the same subject and body options.
- Tokens: one token per successful CV output, none charged when processing fails.

When editing, keep the documented keywords and behavior in sync with the actual CV Engine service.
