
## Setting up service

```bash
$ sudo ln -s sage2.service /etc/systemd/system/sage2.service
$ sudo systemctl start sage2
```

To see the log:

```bash
$ sudo journalctl -u sage2
```

## Setting up certificates using Let's Encrypt

Generate keys:

```bash
$ sudo certbot certonly --manual
```

Installing keys (see https://serverfault.com/a/763145):

```bash
$ cd /home/sage/sage2/keys
$ ln -s /etc/letsencrypt/live/sage2.acis.ufl.edu/fullchain.pem sage2.acis.ufl.edu-ca.crt
$ ln -s /etc/letsencrypt/live/sage2.acis.ufl.edu/cert.pem sage2.acis.ufl.edu-server.crt
$ ln -s /etc/letsencrypt/live/sage2.acis.ufl.edu/privkey.pem sage2.acis.ufl.edu-server.key
```

Probably need to deal with file permissions issues.

