# Gitlab for your own enviroment

## Gitlab installation

edit the docker-compose.yml file and change the following:
- hostname: '#GIT.HOSTNAME.COM#'  Example: hostname: 'git.mydomain.com'
- external_url 'http://### YOU URL TO GIT###' Example : 'http://git.mydomain.com'

Containers are started using the command:

```cmd
docker-compose up -d
```

Once launched, Docker will download GitLab and GitLab Runner images from the servers.

To log in to GitLab for the first time, you need a temporary password, which is generated automatically during installation.
We get the password using the command:
```cmd
docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
```

## GitLab launching
Our GitLab is available at: http://localhost:3030. After going to this address login with:
- Username : root
- Password : This is the password from the above command