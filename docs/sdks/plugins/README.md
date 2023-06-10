# plugins

## Overview

REST APIs for managing and running plugins

### Available Operations

* [getPlugins](#getplugins) - Get all plugins for the current workspace.
* [runPlugin](#runplugin) - Run a plugin
* [upsertPlugin](#upsertplugin) - Upsert a plugin

## getPlugins

Get all plugins for the current workspace.

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
    $response = $sdk->plugins->getPlugins();

    if ($response->plugins !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```


### Response

**[?\zostay\Speakeasy_API\Models\Operations\GetPluginsResponse](../../models/operations/GetPluginsResponse.md)**


## runPlugin

Run a plugin

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\RunPluginRequest;
use \zostay\Speakeasy_API\Models\Shared\Filters;
use \zostay\Speakeasy_API\Models\Shared\Filter;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new RunPluginRequest();
    $request->filters = new Filters();
    $request->filters->filters = [
        new Filter(),
        new Filter(),
        new Filter(),
    ];
    $request->filters->limit = 208876;
    $request->filters->offset = 635059;
    $request->filters->operator = 'consequuntur';
    $request->pluginID = 'repellat';

    $response = $sdk->plugins->runPlugin($request);

    if ($response->boundedRequests !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

### Parameters

| Parameter                                                                                               | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `$request`                                                                                              | [\zostay\Speakeasy_API\Models\Operations\RunPluginRequest](../../models/operations/RunPluginRequest.md) | :heavy_check_mark:                                                                                      | The request object to use for the request.                                                              |


### Response

**[?\zostay\Speakeasy_API\Models\Operations\RunPluginResponse](../../models/operations/RunPluginResponse.md)**


## upsertPlugin

Upsert a plugin

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Shared\Plugin;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new Plugin();
    $request->code = 'mollitia';
    $request->createdAt = DateTime::createFromFormat('Y-m-d\TH:i:sP', '2022-06-30T02:19:51.375Z');
    $request->evalHash = 'commodi';
    $request->pluginId = 'quam';
    $request->title = 'Ms.';
    $request->updatedAt = DateTime::createFromFormat('Y-m-d\TH:i:sP', '2022-05-18T10:03:04.921Z');
    $request->workspaceId = 'quia';

    $response = $sdk->plugins->upsertPlugin($request);

    if ($response->plugin !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `$request`                                                                  | [\zostay\Speakeasy_API\Models\Shared\Plugin](../../models/shared/Plugin.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |


### Response

**[?\zostay\Speakeasy_API\Models\Operations\UpsertPluginResponse](../../models/operations/UpsertPluginResponse.md)**

