# Marketing Write Rules

Status: Source of truth
Authority level: Marketing / Writing rules
Last reviewed: 2026-05-23
Governing docs:
- `ai-context/source-of-truth-rules.md`
- `ai-context/repo-governance/repo-editing-rules.md`
- `ai-context/claim-control/claim-control-system.md`
- `product/claims-and-evidence.md`
- `marketing/marketing-read-rules.md`
Downstream docs:
- Marketing strategy files
- Channel playbooks
- Positioning and messaging docs
- Marketing execution docs
- Post banks, calendars, and performance logs

## Purpose

This file defines how to write or update marketing docs in the `marketing/` folder.

Use it after `marketing/marketing-read-rules.md` has identified which upstream and marketing docs matter for the task.

Marketing docs should translate Orisen product truth, target-customer assumptions, claim boundaries, and narrative into clear external-facing strategy and execution without inventing unsupported claims.

## Mandatory repo-edit trigger

Before any ChatGPT-assisted marketing repo write action, including creating, editing, moving, renaming, deleting, or archiving a file, read:

- `ai-context/repo-governance/repo-editing-rules.md`

This applies even for small one-file edits.

After reading it, state the pre-edit scope before making the write action.

This rule applies before writing or updating marketing docs in GitHub, even when `marketing/marketing-write-rules.md` has already been read.

## File structure section

Every substantial marketing doc should include a top-level file structure section near the top of the file.

Use this section to show the reader what the file contains before the detailed sections begin.

The file structure should be written as bullet points with indented bullet points when needed.

Each bullet should use this pattern:

- `**Section name**`: short definition of what that section is for.

For nested sections, use this pattern:

- `**Parent section**`: short definition of what the parent section is for.
  - `**Nested section**`: short definition of what the nested section is for.

Example structure:

- **Purpose**: defines what the file is for and what it is not for.
- **Source-of-truth hierarchy**: defines which upstream files control the doc's strategy, claims, audience, and narrative.
- **Audience**: defines who the marketing work is written for.
  - **Primary audience**: defines the main customer or reader the doc should serve first.
  - **Secondary audience**: defines supporting audiences that matter but should not distort the main strategy.
- **Claim-safety rules**: defines what can be said safely, what needs careful framing, and what should be avoided.
- **Execution guidance**: defines how the strategy turns into practical marketing actions.
- **Maintenance rules**: defines when the file should be updated and what belongs in other docs.

The file structure section should not become a full summary of the file.

Keep each definition short, practical, and scannable.
