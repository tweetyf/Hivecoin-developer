.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

checkaddresstag
===============

``checkaddresstag address tag_name``

Checks to see if an address has the given tag

Arguments:
~~~~~~~~~~

1. "address"          (string, required) the HVQ address to search
1. "tag_name"         (string, required) the tag to search

Result:
~~~~~~~

::

  "true/false", (boolean) If the address has the tag

Examples:
~~~~~~~~~

::

  hive-cli checkaddresstag "address" "tag_name"

::
    
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "checkaddresstag", "params": ["address" "tag_name"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

