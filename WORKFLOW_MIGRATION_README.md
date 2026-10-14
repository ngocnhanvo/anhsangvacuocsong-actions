# Ánh Sáng Và Cuộc Sống — Workflow migration from Blue Sea

Source (read-only): `ngocnhanvo/xuongmunonbaohiem-actions:main` at `5c5190d725adf592e04eb8680094616a92d28d38`.

Destination (this project): `ngocnhanvo/anhsangvacuocsong-actions:main`.

## Current inventory (14 October 2026)
- All **125** source workflow YAMLs are preserved as immutable-reference templates at `workflow-templates/blue-sea/`; they are not active workflows.
- The last 8 additional workflows cover relative media URLs in Visual Builder, ESC Table cell preview, FTP resume, and SEO Files.
- Source request files for those recent workflows are also preserved; they are reference material, **not** deployment triggers.
- Active workflows in `.github/workflows/` are adapted for this website only:
  - `deploy.yml` and `ftp-artifact-recovery.yml` (strict domain/FTP guards, encrypted FTP archive);
  - `sync-qa.yml` (cross-repository regression tests);
  - `seo-files-production-smoke.yml` (manual-only read-only HTTP smoke of this domain).

## Safeguards
- Never enable a `workflow-templates/blue-sea/*` file as-is. It contains Blue Sea repository names, WordPress/FTP paths and live endpoints.
- Astro code may only be committed to the destination `github` development branch; `master` is production. WordPress PHP is permitted on the destination `master`.
- The Actions `main` deployment uses only `ngocnhanvo/anhsangvacuocsong-astro:master` and verifies `WC_URL_CLIENT=https://anhsangvacuocsong.vn` before upload.
- No database, uploads, FTP files, environment values or GitHub Secrets are copied.
- At the time of this audit, `sync-qa.yml` failed at external repository checkout because `SOURCE_REPO_PAT` was not supplied to the job. Configure this repository's `SOURCE_REPO_PAT` GitHub Actions secret before considering cross-repo CI verified. The FTP contract job passed. Separate Astro/PHP workflow runs were reported as failed without diagnostic step logs; no successful CI should be claimed.
