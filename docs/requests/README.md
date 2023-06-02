# requests

## Overview

REST APIs for retrieving request information

### Available Operations

* [generateRequestPostmanCollection](#generaterequestpostmancollection) - Generate a Postman collection for a particular request.
* [getRequestFromEventLog](#getrequestfromeventlog) - Get information about a particular request.
* [queryEventLog](#queryeventlog) - Query the event log to retrieve a list of requests.

## generateRequestPostmanCollection

Generates a Postman collection for a particular request. 
Allowing it to be replayed with the same inputs that were captured by the SDK.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GenerateRequestPostmanCollectionRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GenerateRequestPostmanCollectionRequest();
    $request->requestID = 'quis';

    $response = $sdk->requests->generateRequestPostmanCollection($request);

    if ($response->postmanCollection !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## getRequestFromEventLog

Get information about a particular request.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetRequestFromEventLogRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetRequestFromEventLogRequest();
    $request->requestID = 'vitae';

    $response = $sdk->requests->getRequestFromEventLog($request);

    if ($response->unboundedRequest !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## queryEventLog

Supports retrieving a list of request captured by the SDK for this workspace.
Allows the filtering of requests on a number of criteria such as ApiID, VersionID, Path, Method, etc.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\QueryEventLogRequest;
use \zostay\Speakeasy_API\Models\Shared\Filters;
use \zostay\Speakeasy_API\Models\Shared\Filter;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new QueryEventLogRequest();
    $request->filters = new Filters();
    $request->filters->filters = [
        new Filter(),
        new Filter(),
        new Filter(),
    ];
    $request->filters->limit = 656330;
    $request->filters->offset = 317202;
    $request->filters->operator = 'odit';

    $response = $sdk->requests->queryEventLog($request);

    if ($response->boundedRequests !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```
