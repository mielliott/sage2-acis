

## Setting up certificates using Let's Encrypt

Generate keys:

```bash
$ sudo certbot certonly --manual
```

Using keys (see https://serverfault.com/a/763145):

```bash
$ cd sage2/keys
$ ln -s /etc/letsencrypt/live/sage2.acis.ufl.edu/fullchain.pem sage2.acis.ufl.edu-ca.crt
$ ln -s /etc/letsencrypt/live/sage2.acis.ufl.edu/cert.pem sage2.acis.ufl.edu-server.crt
$ ln -s /etc/letsencrypt/live/sage2.acis.ufl.edu/privkey.pem sage2.acis.ufl.edu-server.key
```

Probably need to deal with file permissions issues.

