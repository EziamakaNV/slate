---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Access API. You can use our API to access the full suite of endpoints which provide you with the financial tools to provide value to your users

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```python
import accessAPI

api = accessAPI.authorize('secret_key');
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: secret_key"
```

```javascript
const accessAPI = require('accessapi');

let api = accessAPI.authorize('secret_key');
```

> Make sure to replace `secrey_key` with your API key.

Access API uses API keys to allow access to the API. You can register a new Access API key at our [developer portal](http://example.com/developers).

The Access API expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: secret_key`

<aside class="notice">
You must replace <code>secret_key</code> with your personal API key.
</aside>

# Account

## Get Account

```python
import accessAPI

api = accessAPI.authorize('secret_key')
api.account.get(accountNumber='2342242232');
```

```shell
curl "http://api.access.com/account/2342242232"
  -H "Authorization: secret_key"
```

```javascript
const api = require('accessapi');

let api = accessapi.authorize('secret_key');
let kittens = api.account.get('2342242232');
```

> The above command returns JSON structured like this:

```json
  {
    "id": 23234294,
    "name": "Funmilayo Agbaje",
    "opened": "23-01-2013",
    "balance": 4000
  }
```

This endpoint retrieves a particualar account.

<!-- ### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete -->

