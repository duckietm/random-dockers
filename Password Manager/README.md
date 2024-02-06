# Bitwarden Password Vault

### Alternative implementation of the Bitwarden server API written in Rust and compatible with [upstream Bitwarden clients](https://bitwarden.com/download/)*, perfect for self-hosted deployment where running the official resource-heavy service might not be ideal.

## Features

Basically full implementation of Bitwarden API is provided including:

 * Organizations support
 * Attachments and Send
 * Vault API support
 * Serving the static files for Vault interface
 * Website icons API
 * Authenticator and U2F support
 * YubiKey and Duo support
 * Emergency Access

## Installation

```
docker compose up -d
```
This will preserve any persistent data under /vw-data/, you can adapt the path to whatever suits you.

**IMPORTANT**: Most modern web browsers disallow the use of Web Crypto APIs in insecure contexts. In this case, you might get an error like `Cannot read property 'importKey'`. To solve this problem, you need to access the web vault via HTTPS or localhost.

If you have an available domain name, you can get HTTPS certificates with [Let's Encrypt](https://letsencrypt.org/), or you can generate self-signed certificates with utilities like [mkcert](https://github.com/FiloSottile/mkcert). Some proxies automatically do this step, like Caddy / NGINX Proxy manager / Traefik etc. etc.

I would advise to use Nginx Proxy Manager this has build in support for Let's Encrypt, please select the option "Websockets Support".

Needed to read:
- Access to the Admin section : https://github.com/dani-garcia/vaultwarden/wiki/Enabling-admin-page#secure-the-admin_token
- General information : https://github.com/dani-garcia/vaultwarden/wiki
