.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaddressmempool
=================

``getaddressmempool``

Returns all mempool deltas for an address (requires addressindex to be enabled).

Arguments:
~~~~~~~~~~

::

  {
  "addresses"
    [
      "address"  (string) The base58check encoded address
      ,...
    ]
  },

"includeAssets" (boolean, optional, default false)  If true this will return an expanded result which includes asset deltas

Result:
~~~~~~~

::
 
  [
  {
    "address"  (string) The base58check encoded address
    "assetName"  (string) The name of the associated asset (HVQ for Hivecoin)
    "txid"  (string) The related txid
    "index"  (number) The related input or output index
    "satoshis"  (number) The difference of satoshis
    "timestamp"  (number) The time the transaction entered the mempool (seconds)
    "prevtxid"  (string) The previous txid (if spending)
    "prevout"  (string) The previous transaction output index (if spending)
  }
  ]

Examples:
~~~~~~~~~

::

  hive-cli getaddressmempool '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}'

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressmempool", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli getaddressmempool '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}', true

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressmempool", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}, true] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

