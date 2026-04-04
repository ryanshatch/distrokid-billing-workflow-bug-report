<h1>DistroKid Billing-State Workflow Report</h1>

<p>This folder documents a potential billing-state or access-control workflow issue observed in DistroKid.</p>

<h2>Purpose</h2>

<p>The purpose of this report is to document a possible platform flaw in a responsible way.</p>

<p>It is <strong>not</strong> a guide for bypassing payment, reactivating content without authorization, or avoiding normal platform fees.</p>

<h2>Summary</h2>

<p>A previously unavailable release appeared to become active again after a low-impact edit action was saved from within an account area that was still reachable despite an inactive paid plan.</p>

<p>The concern is not the specific UI path itself. The concern is that a user in a lapsed or downgraded billing state may still be able to trigger a release-state change that should likely require an active eligible subscription or a stricter permission check.</p>

<h2>What this folder contains</h2>

<ul>
  <li><code>REPORT.md</code> — issue summary, impact, and high-level reproduction notes</li>
  <li><code>TIMELINE.md</code> — a simple disclosure timeline template</li>
</ul>

<h2>Scope</h2>

<p>This write-up intentionally avoids step-by-step exploit instructions.</p>

<h2>Status</h2>

<p>Unconfirmed by vendor.</p>

<h2>Ongoing review</h2>

<p>I am still reviewing related billing-state and catalog-management behavior before disclosing this privately to DistroKid.</p>

<p>So far, I have observed additional behavior suggesting the issue may extend beyond a single release reactivation path. In at least one case, account-level artist metadata changes appeared to affect distribution status across multiple releases in a way that did not seem consistent with the visible billing or downgrade controls.</p>

<p>At this stage, I am intentionally not publishing the exact workflow, field changes, or platform responses involved. The goal is to document the existence and possible scope of the issue without providing a how-to for reproducing it publicly.</p>

<p>My intent is responsible disclosure and documentation, not monetization or abuse. I am continuing to review the behavior so that any eventual report is accurate, limited to what I directly observed, and useful to the vendor.</p>

<h2>Notes</h2>

<p>I have not publicly released detailed operational information such as exact UI paths, private URLs, release identifiers, invoice data, or account-specific screenshots.</p>

<p>That omission is intentional. I do not want to publish material that could help others abuse a billing-state or catalog-management flaw before the vendor has a chance to review it.</p>

<p>This issue was found accidentally. I am documenting it carefully and reviewing the surrounding behavior before making a private disclosure.</p>
