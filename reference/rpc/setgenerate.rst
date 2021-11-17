.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

setgenerate
===========

``setgenerate generate ( genproclimit )``

Set 'generate' true or false to turn generation on or off.
Generation is limited to 'genproclimit' processors, -1 is unlimited.
See the getgenerate call for the current setting.

Arguments:
~~~~~~~~~~

1. generate         (boolean, required) Set to true to turn on generation, false to turn off.
2. genproclimit     (numeric, optional) Set the processor limit for when generation is on. Can be -1 for unlimited.

Examples:
~~~~~~~~~

Set the generation on with a limit of one processor

::
    
    hive-cli setgenerate true 1

Check the setting

::
    
    hive-cli getgenerate 

Turn off generation

::
    
    hive-cli setgenerate false

Using json rpc

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "setgenerate", "params": [true, 1] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

