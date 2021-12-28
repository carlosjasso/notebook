# Generate SSH keypair

Generate a new Pub/Priv key with:

```bash
ssh-keygen
```

Keys get generated in `cd ~/.ssh`

From `*.pub`, paste value into the desired server `~/.ssh/authorized_keys`.
Use NOT .pub (private key) to login with `ssh -i <path/to/key> user@server` or via ssh client
