# docker-ansible-github-action-test

Integration test repository for [`willhallonline/docker-ansible-github-action`](https://github.com/willhallonline/docker-ansible-github-action).

It doesn't test any real infrastructure. It simply runs a minimal playbook
(`playbooks/site.yml`) against `localhost` using the action, across a matrix
of every actively maintained `willhallonline/ansible` image tag (59 tags,
per the [supported tags table](https://github.com/willhallonline/docker-ansible#supported-tags-and-respective-dockerfile-links)
— unmaintained Ansible versions 2.9-2.15 are excluded), to confirm that:

- the action can pull and run each image tag
- `ansible-playbook` executes successfully inside the container
- facts are gathered and a basic module (`ping`) runs
- the action's `exit-code` output correctly reflects success

See [`.github/workflows/test.yml`](.github/workflows/test.yml) for the test
matrix and [`playbooks/site.yml`](playbooks/site.yml) for the playbook used.
