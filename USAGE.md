<!-- Start SDK Example Usage -->
```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetApisRequest;
use \zostay\Speakeasy_API\Models\Operations\GetApisOp;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetApisRequest();
    $request->metadata = [
        'provident' => [
            'quibusdam',
            'unde',
            'nulla',
        ],
        'corrupti' => [
            'vel',
            'error',
            'deserunt',
            'suscipit',
        ],
        'iure' => [
            'debitis',
            'ipsa',
        ],
    ];
    $request->op = new GetApisOp();
    $request->op->and = false;

    $response = $sdk->apis->getApis($request);

    if ($response->apis !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```
<!-- End SDK Example Usage -->