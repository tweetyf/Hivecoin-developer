.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

uptime
======

``uptime``

Returns the total uptime of the server.

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - n
     - numeric
     - The number of seconds that the server has been running

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli uptime

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "uptime", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

