# embeds

## Overview

REST APIs for managing embeds

### Available Operations

* [getEmbedAccessToken](#getembedaccesstoken) - Get an embed access token for the current workspace.
* [getValidEmbedAccessTokens](#getvalidembedaccesstokens) - Get all valid embed access tokens for the current workspace.
* [revokeEmbedAccessToken](#revokeembedaccesstoken) - Revoke an embed access EmbedToken.

## getEmbedAccessToken

Returns an embed access token for the current workspace. This can be used to authenticate access to externally embedded content.
Filters can be applied allowing views to be filtered to things like particular customerIds.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetEmbedAccessTokenRequest;
use \zostay\Speakeasy_API\Models\Shared\Filters;
use \zostay\Speakeasy_API\Models\Shared\Filter;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetEmbedAccessTokenRequest();
    $request->description = 'laborum';
    $request->duration = 170909;
    $request->filters = new Filters();
    $request->filters->filters = [
        new Filter(),
    ];
    $request->filters->limit = 358152;
    $request->filters->offset = 128926;
    $request->filters->operator = 'nobis';

    $response = $sdk->embeds->getEmbedAccessToken($request);

    if ($response->embedAccessTokenResponse !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## getValidEmbedAccessTokens

Get all valid embed access tokens for the current workspace.

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
    $response = $sdk->embeds->getValidEmbedAccessTokens();

    if ($response->embedTokens !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## revokeEmbedAccessToken

Revoke an embed access EmbedToken.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\RevokeEmbedAccessTokenRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new RevokeEmbedAccessTokenRequest();
    $request->tokenID = 'enim';

    $response = $sdk->embeds->revokeEmbedAccessToken($request);

    if ($response->statusCode === 200) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```
