.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

removeprunedfunds
=================

``removeprunedfunds "txid"``

Deletes the specified transaction from the wallet. Meant for use with pruned wallets and as a companion to importprunedfunds. This will affect wallet balances.

Argument #1 - txid
~~~~~~~~~~~~~~~~~~

**Type:** string, required

The hex-encoded id of the transaction you are deleting

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli removeprunedfunds "a8d0c0184dde994a09ec054286f1ce581bebf46446a512166eae7628734ea0a5"

As a JSON-RPC call::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "removeprunedfunds", "params": ["a8d0c0184dde994a09ec054286f1ce581bebf46446a512166eae7628734ea0a5"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

