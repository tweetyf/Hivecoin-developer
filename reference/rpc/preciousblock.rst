.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

preciousblock
=============

``preciousblock "blockhash"``

Treats a block as if it were received before others with the same work.

A later preciousblock call can override the effect of an earlier one.

The effects of preciousblock are not retained across restarts.

Argument #1 - blockhash
~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

the hash of the block to mark as precious

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli preciousblock "blockhash"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "preciousblock", "params": ["blockhash"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

