## Alert via telegram when user logon via SSH

### Requirement
- curl
- git (much easy to install)

### Install
1) Clone or download to /opt/ folder
```cd /opt/ && git clone https://github.com/kogonia/ssh-login-alert-telegram.git```

2) Edit two configuration variables (KEY, USERID) by editing file:
```vim telegram```

3) Add this script when user connect like this:
```echo "#!/usr/bin/env bash
# Log connection
bash /opt/ssh-login-alert-telegram/alert.sh" > /etc/profile.d/telegram-alert.sh
```

4) Confirm that the script is working by logging you to ssh again.
