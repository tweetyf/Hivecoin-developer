.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

freezerestrictedasset
=====================

``freezerestrictedasset asset_name (change_address) (asset_data)``

Freeze all trading for a specific restricted asset

Arguments:
~~~~~~~~~~

1. "asset_name"       (string, required) the name of the restricted asset you want to unfreeze
2. "change_address"   (string, optional) The change address for the owner token of the restricted asset
3. "asset_data"       (string, optional) The asset data (ipfs or a hash) to be applied to the transfer of the owner token

Result:
~~~~~~~

::

  "txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::

  hive-cli freezerestrictedasset "$RESTRICTED_ASSET"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "freezerestrictedasset", "params": ["$RESTRICTED_ASSET"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
    
     hive-cli freezerestrictedasset "$RESTRICTED_ASSET" "change_address"

::

     curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "freezerestrictedasset", "params": ["$RESTRICTED_ASSET" "change_address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

