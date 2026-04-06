# TestDino Examples

This repository contains ready-to-use Playwright example projects for different CI/CD providers.

Each example:

- runs Playwright tests
- splits CI execution into 4 shards
- merges shard results into `playwright-report/report.json`
- uploads the merged report to TestDino

Pick one folder, copy it into the root of your own repository, add `TESTDINO_TOKEN`, and run the pipeline.

Get your token from [testdino](https://app.testdino.com).

## Available examples

- `playwright/github-actions`
- `playwright/gitlab-ci`
- `playwright/circleci`
- `playwright/jenkins`
- `playwright/azure-devops`
- `playwright/aws-codebuild`
