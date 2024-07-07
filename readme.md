# comment

- Root CA pfx

```
cd /root/.local/share/mkcert
openssl pkcs12 -export -inkey rootCA-key.pem -in rootCA.pem -out rootCA.pfx
```