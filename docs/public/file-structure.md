# File structure

[Documentation index](README.md)

## 📂 File Structure

The repository exposes exactly two cumulative, standalone packages:

```text
/
├── ALSO_MACOS_BP/                  39 BP-compatible JSON artifacts
├── ALSO_MACOS_E5/                  39 cumulative JSON artifacts
├── docs/public/
├── LICENSE
├── README.md
├── README.preview.md
└── SECURITY
```

Both packages currently contain the same source membership because the repository has no E5-only source artifacts. The single `BPE5`-tagged `ALSO_MACOS_MDCA_READY` starter policy is included in BP only under the documented Custom Indicators limitation. Any future Defender for Cloud Apps policies beyond that starter policy belong only in E5.

| Workload folder in each package | JSON files | Classification |
| --- | ---: | --- |
| `ALSO_MACOS_MDE_AUTO_ONBOARDING` | 9 | BP |
| `ALSO_MACOS_MDCA_READY` | 1 | BP only with Custom Indicators; E5 supports the Cloud App Catalog workflow |
| `ALSO_MACOS_COMPLIANCE_POLICIES` | 4 | BP |
| `ALSO_MAC_CA_POLICIES` | 9 | BP |
| `ALSO_MACOS_DEVICE_CONFIG_POLICIES` | 6 | BP |
| `ALSO_MACOS_EDGE_POLICIES` | 5 | BP |
| `ALSO_MACOS_OFFICE365_POLICIES` | 4 | BP |
| `ALSO_MACOS_MDE_AUTO_OFFBOARDING` | 1 | BP |
| **Total** | **39** | **38 standard BP + 1 limited starter policy** |

## Historical source layout

The following original wording is retained to document how the source artifacts were organized before packaging:

All files are organized into categories

```text
/ALSO-Microsoft-Security-MacOS

├── ALSO_MACOS_MDE_AUTO_ONBOARDING/
├── Applications 1 application
├── DeviceConfiguration 8 Device Configuration policy templates
├── SettingsCatalog 1 SettingsCatalog policy template

├── ALSO_MACOS_MDCA_READY/SettingsCatalog
1 policy template

├── ALSO_MACOS_CIMPLIANCE_POLICIES/CompliancePolicies
├── 4 policy templates

├── ALSO_MACOS_CA_POLICIES/
├── Conditional Access 3 policy templates
├── Groups 5 group templates
├── MigrationTable.json

├── ALSO_MACOS_DEVICE_CONFIG_POLICIES/SettingsCatalog
6 policy templates

├── ALSO_MACOS_EDGE_POLICIES/SettingsCatalog
5 policy templates

├──ALSO_MACOS_OFFICE365_POLICIES/SettingsCatalog
4 policy templates

├──ALSO_MACOS_MDE_AUTO_OFFBOARDING/DeviceConfiguration
1 policy template
```

See [Policy and configuration descriptions](policy-collections.md) for the original explanations and [How to import](how-to-import.md) for the illustrated workflow.
