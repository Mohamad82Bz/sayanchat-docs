# storage.yml

Controls database and messaging backends.

## Key Options

- `method`: `SQLITE`, `MYSQL`, or `MARIADB`.
- `host`, `port`, `database`, `username`, `password`, `use-ssl`.
- `pooling-size`: Main connection pool size.
- `threads`, `secondary-threads`: Async executor sizes.
- `messaging-method`: `REDIS` (recommended for networks).
- `redis`: Redis connection pool settings.
- `user-table-optimizations`: Cleanup settings for inactive users.

## Example

```yaml
method: MARIADB
host: localhost
port: 3306
database: minecraft
username: user
password: password
use-ssl: false
threads: 5
pooling-size: 5
messaging-method: REDIS
redis:
  host: localhost
  port: 6379
  user: ''
  password: ''
  max-total: 100
  max-idle: 100
  min-idle: 10
  test-on-borrow: true
  dispatcher-thread-count: 5
  test-on-return: true
  test-while-idle: true
  min-evictable-idle-time-millis: 60000
  time-between-eviction-runs-millis: 30000
  num-tests-per-eviction-run: -1
  block-when-exhausted: true
delete-pooling-size: 5
secondary-threads: 1
minimum-idle: 5
keepalive-time: 0
connection-timeout: 5000
max-lifetime: 1800000
user-table-optimizations:
  enable: true
  ignore-users-that-are-offline-for-days: 30
```
