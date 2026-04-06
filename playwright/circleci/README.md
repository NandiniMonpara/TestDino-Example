# TestDino - CircleCI Playwright Example

This is an example project that shows how to run Playwright tests on CircleCI with 4 parallel containers and upload the merged report to TestDino.

The example config:

- installs dependencies
- runs Playwright tests in 4 shards
- stores blob reports from each shard
- merges the shard reports into `playwright-report/report.json`
- uploads the merged report to TestDino

Set the `TESTDINO_TOKEN` environment variable in CircleCI.

Get your token from [testdino](https://app.testdino.com).

Copy this folder into the root of your repository and keep `.circleci/config.yml` in the same location.

Local commands:

```bash
npm ci
npx playwright install
npx playwright test
npx tdpw upload ./playwright-report --token="YOUR_TESTDINO_TOKEN"
```
