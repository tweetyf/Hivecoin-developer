.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

requestsnapshot
===============

``requestsnapshot "asset_name" block_height``

Schedules a snapshot of the specified asset at the specified block height.

Arguments:
~~~~~~~~~~

1. "asset_name"              (string, required) The asset name for which the snapshot will be taken
2. "block_height"            (number, required) The block height at which the snapshot will be take

Result:
~~~~~~~

::

  {
  request_status: "Added",
  }

Examples:
~~~~~~~~~

::
  
  hive-cli requestsnapshot "TRONCO" 12345

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "requestsnapshot", "params": ["PHATSTACKS" 34987] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

