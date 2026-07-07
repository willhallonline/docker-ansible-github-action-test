# Changelog

## Unreleased

- Expanded the CI test matrix to cover all 59 actively maintained `willhallonline/ansible` image tags (Ansible 2.16-2.21 across Alpine 3.19/3.20/3.21/3.22, Debian Bookworm/Bookworm Slim/Trixie/Trixie Slim, Rocky Linux 10, and Ubuntu 22.04/24.04/26.04, plus the `latest`/`alpine`/`ubuntu` aliases).
- Changed the default branch from `master` to `main`.
- Added `CONTRIBUTING.md` and `CHANGELOG.md`.
- Added the initial CI workflow (`.github/workflows/test.yml`) that runs `willhallonline/docker-ansible-github-action` against a minimal localhost playbook (`playbooks/site.yml`) and verifies the action's `exit-code` output.
