# ansble-role-chkbuild

- Setup chkbuild

## Requirements

- Debian GNU/Linux 9
- Ubuntu 16.04 LTS (xenial)

## Role Variables

see defaults/main.yml

## Dependencies

- systemd

## Example Playbook

    ---
    - hosts: all
      become: yes
      roles:
      - role: znz.chkbuild
      tasks:
      - name: "Install chkbuild dependencies"
        apt:
          name: "{{ item }}"
        with_items:
        - subversion
        - autoconf
        - bison


## License

MIT License
