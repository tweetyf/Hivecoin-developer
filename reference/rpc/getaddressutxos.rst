.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaddressutxos
===============

``getaddressutxos``

Returns all unspent outputs for an address (requires addressindex to be enabled).

Arguments:
~~~~~~~~~~

::

  {
  "addresses"
    [
      "address"  (string) The base58check encoded address
      ,...
    ],
  "chainInfo",  (boolean, optional, default false) Include chain info with results
  "assetName"   (string, optional) Get UTXOs for a particular asset instead of HVQ ('*' for all assets).
  }

Result
~~~~~~

::
  
  [
    {
      "address"  (string) The address base58check encoded
      "assetName" (string) The asset associated with the UTXOs (HVQ for Hivecoin)
      "txid"  (string) The output txid
      "height"  (number) The block height
      "outputIndex"  (number) The output index
      "script"  (strin) The script hex encoded
      "satoshis"  (number) The number of satoshis of the output
    }
  ]

Examples:
~~~~~~~~~

::
  
  hive-cli getaddressutxos '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}'

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli getaddressutxos '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"],"assetName":"MY_ASSET"}'

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"],"assetName":"MY_ASSET"}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

