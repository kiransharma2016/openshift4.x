#### sshd auto setup rootlogin etc
#!/bin/bash
 sudo sed -i "/^[^#]*PasswordAuthentication[[:space:]]no/c\PasswordAuthentication ye
 sed -i "s/.*PermitRootLogin.*/PermitRootLogin yes/" sshd_config
 sed -i "s/.*PubkeyAuthentication.*/PubkeyAuthentication yes/" sshd_config

 sudo service sshd restart
