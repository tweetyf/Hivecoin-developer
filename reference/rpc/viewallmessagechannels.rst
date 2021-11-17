.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

viewallmessagechannels
======================


``viewallmessagechannels``

View all message channels the wallet is subscribed to

Result:
~~~~~~~

::
    [
    "Asset Name"                      (string) The asset channel name

    ]

Examples:
~~~~~~~~~

::
    
    hive-cli viewallmessagechannels 

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "viewallmessagechannels", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

