# magento-test

```
apt update -y
apt install vim -y
cd /var/www/html
chmod -R 777 var/ pub/ generated/
apt-get install php7.4-soap
php bin/magento sampledata:deploy
```