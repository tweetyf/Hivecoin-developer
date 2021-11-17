.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

viewmyrestrictedaddresses
=========================

``viewmyrestrictedaddresses``

View all addresses this wallet owns that have been restricted

Result:
~~~~~~~

::
    
    {
    "Address:"                        (string) The address that was restricted
    "Asset Name:"                     (string) The asset that the restriction applies to
    "[Restricted|Derestricted]:"      (Date) The UTC datetime of the restriction or derestriction in the format (YY-mm-dd HH:MM:SS))
                                         (Only the most recent restriction/derestriction event will be returned for each address)
    }...

Examples:
~~~~~~~~~

::
    
    hive-cli viewmyrestrictedaddresses 

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "viewmyrestrictedaddresses", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

