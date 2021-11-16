.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

submitblock
===========

``submitblock "hexdata" ( "dummy" )``

Attempts to submit new block to network.

See https://en.hivecoin.it/wiki/BIP_0022 for full specification.

Argument #1 - hexdata
~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

the hex-encoded block data to submit

Argument #2 - dummy
~~~~~~~~~~~~~~~~~~~

**Type:** string, optional, default=ignored

dummy value, for compatibility with BIP22. This value is ignored.

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - null
     - json null
     - Returns JSON Null when valid, a string according to BIP22 otherwise

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli submitblock "mydata"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "submitblock", "params": ["mydata"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

