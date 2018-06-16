# BenchPay API Documentation (v1)
Official Documentation For BenchPay API V1 


---

title: BenchPay API Documentation

language_tabs:
   - shell

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

# /API/ACCOUNTS/GETBALANCE
## ***GET***

**Summary:** Get the balance of an account

### HTTP Request
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

# /API/ACCOUNTS/GETPUBLICKEY
## ***GET***

**Summary:** Get the public key of an account

### HTTP Request
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

# /API/ACCOUNTS/DELEGATES/FEE
## ***GET***

**Summary:** Get the delegate fee of an account

### HTTP Request
`***GET*** /api/accounts/delegates/fee`

**Parameters**
none 
**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/ACCOUNTS/DELEGATES
## ***GET***

**Summary:** Get the delegates of an account

### HTTP Request
`***GET*** /api/accounts/delegates`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |
| orderBy | query | A string that specifies the column by which to sort the records. | No | string |
| limit | query | An unsigned integer that specifies the maximum number of records. | No | integer |
| offset | query | An unsigned integer that specified the number of records to skip. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## ***PUT***

**Summary:** Vote for a Delegate by Public Key

### HTTP Request
`***PUT*** /api/accounts/delegates`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/ACCOUNTS
## ***GET***

**Summary:** Returns account information of an address

### HTTP Request
`***GET*** /api/accounts`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/ACCOUNTS/GETALLACCOUNTS
## ***GET***

**Summary:** Get a list of accounts

### HTTP Request
`***GET*** /api/accounts/getAllAccounts`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/ACCOUNTS/TOP
## ***GET***

**Summary:** Get a list of top accounts

### HTTP Request
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

# /API/ACCOUNTS/COUNT
## ***GET***

**Summary:** Get the count of accounts

### HTTP Request
`***GET*** /api/accounts/count`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GET
## ***GET***

**Summary:** Get block by id

### HTTP Request
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

# /API/BLOCKS
## ***GET***

**Summary:** Get all blocks

### HTTP Request
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

# /API/BLOCKS/GETEPOCH
## ***GET***

**Summary:** Get the blockchain epoch

### HTTP Request
`***GET*** /api/blocks/getEpoch`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETHEIGHT
## ***GET***

**Summary:** Get the blockchain height

### HTTP Request
`***GET*** /api/blocks/getHeight`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETNETHASH
## ***GET***

**Summary:** Get the blockchain nethash

### HTTP Request
`***GET*** /api/blocks/getNethash`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETFEE
## ***GET***

**Summary:** Get the transaction fee for sending "normal" transactions

### HTTP Request
`***GET*** /api/blocks/getFee`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETFEES
## ***GET***

**Summary:** Get the network fees

### HTTP Request
`***GET*** /api/blocks/getFees`

**Parameters**
none. 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETMILESTONE
## ***GET***

**Summary:** Get the blockchain milestone

### HTTP Request
`***GET*** /api/blocks/getMilestone`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETREWARD
## ***GET***

**Summary:** Get the blockchain reward

### HTTP Request
`***GET*** /api/blocks/getReward`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETSUPPLY
## ***GET***

**Summary:** Get the blockchain supply

### HTTP Request
`***GET*** /api/blocks/getSupply`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/BLOCKS/GETSTATUS
## ***GET***

**Summary:** Get the blockchain status

### HTTP Request
`***GET*** /api/blocks/getStatus`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/DELEGATES/COUNT
## ***GET***

**Summary:** Get the count of delegates

### HTTP Request
`***GET*** /api/delegates/count`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/DELEGATES/SEARCH
## ***GET***

**Summary:** Search for specific delegates

### HTTP Request
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

# /API/DELEGATES/VOTERS
## ***GET***

**Summary:** Get a list of voters for a delegate

### HTTP Request
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

# /API/DELEGATES/GET
## ***GET***

**Summary:** Get a single delegate

### HTTP Request
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

# /API/DELEGATES
## ***GET***

**Summary:** Get all delegates

### HTTP Request
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

## ***PUT***

**Summary:** Create a new delegate

### HTTP Request
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

# /API/DELEGATES/FEE
## ***GET***

**Summary:** Get the delegate fee

### HTTP Request
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

# /API/DELEGATES/FORGING/GETFORGEDBYACCOUNT
## ***GET***

**Summary:** Get the amount of BEXs forged by an account

### HTTP Request
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

# /API/DELEGATES/GETNEXTFORGERS
## ***GET***

**Summary:** Get the next forger

### HTTP Request
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

# /API/DELEGATES/FORGING/ENABLE
## ***POST***

**Summary:** Enable forging for a delegate

