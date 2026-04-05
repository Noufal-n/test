---
# tasks file for fresco_loops
- name: Install required packages using a loop
  ansible.builtin.pkg:
    name: "{{ item }}"
    state: present
  loop:
    - apache2
    - sqlite3
    - git
 




ansible-playbook -i "localhost," -c local mainplaybook.yml
