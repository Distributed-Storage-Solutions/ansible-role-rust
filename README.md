<img alt="Logo for the Rust programming language" src="https://www.rust-lang.org/logos/rust-logo-256x256-blk.png" style="float:left" height="128" width="128">

# Ansible Role: Rust

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-rust.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-rust)
[![Ansible Rust](https://img.shields.io/badge/galaxy-fubarhouse--rust-22497.svg)](https://galaxy.ansible.com/fubarhouse/rust)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/fubarhouse/ansible-role-rust/master/LICENSE)

* Install Rust from source (when configured)
* Install Rust from recommended installer
* Install cargo packages
* Support 20 linux platforms, as done by the Go and Node roles.

## Requirements

  * curl
  * gcc

## Role Variables

The version of rust is dependent on a source installation.
It will nor otherwise be used, source installs are not tied to any given version.
````
rust_version: 1.20.0
````

By default, the role will not install from source.
````
build_rust_from_source: false
````

After any initial installation, you can make sure the script updates Rust using:
````
rust_update: false
````

To ensure a clean installation on each playbook run, you can use:
````
rust_install_clean: false
````

To ensure the role installs to your shell profiles, you can specify them:
````
shell_profiles:
- .bash_profile
````

And, to install any cargo you can use the `cargo_items` array:
````
cargo_items:
  - ripgrep
````

## Installation

* Install using `ansible-galaxy install fubarhouse.rust`
* Add this role to your playbook.
* Modify above variables as desired.

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Karl Hepworth](https://twitter.com/fubarhouse).