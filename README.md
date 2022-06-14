# First thing you need to register a account and create access key

```
publickey -> username
privatekey -> password
https://marketplace.magento.com/customer/accessKeys/
```

# Switch to Magento Container
```
apt update -y
apt install vim -y

# Install magento
cd /var/www/html
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition

# Fixed magento bugs
cd /var/www/html
chmod -R 777 var/ pub/ generated/
apt-get install php7.4-soap
php bin/magento sampledata:deploy
```

```
bin/magento module:enable --all
bin/magento setup:di:compile

php bin/magento setup:install --base-url=http://127.0.0.1/ \
--db-host=mysql --db-name=homestead --db-user=homestead --db-password=secret \
--admin-firstname=Magento --admin-lastname=User --admin-email=user@example.com \
--admin-user=admin --admin-password=admin123 --language=en_US \
--currency=USD --timezone=America/Chicago --use-rewrites=1 \
--search-engine=elasticsearch7 --elasticsearch-host=elasticsearch \
--elasticsearch-port=9200 -vvv

php bin/magento setup:store-config:set --base-url="https://xxxx.gitpod.io/"
```

# Hello World Module
```
https://www.magespark.com/blog/post/how-to-create-a-simple-hello-world-module-in-magento-2
http://localhost/helloworld/index/helloworld
```