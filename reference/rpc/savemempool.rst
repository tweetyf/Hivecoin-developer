.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

savemempool
===========

``savemempool``

Dumps the mempool to disk. It will fail until the previous dump is fully loaded.

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli savemempool

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "savemempool", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

