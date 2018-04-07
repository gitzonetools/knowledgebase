# Servermangement @ Lossless

At lossless servers are managed in a consistent and predefined way, to allow utmost föexibility at the docker level while keeping a tight standard on our way there.

# Basic Server setup

OS: Ubuntu 16.04 LTS

**Adjusting the hostname**
```shell
hostnamectl set-hostname [YourName]
```

**First command to be run:**

```shell
curl -o- https://curlfresh.ship.zone/setup.sh | sh
```