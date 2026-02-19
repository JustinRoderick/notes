## Run on a totally separate Machine

This is obvious, if something goes wrong your main driver is still safe

## Install necessary packages

```
pacamn -S ufw fail2ban
```
## Change user from root

If someone gains access to the agent they will have privileges to do anything they want on your machine.

```
sudo useradd -m -s /bin/bash name-of-agent

sudo usermod -aG wheel name-of-agent

su - name-of-agent
```

## Use keys for SSH auth

On local Computer
```
ssh-keygen -t ed25519 -a 64 -C "your-email"
```

Copy public key to server
```
ssh-copy-id -i ~/.ssh/id_ed25519.pub youradmin@your.server.ip
```

Disable password login
```
sudo nano /etc/ssh/sshd_config

- `PasswordAuthentication no`
- `PermitRootLogin no`

sudo systemctl restart sshd
```

## Start fail2ban
```
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
```

## Setup Firewall
```
ufw default deny incoming
ufw default allow outgoing
ufw allow 22/tcp comment 'SSH'
ufw enable
ufw status verbose
```

## Install and setup Tailscale
```
curl -fsSL https://tailscale.com/install.sh | sh
tailscale up

# IP that eill access openclaw 
tailscale ip -4
```

## Install Node
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash

nvm install 24.13.1 or node

nvm use node

node --version
npm -v
```

## Install Openclaw
```
npm install -g openclaw@latest

openclaw onboard --install-daemon
```

## Setup Gateway
- edit openclaw.json
```
{
  "gateway": {
    "bind": "100.x.x.x", # This is the tailscale ip
    "port": 39217 # Change this port
  }
}
```

## Restart gateway
```
openclaw gateway restart
```

