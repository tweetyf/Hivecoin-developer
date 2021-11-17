.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getassetdata
============

``getassetdata "asset_name"``

Returns assets metadata if that asset exists

Arguments:
~~~~~~~~~~

1. "asset_name"               (string, required) the name of the asset

Result:
~~~~~~~

::

  {
    name: (string),
    amount: (number),
    units: (number),
    reissuable: (number),
    has_ipfs: (number),
    ipfs_hash: (hash), (only if has_ipfs = 1 and that data is a ipfs hash)
    txid_hash: (hash), (only if has_ipfs = 1 and that data is a txid hash)
    verifier_string: (string)
  }

Examples:
~~~~~~~~~

::

  hive-cli getassetdata "ASSET_NAME"
  
::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getassetdata", "params": ["ASSET_NAME"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

