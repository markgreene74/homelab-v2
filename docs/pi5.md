# pi5 setup

- [pre-work](#pre-work)
- [(re)build pi5](#rebuild-pi5)
- [reference, documentation and useful links](#reference-documentation-and-useful-links)

## pre-work

- start from a base Ubuntu Desktop LTS image (e.g., Ubuntu 24.04.1 LTS)
- install `pipx`
  ```shell
  sudo apt update && sudo apt install pipx
  ```
  ```shell
  pipx ensurepath
  ```
- install `ansible` using `pipx`
  ```shell
  pipx install --include-deps ansible
  ```

## (re)build pi5

- run `ansible-playbook` with the option `--ask-become-pass|-K`
  ```shell
  cd pi5/ansible
  ```
  ```shell
  ansible-playbook main.yml --ask-become-pass
  ```

## reference, documentation and useful links

- https://ubuntu.com/download/raspberry-pi
- https://github.com/pypa/pipx?tab=readme-ov-file#install-pipx
- https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
