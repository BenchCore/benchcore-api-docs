# BenchPay API Documentation (v1)
Official Documentation For BenchPay API V1 

---

title: BenchPay API Documentation

language_tabs:
   - javascript

toc_footers:
   - <a href='https://bex.life'>Powered By BEX Life</a>
   - Copyright 2018 BenchPay Foundation, LLC. All rights reserved.

includes:
   - errors

search: true

---

# Introduction

_The development and maintenance of the documentation are generously sponsored by the **[Bench Community Fund](https://bench.community)** - Thanks!_

This is a documentation for **[benchpay-v1](https://github.com/benchpay/benchpay-v1)**

**Version:** 1.0.0

# Accounts

## /api/accounts
```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').get('bex-address')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "account": {
        "address": "D59NTfV92ca9QevUydvMiFMFdubbCaAVCV",
        "publicKey": "037d035f08b3bad0d5bb605232c7aa41555693c480044dbeb797270a44c339da5a",
        "secondPublicKey": null,
        "vote": "0284a88da69cc04439633217c6961d2800df0f7dff7f85b9803848ee02d0743f1d",
        "username": null,
        "balance": 1023145260990,
        "votebalance": 0
    },
    "success": true
}
```

### ***GET***

**Summary:** Retrieve a BenchPay Account

#### HTTP Request
`***GET*** /api/accounts/`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


## /api/accounts/getBalance

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').balance('bex-address')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "balance": 1023145260990,
    "unconfirmedBalance": 1023145260990,
    "success": true
}
```

### ***GET***

**Summary:** Get the balance of an account

#### HTTP Request
`***GET*** /api/accounts/getBalance`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/accounts/getPublicKey

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').publicKey('bex-address')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "publicKey": "037d035f08b3bad0d5bb605232c7aa41555693c480044dbeb797270a44c339da5a",
    "success": true
}
```

### ***GET***
**Summary:** Get the public key of an account

#### HTTP Request
`***GET*** /api/accounts/getPublickey`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/accounts/delegates

### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').vote('bex-address')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "delegates": [
        {
            "username": "benchx",
            "address": "DRkVSeW5e2zh9v7R5msdLc26fo8axFALGT",
            "publicKey": "0284a88da69cc04439633217c6961d2800df0f7dff7f85b9803848ee02d0743f1d",
            "vote": "13475943400000",
            "producedblocks": 0,
            "missedblocks": 0,
            "rate": 15,
            "approval": "0.10",
            "productivity": "0.00"
        }
    ],
    "success": true
}
```

**Summary:** Get the delegate fee of an account

#### HTTP Request
`***GET*** /api/accounts/delegates`

**Parameters**
| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/accounts/getAllAccounts

### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').all()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "wallets": [
        {
            "address": "D59NTfV92ca9QevUydvMiFMFdubbCaAVCV",
            "publicKey": "037d035f08b3bad0d5bb605232c7aa41555693c480044dbeb797270a44c339da5a",
            "secondPublicKey": null,
            "vote": "0284a88da69cc04439633217c6961d2800df0f7dff7f85b9803848ee02d0743f1d",
            "username": null,
            "balance": 1023145260990,
            "votebalance": 0
        }
    ],
    "success": true
}
```

**Summary:** Get the delegates of an account

#### HTTP Request
`***GET*** /api/getAllAccounts`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| offset | query | The offset of resources that will be returned. | Yes | int32 |
| limit | query | The number of resources per page. | No | int32 |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


## /api/accounts/TOP
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').top()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "accounts": [
        {
            "address": "DGihocTkwDygiFvmg6aG8jThYTic47GzU9",
            "balance": 11499593462120632,
            "publicKey": "024c8247388a02ecd1de2a3e3fd5b7c61ecc2797fa3776599d558333ef1802d231"
        }
    ],
    "success": true
}
```

**Summary:** Get a list of top accounts

#### HTTP Request
`***GET*** /api/accounts/top`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |
| offset | query | An unsigned integer that specified the number of records to skip. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/accounts/count
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('accounts').count()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "count": 841,
    "success": true
}
```

**Summary:** Get the count of accounts

#### HTTP Request
`***GET*** /api/accounts/count`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# Blocks
This makes up the BenchPay `Blocks` API.

