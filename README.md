# portfolio-trades-demo

Single-file static portfolio demo site for GrantOps Consulting's homepage `ProjectsGrid` surface. Brand: **Drygate Plasterworks** — fictional Glasgow plastering studio.

Deployed to `trades-demo.grantopsconsulting.com` via GitHub Actions OIDC on push to `main`. Infrastructure (S3 + Cloudflare DNS) lives in `GrantOps-Consulting/grantops-web-infra` under client slug `portfolio-trades-demo`.

## Notes

- `<meta name="robots" content="noindex, nofollow">` is in the head; the only intended path here is the curated link from grantopsconsulting.com.
- Footer carries: *Portfolio demo by GrantOps Consulting — no real business sits at this address. View our work at [grantopsconsulting.com](https://grantopsconsulting.com/).*
- No build step. `index.html` ships exactly as committed.

## Deploying

Push to `main`. The workflow at `.github/workflows/deploy.yml` syncs to the bucket via OIDC and purges Cloudflare cache.
