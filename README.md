# scoop-bucket

[![Tests](https://github.com/kevinswiber/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/kevinswiber/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/kevinswiber/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/kevinswiber/scoop-bucket/actions/workflows/excavator.yml)

A [Scoop](https://scoop.sh) bucket for tools by [@kevinswiber](https://github.com/kevinswiber).

## Install

```powershell
scoop bucket add kevinswiber https://github.com/kevinswiber/scoop-bucket
scoop install kevinswiber/drop
```

## Manifests

| App | Description |
|-----|-------------|
| [drop](bucket/drop.json) | Run a command on Windows without elevated privileges. A PowerShell port of busybox-w32's drop/pdrop. [Source](https://github.com/kevinswiber/drop-ps1). |

## Maintenance

Manifests carry `checkver` and `autoupdate` fields, and the Excavator
workflow runs `bin/auto-pr.ps1` on a schedule to open pull requests for new
upstream releases. The CI workflow validates every manifest with
`Scoop-Bucket.Tests.ps1`.

Based on [ScoopInstaller/BucketTemplate](https://github.com/ScoopInstaller/BucketTemplate).
