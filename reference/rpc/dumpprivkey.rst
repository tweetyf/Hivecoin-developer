.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

dumpprivkey
===========

``dumpprivkey "address"``

Reveals the private key corresponding to 'address'.

Then the importprivkey can be used with this output

Argument #1 - address
~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The hivecoin address for the private key

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - str
     - string
     - The private key

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli dumpprivkey "myaddress"

::

  hive-cli importprivkey "mykey"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "dumpprivkey", "params": ["myaddress"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

