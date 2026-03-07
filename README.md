[![CI](https://github.com/de-it-krachten/ansible-role-xrdp/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-xrdp/actions?query=workflow%3ACI)


# ansible-role-xrdp

Install and configuration `xrdp`, an open-source Remote Desktop Protocol server.<br>
https://www.xrdp.org/<br>



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- SUSE Linux Enterprise 15<sup>1</sup>
- SUSE Linux Enterprise 16<sup>1</sup>
- openSUSE Leap 15
- openSUSE Leap 16
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 42
- Fedora 43

Note:
<sup>1</sup> : no automated testing is performed on these platforms


## Role Variables
### defaults/main.yml
<pre><code>
# List of packages
xrdp_packages:
  - xrdp

# Open RDP port on firewall
xrdp_firewall: false
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'xrdp'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'xrdp'
      ansible.builtin.include_role:
        name: xrdp
</pre></code>