## /api/blocks/get
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').get('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "block": {
        "id": "17667031254892018837",
        "version": 0,
        "timestamp": 32818936,
        "previousBlock": "17683512654394589083",
        "height": 3035603,
        "numberOfTransactions": 0,
        "totalAmount": 0,
        "totalFee": 0,
        "reward": 200000000,
        "payloadLength": 0,
        "payloadHash": "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855",
        "generatorPublicKey": "02af5e6341efc14f4ba39a9ff65e151cc7304fc742ce7b2678d9aa446c555ee9c1",
        "blockSignature": "3045022100b128be0f76ed92be93cd8ef2bb64e199ab25ee66f72c75190e0f679d85b92f07022048f9c161e0e2055f7e80a663897b05ac6289b309acf9720f232565323c200afd",
        "confirmations": 8
    },
    "success": true
}
```

**Summary:** Get block by id

#### HTTP Request
`***GET*** /api/blocks/get`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').all()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "blocks": [
        {
            "id": "17667031254892018837",
            "version": 0,
            "timestamp": 32818936,
            "previousBlock": "17683512654394589083",
            "height": 3035603,
            "numberOfTransactions": 0,
            "totalAmount": 0,
            "totalFee": 0,
            "reward": 200000000,
            "payloadLength": 0,
            "payloadHash": "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855",
            "generatorPublicKey": "02af5e6341efc14f4ba39a9ff65e151cc7304fc742ce7b2678d9aa446c555ee9c1",
            "blockSignature": "3045022100b128be0f76ed92be93cd8ef2bb64e199ab25ee66f72c75190e0f679d85b92f07022048f9c161e0e2055f7e80a663897b05ac6289b309acf9720f232565323c200afd",
            "confirmations": 0
        },
        {
            "id": "17683512654394589083",
            "version": 0,
            "timestamp": 32818928,
            "previousBlock": "13631091596497440274",
            "height": 3035602,
            "numberOfTransactions": 0,
            "totalAmount": 0,
            "totalFee": 0,
            "reward": 200000000,
            "payloadLength": 0,
            "payloadHash": "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855",
            "generatorPublicKey": "03f264a6d2ebb62279313a6fd7fec4e2244785839b625a0b0c261e689ce5401d87",
            "blockSignature": "3044022076b8af9b9b31fb9f96761a00afb28b8fd95c6815d53a10e906dc781a8ec4aa4102205d7125b7923966e7f8f2aa2a58c40006cf792aa6a3caee1cd80ddcad0b000e18",
            "confirmations": 1
        }
    ],
    "success": true
}
```

**Summary:** Get all blocks

#### HTTP Request
`***GET*** /api/blocks`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |
| orderBy | query | A string that specifies the column by which to sort the records. | No | string |
| offset | query | An unsigned integer that specified the number of records to skip. | No | integer |
| generatorPublicKey | query | A valid BEX Public Key. | No | string |
| totalAmount | query |  | No | integer |
| totalFee | query |  | No | integer |
| reward | query |  | No | integer |
| previousBlock | query |  | No | string |
| height | query |  | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getEpoch
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').epoch()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "epoch": "2017-03-21T13:00:00.000Z",
    "success": true
}
```

**Summary:** Get the blockchain epoch

#### HTTP Request
`***GET*** /api/blocks/getEpoch`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getHeight
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').height()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "height": 3035616,
    "id": "4635377835812759465",
    "success": true
}
```

**Summary:** Get the blockchain height

#### HTTP Request
`***GET*** /api/blocks/getHeight`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getNetHash
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').nethash()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "nethash": "578e820911f24e039733b45e4882b73e301f813a0d2c31330dafda84534ffa23",
    "success": true
}
```

**Summary:** Get the blockchain nethash

#### HTTP Request
`***GET*** /api/blocks/getNethash`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getFee
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').fee('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "fee": 10000000,
    "success": true
}
```

**Summary:** Get the transaction fee for sending "normal" transactions

