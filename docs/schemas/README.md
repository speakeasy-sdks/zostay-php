# schemas

## Overview

REST APIs for managing Schema entities

### Available Operations

* [deleteSchema](#deleteschema) - Delete a particular schema revision for an Api.
* [downloadSchema](#downloadschema) - Download the latest schema for a particular apiID.
* [downloadSchemaRevision](#downloadschemarevision) - Download a particular schema revision for an Api.
* [getSchema](#getschema) - Get information about the latest schema.
* [getSchemaDiff](#getschemadiff) - Get a diff of two schema revisions for an Api.
* [getSchemaRevision](#getschemarevision) - Get information about a particular schema revision for an Api.
* [getSchemas](#getschemas) - Get information about all schemas associated with a particular apiID.
* [registerSchema](#registerschema) - Register a schema.

## deleteSchema

Delete a particular schema revision for an Api.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\DeleteSchemaRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new DeleteSchemaRequest();
    $request->apiID = 'quo';
    $request->revisionID = 'sequi';
    $request->versionID = 'tenetur';

    $response = $sdk->schemas->deleteSchema($request);

    if ($response->statusCode === 200) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## downloadSchema

Download the latest schema for a particular apiID.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\DownloadSchemaRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new DownloadSchemaRequest();
    $request->apiID = 'ipsam';
    $request->versionID = 'id';

    $response = $sdk->schemas->downloadSchema($request);

    if ($response->schema !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## downloadSchemaRevision

Download a particular schema revision for an Api.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\DownloadSchemaRevisionRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new DownloadSchemaRevisionRequest();
    $request->apiID = 'possimus';
    $request->revisionID = 'aut';
    $request->versionID = 'quasi';

    $response = $sdk->schemas->downloadSchemaRevision($request);

    if ($response->schema !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## getSchema

Returns information about the last uploaded schema for a particular API version. 
This won't include the schema itself, that can be retrieved via the downloadSchema operation.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetSchemaRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetSchemaRequest();
    $request->apiID = 'error';
    $request->versionID = 'temporibus';

    $response = $sdk->schemas->getSchema($request);

    if ($response->schema !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## getSchemaDiff

Get a diff of two schema revisions for an Api.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetSchemaDiffRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetSchemaDiffRequest();
    $request->apiID = 'laborum';
    $request->baseRevisionID = 'quasi';
    $request->targetRevisionID = 'reiciendis';
    $request->versionID = 'voluptatibus';

    $response = $sdk->schemas->getSchemaDiff($request);

    if ($response->schemaDiff !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## getSchemaRevision

Returns information about the last uploaded schema for a particular schema revision. 
This won't include the schema itself, that can be retrieved via the downloadSchema operation.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetSchemaRevisionRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetSchemaRevisionRequest();
    $request->apiID = 'vero';
    $request->revisionID = 'nihil';
    $request->versionID = 'praesentium';

    $response = $sdk->schemas->getSchemaRevision($request);

    if ($response->schema !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## getSchemas

Returns information the schemas associated with a particular apiID. 
This won't include the schemas themselves, they can be retrieved via the downloadSchema operation.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\GetSchemasRequest;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new GetSchemasRequest();
    $request->apiID = 'voluptatibus';
    $request->versionID = 'ipsa';

    $response = $sdk->schemas->getSchemas($request);

    if ($response->schemata !== null) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```

## registerSchema

Allows uploading a schema for a particular API version.
This will be used to populate ApiEndpoints and used as a base for any schema generation if present.

### Example Usage

```php
<?php

declare(strict_types=1);
require_once 'vendor/autoload.php';

use \zostay\Speakeasy_API\SpeakeasyAPI;
use \zostay\Speakeasy_API\Models\Shared\Security;
use \zostay\Speakeasy_API\Models\Operations\RegisterSchemaRequest;
use \zostay\Speakeasy_API\Models\Operations\RegisterSchemaRequestBody;
use \zostay\Speakeasy_API\Models\Operations\RegisterSchemaRequestBodyFile;

$sdk = SpeakeasyAPI::builder()
    ->build();

try {
    $request = new RegisterSchemaRequest();
    $request->requestBody = new RegisterSchemaRequestBody();
    $request->requestBody->file = new RegisterSchemaRequestBodyFile();
    $request->requestBody->file->content = 'omnis';
    $request->requestBody->file->file = 'voluptate';
    $request->apiID = 'cum';
    $request->versionID = 'perferendis';

    $response = $sdk->schemas->registerSchema($request);

    if ($response->statusCode === 200) {
        // handle response
    }
} catch (Exception $e) {
    // handle exception
}
```
