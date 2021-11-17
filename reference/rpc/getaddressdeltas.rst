.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaddressdeltas
================


``getaddressdeltas``

Returns all changes for an address (requires addressindex to be enabled).

Arguments:
~~~~~~~~~~

::

  {
    "addresses"
      [
        "address"  (string) The base58check encoded address
        ,...
      ]
    "start" (number) The start block height
    "end" (number) The end block height
    "chainInfo" (boolean) Include chain info in results, only applies if start and end specified
    "assetName"   (string, optional) Get deltas for a particular asset instead of HVQ.
  }

Result:
~~~~~~~

::

  [
    {
      "assetName"  (string) The asset associated with the deltas (HVQ for Hivecoin)
      "satoshis"  (number) The difference of satoshis
      "txid"  (string) The related txid
      "index"  (number) The related input or output index
      "height"  (number) The block height
      "address"  (string) The base58check encoded address
    }
  ]

Examples:
~~~~~~~~~

::

  hive-cli getaddressdeltas '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}'

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli getaddressdeltas '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"],"assetName":"MY_ASSET"}'

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"],"assetName":"MY_ASSET"}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

