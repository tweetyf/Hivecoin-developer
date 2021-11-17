.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

clearmessages
=============

``clearmessages``

Delete current database of messages

Result:
~~~~~~~

::

  [ 

  ]

Examples:
~~~~~~~~~

::
    
  hive-cli clearmessages 

::
    
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "clearmessages", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

