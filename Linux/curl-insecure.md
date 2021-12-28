# CURL - Insecure request

Example: 

```bash
curl -k -X POST "<url>" \
-F "<form-field-name>=<form-field-value>" \
-F "<form-field-name>=<form-field-value>" \
-D result.header \
-o result.json \
--ciphers 'DEFAULT:!DH'
```
