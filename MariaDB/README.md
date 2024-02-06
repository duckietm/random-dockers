# MariaDB as docker container

It’s always recommended to use the official MariaDB Docker images as they are maintained by the team that best knows MariaDB.
Here are some of these images avalible from MariaDB:

- MariaDB Community Server
- MariaDB Community Server with ColumnStore
- MariaDB MaxScale
- MariaDB Xpand (single node)

It’s worth mentioning that there also is a MariaDB Enterprise Docker Registry which provides Docker images for MariaDB Enterprise Server (a hardened, optimized version of MariaDB plus additional components for high levels of scalability, security, reliability, and uptime).

Spinning up a MariaDB container for development doesn’t require major configurations. 

Typically you’ll need to expose a port and set a root password. 

This can be done using environment variables.

Check each image documentation to learn about the available parameters.

Additionally, you might want to set up a custom Docker network and volume.

But please be aware for heavy production enviroment a MAriaDB container performs always a bit less then it would when installed on the OS.
