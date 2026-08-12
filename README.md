# github-backups
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

This repository contains a CloudFormation template which deploys:

- an S3 bucket
- a Bucket Policy
- an IAM role for GitHub to assume, so it can `PutObject`

This will allow any repository in the relevant organization to use a
shared GitHub workflow to upload files created by `git bundle` to the bucket.

The bucket itself is tagged with our `BackupFrequency` vocabulary, so its
contents will be backed up by
[backup-as-a-service](https://github.com/govuk-one-login/backup-as-a-service)
(so we get backups of our backups).

## Licence
[MIT License](LICENSE)
