.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listaddressesfortag
===================

``listaddressesfortag tag_name``

List all addresses that have been assigned a given tag

Arguments:
~~~~~~~~~~

1. "tag_name"          (string, required) the tag asset name to search for

Result:
~~~~~~~

::

    ["address",        (string) The address
    ...,
    ]

Examples:
~~~~~~~~~


::
    
    hive-cli listaddressesfortag "#TAG"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listaddressesfortag", "params": ["#TAG"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

