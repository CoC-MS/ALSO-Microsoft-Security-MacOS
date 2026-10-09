# 🏷️ Short-name exceptions

[Documentation index](README.md) | [Policy naming](policy-naming.md)

Not every exported resource uses the common policy naming pattern. This repository includes Conditional Access resources named with a `BP-ALSO-CA...` prefix, group resources with shorter `ALSO-...` or `BP-ALSO-...` names, an application named `Microsoft Defender for Endpoint (macOS)`, and a `MigrationTable.json`.

Compliance export names also differ in punctuation and version formatting from the Settings Catalog examples. Existing names include inconsistent spacing, hyphens and typographic dashes, capitalization such as `MacOS`/`MacOs`, and both `v1.0` and `v.1.0`.

These are existing export names, not naming guidance for new resources. Do not infer a missing license label, tier, platform, or assignment scope from a short name. Inspect the resource contents, description, dependencies, licensing, and intended scope before deployment.

The Conditional Access folder contains distinct policy, group, and migration-table resources; review how they relate before importing. See [Policy collections](file-structure.md) for the current folder contents.
