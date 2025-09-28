# Ansible Role: uv

[![Ansible Galaxy](https://img.shields.io/ansible/role/d/aymericderbois/uv)](https://galaxy.ansible.com/aymericderbois/uv)
[![MIT License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/aymericderbois/ansible-role-uv/blob/main/LICENSE)

Installe [uv](https://github.com/astral-sh/uv), un gestionnaire de paquets Python extrêmement rapide, écrit en Rust.

## Plateformes supportées

- Debian 11 (Bullseye)  
- Debian 12 (Bookworm)

## Utilisation

```yaml
- hosts: servers
  become: true
  roles:
    - aymericderbois.uv
```

## Variables principales

```yaml
# Version d'uv à installer
uv_version: "0.8.22"

# Force la réinstallation
uv_force_install: false
```

Voir `defaults/main.yml` pour toutes les variables disponibles.

## Tests

```bash
# Installer les dépendances (venv recommandé)
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt

# Tests
make test        # Debian 12
make test-all    # Debian 11 + 12
make lint        # Linters
```

## Licence

MIT - [aymericderbois](https://github.com/aymericderbois)