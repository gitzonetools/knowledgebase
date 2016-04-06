# SSL

## Generate self-singed SSL
```
#!/bin/bash
echo "Generating an SSL private key to sign your certificate..."
openssl genrsa -des3 -out ./newssl/server.key 2048

echo "Generating a Certificate Signing Request..."
openssl req -new -key ./newssl/server.key -out ./newssl/server.csr

echo "Removing passphrase from key (for nginx)..."
cp ./newssl/server.key ./newssl/server.key.org
openssl rsa -in ./newssl/server.key.org -out ./newssl/server.key
rm ./newssl/server.key.org

echo "Generating certificate..."
openssl x509 -req -days 365 -in ./newssl/server.csr -signkey ./newssl/server.key -out ./newssl/server.crt

echo "SSL script finished"

```

> Note: The script above creates a self signed certificate, which will throw trust errors when used in common browsers like Google Chrome, Apple Safari or Mozilla Direfox. You can create free valid certificates using letsencrypt.
