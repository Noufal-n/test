ansible localhost -m file -a "path=/home/user/test state=directory"


touch simplefile.txt



- name: Check if the file already exists in the destination
  stat:
    path: /home/user/test/simplefile.txt
  register: file_data

- name: Move simplefile.txt to the test directory
  command: mv simplefile.txt /home/user/test/simplefile.txt
  when: not file_data.stat.exists
