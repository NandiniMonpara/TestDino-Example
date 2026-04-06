# TestDino - Azure DevOps Playwright Example

This is an example project that shows how to run Playwright tests on Azure DevOps with 4 shards and upload the merged report to TestDino.

The example pipeline:

- installs dependencies and Playwright browsers
- runs Playwright tests in 4 matrix shards
- stores blob reports from each shard
- merges the shard reports into `playwright-report/report.json`
- uploads the merged report to TestDino

Set the `TESTDINO_TOKEN` secret pipeline variable.

Get your token from [testdino](https://app.testdino.com).

Copy this folder into the root of your repository and keep `azure-pipelines.yml` at the repository root.

Local commands:

```bash
npm ci
npx playwright install
npx playwright test
npx tdpw upload ./playwright-report --token="YOUR_TESTDINO_TOKEN"
```
