# 📥 How to import

[Documentation index](README.md)

Complete [General prerequisites](general-prerequisites.md) and review [macOS prerequisites](macos-prerequisites.md) and [Policy collections](file-structure.md) before importing.

The repository README refers to the [Micke M Intune Management Tool](https://github.com/Micke-K/IntuneManagement) for importing the exported resources. Follow the tool's current setup, authentication, platform, and permission instructions. This repository does not include an import script or command.

## Review and prepare

1. Download or clone this repository and inspect the collection and individual JSON resources you plan to use.
2. Read the policy descriptions and confirm the target tenant, licensing, settings, tenant-specific values, dependencies, and device or user scope.
3. Prepare any required tenant-specific Defender onboarding or offboarding content. Do not assume those packages are included in this repository.
4. Sign in to the intended Intune tenant using an account with the necessary permissions. Review and approve any requested API consent through your organization's process.

## Import selected resources

1. In the import tool, select **Bulk > Import** as described in the repository README and the tool's current documentation.
2. Select only the intended collection and resources. Do not select the repository root or import unrelated collections together.
3. Import prerequisite resources first. In particular, the `ALSO_MACOS_MDCA_READY` description requires MDE onboarding policies to be deployed first.
4. For the MDE onboarding collection, review the app and all related policies, and configure the tenant-specific onboarding content according to current Microsoft guidance.
5. For offboarding, use the macOS MDM offboarding package downloaded from the Defender portal with the offboarding policy, as described in the repository README.
6. Import Conditional Access policies in **Off** mode. The repository README also calls for the Conditional Access Administrator role. Review policy conditions, group resources, exclusions, assignments, and effects before enabling a policy.
7. Inspect import results and the resulting Intune objects. Assign to a pilot group, validate deployment and user impact, and expand in stages only after review.

> [!WARNING]
> Do not bulk-assign imported policies or enable Conditional Access policies without reviewing their scope and effect. Keep an appropriate recovery or rollback plan.

For import problems or documentation corrections, see [Reporting issues](reporting-issues.md).
