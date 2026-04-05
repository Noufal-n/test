---
# tasks file for fresco_nginx
- name: Install nginx and postgresql
  package:
    name:
      - nginx
      - postgresql
    state: present




  ansible-playbook -i "localhost," -c local mainplaybook.yml
