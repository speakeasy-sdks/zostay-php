# SpeakeasyAPI SDK

## Overview

Speakeasy API: The Speakeasy API allows teams to manage common operations with their APIs

The Speakeasy Platform Documentation
<https://docs.speakeasyapi.dev>
### Available Operations

* [validateApiKey](#validateapikey) - Validate the current api key.

## validateApiKey

Validate the current api key.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $response = $sdk->speakeasyAPI->validateApiKey();

    if ($response->statusCode === 200) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```


### Response

**[?\zostay\Speakeasy_API\Models\Operations\ValidateApiKeyResponse](../../models/operations/ValidateApiKeyResponse.md)**

