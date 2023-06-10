# SchemaDiff

A SchemaDiff represents a diff of two Schemas.


## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `additions`                                                                          | array<*string*>                                                                      | :heavy_check_mark:                                                                   | Holds every addition change in the diff.                                             |
| `deletions`                                                                          | array<*string*>                                                                      | :heavy_check_mark:                                                                   | Holds every deletion change in the diff.                                             |
| `modifications`                                                                      | array<string, [SchemaDiffValueChange](../../models/shared/SchemaDiffValueChange.md)> | :heavy_check_mark:                                                                   | Holds every modification change in the diff.                                         |