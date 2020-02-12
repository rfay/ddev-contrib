# Redis

This recipe adds a Redis container to a project.

## Installation

* Copy `docker-compose.redis.yaml` to the `.ddev` folder of your project.
* Copy the `commands/redis` directory to the commands folder of your project DDEV folder; you should end up with `.ddev/commands/redis/redis-cli` (make sure it's executable, `chmod +x .ddev/commands/redis/redis-cli`.)
* Add *redis-tools* to the list of webimage_extra_packages in `config.yaml`: `webimage_extra_packages: [redis-tools]`
* Start (or restart) DDEV to have the service initialized: `ddev start`

Now you can use `ddev redis-cli` to access the redis cli in the redis container.

**Contributed by [@gormus](https://github.com/gormus)**
