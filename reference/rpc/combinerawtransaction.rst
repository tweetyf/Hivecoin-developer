.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

combinerawtransaction
=====================

``combinerawtransaction ["hexstring",...]``

Combine multiple partially signed transactions into one transaction.

The combined transaction may be another partially signed transaction or a
fully signed transaction.

Argument #1 - txs
~~~~~~~~~~~~~~~~~

**Type:** json array, required

The hex strings of partially signed transactions

::

     [
       "hexstring",    (string) A hex-encoded raw transaction
       ...
     ]

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - str
     - string
     - The hex-encoded raw transaction with signature(s)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli combinerawtransaction '["myhex1", "myhex2", "myhex3"]'

