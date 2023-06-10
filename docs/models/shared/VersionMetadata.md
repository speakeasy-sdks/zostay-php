# VersionMetadata

A set of keys and associated values, attached to a particular version of an Api.


## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `apiId`                                                       | *string*                                                      | :heavy_check_mark:                                            | The ID of the Api this Metadata belongs to.                   |
| `createdAt`                                                   | [\DateTime](https://www.php.net/manual/en/class.datetime.php) | :heavy_check_mark:                                            | Creation timestamp.                                           |
| `metaKey`                                                     | *string*                                                      | :heavy_check_mark:                                            | The key for this metadata.                                    |
| `metaValue`                                                   | *string*                                                      | :heavy_check_mark:                                            | One of the values for this metadata.                          |
| `versionId`                                                   | *string*                                                      | :heavy_check_mark:                                            | The version ID of the Api this Metadata belongs to.           |
| `workspaceId`                                                 | *string*                                                      | :heavy_check_mark:                                            | The workspace ID this Metadata belongs to.                    |