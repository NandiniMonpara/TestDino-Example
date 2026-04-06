# TestDino - Jenkins Playwright Example

This is an example project that shows how to run Playwright tests on Jenkins with 4 shards and upload the merged report to TestDino.

The example pipeline:

- installs dependencies and Playwright browsers
- runs Playwright tests in 4 parallel shards
- stores blob reports from each shard
- merges the shard reports into `playwright-report/report.json`
- uploads the merged report to TestDino

Create a Jenkins secret text credential with ID `TESTDINO_TOKEN`.

Copy this folder into the root of your repository and keep `Jenkinsfile` at the repository root.

Local commands:

```bash
npm ci
npx playwright install
npx playwright test
npx tdpw upload ./playwright-report --token="YOUR_TESTDINO_TOKEN"
```
