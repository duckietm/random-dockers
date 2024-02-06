# Mail server

## About
Production-ready fullstack but simple mail server (SMTP, IMAP, LDAP, Antispam, Antivirus, etc.) running inside a container.

## Get starting
Copy the content to /docker/mailserver

Edit the docker-compose.yml (set mailserver DNS)

Next run:
```
cd /docker/mailserver/
chmod +x setup.sh
```

Then run : ```docker compose up -d```

At the first first run you have 120 Secconds to run the following command:
```docker exec -i mailserver  setup email add info@mydomain.com ###PASSWORD###```
Change the mydomain / password and that will start the mailserver

Now i do advise you to read the documents to get one with the mailserver, like DKIM, DMARC etc. etc.

Resources

- github : https://github.com/docker-mailserver/docker-mailserver
- configuration : https://docker-mailserver.github.io/docker-mailserver/latest/config/environment/

So happy codeing!
