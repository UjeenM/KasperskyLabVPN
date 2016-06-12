## Requirements
- Ansible 2.0  
- Fedora 23 (x86_64)
- sudo without password prompt (use appropriate ansible options otherwise)

### Install Ansible 2.0
`dnf --enablerepo updates-testing install ansible python-dnf libselinux-python -y`

### Install SafeNet Authentication Client on Fedora 23
- request the software using http://www.aladdin-rd.ru/support/request.php or use default url in SafeNet.yml (until it expires)
- install SafeNet Authentication Client with  
  `ansible-playbook SafeNet.yml` 
- check with  
  `sudo pkcs11-tool --module /usr/lib64/libeTPkcs11.so -L`

### Setup certificates
`ansible-playbook certificates.yml`

### Setup ppp
`ansible-playbook ppp.yml.yml`
