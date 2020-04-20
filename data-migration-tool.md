Data-Migration-tool
---
Data migration tool is a tool, developed by Magento to migrate data from Magento1 to Magento2

## How use it

* run `composer require magento/data-migration-tool:{version-of-your-magento2}`
* go to the folder *vendor/magento/data-migration-tool/etc/opensource-to-commerce/{version-of-your-magento1}*
* rename the file config.xml.dist in config.xml
* set the correct configuration of Magento1 database and Magento2 database
```
 <source>
        <database host="localhost" name="magento1" user="root" />
    </source>
    <destination>
        <database host="localhost" name="magento2" user="root" />
    </destination>
```
* Run `php bin/magento migrate:settings vendor/magento/data-migration-tool/etc/opensource-to-commerce/1.9.4.4/config.xml`
to migrate settings
* Run `php bin/magento migrate:data vendor/magento/data-migration-tool/etc/opensource-to-commerce/1.9.4.4/config.xml`
to migrate data (products, orders, customers)
