beginMetadata:
{
    "id": "11a4b5c6-a8da-40e0-adbe-4276b2743089",
    "documentNumber": 98,
    "author": "jxxcarlson",
    "title": "DevOps Manual",
    "path": "devops-manual/index.md",
    "tags": [
        "unix",
        "linux",
        "server",
        "sysadmin"
    ],
    "keyString": "devops manual a=jxxcarlson devops-manual/index.md t=unix t=linux t=server t=sysadmin",
    "timeCreated": 1598797208553,
    "timeModified": 1603154065647,
    "public": false,
    "collaborators": [],
    "docType": "markdown",
    "versionNumber": 0,
    "versionDate": 0
}
endMetadata
# DevOps Manual

**Motto:** *Simplify*

[SSH keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)

[Digital Ocean SSH](https://medium.com/sharma02gaurav/digitalocean-ssh-authentication-and-removing-password-login-ee42b54b622f)

[Keep process running](https://ostechnix.com/4-ways-keep-command-running-log-ssh-session/)

[Creating your own service](https://medium.com/@benmorel/creating-a-linux-service-with-systemd-611b5c8b91d6)

[Let's Encrypt](https://letsencrypt.org/)

## Command Line

```elm
$ sudo netstat -tlpn
$ sudo tcptraceroute 161.35.125.40 80

$ sudo lsof -n -i :3000

$ sudo ufw allow 80
$ sudo ufw enable
```
SSH Keys

```elm
$ cat ~/.ssh/id_rsa.pub
$ pbcopy < ~/.ssh/id_rsa.pub
$ sudo nano /etc/ssh/sshd_config # see PasswordAuthentication
$ systemctl restart sshd
$ ls .ssh/authorized_keys
```

## LetsEncrypt

Certificate and chain:

```elm
/etc/letsencrypt/live/shoobox.io/fullchain.pem
```

Key file:

```elm
/etc/letsencrypt/live/shoobox.io/privkey.pem
```

## NGINX

[Letsencrypt and Nginx](https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/)!!!

[Nginx CORS](https://enable-cors.org/server_nginx.html)

```elm
sudo certbot --nginx -d shoobox.io
```

[Installing Nginx on DigitialOcean](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04)

[Configure reverse proxy](https://www.digitalocean.com/community/tutorials/how-to-configure-nginx-as-a-web-server-and-reverse-proxy-for-apache-on-one-ubuntu-16-04-server)

```elm
$ sudo ufw status
$ sudo ufw app list
$ sudo ufw allow 'Nginx HTTP'
$  sudo ufw status
$  systemctl status nginx

$ sudo ln -s /etc/nginx/sites-available/pdefserver /etc/nginx/sites-enabled/pdfserver
$ sudo nginx -t
$ sudo nano /etc/nginx/sites-available/pdfserver

$ sudo unlink /etc/nginx/sites-enabled/default
```

Config

```elm
server {
    listen 80;
    server_name shoobox.io;

    location / {
        proxy_pass http://161.35.125.40:3000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```


## Database 

###  Restoring from a backup 

- Download backup from Autobus

- Upload backup to S3, make public, copy URL

- Execute the following command: 
`heroku pg:backups:restore <S3_URL> DATABASE_URL --app math-markdown` where `S3_URL` is the URL of the uploaded backup  and `DATABASE_URL` is literally that.


@ilink1[uuid:3bb611ee-e549-42d5-aa56-b2e95387978e > Amazon S3]


@ilink1[uuid:8162e985-5fc4-40bf-ad41-69558721cf04 > Postgres]

