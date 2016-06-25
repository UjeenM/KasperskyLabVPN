## Requirements
- Ansible 2.0  
- Fedora >= 23

### Install Ansible 2.0
`dnf --enablerepo updates-testing install ansible python-dnf libselinux-python -y`

### Install SafeNet Authentication Client on Fedora 23
- request the software using http://www.aladdin-rd.ru/support/request.php
- they will send you link to Google Drive, download it somewhere on your computer, e.g. to ~/Downloads
- install SafeNet Authentication Client with  
  `ansible-playbook SafeNet.yml`
- check with  
  `sudo pkcs11-tool --module /usr/lib64/libeTPkcs11.so -L`

### Setup certificates
`ansible-playbook certificates.yml`

### Setup ppp
`ansible-playbook ppp.yml`
