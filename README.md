# Ansible

A lightweight, production-ready Ansible Docker image for running playbooks in CI/CD pipelines or local automation, pre-loaded with common community collections and WinRM support for managing Windows nodes.

<!-- sf:project:start -->
[![GitHub](https://img.shields.io/badge/GitHub-mirror-181717?logo=github)](https://github.com/HomeLabHD/ansible) [![GitLab](https://img.shields.io/badge/GitLab-source-FC6D26?logo=gitlab)](https://gitlab.prplanit.com/HomeLabHD/ansible) [![license](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/license.svg)](https://github.com/HomeLabHD/ansible/blob/main/LICENSE) [![Open Issues](https://img.shields.io/github/issues/HomeLabHD/ansible)](https://github.com/HomeLabHD/ansible/issues) [![Open PRs](https://img.shields.io/github/issues-pr/HomeLabHD/ansible)](https://github.com/HomeLabHD/ansible/pulls) [![Contributors](https://img.shields.io/github/contributors/HomeLabHD/ansible)](https://github.com/HomeLabHD/ansible/graphs/contributors) [![donate](https://img.shields.io/badge/donate-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/T6T41IT163) [![sponsor](https://img.shields.io/badge/sponsor-EA4AAA?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/HomeLabHD)
<!-- sf:project:end -->
<!-- sf:badges:start -->
[![release](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/release.svg)](https://github.com/HomeLabHD/ansible/releases) [![build](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/build.svg)](https://gitlab.prplanit.com/HomeLabHD/ansible/-/pipelines) [![Last Commit](https://img.shields.io/github/last-commit/HomeLabHD/ansible)](https://github.com/HomeLabHD/ansible/commits) [![StageFreight](https://img.shields.io/badge/StageFreight-0.9.2--dev+86a1675-310937?logo=readthedocs&logoColor=white)](https://stagefreight.prplanit.com)
<!-- sf:badges:end -->
<!-- sf:image:start -->
[![GHCR](https://img.shields.io/badge/GHCR-homelabhd%2Fansible-181717?logo=github&logoColor=white)](https://github.com/HomeLabHD/ansible/pkgs/container/ansible) [![Docker](https://img.shields.io/badge/Docker-hlhd%2Fansible-2496ED?logo=docker&logoColor=white)](https://hub.docker.com/r/hlhd/ansible) [![pulls](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/pulls.svg)](https://hub.docker.com/r/hlhd/ansible) [![Harbor](https://img.shields.io/badge/Harbor-hlhd%2Fansible-60b932)](https://cr.pcfae.com/harbor/projects)

[![latest](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/release-latest.svg)](https://github.com/HomeLabHD/ansible/pkgs/container/ansible) ![updated](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/release-updated.svg) [![size](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/release-size.svg)](https://github.com/HomeLabHD/ansible/pkgs/container/ansible) [![latest-dev](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/dev-latest.svg)](https://github.com/HomeLabHD/ansible/pkgs/container/ansible) ![updated](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/dev-updated.svg) [![size](https://raw.githubusercontent.com/HomeLabHD/ansible/main/.stagefreight/scribe/dev-size.svg)](https://github.com/HomeLabHD/ansible/pkgs/container/ansible)
<!-- sf:image:end -->

### Image Contents

<!-- sf:versions:start -->
[![python 3.14.7](https://img.shields.io/badge/python-3.14.7-0078D4?style=flat)](https://hub.docker.com/_/python)
<!-- sf:versions:end -->

### System Packages

<!-- sf:apk:start -->
[![bash](https://img.shields.io/badge/bash-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=bash) [![coreutils](https://img.shields.io/badge/coreutils-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=coreutils) [![curl](https://img.shields.io/badge/curl-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=curl) [![git](https://img.shields.io/badge/git-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=git) [![jq](https://img.shields.io/badge/jq-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=jq) [![openssh](https://img.shields.io/badge/openssh-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=openssh) [![openssh-keygen](https://img.shields.io/badge/openssh--keygen-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=openssh-keygen) [![rage](https://img.shields.io/badge/rage-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=rage) [![rsync](https://img.shields.io/badge/rsync-555?style=flat)](https://pkgs.alpinelinux.org/packages?name=rsync)
<!-- sf:apk:end -->

### Python Packages

<!-- sf:pip:start -->
[![ansible-core 2.20.4](https://img.shields.io/badge/ansible--core-2.20.4-2ea043?style=flat)](https://pypi.org/project/ansible-core/) [![ansible-lint 26.3.0](https://img.shields.io/badge/ansible--lint-26.3.0-2ea043?style=flat)](https://pypi.org/project/ansible-lint/) [![hvac](https://img.shields.io/badge/hvac-555?style=flat)](https://pypi.org/project/hvac/) [![kubernetes](https://img.shields.io/badge/kubernetes-555?style=flat)](https://pypi.org/project/kubernetes/) [![pip](https://img.shields.io/badge/pip-555?style=flat)](https://pypi.org/project/pip/) [![pywinrm](https://img.shields.io/badge/pywinrm-555?style=flat)](https://pypi.org/project/pywinrm/) [![requests](https://img.shields.io/badge/requests-555?style=flat)](https://pypi.org/project/requests/)
<!-- sf:pip:end -->

### Ansible Collections

<!-- sf:galaxy:start -->
[![ansible.posix](https://img.shields.io/badge/ansible.posix-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/ansible/posix/) [![ansible.windows](https://img.shields.io/badge/ansible.windows-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/ansible/windows/) [![community.docker](https://img.shields.io/badge/community.docker-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/community/docker/) [![community.hashi_vault](https://img.shields.io/badge/community.hashi__vault-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/community/hashi_vault/) [![community.sops](https://img.shields.io/badge/community.sops-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/community/sops/) [![kubernetes.core](https://img.shields.io/badge/kubernetes.core-555?style=flat)](https://galaxy.ansible.com/ui/repo/published/kubernetes/core/)
<!-- sf:galaxy:end -->

### Binary Tools

<!-- sf:binaries:start -->
[![kubectl v1.34.8](https://img.shields.io/badge/kubectl-v1.34.8-2ea043?style=flat)](https://dl.k8s.io/release/${KUBECTL_VERSION}/bin/linux/amd64/kubectl) [![kustomize v5.8.1](https://img.shields.io/badge/kustomize-v5.8.1-2ea043?style=flat)](https://github.com/kubernetes-sigs/kustomize/releases/download/kustomize%2F${KUSTOMIZE_VERSION}/kustomize_${KUSTOMIZE_VERSION}_linux_amd64.tar.gz) [![sops v3.13.3](https://img.shields.io/badge/sops-v3.13.3-2ea043?style=flat)](https://github.com/getsops/sops/releases/download/${SOPS_VERSION}/sops-${SOPS_VERSION}.linux.amd64) [![yq v4.53.6](https://img.shields.io/badge/yq-v4.53.6-2ea043?style=flat)](https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/yq_linux_amd64)
<!-- sf:binaries:end -->

### Documentation

| Topic | |
|-------|-|
| [Usage](docs/Usage.md) | Running the image locally and in CI/CD |
| [CI Component](docs/Component.md) | GitLab CI component inputs and setup |
| [Windows](docs/Windows.md) | WinRM configuration and inventory |

## Installation

```bash
docker run --rm -v $(pwd):/app -w /app docker.io/hlhd/ansible:latest ansible-playbook playbook.yaml
```

## License

Distributed under the [GPL-3.0](LICENSE) License.
