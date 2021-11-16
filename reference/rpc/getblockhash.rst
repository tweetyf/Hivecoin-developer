.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

getblockhash
============

``getblockhash height``

Returns hash of block in best-block-chain at height provided.

Argument #1 - height
~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, required

The height index

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - hex
     - string
     - The block hash

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli getblockhash 1000

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getblockhash", "params": [1000]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

