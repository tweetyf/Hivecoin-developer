.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

subscribetochannel
==================

``subscribetochannel``

Subscribe to a certain message channel

Arguments:
~~~~~~~~~~

1. "channel_name"            (string, required) The channel name to subscribe to, it must end with '!' or have an '~' in the name

Result:
~~~~~~~

::

  [

  ]

Examples:
~~~~~~~~~

::
    
    hive-cli subscribetochannel "ASSET_NAME!"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "subscribetochannel", "params": ["ASSET_NAME!"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

