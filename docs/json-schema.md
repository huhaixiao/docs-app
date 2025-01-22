# jsom schema

- https://json-schema.org/
- integer - 整数
- number - 包含小数

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://example.com/product.schema.json",
  "title": "Product",
  "description": "A product from Acme's catalog",
  "type": "object",
  "properties": {
    "productId": {
      "description": "The unique identifier for a product",
      "type": "integer"
    },
    "productName": {
      "description": "Name of the product",
      "type": "string"
    },
    "price": {
      "description": "The price of the product",
      "type": "number",
      "exclusiveMinimum": 0
    },
    "tags": {
      "description": "Tags for the product",
      "type": "array",
      "items": {
        "type": "string"
      },
      "minItems": 1,
      "uniqueItems": true
    },
    "dimensions": {
      "type": "object",
      "properties": {
        "length": {
          "type": "number"
        },
        "width": {
          "type": "number"
        },
        "height": {
          "type": "number"
        }
      },
      "required": ["length", "width", "height"]
    },
    "warehouseLocation": {
      "description": "Coordinates of the warehouse where the product is located.",
      "$ref": "https://example.com/geographical-location.schema.json"
    }
  },
  "required": ["productId", "productName", "price"]
}
```

## ajv

```js
const Ajv = require('ajv');
const schema = {
  type: 'object',
  properties: {
    name: { type:'string' },
    age: { type: 'number' }
  },
  required: ['name', 'age']
};

const ajv = new Ajv();
const validate = ajv.compile(schema);

const data = {
  name: 'John Doe',
  age: 30
};

const valid = validate(data);
if (!valid) {
  console.log(validate.errors);
}
```