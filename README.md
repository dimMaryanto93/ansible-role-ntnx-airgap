`dimmaryanto93.ntnx_airgap`
=========

Repository ini digunakan untuk Install dan upload darksite package Nutanix seperti NKE Airgap dan Object storage.

Support platform

- CentOS 7
- OracleLinux 9


Ansible - User Guide
------------

Persiapan yang harus di lalukan, diantaranya

1. Authenticate with private-key for login ssh, generate ssh key on your local machine then use `ssh-copy-id user@your-ip-server` to copy public key to your server.


Requirements
------------

Untuk menggunakan role ini, kita membutuhkan Installer/package lcm bundle kita perlu download dari [Nutanix Portal (support & insight)](https://portal.nutanix.com/page/downloads/list)


Role Variables
--------------

Ada beberapa variable yang temen-temen bisa gunakan untuk install oracle jdk, diantaranya seperti berikut:

| Variable name          | Example value | Description |
| :---                   | :---          | :---        |
| `default_nke_airgap_folder`  | `~/Downloads/nke/2.8.0` | |
| `default_object_airgap_folder`  | `~/Downloads/object/3.6` | |
| `direct_download`  | `false` | |

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```ansible
- hosts: ["all"]
  become: true
  vars:
    direct_download: false
    default_nke_airgap_folder: /Volumes/data/packages/Nutanix/nke/2.8.0
    default_object_airgap_folder: /Volumes/data/packages/Nutanix/object/3.6
  roles:
    - ../../ansible-role-ntnx-airgap
```

License
-------

MIT
