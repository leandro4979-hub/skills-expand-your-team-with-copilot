# Agent Lab Operating Model

## Purpose

Use this repository to evaluate agent behavior before copying any capability into a production project.

## Workflow

### 1. Prototype

Create a focused branch and define one experiment. Examples:

- GitHub Copilot issue delegation
- Codex implementation or review
- repository instructions
- reusable skills
- MCP server integration
- automated pull-request workflows
- CI-driven agent validation

Keep the experiment narrow enough that success or failure is obvious.

### 2. Validate

Record:

- intended behavior
- exact files changed
- tests executed
- CI result
- permissions requested
- external services contacted
- known failure modes
- rollback method
- security observations

A successful demo is not sufficient by itself. Re-run the important path and test at least one expected failure case when practical.

### 3. Promote

If the experiment passes, prepare a production migration note containing:

- capability being promoted
- source files or concepts to port
- dependencies required
- configuration required
- security implications
- tests required in the destination repository
- rollback procedure

Promotion should happen in the destination repository on a new branch and through its normal review process.

## CARINA boundary

CARINA is treated as a protected production target. This lab may design or validate CARINA-compatible ideas, but it must not assume access to CARINA or modify it implicitly.

Any future CARINA implementation should begin from a fresh inspection of the actual CARINA workspace and its current guardrails.

## Definition of done

An experiment is done when another agent or developer can understand what was tested, reproduce the validation, and decide whether it is safe to promote without relying on hidden context.