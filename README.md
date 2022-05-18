# Laravel Theme Store

[![EgoistDeveloper Laravel License Connector](https://preview.dragon-code.pro/EgoistDeveloper/License-Connector.svg?brand=laravel)](https://github.com/laravel-ready/license-server)

[![Stable Version][badge_stable]][link_packagist]
[![Unstable Version][badge_unstable]][link_packagist]
[![Total Downloads][badge_downloads]][link_packagist]
[![License][badge_license]][link_license]


License Connector is continous integration tool for [License Server](https://github.com/laravel-ready/license-server) package. This package is using for connect your Laravel project with License Server.

## Installation (for Client App)

Publish store migrations

Get via composer

`composer require laravel-ready/license-connector`

Configs are very important. You can find them in [license-connector.php](config/license-connector.php) file. You should read all configs and configure for your needs.

```bash
#publish configs

php artisan vendor:publish --tag=license-connector-configs
```

## Validate License

```php
use LaravelReady\LicenseConnector\Services\ConnectorService;

...

$licenseKey = '46fad906-bc51-435f-9929-db46cb4baf13';
$licenseStatus = ConnectorService::validateLicense($licenseKey);

if ($liceseStatus) {
    // License is valid
} else {
    // License is invalid
}
```


[badge_downloads]:      https://img.shields.io/packagist/dt/laravel-ready/license-server.svg?style=flat-square

[badge_license]:        https://img.shields.io/packagist/l/laravel-ready/license-server.svg?style=flat-square

[badge_stable]:         https://img.shields.io/github/v/release/laravel-ready/license-server?label=stable&style=flat-square

[badge_unstable]:       https://img.shields.io/badge/unstable-dev--main-orange?style=flat-square

[link_license]:         LICENSE

[link_packagist]:       https://packagist.org/packages/laravel-ready/license-server
