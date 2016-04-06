# SSH
SSH is a ever handy tool from git to server management - SSH is your friend and time-saver.  
SSH keys are very usefull for server communication.

### Generate a SSH key pair

type in a terminal:

```sh
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
# Creates a new ssh key, using the provided email as a label
# Generating public/private rsa key pair.
```

> Note: Your default SSH idendentity will be stored at `~/.ssh/id_rsa`. It'll be used for SSH authentication without any config. You can use multiple identities and wire them up with a config file at `~/.ssh/config`.

### Store SSH key in Env-Vars

```sh
# creates base 64 encoded var 
openssl base64 -A -in id_rsa -out id_rsa64
```

then store it in an ENV Variable.

then when you need to read the key:

```shell
# writes the key to disk in base64 encoding
echo $RESIN_SSHKEY > ~/.ssh/id_rsa64

# converts it to valid SSH key
openssl base64 -d -A -in ~/.ssh/id_rsa64 -out ~/.ssh/id_rsa 
```
