# pa-permission-rollback-simulator
Simulates the impact of permission rollbacks (removal of access) to identify directly impacted resources and orphaned resources, meaning resources no user can still access after the rollback. This tool only simulates: it changes no file, permission, or account state. Uses networkx to build access graphs and simulate removals. An unknown user and an empty data file exit 1. - Focused on Tools for analyzing and assessing file system permissions

## Install
`git clone https://github.com/ShadowStrikeHQ/pa-permission-rollback-simulator`

## Usage
`./pa-permission-rollback-simulator [params]`

## Parameters
- `-h`: Show help message and exit
- `--user`: The user whose permissions are being rolled back.
- `--data_file`: No description provided

## License
Copyright (c) ShadowStrikeHQ