#### HTTP Request
`***GET*** /api/blocks/getFee`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getFees
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').fees()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "fees": {
    "send": 10000000,
    "vote": 100000000,
    "secondsignature": 500000000,
    "delegate": 2500000000,
    "multisignature": 500000000
  }
}
```

**Summary:** Get the network fees

#### HTTP Request
`***GET*** /api/blocks/getFees`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getMilestone
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').milestone()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "milestone": 1,
    "success": true
}
```

**Summary:** Get the blockchain milestone

#### HTTP Request
`***GET*** /api/blocks/getMilestone`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getReward
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').reward()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "reward": 200000000,
    "success": true
}
```

**Summary:** Get the blockchain reward

#### HTTP Request
`***GET*** /api/blocks/getReward`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getSupply
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').supply()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "supply": 13092004200000000,
    "success": true
}
```

**Summary:** Get the blockchain supply

#### HTTP Request
`***GET*** /api/blocks/getSupply`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/blocks/getStatus
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('blocks').status()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "epoch": "2017-03-21T13:00:00.000Z",
    "height": 3035628,
    "fee": 10000000,
    "milestone": 1,
    "nethash": "578e820911f24e039733b45e4882b73e301f813a0d2c31330dafda84534ffa23",
    "reward": 200000000,
    "supply": 13092005600000000,
    "success": true
}
```

**Summary:** Get the blockchain status

#### HTTP Request
`***GET*** /api/blocks/getStatus`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# Delegates

## /api/delegates
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').all()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "delegates": [
        {
            "username": "jaredricesr",
            "address": "D5PXQVeJmchVrZFHL7cALZK8mWWzjCaVfz",
            "publicKey": "02a9a0ac34a94f9d27fd9b4b56eb3c565a9a3f61e660f269775fb456f7f3301586",
            "vote": "02a9a0ac34a94f9d27fd9b4b56eb3c565a9a3f61e660f269775fb456f7f3301586"
        }
    ],
    "success": true
}
```

**Summary:** List all delegates

#### HTTP Request
`***GET*** /api/delegates`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderBy | query | A string that specifies the column by which to sort the records. | No | string |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |
| offset | query | An unsigned integer that specified the number of records to skip. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

### ***PUT***

```javascript
var bpAPI = require("benchpay-api-v1");
bpAPI.getBalance("Address of the account",
  function(error, success, response) {
    console.log(response);
});
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "balance": "Balance of account",
  "unconfirmedBalance": "Unconfirmed balance of account"
}
```

**Summary:** Create a new delegate

#### HTTP Request
`***PUT*** /api/delegates`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | A valid BEX delegate object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


## /api/delegates/count
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').count()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "count": 197,
    "success": true
}
```

**Summary:** Get the count of delegates

#### HTTP Request
`***GET*** /api/delegates/count`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/delegates/search
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').search({ ... })

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "delegates": [
    {
      "username": "testdelegate1",
      "address": "AWV3WnR14keWUHKyNcafucLD5R8aVXZBUE",
      "publicKey": "03a998ddb8fe8503e713c8108e0b8a9541a4212143f9230ae673c39d5f38de09d1",
      "vote": "0",
      "producedblocks": 0,
      "missedblocks": 0
    }
  ]
}
```

**Summary:** Search for specific delegates

#### HTTP Request
`***GET*** /api/delegates/search`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| q | query | A search query. | Yes | string |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/delegates/voters
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').voters('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "accounts": [
        {
            "username": null,
            "address": "D5mbS6mpP5UheuciNscpDLgC127kYjRtkK",
            "publicKey": "03f7e0b1ab14985990416f72ed0b206c20b9efa35156e4528c8ff749fa0eea5d5a",
            "balance": 400000000
        }
    ],
    "success": true
}
```

**Summary:** Get a list of voters for a delegate

#### HTTP Request
`***GET*** /api/delegates/voters`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| publicKey | query | A valid BEX Public Key. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/delegates/get
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').get('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "delegates": [
        {
            "username": "nomoreheroes",
            "address": "D5PXQVeJmchVrZFHL7cALZK8mWWzjCaVfz",
            "publicKey": "02a9a0ac34a94f9d27fd9b4b56eb3c565a9a3f61e660f269775fb456f7f3301586",
            "vote": "02a9a0ac34a94f9d27fd9b4b56eb3c565a9a3f61e660f269775fb456f7f3301586"
        },
        {
            "username": "nickeles",
            "address": "D5gqHU5UkDrugaemW2NNFH4hDyvfW2TEix",
            "publicKey": "022289579cd6336d9b940576170c016aa95c3003d9ceb16dbdb67098d35f6219d8",
            "vote": null
        }
    ],
    "success": true
}
```

