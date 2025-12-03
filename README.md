# Ton Console
Launch a successful business with TON blockchain: manage dapps, tokens and payments in one place with powerful API and deep commercial integrations

[Try it](https://tonconsole.com/)

![alt text](https://github.com/tonkeeper/ton-console/blob/master/public/og-image.png "")

## Run locally
1. `nvm use`
2`npm i`
3`npm run dev`

### Generate api
1. Put new swagger.yaml to the `./scripts`
2. `npm run generate-api`

### Lint & test
- lint (eslint & prettier): `npm run lint`
- test (vitest): `npm run test`
- check typings (vite DOESN'T do it automatically): `npx tsc --noEmit`

### Husky pre-commit hook
Runs lint for staged files and checks typescript typings
(You don't have to install or configure husky, it is done automatically) 

## Build for dev
1. `nvm use`
2. `npm ci`
3. `npm run build:staging`

## Build for dev2
1. `nvm use`
2. `npm ci`
3. `npm run build:staging2`

## Build for prod
1. `nvm use`
2. `npm ci`
3. `npm run build`

## Security Scanning

### Manual Workflow (workflow_dispatch only)
A manual-only GitHub Actions workflow is available at `.github/workflows/security-scan.yml`. This workflow:
- Runs only on manual dispatch (workflow_dispatch) - never on push or PR
- Scans for suspicious patterns (CI downloads, eval/exec usage, base64/obfuscation)
- Lists recent commits (30 days)
- Uploads artifacts for review

To run: Go to Actions → "security-scan" → "Run workflow"

### Local Helper Script
Use `scan-repo.sh` to run security scans locally on a mirror or working clone:
```bash
./scan-repo.sh /path/to/repo [output-dir]
```

