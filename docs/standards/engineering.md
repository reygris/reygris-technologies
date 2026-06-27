# Engineering Standards

ReyGris engineering standards apply to all code we write, review, and maintain — internal tools, client work, and products.

## Principles

1. **Readable over matures; clever code rots.**
2. **Defaults should be safe** — secure, accessible, and observable.
3. **Document the why**, not just the what.
4. **Automate repetition**; reserve human attention for judgment.

## Repository hygiene

- Every repo has a README: purpose, setup, run, deploy
- Use meaningful commit messages (imperative mood, explain why when non-obvious)
- Keep `main`/`master` deployable; use branches for work in progress
- Do not commit secrets — use environment variables and secret managers

## Code quality

| Area | Standard |
|------|----------|
| Naming | Descriptive, consistent with project conventions |
| Functions | Single responsibility; avoid deep nesting |
| Comments | Explain non-obvious intent; do not narrate obvious code |
| Dead code | Remove it; version control remembers |
| Dependencies | Justify new deps; prefer fewer, maintained libraries |

## Architecture

- Prefer simple architectures that match current scale
- Draw boundaries explicitly (modules, services, APIs)
- Design for change at stable interfaces
- Record significant decisions in ADRs (Architecture Decision Records) when impact is long-lived

## Version control & review

- All non-trivial changes go through review when working with a team
- PRs describe **what** changed and **why**
- Reviewers check: correctness, clarity, security, tests, docs impact

## Testing

- Test behavior users and systems depend on
- Critical paths require automated tests before merge
- Manual exploratory testing for UX and edge cases automation misses
- See [Quality Standards](quality.md) for depth on testing strategy

## Security baseline

- Validate and sanitize all external input
- Use parameterized queries / ORM safely — no string-built SQL
- Apply least-privilege for credentials and IAM
- Keep dependencies updated; monitor CVEs
- Never log secrets, tokens, or full PII

## Performance

- Measure before optimizing
- Set budgets for page load, API latency, and bundle size where relevant
- Cache intentionally; invalidate correctly

## Deployment

- Deployments are repeatable and documented
- Prefer rollback-capable releases
- Monitor production: errors, latency, saturation

## Documentation

Each project should include:

- Setup instructions a new developer can follow unaided
- Environment variable reference
- Deployment steps
- Known limitations and tradeoffs

## Tooling

Choose tools that fit the project and team. ReyGris does not mandate a single stack — we mandate **standards of outcome**: reliability, clarity, and maintainability.

When introducing new tooling, document the decision and onboarding path.
