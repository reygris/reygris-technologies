# Quality Standards

Quality at ReyGris is vigilance made habitual. These standards define what "done" means.

## Definition of done

Work is not complete until:

- [ ] Requirements and acceptance criteria are met
- [ ] Code is reviewed (when applicable)
- [ ] Tests cover critical behavior
- [ ] Documentation is updated if behavior or setup changed
- [ ] Security and accessibility baselines are satisfied
- [ ] It runs successfully in a staging or production-like environment

## Testing strategy

| Layer | Purpose |
|-------|---------|
| Unit | Isolated logic, fast feedback |
| Integration | Components and services working together |
| End-to-end | Critical user journeys |
| Manual / exploratory | UX, edge cases, visual polish |

Prioritize tests that fail when users would be hurt — data loss, auth bypass, payment errors, broken core flows.

## Accessibility (a11y)

Accessibility is not optional or a "phase two" item.

- Semantic HTML first
- Keyboard navigable interfaces
- Sufficient color contrast (WCAG AA minimum for text)
- Alt text for meaningful images; decorative images marked appropriately
- Form labels, error messages, and focus states implemented
- Test with keyboard-only navigation and at least one screen reader periodically

## Security

See [Engineering Standards](engineering.md) for technical baselines. Quality adds:

- Threat modeling for features handling auth, payments, or sensitive data
- Regular dependency audits
- Penetration testing or external review for high-risk systems when appropriate

## Performance

Define targets per project, for example:

- Largest Contentful Paint under 2.5s on representative devices
- API p95 latency under agreed threshold
- No unbounded N+1 queries or memory leaks in hot paths

Measure in CI or staging where feasible; regressions block release.

## Observability

Production systems should expose:

- Structured logs (no secrets)
- Error tracking
- Metrics for latency, throughput, and saturation
- Alerts on user-impacting failures

## Release quality

- Changelogs or release notes for user-facing changes
- Feature flags for risky rollouts when appropriate
- Rollback plan documented before high-risk deploys

## Technical debt

Debt is tracked, not hidden.

- Record known debt with impact and suggested remediation
- Pay down debt that blocks velocity or increases incident risk
- Do not accumulate debt silently to hit arbitrary dates without stakeholder consent

## Continuous improvement

After significant releases or incidents:

- Retrospective within one week
- Action items assigned and dated
- Update standards in this repo when we learn something reusable
