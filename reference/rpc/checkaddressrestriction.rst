.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

checkaddressrestriction
=======================

``checkaddressrestriction address restricted_name``

Checks to see if an address has been frozen by the given restricted asset

Arguments:
~~~~~~~~~~

1. "address"          (string, required) the HVQ address to search
1. "restricted_name"   (string, required) the restricted asset to search

Result:
~~~~~~~

::

  "true/false", (boolean) If the address is frozen

Examples:
~~~~~~~~~

::

  hive-cli checkaddressrestriction "address" "restricted_name"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "checkaddressrestriction", "params": ["address" "restricted_name"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

