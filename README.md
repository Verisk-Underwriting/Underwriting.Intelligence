# Verisk Underwriting Intelligence Plugin

Bundles the **Verisk Underwriting Intelligence** MCP connector with the **ISO Premium Audit Advisory (PAAS)** skill, giving Claude governed access to Verisk's Premium Audit Advisory Service for commercial casualty insurance.

## What's included

- **Connector** — `Verisk Underwriting Intelligence` remote MCP server, providing the `iso_premium_audit_advisory_get` tool.
- **Skill** — `iso-premium-audit-advisory-get`, governing PAAS queries for General Liability (GL), Businessowners Policy (BOP/BP), and Commercial Auto (CA): classification codes, payroll/exposure bases, audit procedures, and state-specific rules.

## Usage

Ask audit or PAAS-related questions in plain language, for example:

- "What is the payroll limitation for GL classification?"
- "What is class code 91340?"
- "GL and BOP audit rules in NY, NJ, and PA"

## Scope

Covers GL, BOP/BP, and CA. Not intended for loss costs, rate filings, underwriting pricing, or coverage comparisons. Requires a Verisk account authorized for PAAS access.
