.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

freezeaddress
=============

``freezeaddress asset_name address (change_address) (asset_data)``

Freeze an address from transferring a restricted asset

Arguments:
~~~~~~~~~~

1. "asset_name"       (string, required) the name of the restricted asset you want to freeze
2. "address"          (string, required) the address that will be frozen
3. "change_address"   (string, optional) The change address for the owner token of the restricted asset
4. "asset_data"       (string, optional) The asset data (ipfs or a hash) to be applied to the transfer of the owner token

Result:
~~~~~~~

::

  "txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
  
  hive-cli freezeaddress "$RESTRICTED_ASSET" "address"

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "freezeaddress", "params": ["$RESTRICTED_ASSET" "address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
 
  hive-cli freezeaddress "$RESTRICTED_ASSET" "address" "change_address"

::
 
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "freezeaddress", "params": ["$RESTRICTED_ASSET" "address" "change_address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

