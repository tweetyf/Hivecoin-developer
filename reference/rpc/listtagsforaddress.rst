.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listtagsforaddress
==================

``listtagsforaddress address``

List all tags assigned to an address

Arguments:
~~~~~~~~~~

1. "address"          (string, required) the address to list tags for

Result:
~~~~~~~

::

  ["tag_name",        (string) The tag name
  ...,  
  ]

Examples:
~~~~~~~~~

::

  hive-cli listtagsforaddress "address"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listtagsforaddress", "params": ["address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

