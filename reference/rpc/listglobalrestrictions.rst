.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listglobalrestrictions
======================

``listglobalrestrictions``

List all global restricted assets

Result:
~~~~~~~


::
    
    ["asset_name", (string) The asset name
    ...,
    ]

Examples:
~~~~~~~~~

::
    
    hive-cli listglobalrestrictions 

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listglobalrestrictions", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

