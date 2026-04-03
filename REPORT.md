# Report

## Title

Potential billing-state workflow issue allowing unintended release reactivation

## Category

Business logic / authorization / billing-state enforcement

## Severity

Medium, pending vendor validation.

## Summary

An account with a lapsed or otherwise inactive paid state still appeared to retain access to a release-related workflow that may have allowed a previously unavailable release to become active again after a minimal metadata save.

The issue may indicate that:

1. access to a sensitive release-management path is not fully blocked after billing-state change, or
2. saving low-impact metadata can trigger a state transition without a second eligibility check.

## Affected area

- Release management
- Billing / subscription gating
- Release activation or restoration workflow
- Account area reachable after plan lapse

## High-level reproduction

1. Use an account that previously had paid release-management capability.
2. Let the account lapse or transition to a lower billing state.
3. Access a previously reachable release-related account path that is still exposed post-lapse.
4. Open a release that is unavailable or removed from stores.
5. Make a harmless metadata change.
6. Save the change.
7. Observe whether the release state changes from unavailable to active, restored, or resubmitted.

## Expected result

A lapsed or ineligible account should not be able to restore, reactivate, resubmit, or otherwise materially change release state unless current billing and authorization checks pass at save time.

## Observed result

A release appeared to become active again after a minimal save action.

## Impact

Potential impacts include:

- unpaid access to paid distribution functionality
- inconsistent billing enforcement
- unauthorized restoration of catalog items
- possible royalty, reporting, and store-state inconsistencies
- trust and accounting issues between subscription tier, catalog state, and platform behavior

## Evidence to attach privately, not publicly

- screenshots showing account plan state
- screenshots showing release state before and after
- timestamps
- redacted release identifiers
- any vendor emails about inactive plan or removal status

## Recommended remediation

- re-check billing and authorization at final save, not only on page access
- block state-changing operations for ineligible billing states
- separate cosmetic metadata edits from restore/resubmit/release-state transitions
- log and review release-state changes initiated from post-lapse workflows
- add regression tests covering lapsed-plan edit paths

## Disclosure note

This report is written to support responsible disclosure. It intentionally omits operational detail that would make abuse easier.
