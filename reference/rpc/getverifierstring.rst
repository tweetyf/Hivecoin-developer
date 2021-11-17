.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getverifierstring
=================

``getverifierstring restricted_name``

Retrieve the verifier string that belongs to the given restricted asset

Arguments:
~~~~~~~~~~

1. "restricted_name"          (string, required) the asset_name

Result:
~~~~~~~

"verifier_string", (string) The verifier for the asset

Examples:
~~~~~~~~~

::
    
    hive-cli getverifierstring "restricted_name"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getverifierstring", "params": ["restricted_name"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

