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
- `VENDOR-CONTACT.md` — a clean contact template for responsible disclosure

## Scope

This write-up intentionally avoids step-by-step exploit instructions.

## Suggested title

Potential billing-state workflow issue allowing unintended release reactivation

## Status

Unconfirmed by vendor.

## Notes

So far I have not publicly released any in depth information to redact, release IDs, invoice data, private URLs, etc,. because quite frankly I know that Distrokid will not only ignore my findings, but will remove my art along with the work around. Thus, this publishing is honest, nonetheless I have kept it to myself in order to avoid loosing access to my art. I entirely found this on accident and decided to treat it unlike the way I treated my findings with Namecheaps ability to generate unlimited free SSL certificates.
