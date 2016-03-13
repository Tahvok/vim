Role Name
=========

Install vim and configure with vundle (providing vimrc)

You should review templates/vimrc.j2 and change it to your needs.
The provided vimrc has been checked on remote Debian/Ubuntu and RedHat/Centos systems.

Requirements
------------

Git and vim are checked in this role, so no package requirements, however, it will install .vimrc file provided by this role in templates/vimrc.j2. You may want to change it.

Role Variables
--------------

defaults/main.yml:

```
# github vundle repo url
vim_vundle_repo: "https://github.com/VundleVim/Vundle.vim.git" 

# where to install the vundle package
vim_vundle_dest: "{{ ansible_user_dir }}/.vim/bundle/Vundle.vim" 

# vimrc template file
vim_vimrc_src: "vimrc.j2" 

# where vimrc should be installed on dest
vim_vimrc_dest: "{{ ansible_user_dir }}/.vimrc" 
```

Dependencies
------------


Example Playbook
----------------

    - hosts: servers
      roles:
         - Tahvok.vim

License
-------

MIT

Author Information
------------------

Albert Mikaelyan
http://tahvok.com

