.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

combinepsbt
===========

``combinepsbt ["psbt",...]``

Combine multiple partially signed hivecoin transactions into one transaction.

Implements the Combiner role.

Argument #1 - txs
~~~~~~~~~~~~~~~~~

**Type:** json array, required

The base64 strings of partially signed transactions

::

     [
       "psbt",    (string) A base64 string of a PSBT
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
     - The base64-encoded partially signed transaction

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli combinepsbt '["mybase64_1", "mybase64_2", "mybase64_3"]'