**Summary:** Get a single delegate

#### HTTP Request
`***GET*** /api/delegates/get`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| publicKey | query | A valid BEX Public Key. | No | string |
| username | query | A valid BEX Delegate username. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


## /api/delegates/fee
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').fee()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "delegate": {
        "username": "nomoreheroes",
        "address": "DARiJqhogp2Lu6bxufUFQQMuMyZbxjCydN",
        "publicKey": "022cca9529ec97a772156c152a00aad155ee6708243e65c9d211a589cb5d43234d",
        "vote": "0257b7724e97cd832e0c28533a86da5220656f9b5122141daab20e8526decce01f"
    },
    "success": true
}
```

**Summary:** Get the delegate fee

#### HTTP Request
`***GET*** /api/delegates/fee`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/delegates/forging/getForgedByAccount
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('delegates').forged('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "fees": 66670000000,
    "rewards": 11968200000000,
    "forged": 12034870000000,
    "success": true
}
```

**Summary:** Get the amount of BEXs forged by an account

#### HTTP Request
`***GET*** /api/delegates/forging/getForgedByAccount`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| generatorPublicKey | query |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/delegates/getNextForgers
### ***GET***

```javascript
var bpAPI = require("benchpay-api-v1");
bpAPI.getBalance("Address of the account",
  function(error, success, response) {
    console.log(response);
});
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "balance": "Balance of account",
  "unconfirmedBalance": "Unconfirmed balance of account"
}
```

**Summary:** Get the next forger

#### HTTP Request
`***GET*** /api/delegates/getNextForgers`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


# Loader
## /api/loader/status
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('loader').status()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "loaded": false,
    "now": 3034441,
    "blocksCount": -26,
    "success": true
}
```

**Summary:** Get the blockchain status

#### HTTP Request
`***GET*** /api/loader/status`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/loader/status/sync
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('loader').syncing()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "syncing": true,
    "blocks": -31,
    "height": 3034446,
    "id": "16245805386023811986",
    "success": true
}
```

**Summary:** Get the synchronisation status of the client

#### HTTP Request
`***GET*** /api/loader/status/sync`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/loader/autoconfigure
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('loader').configuration()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "network": {
        "nethash": "578e820911f24e039733b45e4882b73e301f813a0d2c31330dafda84534ffa23",
        "token": "DEX",
        "symbol": "DEX",
        "explorer": "https://dexplorer.benchpay.io",
        "version": 30,
      	"ports": {
					"@benchpay/core-p2p": 6620,
          "@benchpay/core-api": 6623,
          "@benchpay/graphql": 6625,
          "@benchpay/rpc": 8080
        },
        "feeStatistics": [
          {
            "type": 0,
            "fees": {
              "minFee": 268421,
              "maxFee": 597781,
              "avgFee": 404591
            }
          }
        ]
    },
    "success": true
}
```

**Summary:** Auto-configure the client loader

#### HTTP Request
`***GET*** /api/loader/autoconfigure`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# Peers
## /api/peers/get
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('peers').get('127.0.0.1')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "peer": {
        "ip": "145.239.88.101",
        "port": 4002,
        "version": "1.1.1",
        "status": "OK",
        "os": "linux4.4.0-109-generic",
        "delay": 254
    },
    "success": true
}
```

**Summary:** Get a single peer

#### HTTP Request
`***GET*** /api/peers/get`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| ip | query | A valid server IP. | Yes | string |
| port | query | A valid server Port. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/peers
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('peers').all()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "peers": [
        {
            "ip": "62.113.246.106",
            "port": 4002,
            "version": "1.1.1",
            "height": 3035375,
            "status": "OK",
            "os": "linux2.6.32-042stab127.2",
            "delay": 109
        }
    ],
    "success": true
}
```

**Summary:** Get all peers

#### HTTP Request
`***GET*** /api/peers`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| port | query | A valid server port. | No | integer |
| state | query | An unsigned integer that specifies the peer state. | No | integer |
| os | query | A valid operating system. | No | string |
| version | query | A valid benchpay-v1 version. | No | string |
| orderBy | query | A string that specifies the column by which to sort the records. | No | string |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |
| offset | query | An unsigned integer that specified the number of records to skip. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/peers/version
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('peers').version()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "version": "1.0.0",
    "success": true
}
```

