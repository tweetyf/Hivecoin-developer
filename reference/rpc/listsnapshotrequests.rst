.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listsnapshotrequests
====================

``listsnapshotrequests ["asset_name" [block_height]]``

List snapshot request details.

Arguments:
~~~~~~~~~~

asset_name: (string, optional) List only requests for a specific asset (default is "" for ALL)
block_height: (number, optional) List only requests for a particular block height (default is 0 for ALL)

Result:
~~~~~~~

::
  
  [
  {
    asset_name: (string),
    block_height: (number)
  }
  ]

Examples:
~~~~~~~~~

::
  
  hive-cli listsnapshotrequests 

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listsnapshotrequests", "params": ["TRONCO" 345333] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

