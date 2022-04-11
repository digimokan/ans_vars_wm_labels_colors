# ans_role_vars_ucode_icons

Define a set of icons and labels for workspaces, tray items, etc.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_vars_ucode_icons.svg?label=release)](https://github.com/digimokan/ans_role_vars_ucode_icons/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Requirements](#requirements)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Vars](#role-vars)
* [Contributing](#contributing)

## Purpose

* Define common set of icons and labels for use in window manager panels,
  trays, indicator boxes, etc.

## Requirements

* A supporting unicode font, such as [DejaVu](https://dejavu-fonts.github.io/)
  or [Droid](https://en.wikipedia.org/wiki/Droid_(typeface)).

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_vars_ucode_icons
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role with `import_role`, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Define the icons and labels for workspaces, tray items, etc"
         ansible.builtin.import_role:
           name: ans_role_vars_ucode_icons
   ```

## Role Vars

See the role `vars` file:

  * [vars/main.yml](../vars/main.yml)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_vars_ucode_icons/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

