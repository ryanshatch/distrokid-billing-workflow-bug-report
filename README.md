<h1 align="center">DistroKid Billing-State Workflow Report</h1>

<p align="center">
  <strong>Responsible disclosure documentation for a possible billing-state or catalog-availability issue.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Reviewed-green" alt="Status">
  <img src="https://img.shields.io/badge/Disclosure-Responsible%20Disclosure-blue" alt="Disclosure">
  <img src="https://img.shields.io/badge/Reproduction%20Steps-Omitted-red" alt="Reproduction Steps Omitted">
  <img src="https://img.shields.io/badge/Intent-Defensive%20Documentation-green" alt="Intent">
</p>

<hr>

<h2>Table of Contents</h2>

<ul>
  <li><a href="#overview">Overview</a></li>
  <li><a href="#purpose">Purpose</a></li>
  <li><a href="#summary">Summary</a></li>
  <li><a href="#responsible-disclosure-position">Responsible Disclosure Position</a></li>
  <li><a href="#scope">Scope</a></li>
  <li><a href="#observed-behavior">Observed Behavior</a></li>
  <li><a href="#potential-impact">Potential Impact</a></li>
  <li><a href="#recommended-review-areas">Recommended Review Areas</a></li>
  <li><a href="#private-evidence-handling">Private Evidence Handling</a></li>
  <li><a href="#repository-contents">Repository Contents</a></li>
  <li><a href="#status">Status</a></li>
  <li><a href="#contact">Contact</a></li>
</ul>

<hr>

<h2 id="overview">Overview</h2>

<p>
  This repository documents a possible billing-state or catalog-availability issue observed in DistroKid.
</p>

<p>
  The issue was noticed while reviewing my own account and publicly visible music listings. Some music associated with my account appeared to remain available on third-party music platforms even though my visible account state did not appear to support that result.
</p>

<p>
  This repository exists to document the concern in a careful, limited, and responsible way without publishing reproduction steps as a proof of concept to this bug finding.
</p>

<hr>

<h2 id="purpose">Purpose</h2>

<p>
  The purpose of this report is to document a possible platform flaw in a responsible way.
</p>

<p>
  The goal is to give DistroKid enough public context to understand the type of issue being reported while keeping sensitive details private for vendor review.
</p>

<p>
  This report is written from a defensive documentation perspective. It is intended to support responsible disclosure, vendor triage, and correction of any unintended catalog or billing-state behavior.
</p>

<hr>

<h2 id="summary">Summary</h2>

<p>
  While reviewing my own account and publicly visible music listings, I observed that certain releases appeared to remain available on third-party music platforms even though my visible account state did not appear to support that result.
</p>

<p>
  The concern is that billing-state, catalog-state, release-management, and store-availability checks may not be fully aligned across all relevant workflows.
</p>

<p>
  In plain terms, the issue may involve a mismatch between what the account state appears to allow and what remains visible or active across external music platforms.
</p>

<hr>

<h2 id="responsible-disclosure-position">Responsible Disclosure Position</h2>

<p>
  This issue was found accidentally while reviewing my own account and public store listings.
</p>

<p>
  My intent is responsible disclosure, not monetization, misuse, bypassing payment, or retaining any unintended benefit.
</p>

<p>
  I used only my own account and publicly visible listings. I am not publishing reproduction steps, URLs, UIDs, etc.,
</p>

<p>
  Detailed evidence will shared privately with the vendor only.
</p>

<hr>

<h2 id="what-this-repository-is-not">What This Repository Is Not</h2>

<p>
  This repository is <strong>not</strong> a guide for bypassing payment, reactivating content without authorization, avoiding normal platform fees, or reproducing the issue publicly.
</p>

<p>
  Any sensitive material will remain private and will only be provided directly to DistroKid through the appropriate support, security, billing, trust/safety, or engineering channel.
</p>

<hr>

<h2 id="scope">Scope</h2>

<p>
  This public write-up is intentionally limited.
</p>

<p>
  It describes the suspected issue category and the general concern without providing operational detail that could make misuse easier.
</p>

<p>
  The public scope includes:
</p>

