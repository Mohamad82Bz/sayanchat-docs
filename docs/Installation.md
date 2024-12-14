# Installation

!!! warning "Internet Connection Required"
    SayanChat requires an active internet connection to download external libraries. Ensure your server is connected to the internet during the initial startup.

### Bukkit Installation

#### Plugin Installation

1. Download the Plugin
    - Download the SayanChat Bukkit jar file.
2. Install the Plugin
    - Place the downloaded jar file inside the `plugins` folder.
3. Restart the Server
    - Restart your Minecraft server to load the plugin.
4. (If you are running a Proxy server)
    - Change `server-id` in the `settings.yml` file to the server ID of the server you are running the plugin on.
    - Follow Database Configuration steps below.

!!! info
    If you have a proxy server with two or more servers, make sure to connect to a MySQL/MariaDB database.

#### Database Configuration
For single server installations, SQLite is suitable. However, for multi-server owners for network-wide features like synchronized chat boxes and chat history, a MySQL or MariaDB database is required. To configure the database, follow these steps:

??? warning "If you're using MariaDB"
    Unlike most places, If you are using MariaDB, you must use the `MARIADB` method in the configuration file. The `MYSQL` method will not work with MariaDB.

1. Make sure you have run the plugin at least once to generate the configuration files.
2. Open the `storage.yml` file located in the `plugins/SayanChat` folder.
3. Configure the database settings as follows:
``` { .yaml .no-copy }
method: SQLITE # Options: SQLITE, MYSQL, MARIADB
```
4. (If you chose `MYSQL` or `MARIADB`, configure the database settings)
``` .yaml
host: localhost # Database host
port: 3306 # Database port
database: minecraft # Database name
username: user # Database username
password: password # Database password
use-ssl: false # Use SSL for database connection
pooling-size: 5 # Connection pooling size. 5 is suitable for most servers. increase if you have a large player base and when you see database slow down.
```
5. Save the file and restart the server.

### Proxy Installation

!!! info
    SayanChat supports Velocity and Bungeecord (including Waterfall) proxies.

1. Install the Plugin
    - Place the downloaded jar file inside the `plugins` folder.
2. Restart the Proxy
    - Restart your Proxy server to load the plugin.

!!! info
    SayanChat does not require any configuration or database connection on the proxy. There is only rules configuration, which also exists on the server side. The proxy one will be applied to all servers.