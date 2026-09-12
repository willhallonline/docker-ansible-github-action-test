# Changelog

## v1.1.0 - 2026-09-12

- Updated the CI test to use `willhallonline/docker-ansible-github-action@v1.1.0`.
- Replaced retired Alpine 3.19 and 3.20 images with Alpine 3.23 and 3.24 images, expanding the matrix to all 61 actively maintained image tags.
- Added a smoke-test assertion for the non-root `ansible` user used by current `willhallonline/ansible` images.

## v1.0.0 - 2026-07-07

- Expanded the CI test matrix to cover all 59 actively maintained `willhallonline/ansible` image tags (Ansible 2.16-2.21 across Alpine 3.19/3.20/3.21/3.22, Debian Bookworm/Bookworm Slim/Trixie/Trixie Slim, Rocky Linux 10, and Ubuntu 22.04/24.04/26.04, plus the `latest`/`alpine`/`ubuntu` aliases).
- Changed the default branch from `master` to `main`.
- Added `CONTRIBUTING.md` and `CHANGELOG.md`.
- Added the initial CI workflow (`.github/workflows/test.yml`) that runs `willhallonline/docker-ansible-github-action` against a minimal localhost playbook (`playbooks/site.yml`) and verifies the action's `exit-code` output.
