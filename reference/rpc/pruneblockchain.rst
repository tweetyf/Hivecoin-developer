.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

pruneblockchain
===============

``pruneblockchain height``


Argument #1 - height
~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, required

The block height to prune up to. May be set to a discrete height, or to a UNIX epoch time
       to prune blocks whose block time is at least 2 hours older than the provided timestamp.

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - n
     - numeric
     - Height of the last block pruned

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli pruneblockchain 1000

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "pruneblockchain", "params": [1000]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