### HTTP Request
`***POST*** /api/delegates/forging/enable`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| secret | query | A valid BEX Passphrase. | Yes | string |
| publicKey | query | A valid BEX Public Key. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/DELEGATES/FORGING/DISABLE
## ***POST***

**Summary:** Disable forging for a delegate

### HTTP Request
`***POST*** /api/delegates/forging/disable`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| secret | query | A valid BEX Passphrase. | Yes | string |
| publicKey | query | A valid BEX Public Key. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/LOADER/STATUS
## ***GET***

**Summary:** Get the blockchain status

### HTTP Request
`***GET*** /api/loader/status`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/LOADER/STATUS/SYNC
## ***GET***

**Summary:** Get the synchronisation status of the client

### HTTP Request
`***GET*** /api/loader/status/sync`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/LOADER/AUTOCONFIGURE
## ***GET***

**Summary:** Auto-configure the client loader

### HTTP Request
`***GET*** /api/loader/autoconfigure`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/MULTISIGNATURES/PENDING
## ***GET***

**Summary:** Get pending multi signature transactions

### HTTP Request
`***GET*** /api/multisignatures/pending`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| publicKey | query | A valid BEX Public Key. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/MULTISIGNATURES/SIGN
## ***POST***

**Summary:** Sign a new multi signature

### HTTP Request
`***POST*** /api/multisignatures/sign`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| secret | query | A valid BEX Passphrase. | Yes | string |
| secondSecret | query | A valid secondary BEX Passphrase. | No | string |
| publicKey | query | A valid BEX Public Key. | No | string |
| transactionId | query | A valid transaction ID. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/MULTISIGNATURES
## ***PUT***

**Summary:** Create a new multi signature

### HTTP Request
`***PUT*** /api/multisignatures`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | A valid multi signature object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/MULTISIGNATURES/ACCOUNTS
## ***GET***

**Summary:** Get a list of accounts

### HTTP Request
`***GET*** /api/multisignatures/accounts`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| publicKey | query | A valid BEX Public Key. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/PEERS/GET
## ***GET***

**Summary:** Get a single peer

### HTTP Request
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

# /API/PEERS
## ***GET***

**Summary:** Get all peers

### HTTP Request
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

# /API/PEERS/VERSION
## ***GET***

**Summary:** Get the peer version

### HTTP Request
`***GET*** /api/peers/version`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/SIGNATURES/FEE
## ***GET***

**Summary:** Get the fee for a signature

### HTTP Request
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

# /API/SIGNATURES
## ***PUT***

**Summary:** Create a new signature

### HTTP Request
`***PUT*** /api/signatures`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | A valid signature object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/TRANSACTIONS/GET
## ***GET***

**Summary:** Get a single transaction

### HTTP Request
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

# /API/TRANSACTIONS
## ***GET***

**Summary:** Get all transactions

### HTTP Request
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

## ***PUT***

**Summary:** Create a new transaction

### HTTP Request
`***PUT*** /api/transactions`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | A valid transaction object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /API/TRANSACTIONS/UNCONFIRMED/GET
## ***GET***

**Summary:** Get a single unconfirmed transaction

### HTTP Request
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

# /API/TRANSACTIONS/UNCONFIRMED
## ***GET***

**Summary:** Get all unconfirmed transactions

### HTTP Request
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

# /PEER/LIST
## ***GET***

**Summary:** Get a list of peers

### HTTP Request
`***GET*** /peer/list`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/BLOCKS/COMMON
## ***GET***

**Summary:** Get a list of blocks by ids

### HTTP Request
`***GET*** /peer/blocks/common`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| ids | query | A list of block IDs. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/BLOCK
## ***GET***

**Summary:** Get a single block

### HTTP Request
`***GET*** /peer/block`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/BLOCKS
## ***GET***

**Summary:** Get all blocks

### HTTP Request
`***GET*** /peer/blocks`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | A valid BEX Address. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/TRANSACTIONS
## ***GET***

**Description:** Get all transactions

### HTTP Request
`***GET*** /peer/transactions`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

## ***POST***

**Summary:** Create a new transaction

### HTTP Request
`***POST*** /peer/transactions`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| transactions | body | A valid transaction object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/TRANSACTIONSFROMIDS
## ***GET***

**Summary:** Get a list of transactions by ids

### HTTP Request
`***GET*** /peer/transactionsFromIds`

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| ids | query | A list of transaction IDs. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/HEIGHT
## ***GET***

**Summary:** Get the blockchain height

### HTTP Request
`***GET*** /peer/height`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

# /PEER/STATUS
## ***GET***

**Summary:** Get the blockchain status

### HTTP Request
`***GET*** /peer/status`

**Parameters**
none.

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| default | Unexpected error |

