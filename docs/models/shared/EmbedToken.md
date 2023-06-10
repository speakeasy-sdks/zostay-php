# EmbedToken

A representation of an embed token granted for working with Speakeasy components.


## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `createdAt`                                                   | [\DateTime](https://www.php.net/manual/en/class.datetime.php) | :heavy_check_mark:                                            | Creation timestamp.                                           |
| `createdBy`                                                   | *string*                                                      | :heavy_check_mark:                                            | The ID of the user that created this token.                   |
| `description`                                                 | *string*                                                      | :heavy_check_mark:                                            | A detailed description of the EmbedToken.                     |
| `expiresAt`                                                   | [\DateTime](https://www.php.net/manual/en/class.datetime.php) | :heavy_check_mark:                                            | The time this token expires.                                  |
| `filters`                                                     | *string*                                                      | :heavy_check_mark:                                            | The filters applied to this token.                            |
| `id`                                                          | *string*                                                      | :heavy_check_mark:                                            | The ID of this EmbedToken.                                    |
| `lastUsed`                                                    | [\DateTime](https://www.php.net/manual/en/class.datetime.php) | :heavy_minus_sign:                                            | The last time this token was used.                            |
| `revokedAt`                                                   | [\DateTime](https://www.php.net/manual/en/class.datetime.php) | :heavy_minus_sign:                                            | The time this token was revoked.                              |
| `revokedBy`                                                   | *?string*                                                     | :heavy_minus_sign:                                            | The ID of the user that revoked this token.                   |
| `workspaceId`                                                 | *string*                                                      | :heavy_check_mark:                                            | The workspace ID this token belongs to.                       |