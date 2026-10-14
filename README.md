# Ánh Sáng và Cuộc Sống Actions Hub

This repo is exclusively for anhsangvacuocsong.vn.

- **sync-qa.yml**: read-only QA of Astro `github`, PHP `master`, FTP recovery script.
- **deploy.yml**: WordPress `wp_trigger_build` or manual GitHub workflow for Astro `master` only. Requires matching `WC_URL_CLIENT=https://anhsangvacuocsong.vn`, matching FTP path `/domains/anhsangvacuocsong.vn/public_html/`, valid SEO artifact, and signed remote unzip preflight.
- Secrets: `SOURCE_REPO_PAT`, `ENV_FILE`, `FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD`.
- WordPress PHP must configure `VCS_GH_REPO=anhsangvacuocsong-actions`.
- Code ported into Astro `github` must be integrated safely into `master` before production deploy. The current histories are unrelated; **do not force-push or overwrite master**.
- The original Blue Sea workflows under `workflow-templates/blue-sea/` are historical, INACTIVE and not runnable for this project.
