# DistroKid Billing-State Workflow Report

This folder documents a potential billing-state or access-control workflow issue observed in DistroKid.

## Purpose

The purpose of this report is to document a possible platform flaw in a responsible way.

It is **not** a guide for bypassing payment, reactivating content without authorization, or avoiding normal platform fees.

## Summary

A previously unavailable release appeared to become active again after a low-impact edit action was saved from within an account area that was still reachable despite an inactive paid plan.

The concern is not the specific UI path itself. The concern is that a user in a lapsed or downgraded billing state may still be able to trigger a release-state change that should likely require an active eligible subscription or a stricter permission check.

## What this folder contains

- `REPORT.md` — issue summary, impact, and high-level reproduction notes
- `TIMELINE.md` — a simple disclosure timeline template

## Scope

This write-up intentionally avoids step-by-step exploit instructions.

## Status

Unconfirmed by vendor.

## Ongoing review

I am still reviewing related billing-state and catalog-management behavior before disclosing this privately to DistroKid.

So far, I have observed additional behavior suggesting the issue may extend beyond a single release reactivation path. In at least one case, account-level artist metadata changes appeared to affect distribution status across multiple releases in a way that did not seem consistent with the visible billing or downgrade controls.

At this stage, I am intentionally not publishing the exact workflow, field changes, or platform responses involved. The goal is to document the existence and possible scope of the issue without providing a how-to for reproducing it publicly.

My intent is responsible disclosure and documentation, not monetization or abuse. I am continuing to review the behavior so that any eventual report is accurate, limited to what I directly observed, and useful to the vendor.

## Notes

I have not publicly released detailed operational information such as exact UI paths, private URLs, release identifiers, invoice data, or account-specific screenshots.

That omission is intentional. I do not want to publish material that could help others abuse a billing-state or catalog-management flaw before the vendor has a chance to review it.

This issue was found accidentally. I am documenting it carefully and reviewing the surrounding behavior before making a private disclosure.
