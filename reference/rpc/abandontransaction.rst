.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

abandontransaction
==================

``abandontransaction "txid"``

Mark in-wallet transaction <txid> as abandoned
This will mark this transaction and all its in-wallet descendants as abandoned which will allow
for their inputs to be respent.  It can be used to replace "stuck" or evicted transactions.

It only works on transactions which are not included in a block and are not currently in the mempool.

It has no effect on transactions which are already abandoned.

Argument #1 - txid
~~~~~~~~~~~~~~~~~~

**Type:** string, required

The transaction id

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli abandontransaction "1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "abandontransaction", "params": ["1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

