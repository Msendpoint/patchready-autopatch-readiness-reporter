# PatchReady

> Automated Windows Autopatch readiness reporting that turns Graph API data into actionable dashboards and helpdesk tickets before Patch Tuesday hits.

## Overview

PatchReady is a scheduled Azure Automation runbook plus Power BI template bundle that continuously queries the Microsoft Graph windowsUpdates API, aggregates per-device readiness signals, and auto-generates prioritized remediation reports. It categorizes blocking issues by type (driver conflicts, missing prerequisites, policy mismatches, check-in failures) and optionally pushes non-ready devices directly into ServiceNow, Jira, or Freshservice as pre-built tickets. IT teams stop manually triangulating three disconnected data sources and get a single pane of glass with zero-touch reporting.

## Problem This Solves

Before Patch Tuesday, admins have no fast, consolidated way to know which devices will fail updates and why — forcing them to cross-reference Windows Update for Business reports, Intune compliance dashboards, and Update Compliance workbooks manually, which takes hours and still produces stale data.

## Target Audience

IT admins and endpoint managers at mid-market organizations managing 200–5,000 devices who use Intune and Windows Autopatch but lack dedicated reporting engineers or Power BI developers.

## Tech Stack

PowerShell, Microsoft Graph API, Azure Automation, Power BI, JSON

## Quick Start

```powershell
# Clone the repository
git clone https://github.com/patchready-autopatch-readiness-reporter.git
cd patchready-autopatch-readiness-reporter

# One-click install & run
.\Install.ps1

# Or run the script directly
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
.\scripts\{patchready-autopatch-readiness-reporter}.ps1
```

## Usage



## Monetization Strategy

Tiered licensing sold on Gumroad and Lemon Squeezy: Core Tier ($49 one-time) includes the PowerShell runbook, CSV exporter, and pre-built Power BI .pbix template; Pro Tier ($99 one-time) adds ticketing system integration scripts and a setup guide; MSP License ($199/year) covers unlimited client tenants with white-label branding. Upsell a 2-hour implementation consulting session via Calendly at $250/session.

| Metric | Value |
|--------|-------|
| Revenue Potential | HIGH |
| Estimated Effort  | 1-2weeks |

## About the Author