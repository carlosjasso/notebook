# Check SSL Certs properties

`openssl x509 -noout -text -in /path/to/file`

This should output the same MD5 value:

- `openssl x509 -noout -modulus -in /path/to/crtFile | md5sum`
- `openssl rsa -noout -modulus -in /path/to/keyFile | md5sum`
