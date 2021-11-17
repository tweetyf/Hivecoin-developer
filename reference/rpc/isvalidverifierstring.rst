.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

isvalidverifierstring
=====================

``isvalidverifierstring verifier_string``

Checks to see if the given verifier string is valid

Arguments:
~~~~~~~~~~

1. "verifier_string"   (string, required) the verifier string to check

Result:
~~~~~~~

"xxxxxxx", (string) If the verifier string is valid, and the reason

Examples:
~~~~~~~~~

::
    
    hive-cli isvalidverifierstring "verifier_string"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "isvalidverifierstring", "params": ["verifier_string"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

