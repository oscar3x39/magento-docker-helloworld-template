# magento-test

Switch to Magento Container
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
