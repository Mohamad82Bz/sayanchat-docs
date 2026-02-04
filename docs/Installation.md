# Installation

!!! warning "Internet Connection Required"
    SayanChat downloads external libraries on first startup. Make sure your server has internet access.

## Bukkit/Paper Installation

1. Drop the SayanChat jar into `plugins/`.
2. Start the server once to generate configs in `plugins/SayanChat/`.
3. Stop the server and configure `storage.yml`, `settings.yml`, and other files as needed.
4. Start the server again.

## Proxy Installation (Velocity/Bungee)

1. Drop the SayanChat proxy jar into the proxy `plugins/` folder.
2. Start the proxy once to generate configs in `plugins/sayanchat/`.
3. Configure `storage.yml` and `server_aliases.yml` if needed.

!!! info
    The proxy side handles rules and server aliasing. Most chat behavior is configured on the Bukkit/Paper servers.

## Database Configuration

For a single server, SQLite works out of the box. For networks, use MariaDB or MySQL.

Open `plugins/SayanChat/storage.yml` and set:

```yaml
method: SQLITE # SQLITE, MYSQL, MARIADB
```

If you use MySQL or MariaDB, also configure the connection section:

```yaml
host: localhost
port: 3306
database: minecraft
username: user
password: password
use-ssl: false
pooling-size: 5
```

!!! warning "MariaDB"
    Use `method: MARIADB`. `MYSQL` will not work with MariaDB.

## Redis Messaging (Recommended for Networks)

SayanChat uses Redis for cross-server messaging when proxy/network features are enabled.

In `storage.yml`, set:

```yaml
messaging-method: REDIS
redis:
  host: localhost
  port: 6379
  user: ''
  password: ''
```
