.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listaddressrestrictions
=======================

``listaddressrestrictions address``

List all assets that have frozen this address

Arguments:
~~~~~~~~~~

1. "address"          (string), required) the address to list restrictions for

Result:
~~~~~~~

::

    ["asset_name",        (string) The restriction name
    ...,
    ]

Examples:
~~~~~~~~~

::
    
    hive-cli listaddressrestrictions "address"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listaddressrestrictions", "params": ["address"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

