.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaddresstxids
===============

getaddresstxids

Returns the txids for an address(es) (requires addressindex to be enabled).

Arguments:
~~~~~~~~~~

::

  {
  "addresses"
    [
      "address"  (string) The base58check encoded address
      ,...
    ]
  "start" (number, optional) The start block height
  "end" (number, optional) The end block height
  },
  "includeAssets" (boolean, optional, default false)  If true this will return an expanded result which includes asset transactions

Result:
~~~~~~~

:: 

  [
  "transactionid"  (string) The transaction id
  ,...
  ]

Examples:
~~~~~~~~~

::
  
  hive-cli getaddresstxids '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}'

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddresstxids", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli getaddresstxids '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}', true

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddresstxids", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}, true] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

