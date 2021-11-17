.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

unsubscribefromchannel
======================

``unsubscribefromchannel``

Unsubscribe from a certain message channel

Arguments:
~~~~~~~~~~

1. "channel_name"            (string, required) The channel name to unsubscribe from, must end with '!' or have an '~' in the name

Result:
~~~~~~~

::
    
    [

    ]

Examples:
~~~~~~~~~

::
    
    hive-cli unsubscribefromchannel "ASSET_NAME!"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "unsubscribefromchannel", "params": ["ASSET_NAME!"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

