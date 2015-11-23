composer.json

"autoload": {
    "psr-4": {
        "Davidsneal\\MaxCDN\\": "vendor/davidsneal/php-maxcdn/src"
    }
},

config/app.php

'providers' => [
    Davidsneal\MaxCDN\MaxCDNServiceProvider::class,
],
 
## Usage
```php
<?php

$api = new MaxCDN("my_alias","consumer_key","consumer_secret");

// get account information
echo  $api->get('/account.json');

// delete a file from the cache
$params = array('file' => '/robots.txt');
echo $api->delete('/zones/pull.json/6055/cache', $params);

?>
```

## Methods

It has support for `GET`, `POST`, `PUT` and `DELETE` OAuth signed requests.
