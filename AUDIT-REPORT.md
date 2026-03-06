# _d-underscored Theme Audit Report

Date: 2026-03-06
Scope: WordPress compatibility, performance, privacy/compliance, and security hardening.

## Repository reality check

This repository currently contains:
- CSS customization file (`_d-underscored.css`)
- Header tweak instructions (`4header_php.md`)
- Project README and license

It does **not** currently include full theme PHP templates (`functions.php`, `header.php`, `index.php`, etc.).

Because of that, this remediation pass targets the assets and guidance that exist in this repo.

## Findings and remediation

## 1) Compatibility

### Finding
Sticky-footer implementation relied on manual template edits (`<div class="push"></div>`), which is brittle and easy to miss.

### Remediation
- Replaced push-div dependency with flexbox sticky-footer behavior in CSS.
- Updated README to remove manual push-div instructions.

## 2) Privacy / compliance

### Finding
CSS guidance included a rule to hide `.grecaptcha-badge`, which can conflict with provider terms and transparency expectations.

### Remediation
- Removed recaptcha badge hiding rule from `_d-underscored.css`.
- Added compliance-safe note in README to keep required notices visible.

## 3) Accessibility and UX

### Finding
No explicit keyboard focus styles for links/buttons in custom CSS.

### Remediation
- Added `:focus-visible` styles for links and buttons.
- Removed mobile absolute positioning from `.site-info` that could cause overlap issues.

## 4) Performance / maintainability

### Finding
Sticky footer used negative-margin hacks and extra placeholder elements.

### Remediation
- Simplified layout with modern flexbox approach.
- Reduced complexity and dependency on per-template modifications.

## Changed files

- `_d-underscored.css`
- `README.md`
- `4header_php.md`

## Recommended next step (for full-theme audit parity)

To run a full Vofa-style deep audit, include the complete theme source (at least):
- `style.css` (with theme header)
- `functions.php`
- `header.php`, `footer.php`
- `index.php`, `single.php`, `page.php`, `search.php`
- `inc/` files (if present)

With those files present, we can perform full static review for escaping/sanitization, enqueue correctness, template hierarchy behavior, and plugin compatibility.
