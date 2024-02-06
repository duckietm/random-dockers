![](https://github.com/ngoduykhanh/wireguard-ui/workflows/wireguard-ui%20build%20release/badge.svg)

# wireguard-ui

A web user interface to manage your WireGuard setup.

## Features

- Friendly UI
- Authentication
- Manage extra client information (name, email, etc)
- Retrieve client config using QR code / file / email

![wireguard-ui 0.3.7](https://user-images.githubusercontent.com/37958026/177041280-e3e7ca16-d4cf-4e95-9920-68af15e780dd.png)

## Run WireGuard-UI

> ⚠️The default username and password are `admin`. Please change it to secure your setup.

### Using docker compose

Start the docker like below:

```
docker compose up -d
```

## Environment Variables

These environment variables only apply to the docker container.

| Variable              | Description                                                   | Default |
|-----------------------|------------------------------------------------------------------------------------------------------------|----------------|
| `SENDGRID_API_KEY `   | Set the Sendgrid API key to send out emails                                                                | N/A            |
| `EMAIL_FROM_ADDRESS`  | Set the from addrress in the email                                                                         | N/A            |
| `EMAIL_FROM_NAME`     | The sender name                                                                                            | `WireGuard UI` |
| `SESSION_SECRET`      | The secret key used to encrypt the session cookies. Set this to a random value                             | N/A            |
| `WGUI_USERNAME`       | The username for the login page. Used for db initialization only                                           | `admin`        |
| `WGUI_PASSWORD`       | The password for the user on the login page. Will be hashed automatically. Used for db initialization only | `admin`        |
| `WG_CONF_TEMPLATE`    | The custom `wg.conf` config file template.                                                                 | N/A            |
| `WGUI_MANAGE_START`   | Start/stop WireGuard when the container is started/stopped                                                 | `false`        |
| `WGUI_MANAGE_RESTART` | Auto restart WireGuard when we Apply Config changes in the UI                                              | `false`        |