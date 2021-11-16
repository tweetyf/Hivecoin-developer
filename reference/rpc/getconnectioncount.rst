.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

getconnectioncount
==================

``getconnectioncount``

Returns the number of connections to other nodes.

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - n
     - numeric
     - The connection count

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli getconnectioncount

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getconnectioncount", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

