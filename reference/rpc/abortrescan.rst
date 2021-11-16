.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

abortrescan
===========

``abortrescan``

Stops current wallet rescan triggered by an RPC call, e.g. by an importprivkey call.

Note: Use "getwalletinfo" to query the scanning progress.

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - true|false
     - boolean
     - Whether the abort was successful

Examples
~~~~~~~~


.. highlight:: shell

Import a private key::

  hive-cli importprivkey "mykey"

Abort the running wallet rescan::

  hive-cli abortrescan

As a JSON-RPC call::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "abortrescan", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

