# Server Support Service

Share server access securely

## Passowrd less SSH access

You can avoid disclosing passwords by installing our public [SSH keys](https://raw.githubusercontent.com/askmage/support/master/id_rsa.pub) into list of authorized keys, by default they are located in `/root/.ssh/authorized_keys`

Make sure `PubkeyAuthentication` option is enabled in ssh configuration:
```
# grep PubkeyAuthentication /etc/ssh/sshd_config
PubkeyAuthentication yes
```

Use the following command to install the public key:
```
# curl https://raw.githubusercontent.com/askmage/support/master/id_rsa.pub >> /root/.ssh/authorized_keys
```

## Firewall

If remote access to the server is limited with firewall, please make sure that it is allowed from our jumper server IP addresses

```
35.238.176.232
```

Keys may be removed after conclusion of support incident.
