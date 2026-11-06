# pa-permission-rollback-simulator
Simulates the impact of permission rollbacks (removal of access) to identify directly impacted resources and orphaned resources, meaning resources no user can still access after the rollback. This tool only simulates: it changes no file, permission, or account state. Uses networkx to build access graphs and simulate removals. An unknown user and an empty data file exit 1. - Focused on Tools for analyzing and assessing file system permissions

## Install
`git clone https://github.com/ShadowGuard-AI/pa-permission-rollback-simulator`
`cd pa-permission-rollback-simulator`
`pip install -r requirements.txt`

## Usage
`python3 main.py --user <user> --data_file <file.json>`

The data file is JSON mapping each resource path to a list of users or groups with access, for example `{"/etc/shadow": ["alice", "root"]}`. A sample run with `--user alice` listed the two resources alice could access as directly impacted and exited 0.

## Parameters
- `-h`: Show help message and exit
- `--user` (required): The user whose permissions are being rolled back.
- `--data_file` (required): Path to a JSON file containing file system data (permissions).

## License
Licensed under the MIT License, see LICENSE.