<ul>
  <li>high-level issue category</li>
  <li>general observed behavior</li>
  <li>possible impact areas</li>
  <li>recommended review areas</li>
  <li>responsible disclosure position</li>
</ul>

<p>
  The public scope does not include reproduction steps or private evidence.
</p>

<hr>

<h2 id="observed-behavior">Observed Behavior</h2>

<p>
  Some music associated with my account appeared to remain available on third-party platforms despite my visible account state.
</p>

<p>
  Based on the visible account status, I did not expect certain releases to remain available or active across external music platforms.
</p>

<p>
  This may point to a catalog-state or billing-state consistency issue, but final validation belongs to DistroKid.
</p>

<hr>

<h2 id="potential-impact">Potential Impact</h2>

<p>
  If validated by the vendor, this type of issue could affect consistency between billing state, release state, and third-party store availability.
</p>

<p>
  Potential areas of concern include:
</p>

<ul>
  <li>billing-state enforcement inconsistency</li>
  <li>catalog-state inconsistency</li>
  <li>unexpected third-party store availability</li>
  <li>release-management state mismatch</li>
  <li>possible royalty, reporting, or accounting inconsistencies</li>
  <li>confusion between account eligibility and catalog availability</li>
</ul>

<p>
  These are possible impact areas only. They require vendor review and validation.
</p>

<hr>

<h2 id="recommended-review-areas">Recommended Review Areas</h2>

<p>
  The following areas worth reviewing internally:
</p>

<ul>
  <li>billing-state checks across catalog-management workflows</li>
  <li>release-state and store-availability synchronization</li>
  <li>account eligibility checks before catalog-state changes</li>
  <li>handling of inactive, lapsed, downgraded, or ineligible accounts</li>
  <li>logging for catalog-state changes after billing-state changes</li>
  <li>store distribution status after account-state transitions</li>
  <li>separation between cosmetic metadata handling and release availability state</li>
</ul>

<p>
  These recommendations are high-level and intentionally do not describe the exact workflow observed.
</p>

<hr>

<h2 id="private-evidence-handling">Private Evidence Handling</h2>

<p>
  Supporting evidence will be handled privately.
</p>

<p>
  Evidence that will be useful to the vendor includes:
</p>

<ul>
  <li>account email or account identifier</li>
  <li>affected artist or release names</li>
  <li>third-party platform links</li>
  <li>screenshots showing account state</li>
  <li>screenshots showing store availability</li>
  <li>approximate discovery and review timeline</li>
  <li>relevant DistroKid emails or account notices</li>
</ul>

<p>
  This evidence is intentionally omitted from the public repository.
</p>

<hr>

<h2 id="repository-contents">Repository Contents</h2>

<table>
  <thead>
    <tr>
      <th>File</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>README.md</code></td>
      <td>Main public overview and responsible disclosure position.</td>
    </tr>
    <tr>
      <td><code>REPORT.md</code></td>
      <td>Sanitized issue report without reproduction details.</td>
    </tr>
    <tr>
      <td><code>TIMELINE.md</code></td>
      <td>Simple disclosure timeline and current review status.</td>
    </tr>
    <tr>
      <td><code>LICENSE</code></td>
      <td>Use restrictions and documentation notice.</td>
    </tr>
    <tr>
      <td><code>.gitattributes</code></td>
      <td>GitHub Linguist configuration for repository display.</td>
    </tr>
  </tbody>
</table>

<hr>

<h2 id="status">Status</h2>

<p>
  Current status: <strong>Pending private vendor review.</strong>
</p>

<p>
  Public disclosure is not an option unless approved and deemed appropriate after vendor review.
</p>

<p>
  This repository will remain limited to sanitized documentation only.
</p>

<hr>

<h2 id="contact">Contact</h2>

<p>
  Maintainer: Ryan Hatch
</p>

<p>
  GitHub: <a href="https://github.com/ryanshatch">https://github.com/ryanshatch</a>
</p>

<p>
  Email: <a href="mailto:ryanshatch@gmail.com">ryanshatch@gmail.com</a>
</p>

<hr>

<p align="center">
  <strong>As a Blue Teamer and Bug Finder, I intend to keep full responsible disclosure for this finding.</strong><br>
  <em>No reproduction steps or malicious intent.</em>
</p>
