# Verisk Underwriting Intelligence Plugin

This plugin bundles the **Verisk Underwriting Intelligence** MCP connector with the
**ISO Premium Audit Advisory (PAAS)** skill, giving Claude direct, governed access to
Verisk's Premium Audit Advisory Service for commercial casualty insurance.

## What's included

### Connector
- **Verisk Underwriting Intelligence** (remote MCP server)
  `https://gatewaymcp.verisk.com/underwriting/intelligencemcp/v1`
  Provides the `iso_premium_audit_advisory_get` tool and related ISO underwriting
  intelligence tools.

### Skill
- **iso-premium-audit-advisory-get** — Governs how Claude queries PAAS for
  audit-specific questions on General Liability (GL), Businessowners Policy (BOP/BP),
  and Commercial Auto (CA):
  - Classification codes, payroll/exposure bases, audit procedures, and
    state-specific audit rules
  - Strict single-source-of-truth behavior: answers come only from the PAAS tool,
    never from model knowledge or the web
  - Consistent Answer / Sources / Suggestions response format
  - Defined handling for out-of-scope questions (loss costs, rate filings,
    underwriting pricing), Workers' Compensation redirects, and error states

## Requirements

- A Verisk account authorized for PAAS access. Users without full access will
  receive an authorization notice directing them to their Verisk account executive
  or PremiumA@verisk.com.
- The connector authenticates via the standard Claude connector authentication flow.

## Usage

Once installed, ask audit or PAAS-related questions in plain language, for example:

- "What is the payroll limitation for GL classification?"
- "What is class code 91340?"
- "GL and BOP audit rules in NY, NJ, and PA"

Claude will automatically invoke the PAAS skill and return the advisory answer with
titled source links and suggested follow-up questions when available.

## Scope notes

- Covers GL, BOP/BP, and CA lines. Workers' Compensation questions are redirected
  to https://core.verisk.com/PAAS.
- Not intended for loss costs, rate filings, underwriting pricing, coverage
  comparisons, or policy structure questions.

## Support

Contact your Verisk account executive or the PAAS team at PremiumA@verisk.com.
