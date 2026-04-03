# Vendor Contact Template

Subject: Potential billing-state workflow issue affecting release reactivation

Hello DistroKid,

I am reporting a possible business-logic or authorization issue involving release-management behavior after a billing-state change.

In short, an account in a lapsed or ineligible paid state appeared to retain access to a release-related workflow that may allow a previously unavailable release to become active again after saving a minimal metadata change.

I am not publishing operational details that would make reproduction easier. If your team wants validation material, I can provide redacted screenshots, timestamps, and account-state context privately.

Potential impact:
- unintended access to paid distribution functionality
- unauthorized release restoration or resubmission
- billing-state enforcement inconsistency

Suggested review areas:
- billing checks at save time
- release-state transitions triggered by metadata edits
- access to release-management paths after plan lapse

Please confirm receipt and let me know the best channel for sharing private evidence.

Thanks
