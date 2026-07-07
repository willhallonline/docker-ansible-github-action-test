# docker-ansible-github-action-test

Integration test repository for [`willhallonline/docker-ansible-github-action`](https://github.com/willhallonline/docker-ansible-github-action).

It doesn't test any real infrastructure. It simply runs a minimal playbook
(`playbooks/site.yml`) against `localhost` using the action, across a matrix
of `willhallonline/ansible` image tags, to confirm that:

- the action can pull and run each image tag
- `ansible-playbook` executes successfully inside the container
- facts are gathered and a basic module (`ping`) runs
- the action's `exit-code` output correctly reflects success

See [`.github/workflows/test.yml`](.github/workflows/test.yml) for the test
matrix and [`playbooks/site.yml`](playbooks/site.yml) for the playbook used.
