.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getsnapshot
===========

``getsnapshot "asset_name" block_height``

Returns details for the asset snapshot, at the specified height

Arguments:
~~~~~~~~~~

1. "asset_name"               (string, required) the name of the asset
2. block_height                 (int, required) the block height of the snapshot

Result:
~~~~~~~

::

  {
  name: (string),
  height: (number),
  owners: [
    {
      address: (string),
      amount_owned: (number),
    }
  }

Examples:
~~~~~~~~~

::
   
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getsnapshot", "params": ["ASSET_NAME" 28546] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

