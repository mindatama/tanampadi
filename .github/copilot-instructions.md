<!-- Copilot / AI agent guidance for the `tanampadi` repo -->
# Copilot instructions — tanampadi

Purpose
- Help AI agents be immediately productive editing docs and small Ansible examples in this repo.

Big picture
- This repository is primarily a documentation and tutorial collection about sysadmin and network projects maintained by the author.
- Major content lives in `README.md` and `Proyek/` (numbered project writeups). The repo contains no build system, tests, or compiled code.

Key files and patterns
- `README.md`: high-level site index and links to project pages.
- `Proyek/01-*.md`, `Proyek/02-*.md`, `Proyek/03-*.md`: step-by-step Ansible examples (inventory snippets, playbooks, run examples). Files are numbered with a two-digit prefix to indicate ordering.
- `img/`: screenshots referenced from project pages. Keep image link paths unchanged when editing docs.

Project-specific conventions
- Language: content is mostly Indonesian; preserve tone and terminology (e.g., "inventory", "playbook", "ansible").
- Ansible examples target `ansible 2.10.8` and reference `/etc/ansible/ansible.cfg` — do not change the documented version without confirmation.
- Inventory files are shown as `invcisco.ini` with `ansible_user`, `ansible_password`, `ansible_connection=network_cli`, and `ansible_network_os=ios` variables. Treat credential values as placeholders (do not invent real secrets).

Integration points & modules to note
- Ansible modules used in examples: `ios_logging` and `cisco.ios.ios_config` (from `cisco.ios` collection). If adding runnable playbooks, ensure required collections are declared (e.g., `ansible-galaxy collection install cisco.ios`).
- Example runtime targets referenced: managed devices at `10.10.0.[1:40]`, and backup destinations like `/srv/ftp/backup-cisco-config`.

How to edit (for AI agents)
- When improving a `Proyek/*.md` page: keep the three-stage structure (inventory → playbook → execute) used in existing files.
- Preserve code fences and shell examples exactly; when updating snippets, include a short explanation paragraph in Indonesian consistent with the author's voice.
- Never insert real credentials or IPs; use the same placeholder style as existing files (e.g., `user-cisco-kalian`, `password-cisco-kalian`).
- If adding new runnable playbooks to the repo, add a short README excerpt showing the exact `ansible-playbook` command used in the docs (examples in `Proyek/01-...` and `Proyek/02-...`).

Run / verification notes
- No CI/test harness detected. The canonical execution examples are in the docs, e.g.:

  `ansible-playbook /etc/.../logging-trap-errors-cisco.yaml -i /etc/.../invcisco.ini`

- To make examples runnable in-repo, add a `playbooks/` folder and include `requirements.yml` (Ansible collections) and a README with the `ansible-galaxy` and `ansible-playbook` commands.

Examples from this repo to reference
- Inventory example: `Proyek/01-ansible-config-log-trap-cisco.md` (shows `invcisco.ini` layout and `10.10.0.[1:40]`).
- Playbook example: `Proyek/02-ansible-config-backup-cisco.md` (uses `cisco.ios.ios_config` with `backup_options.dir_path`).

If uncertain
- Ask the repo owner before changing documented Ansible versions, switching module collections, or replacing Indonesian wording with English.
- For missing runnable artifacts (inventories or playbooks), propose adding a `playbooks/` and `inventory/` folder and present a minimal, non-sensitive example for approval.

Keep updates concise and incremental so the author can review changes easily.
