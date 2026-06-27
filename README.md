# devsignal-ci-test

Test repository for DevSignal CI failure detection.

This repo contains intentionally broken and flaky GitHub Actions workflows
to verify that DevSignal correctly identifies:

- 100% failure rate workflows
- Flaky (random) workflows  
- Healthy workflows
- High compute waste workflows

## Workflows

| Workflow | Expected Behavior |
|---|---|
| Always Failing Test | 100% failure rate — HIGH RISK |
| Flaky Test | ~50% failure rate — WATCH |
| Always Passing Build | 0% failure rate — HEALTHY |
| Slow Then Fail | 100% failure + compute waste — HIGH RISK |

## Purpose

Used to verify DevSignal detection at [devsignal.dev](https://devsignal.dev)
