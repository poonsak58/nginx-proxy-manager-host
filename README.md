# Running
```bash
docker-compose up -d
```

# Login to Admin UI
http://127.0.0.1:81

### Default Admin User:
```bash
Email: admin@example.com
Password: changeme
```

# Firewall UFW (Ubuntu or Debian)
## important!! 

this for disable port 81 (Admin UI) access from outside.

`ufw` is installed by default on Ubuntu. You can check your already install it by command
```bash
ufw version
```
you can install it with `sudo apt install ufw`

## Checking UFW Status and Rules
```bash
sudo ufw status
```

## Enabling UFW
```bash
sudo ufw enable
```

## Allowing Connections
```bash
sudo ufw allow 21
sudo ufw allow 80
sudo ufw allow 443
```

## Deleing Rules
```bash
sudo ufw delete allow 443
```

## Disabling UFW
```bash
sudo ufw disable
```
or resetting (optional) by command
```bash
sudo ufw reset
```


## Access port 81 (Admin UI) by ssh tunnelling
```bash
ssh -L 81:127.0.0.1:81 <user>@<ip>
```
now open http://127.0.0.1:81 you can access it from your browser.