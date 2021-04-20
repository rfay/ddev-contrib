# ddev-contrib: Contrib for DDEV-Local
ignore this

Contrib space for DDEV-Local services, tools, snippets, approaches.

## config.yaml hook examples

* [Import a sql dump if database is empty](hook-examples/import-db-if-empty/)

## docker-compose.*.yaml snippets to solve simple problems

Don't forget the [Official documentation](https://ddev.readthedocs.io/en/stable/users/extend/custom-compose-files/).

* [Mounting a directory into web container](docker-compose-snippets/mounting-directory/)
* [Setting an environment variable](docker-compose-snippets/environment-variable/docker-compose.env.yaml)
* [Communication between two ddev projects](docker-compose-snippets/project-communication/)
* [Set default language (or other settings) in phpmyadmin](docker-compose-snippets/phpmyadmin-user-settings/)

## Custom command examples

Ddev's [custom commands](https://ddev.readthedocs.io/en/latest/users/extend/custom-commands/) are a great way to add team-level or project-level commands. They're simple scripts that can be run in any of the containers or on the host. Note that several examples are already shipped with ddev, you'll find them in .ddev/commands/*/*.example, and then can be enabled by symlinking or copying.)

* [Dump and deploy SQL from/to remote servers](custom-commands/dump-and-deploy-db/)
* [Fetch Production DB from remote server](custom-commands/fetchproductiondb/)
* [Exclude ddev directory from git: git-exclude](custom-commands/git-exclude)
* [Enable and view MySQL/MariaDB GENERAL_LOG](custom-commands/general-log/)
* [inotify-proxy to enable file watchers on NFS shares](custom-commands/inotify-proxy)
* [Executing Symfony console and phpunit commands without ssh](custom-commands/symfony/)

## Additional services added via docker-compose.\<service\>.yaml

General information on how to do additional services and some additional examples are [in the docs](https://ddev.readthedocs.io/en/latest/users/extend/additional-services/).

* [Behat, Selenium, Drupal 8/9](docker-compose-services/drupal8-behat-selenium)
* [DrupalCI with Headless Chrome and Behat](docker-compose-services/drupalci-chromedriver). This example uses Drupal's DrupalCI approach, supports Behat, DrupalCI, etc.
* [Elasticsearch](docker-compose-services/elasticsearch)
* [Elastichq](docker-compose-services/elastichq)
* [Headless Chrome for Behat Testing](docker-compose-services/headless-chrome)
* [MongoDB](docker-compose-services/mongodb/)
* [Old PHP Versions to run old sites](docker-compose-services/old_php)
* [Portainer Service for DDEV](docker-compose-services/portainer)
* [PostgreSQL](docker-compose-services/postgres/)
* [Drupal Solr 4 Integration](docker-compose-services/solr4)  
* [Drupal Solr 5 Integration](docker-compose-services/solr-5)
* [Drupal Solr 7 Integration](docker-compose-services/solr-7)
* [TYPO3 Solr Integration](docker-compose-services/typo3-solr)
* [RabbitMQ](docker-compose-services/rabbitmq)
* [redis](docker-compose-services/redis)
* [redis-commander](docker-compose-services/redis-commander)
* [Varnish](docker-compose-services/varnish)

## .ddev/web-build/Dockerfile examples to customize web container

* [Laravel Queue-Worker](web-container-dockerfiles/laravel-queue-worker) (This is also a good example of adding an additional process to supervisord,)
* [Stripe CLI](web-container-dockerfiles/stripe-cli) (This is also a good example of adding any non-standard Debian repository.)
* [gRPC](web-web-container-dockerfiles/grpc) (This is also a good example of adding a pecl module that is not supported via apt-get.)

## Full recipes

* [Using ddev with a corporate (or other) web proxy](recipes/proxy)
* [enable TYPO3 cronjob on start or on demand (typo3 scheduler:run)](recipes/cronjob/)
* [Setting up Drupal 8 multisite, including Drush support](recipes/drupal8-multisite/)
* [Bludit CMS](recipes/bludit-cms)
* [Drupal 7 in a Subfolder of Main Site](recipes/drupal7-subfolder)
* [Flexitype CMS](recipes/flexitype-cms)
* [REDAXO CMS](recipes/redaxo-cms)
* [SSH Server](recipes/sshd): Adding a "real" sshd server in web container
* [Puppeteer Headless Chrome support](recipes/puppeteer-headless-chrome-support/README.md)
