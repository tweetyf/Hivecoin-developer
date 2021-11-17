.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getgenerate
===========

getgenerate

Return if the server is set to generate coins or not. The default is false.
It is set with the command line argument -gen (or hive.conf setting gen)
It can also be set with the setgenerate call.

Result
~~~~~~

true|false      (boolean) If the server is set to generate coins or not

Examples:
~~~~~~~~~

::

  hive-cli getgenerate 

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getgenerate", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

