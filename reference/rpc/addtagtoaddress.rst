.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

addtagtoaddress
===============

``addtagtoaddress tag_name to_address (change_address) (asset_data)``

Assign a tag to a address

Arguments:
~~~~~~~~~~

1. "tag_name"            (string, required) the name of the tag you are assigning to the address, if it doens't have '#' at the front it will be added
2. "to_address"          (string, required) the address that will be assigned the tag
3. "change_address"      (string, optional) The change address for the qualifier token to be sent to
4. "asset_data"          (string, optional) The asset data (ipfs or a hash) to be applied to the transfer of the qualifier token

Result:
~~~~~~~

::

  "txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::

  hive-cli addtagtoaddress "#TAG" "to_address"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "addtagtoaddress", "params": ["#TAG" "to_address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::

  hive-cli addtagtoaddress "#TAG" "to_address" "change_address"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "addtagtoaddress", "params": ["#TAG" "to_address" "change_address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

