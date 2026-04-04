<h1>Report</h1>

<h2>Title</h2>

<p>Potential billing-state workflow issue allowing unintended release reactivation</p>

<h2>Category</h2>

<p>Business logic / authorization / billing-state enforcement</p>

<h2>Severity</h2>

<p>Medium, pending vendor validation.</p>

<h2>Summary</h2>

<p>An account with a lapsed or otherwise inactive paid state still appeared to retain access to a release-related workflow that may have allowed a previously unavailable release to become active again after a minimal metadata save.</p>

<p>The issue may indicate that:</p>

<ol>
  <li>access to a sensitive release-management path is not fully blocked after billing-state change, or</li>
  <li>saving low-impact metadata can trigger a state transition without a second eligibility check.</li>
</ol>

<h2>Affected area</h2>

<ul>
  <li>Release management</li>
  <li>Billing / subscription gating</li>
  <li>Release activation or restoration workflow</li>
  <li>Account area reachable after plan lapse</li>
</ul>

<h2>High-level reproduction</h2>

<ol>
  <li>Use an account that previously had paid release-management capability.</li>
  <li>Let the account lapse or transition to a lower billing state.</li>
  <li>Access a previously reachable release-related account path that is still exposed post-lapse.</li>
  <li>Open a release that is unavailable or removed from stores.</li>
  <li>Make a harmless metadata change.</li>
  <li>Save the change.</li>
  <li>Observe whether the release state changes from unavailable to active, restored, or resubmitted.</li>
</ol>

<h2>Expected result</h2>

<p>A lapsed or ineligible account should not be able to restore, reactivate, resubmit, or otherwise materially change release state unless current billing and authorization checks pass at save time.</p>

<h2>Observed result</h2>

<p>A release appeared to become active again after a minimal save action.</p>

<h2>Additional observations under review</h2>

<p>During follow-up review, I observed signs that the behavior may not be limited to a single release-level edit path.</p>

<p>In at least one account state, artist-related metadata changes appeared to produce broader catalog effects than expected, including changes that may have influenced store availability or artist mapping across multiple releases.</p>

<p>Because this behavior is still being reviewed, and because publishing the exact sequence would make misuse easier, the precise trigger conditions are being withheld from the public report pending private disclosure.</p>

<h2>Impact</h2>

<p>Potential impacts include:</p>

<ul>
  <li>unpaid access to paid distribution functionality</li>
  <li>inconsistent billing enforcement</li>
  <li>unauthorized restoration of catalog items</li>
  <li>possible royalty, reporting, and store-state inconsistencies</li>
  <li>trust and accounting issues between subscription tier, catalog state, and platform behavior</li>
</ul>

<h2>Evidence to attach privately, not publicly</h2>

<ul>
  <li>screenshots showing account plan state</li>
  <li>screenshots showing release state before and after</li>
  <li>timestamps</li>
  <li>redacted release identifiers</li>
  <li>any vendor emails about inactive plan or removal status</li>
</ul>

<h2>Recommended remediation</h2>

<ul>
  <li>re-check billing and authorization at final save, not only on page access</li>
  <li>block state-changing operations for ineligible billing states</li>
  <li>separate cosmetic metadata edits from restore/resubmit/release-state transitions</li>
  <li>log and review release-state changes initiated from post-lapse workflows</li>
  <li>add regression tests covering lapsed-plan edit paths</li>
</ul>

<h2>Disclosure note</h2>

<p>This report is written to support responsible disclosure. It intentionally omits operational detail that would make abuse easier.</p>
