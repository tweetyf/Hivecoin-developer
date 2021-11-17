.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

clearmempool
============

``clearmempool``

Removes all transaction from the mempool

Examples:
~~~~~~~~~

::

  hive-cli clearmempool 

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "clearmempool", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

