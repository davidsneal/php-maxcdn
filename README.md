## composer.json
```php
"repositories": [
    {
        "type": "vcs", "url": "https://github.com/davidsneal/php-maxcdn"
    }
],
"require": {
    "davidsneal/php-maxcdn": "dev-master"
},
```

## config/app.php

```php
'providers' => [
    Davidsneal\MaxCDN\MaxCDNServiceProvider::class,
],
```

## YourController.php

```php
use MaxCDN;
```
 
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