**Summary:** Get the peer version

#### HTTP Request
`***GET*** /api/peers/version`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# Signatures
## /api/signatures/fee
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('signatures').fee()

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "fee": 500000000,
    "success": true
}
```

**Summary:** Get the fee for a signature

#### HTTP Request
`***GET*** /api/signatures/fee`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


# Transactions
## /api/transactions/get
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('transactions').get('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
    "transaction": {
        "id": "5c6ce775447a5acd22050d72e2615392494953bb1fb6287e9ffb3c33eaeb79aa",
        "blockid": "4271682877946294396",
        "type": 0,
        "timestamp": 32794053,
        "amount": 32106400000,
        "fee": 10000000,
        "recipientId": "DQnQNoJuNCvpjYhxL7fsnGepHBqrumgsyP",
        "senderId": "DDiTHZ4RETZhGxcyAi1VruCXZKxBFqXMeh",
        "senderPublicKey": "027742333b7f06acef9d3a7b3a9a924dbe6b9ddd3dd164c808546cacd49f6e8682",
        "signature": "3044022047c39f6f45a46a87f91ca867f9551dbebf0035adcfcbdc1370222c7a1517fc0002206fb5ecc10460e0352a8b626a508e2fcc76e39e490b0a2581dd772ebc8079696e",
        "confirmations": 2279
    },
    "success": true
}
```

**Summary:** Get a single transaction

#### HTTP Request
`***GET*** /api/transactions/get`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | A valid transaction ID. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/TRANSACTIONS
### ***GET***

```javascript
var bpAPI = require("benchpay-api-v1");
bpAPI.getBalance("Address of the account",
  function(error, success, response) {
    console.log(response);
});
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "balance": "Balance of account",
  "unconfirmedBalance": "Unconfirmed balance of account"
}
```

**Summary:** Get all transactions

#### HTTP Request
`***GET*** /api/transactions`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| blockId | query | An unsigned integer that specifies the block ID. | No | string |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |
| type | query | An unsigned integer that specifies the transaction type. | No | integer |
| orderBy | query | A string that specifies the column by which to sort the records. | No | string |
| offset | query | An unsigned integer that specified the number of records to skip. | No | integer |
| senderPublicKey | query | A valid BEX Public Key. | No | string |
| vendorField | query | A string that specifies the SmartBridge used. | No | string |
| ownerPublicKey | query | A valid BEX Address. | No | string |
| ownerAddress | query | A valid BEX Address. | No | string |
| senderId | query | A valid BEX Address. | No | string |
| recipientId | query | A valid BEX Address. | No | string |
| amount | query | An unsigned integer that specifies the transaction amount. | No | integer |
| fee | query | An unsigned integer that specifies the transaction fee. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |


## /api/transactions/unconfirmed/get
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('transactions').allUnconfirmed({ ... })

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "balance": "Balance of account",
  "unconfirmedBalance": "Unconfirmed balance of account"
}
```

**Summary:** Get a single unconfirmed transaction

#### HTTP Request
`***GET*** /api/transactions/unconfirmed/get`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | A valid unconfirmed transaction ID. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## /api/transactions/unconfirmed
### ***GET***

```javascript
import Bex from '@benchpay/client'

try {
  const client = (new Bex()).getClient()
  client.setVersion(1)

  const response = await client.api('transactions').getUnconfirmed('parameter-here')

  console.log(response)
} catch (e) {
  console.log(e.message)
}
```

> The above command returns JSON structured like this:

```json
{
  "success": false,
  "error": "Transaction not found"
}
```

**Summary:** Get all unconfirmed transactions

#### HTTP Request
`***GET*** /api/transactions/unconfirmed`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| senderPublicKey | query | A valid BEX Public Key. | No | string |
| address | query | A valid BEX Address. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |
