## Schema
```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$ref": "#/$defs/Attestor",
  "$defs": {
    "Attestor": {
      "properties": {
        "lockfiles": {
          "items": {
            "$ref": "#/$defs/LockfileInfo"
          },
          "type": "array"
        }
      },
      "additionalProperties": false,
      "type": "object",
      "required": [
        "lockfiles"
      ]
    },
    "DigestSet": {
      "additionalProperties": {
        "type": "string"
      },
      "type": "object"
    },
    "LockfileInfo": {
      "properties": {
        "filename": {
          "type": "string"
        },
        "content": {
          "type": "string"
        },
        "digest": {
          "$ref": "#/$defs/DigestSet"
        }
      },
      "additionalProperties": false,
      "type": "object",
      "required": [
        "filename",
        "content",
        "digest"
      ]
    }
  }
}
```
