.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

viewmytaggedaddresses
=====================

``viewmytaggedaddresses``

View all addresses this wallet owns that have been tagged

Result:
~~~~~~~

::
    
    {
    "Address:"                        (string) The address that was tagged
    "Tag Name:"                       (string) The asset name
    "[Assigned|Removed]:"             (Date) The UTC datetime of the assignment or removal of the tag in the format (YY-mm-dd HH:MM:SS)
                                         (Only the most recent tagging/untagging event will be returned for each address)
    }...

Examples:
~~~~~~~~~

::
    
    hive-cli viewmytaggedaddresses 

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "viewmytaggedaddresses", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

