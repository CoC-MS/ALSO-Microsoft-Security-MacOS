# 📖 Policy naming

[Documentation index](README.md) | [Short-name exceptions](short-name-exceptions.md)

Many policy display names in this repository follow a pattern similar to:

```text
ALSO – <Impact> – <License label> – <Tier> – <Version> – MacOS – <Category> - <Policy purpose> - <Scope>
```

For example, an MDE onboarding resource is named `ALSO – LI – BP – Basic – v1.0– MacOS – Device Configuration - MDE System Extensions - D`.

## Naming components

| Component | Description | Examples observed |
| --- | --- | --- |
| `ALSO` | Template provider | `ALSO` |
| `Impact` | Impact label in the exported name | `LI`, `MI`, `HI` |
| `License label` | Label included in some exported names; verify requirements independently | `BP`, `BPE5` |
| `Tier` | Baseline tier where present | `Basic`, `Adv` |
| `Version` | Version text where present | `v1.0`, `v.1.0` |
| `Platform` | Target platform where present | `MacOS`, `MacOs` |
| `Category` | Intune workload or configuration area | `Device Configuration`, `Compliance`, `Microsoft Edge` |
| `Policy purpose` | Short description of configured settings | `FileVault`, `MDE System Extensions` |
| `Scope` | Assignment hint where present | `D` (device), `U` (user) |

Names and filenames are copied from the exports and have not been normalized. Spacing, dash characters, spelling, and capitalization vary. Do not rename imported objects or infer licensing, settings, assignment, or applicability solely from a name. See [Short-name exceptions](short-name-exceptions.md).
