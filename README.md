TD;DR

run: 

```
SERVER_TO_BE_SECURED_IP=server_id SERVER_MANAGER_USER_PASSWORD=password sh run.sh
```

This is an Ansible project that aims to setup the security generic related sever configuration. What it covers:

1. Upgrades current packages
2. Creates a **sudo** deploy user with a specific password
3. Gets the ssh keys from a set of github accounts and authorizes a ssh connection using them
4. Changes the permission of the .ssh/authorized_keys to 400
5. Disables empty password login
6. Disables password login
7. Disables remote root login
8. Installs a set of basic security packages like:
  8.1.  ufw
  8.2. fail2ban
  8.3. unattended-upgrades
9. Configures automatic updates
10. Change ssh port to 300 ( you can change it on the variables.yml )
11. Setups ufw
12. Allows ssh connection on the port defined before
13. Restarts server

Feel free to customize the deploy user name and other small things on the **variables.yml** file.
