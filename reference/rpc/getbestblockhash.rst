.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

getbestblockhash
================

``getbestblockhash``

Returns the hash of the best (tip) block in the most-work fully-validated chain.

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - hex
     - string
     - the block hash, hex-encoded

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli getbestblockhash

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getbestblockhash", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

