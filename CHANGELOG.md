# Changelog

## v1.1.1 - 2026-11-20

- Updated the CI test to use `willhallonline/docker-ansible-github-action@v1.1.1`.
- Clarified that the 61-tag matrix is compatibility coverage, with 41 current tags and aliases and 20 retained tags for legacy Ansible 2.16/2.17.
- Added explicit matrix comments distinguishing current upstream support from compatibility coverage.

## v1.1.0 - 2026-09-12

- Updated the CI test to use `willhallonline/docker-ansible-github-action@v1.1.0`.
- Replaced retired Alpine 3.19 and 3.20 images with Alpine 3.23 and 3.24 images, expanding the compatibility matrix to 61 image tags.
- Added a smoke-test assertion for the non-root `ansible` user used by current `willhallonline/ansible` images.

## v1.0.0 - 2026-07-07

- Expanded the CI test matrix to 59 compatibility tags (Ansible 2.16-2.21 across Alpine 3.19/3.20/3.21/3.22, Debian Bookworm/Bookworm Slim/Trixie/Trixie Slim, Rocky Linux 10, and Ubuntu 22.04/24.04/26.04, plus the `latest`/`alpine`/`ubuntu` aliases).
- Changed the default branch from `master` to `main`.
- Added `CONTRIBUTING.md` and `CHANGELOG.md`.
- Added the initial CI workflow (`.github/workflows/test.yml`) that runs `willhallonline/docker-ansible-github-action` against a minimal localhost playbook (`playbooks/site.yml`) and verifies the action's `exit-code` output.
