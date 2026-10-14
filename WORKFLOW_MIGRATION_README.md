# Ánh Sáng Và Cuộc Sống — Blue Sea Actions source copy

This repository was synchronized from `ngocnhanvo/xuongmunonbaohiem-actions:main` (source commit `7c59237c36b13b97101ce95dd3ac0acceb5f8509`).

- `github` branch contains the complete original source snapshot at its original file paths (234/234 files, Git blob SHA parity).
- `main` contains all 117 non-workflow source files at their original paths, including scripts, reports, and request templates.
- All 117 original workflow YAML files are preserved byte-for-byte in `workflow-templates/blue-sea/`, *not* in the active `.github/workflows/` folder.
- This is intentional: old workflows refer to the Blue Sea Astro/PHP repositories, domains, FTP deployment targets, and production/admin endpoints. Copying them into the active directory could deploy or modify the **wrong website**. No deployment was requested or performed.
- Before enabling an individual workflow for this project, carefully replace Blue Sea repository references and domains, validate environment/secrets and FTP paths, decide triggers, and test read-only first. Restore the workflow into `.github/workflows/` only after confirming the target is `anhsangvacuocsong`.
- Do not treat this repository copy as a WordPress database, uploads, FTP files or GitHub Secrets migration. Only tracked Git files were copied.

Source code: `ngocnhanvo/xuongmunonbaohiem-actions`.
Destination: `ngocnhanvo/anhsangvacuocsong-actions`.
