# Usage

## Run Locally

```bash
docker run --rm -v $(pwd):/app -w /app docker.io/hlhd/ansible:latest ansible-playbook playbook.yaml
```

### Advanced Example

```bash
docker run --rm \
  -v ./playbook.yaml:/root/playbook.yaml \
  -v /srv/gitops/project:/srv/gitops/project \
  -v ~/.ssh/id_rsa:/root/.ssh/id_rsa \
  docker.io/hlhd/ansible:latest \
  ansible-playbook --private-key /root/.ssh/id_rsa \
    -i /srv/gitops/project/ansible/inventory \
    /root/playbook.yaml \
    -e ansible_windows_password=$WINDOWS_ANSIBLE_PASSWORD
```

## GitLab CI/CD

```yaml
ansible-deploy:
  stage: deploy
  image: docker.io/hlhd/ansible:latest
  script:
    - ansible-playbook ansible/deploy.yaml -i ansible/inventory
```

## File Structure

The image expects playbooks and configuration inside `/app` by default.

```
/app
├── ansible.cfg
├── inventory
├── playbook.yaml
└── roles/
```

## Environment Variables

| Variable                    | Default | Description                                    |
| --------------------------- | ------- | ---------------------------------------------- |
| `ANSIBLE_HOST_KEY_CHECKING` | `false` | Disables host key checking for smoother CI use |

## Included Tools

<!-- sf:usage-tools:start -->
[![ansible-core 2.20.4](https://img.shields.io/badge/ansible--core-2.20.4-2ea043?style=flat)](https://pypi.org/project/ansible-core/) [![ansible-lint 26.3.0](https://img.shields.io/badge/ansible--lint-26.3.0-2ea043?style=flat)](https://pypi.org/project/ansible-lint/) [![hvac](https://img.shields.io/badge/hvac-555?style=flat)](https://pypi.org/project/hvac/) [![kubernetes](https://img.shields.io/badge/kubernetes-555?style=flat)](https://pypi.org/project/kubernetes/) [![pip](https://img.shields.io/badge/pip-555?style=flat)](https://pypi.org/project/pip/) [![pywinrm](https://img.shields.io/badge/pywinrm-555?style=flat)](https://pypi.org/project/pywinrm/) [![requests](https://img.shields.io/badge/requests-555?style=flat)](https://pypi.org/project/requests/)
<!-- sf:usage-tools:end -->

## Ansible Collections

<!-- sf:usage-galaxy:start -->
[![ansible.posix](https://img.shields.io/badge/ansible.posix-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/ansible/posix/) [![ansible.windows](https://img.shields.io/badge/ansible.windows-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/ansible/windows/) [![community.docker](https://img.shields.io/badge/community.docker-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/community/docker/) [![community.hashi_vault](https://img.shields.io/badge/community.hashi__vault-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/community/hashi_vault/) [![community.sops](https://img.shields.io/badge/community.sops-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/community/sops/) [![kubernetes.core](https://img.shields.io/badge/kubernetes.core-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/kubernetes/core/)
<!-- sf:usage-galaxy:end -->

## SSH Key Handling

The [CI component](Component.md) handles this automatically. When running the image directly, mount your key and add it to the agent:

```bash
docker run --rm \
  -v ~/.ssh/id_rsa:/root/.ssh/id_rsa:ro \
  docker.io/hlhd/ansible:latest \
  ansible-playbook --private-key /root/.ssh/id_rsa -i inventory playbook.yaml
```

## Notes

- This image is a control node only — it does not contain systemd or sshd.
- `CMD` defaults to `ansible-playbook --version`. Override by providing your own command.
