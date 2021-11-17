.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getsnapshotrequest
==================

``getsnapshotrequest "asset_name" block_height``

Retrieves the specified snapshot request details.

Arguments:
~~~~~~~~~~

1. "asset_name"              (string, required) The asset name for which the snapshot will be taken
2. "block_height"            (number, required) The block height at which the snapshot will be take

Result:
~~~~~~~

::
  
  {
  asset_name: (string),
  block_height: (number),
  }

Examples:
~~~~~~~~~

::
  
  hive-cli getsnapshotrequest "TRONCO" 12345

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getsnapshotrequest", "params": ["PHATSTACKS" 34987] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

