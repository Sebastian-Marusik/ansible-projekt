# Ansible Ubuntu

Projekt demonstracyjny przedstawiający konfigurację i wstępne zabezpieczenie maszyny Ubuntu za pomocą Ansible.

## Wykorzystane narzędzia:
- Ubuntu Server 22.04 (VM)
- Ansible
- SSH
- Bash

## Struktura projektu
- `hosts` – plik inwentarza z IP maszyny
- `setup.yml` – playbook konfigurujący m.in. użytkownika, SSH i pakiety
- `harden.yml` – playbook z twardym zabezpieczeniem systemu

## Jak uruchomić:
```bash
ansible -i hosts all -m ping
ansible-playbook -i hosts setup.yml --ask-become-pass
ansible-playbook -i hosts harden.yml --ask-become-pass
