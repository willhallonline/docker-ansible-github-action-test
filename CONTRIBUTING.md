# Contributing to docker-ansible-github-action-test

Thank you for considering contributing! This repository is an integration test suite for [`willhallonline/docker-ansible-github-action`](https://github.com/willhallonline/docker-ansible-github-action), verifying that the action works correctly across every actively maintained [`willhallonline/ansible`](https://hub.docker.com/r/willhallonline/ansible) image tag.

## How Can I Contribute?

### Reporting Bugs

1. **Check Current Issues**: Before you create a new issue, please search for similar issues in the [Issue Tracker](https://github.com/willhallonline/docker-ansible-github-action-test/issues).
2. **Create a New Issue**: If your issue is new, please include:
   - **Title**: A succinct title that describes the issue.
   - **Description**: A detailed description, including steps to reproduce, and environment details (e.g., failing image tag, workflow run link).
   - **Logs and Error Messages**: Any relevant logs or error messages, ideally a link to the failing GitHub Actions run.

### Suggesting Features

If you have an idea to improve the test coverage or workflow, submit a feature request in the [Issue Tracker](https://github.com/willhallonline/docker-ansible-github-action-test/issues).

### Submitting Pull Requests

1. **Fork the Repository**: Create a fork of the repository on GitHub.
2. **Clone Your Fork**:

   ```bash
   git clone https://github.com/your-username/docker-ansible-github-action-test.git
   cd docker-ansible-github-action-test
   ```

3. **Create a Branch**:

   ```bash
   git checkout -b feature/your-feature-name
   ```

4. **Make Changes**: Develop your feature or fix in your local repository.
5. **Commit Changes**:

   ```bash
   git add .
   git commit -m "Description of your changes"
   ```

6. **Push Changes**:

   ```bash
   git push origin feature/your-feature-name
   ```

7. **Open a Pull Request**: Go to the repository on GitHub and open a pull request against `main`.

### Code Style and Testing

- **Keep the playbook minimal**: `playbooks/site.yml` should stay dependency-free and runnable entirely against `localhost`, so it works unmodified against every image tag in the matrix.
- **Keep the matrix in sync with upstream**: When `willhallonline/docker-ansible` adds or removes a supported tag, update the `image-tag` matrix in [`.github/workflows/test.yml`](.github/workflows/test.yml) to match, and verify new tags exist on [Docker Hub](https://hub.docker.com/r/willhallonline/ansible/tags) before adding them.
- **Testing**: Open a pull request so the workflow runs against the full matrix before merging. Ensure all matrix jobs pass.
- **Documentation**: Update `README.md` or `CHANGELOG.md` if your changes affect users.

### Reviewing and Approval

Pull requests are reviewed and merged once the full test matrix passes. Thanks for your patience during the review process.
