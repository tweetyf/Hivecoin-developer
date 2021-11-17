.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

checkglobalrestriction
======================

``checkglobalrestriction restricted_name``

Checks to see if a restricted asset is globally frozen

Arguments:
~~~~~~~~~~

1. "restricted_name"   (string, required) the restricted asset to search

Result:
~~~~~~~

::

 "true/false", (boolean) If the restricted asset is frozen globally

Examples:
~~~~~~~~~

::

  hive-cli checkglobalrestriction "restricted_name"

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "checkglobalrestriction", "params": ["restricted_name"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

