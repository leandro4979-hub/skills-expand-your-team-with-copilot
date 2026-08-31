# Agent Lab Guardrails

This repository is the experimental proving ground for GitHub Copilot, Codex, skills, MCP integrations, issue delegation, pull-request automation, and related agent workflows.

## Mission

Prototype -> Validate -> Promote.

Experiments happen here first. Production projects, especially CARINA, must not be modified as part of an experiment from this repository.

## Agent rules

1. Work only inside this repository unless the user explicitly names another repository and approves that change.
2. Prefer a dedicated branch for every experiment.
3. Do not commit API keys, access tokens, credentials, signing assets, device identifiers, or other secrets.
4. Do not weaken tests, CI, branch protections, approval boundaries, authentication, replay protection, or security checks merely to make an experiment pass.
5. Keep external side effects off by default. Network calls, deployments, releases, device actions, or writes to external systems require explicit intent and should be isolated behind testable adapters when possible.
6. Preserve existing exercises and learning material unless the task explicitly requires changing them.
7. Add or update tests for behavior-changing code.
8. Document what was tested, what failed, and what remains unverified.
9. Use pull requests for promotion candidates. Do not treat an experiment as production-ready merely because it runs once.
10. Never promote code directly into CARINA from this repository. Produce a promotion plan or clean patch that can be reviewed separately in the CARINA workspace.

## Required validation before promotion

A candidate is promotable only when all applicable checks pass:

- Behavior works as intended in this lab.
- Automated tests pass.
- CI checks pass.
- No secrets are present in code, logs, fixtures, or history introduced by the change.
- Permissions are least-privilege.
- Failure and rollback behavior are understood.
- External side effects are bounded and documented.
- Public interfaces and compatibility impact are documented.
- Security-sensitive changes receive manual review.
- A concise promotion note identifies exactly what should move into the production repository.

## Agent roles

- GitHub Copilot: GitHub-native issue, repository, pull-request, review, and delegated-task workflows.
- Codex: implementation, debugging, architectural analysis, migrations, tests, and code review.
- CARINA: production runtime/orchestration target. It consumes validated capabilities; it is not the default experimentation surface.

When agents disagree, prefer the safer interpretation, preserve existing behavior, and surface the conflict for review.