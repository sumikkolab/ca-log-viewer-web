<h1 align="center">CA Log Viewer</h1>

<p align="center">
  Read Conditional Access sign-in logs in context — on your Windows desktop, locally.
</p>

<p align="center">
  <!-- Microsoft Store badge will be added after publication. -->
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%2010%2F11-blue" />
  <img alt=".NET 8" src="https://img.shields.io/badge/.NET-8.0-purple" />
  <img alt="License" src="https://img.shields.io/badge/license-Proprietary-lightgrey" />
</p>

<p align="center">
  <a href="README_ja.md">日本語版はこちら</a>
</p>

---

## Overview

**CA Log Viewer** is a Windows desktop app that fetches Microsoft Entra ID sign-in logs via Microsoft Graph and helps administrators **read Conditional Access (CA) related entries** — CA evaluation result, applied policies, device compliance — through a focused UI and an HTML audit report.

- **Local-only processing**: No external transmission beyond Microsoft Graph
- **PII protection**: Plain UPN is not stored in the database; display goes through a short-term DPAPI-encrypted cache (TTL 7 days)
- **HTML audit report with 3-axis aggregation**: by user / by app / by policy (top 20 + others)
- **ja / en UI**: full bilingual support
- **Demo mode**: 110 records / 6 scenarios with `*.example` domains and RFC 5737 IPs only (excluded from Microsoft Store builds)

## Quick Links

- 🌐 Product page: <https://ca-log-viewer.sumikkolab.com/>
- 📖 Manual: <https://ca-log-viewer.sumikkolab.com/manual/>
- 🔒 Privacy Policy: <https://ca-log-viewer.sumikkolab.com/privacy-policy.html>
- 📋 Terms of Use: <https://ca-log-viewer.sumikkolab.com/terms-of-use.html>
- 🛟 Support: <https://ca-log-viewer.sumikkolab.com/support.html>

## Features

- Entra ID sign-in logs fetch via Microsoft Graph (delegated auth, `AuditLog.Read.All`)
- Conditional Access evaluation result classification
- Applied policy listing per sign-in
- Device compliance status
- Unified filter: range / user / CA status / judgment / device / special, multi-select OR
- Detail pane with 7 sections + conclusion (6-tier priority)
- HTML audit report with Aggregation (by user / by app / by policy, top 20 + others)
- CSV export
- Demo mode (no real tenant)
- ja / en UI with full localization

## Required Microsoft Graph permissions

- `AuditLog.Read.All`
- `Policy.Read.ConditionalAccess`
- `User.Read.All`

## Status

Pre-release. Microsoft Store submission is in preparation.

## Contact

Email: support@sumikkolab.com

---

&copy; 2026 Sumikko Lab
