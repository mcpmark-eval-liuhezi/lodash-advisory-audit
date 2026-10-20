# Security Notes

## Summary

This document records the security context for the dependency pin added on this branch.

- **Advisory (GHSA ID):** GHSA-j8xg-fqg3-53r7
- **CVE:** CVE-2023-26115
- **Fixed version:** 1.2.4

## What the advisory says

The GitHub Advisory Database entry for `GHSA-j8xg-fqg3-53r7` is `word-wrap` vulnerable to Regular Expression Denial of Service (ReDoS), tracked as **CVE-2023-26115**. The first patched version recorded by the advisory is **1.2.4** (vulnerable range `< 1.2.4`), severity **medium** (CVSS 5.3), CWE-1333 (Inefficient Regular Expression Complexity).

> **Discrepancy note:** Our team's doc trail described this advisory as a `lodash` prototype-pollution issue, but the advisory record for GHSA-j8xg-fqg3-53r7 is actually about the **word-wrap** package (ReDoS), not lodash. The patched version **1.2.4** has been used exactly as returned by the lookup, as requested. Before shipping the pin for real, please confirm which advisory actually applies to our lodash usage, and note that **1.2.4 is not a real lodash release**.

## Change on this branch

- `package.json` pins the dependency to the patched version from the advisory: **1.2.4**.
- CI placeholder: `advisory-audit-ci` workflow (`.github/workflows/advisory-audit-ci.yml`).

## References

- Advisory: https://github.com/advisories/GHSA-j8xg-fqg3-53r7
- CVE: https://nvd.nist.gov/vuln/detail/CVE-2023-26115
- Snyk: https://security.snyk.io/vuln/SNYK-JS-WORDWRAP-3149973
- Fix reference: https://github.com/jonschlinkert/word-wrap/releases/tag/1.2.4
