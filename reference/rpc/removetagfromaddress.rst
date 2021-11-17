.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

removetagfromaddress
====================

``removetagfromaddress tag_name to_address (change_address) (asset_data)``

Remove a tag from a address

Arguments:
~~~~~~~~~~

1. "tag_name"            (string, required) the name of the tag you are removing from the address
2. "to_address"          (string, required) the address that the tag will be removed from
3. "change_address"      (string, optional) The change address for the qualifier token to be sent to
4. "asset_data"          (string, optional) The asset data (ipfs or a hash) to be applied to the transfer of the qualifier token

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli removetagfromaddress "#TAG" "to_address"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "removetagfromaddress", "params": ["#TAG" "to_address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
    
    hive-cli removetagfromaddress "#TAG" "to_address" "change_address"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "removetagfromaddress", "params": ["#TAG" "to_address" "change_address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

