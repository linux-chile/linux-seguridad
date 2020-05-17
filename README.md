# Linux-seguridad

## SSH Cambiar puerto
```
nano /etc/ssh/sshd_config
/etc/init.d/sshd restart
```

## Log
```
tail -f /var/log/auth.log
```

## fail2ban proteger acceso ssh
```
sudo apt-get update
sudo apt-get upgrade

sudo apt-get install -y fail2ban

sudo systemctl start fail2ban
sudo systemctl enable fail2ban

sudo nano /etc/fail2ban/jail.conf
sudo systemctl restart fail2ban
sudo fail2ban-client set sshd unbanip IP_ADDRESS
```
