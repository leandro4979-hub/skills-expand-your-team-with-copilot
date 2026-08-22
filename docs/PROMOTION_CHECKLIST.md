# Promotion Checklist

Use this before moving any experiment into CARINA or another production repository.

## Scope

- [ ] The capability has one clear purpose.
- [ ] The destination repository and integration point are known.
- [ ] Unrelated experimental code is excluded.

## Validation

- [ ] The happy path was tested.
- [ ] At least one meaningful failure path was tested when applicable.
- [ ] Automated tests pass.
- [ ] CI passes.
- [ ] Re-running the workflow does not create unsafe duplicate side effects.

## Security

- [ ] No secrets or credentials are committed.
- [ ] Permissions follow least privilege.
- [ ] Authentication and approval boundaries are preserved.
- [ ] Inputs are validated at trust boundaries.
- [ ] Logs do not expose sensitive values.
- [ ] External writes or device actions are explicit and bounded.

## Compatibility

- [ ] Existing public behavior is preserved or intentional changes are documented.
- [ ] Required dependencies and versions are documented.
- [ ] Configuration and environment requirements are documented.
- [ ] Rollback steps are documented.

## Promotion package

- [ ] Exact files or concepts to port are identified.
- [ ] Destination-specific tests are listed.
- [ ] Manual review areas are called out.
- [ ] A new destination-repository branch will be used.
- [ ] Production code will not be copied blindly from the experiment.

## Decision

Promotion status: NOT READY / READY FOR REVIEW / APPROVED

Reviewer notes:

- What passed:
- What remains unverified:
- Security notes:
- Destination changes required:
