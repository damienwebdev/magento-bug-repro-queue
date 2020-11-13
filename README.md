# Repro Instructions for Cloud Exchange Issue

To verify, follow along.

* [Setup your environment](./#setup-your-environment)
* [bin/magento setup:upgrade](./#upgrade)
* [Check RabbitMQ Management](./#setup-your-environment)

## Setup your environment
[Follow along with cloud-docker docs.](https://devdocs.magento.com/cloud/docker/docker-mode-production.html)

```bash 
./vendor/bin/ece-docker build:compose --rmq=3.8-management --php=7.2
```

> You will need to expose port 15672 on the RabbitMQ container to see the UI to verify that the exchange exists/doesn't exist.

## Check RabbitMQ Management
* http://magento2.docker:15672/#/exchanges

