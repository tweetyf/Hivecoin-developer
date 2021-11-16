.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

generatetoaddress
=================

``generatetoaddress nblocks "address" ( maxtries )``

Mine blocks immediately to a specified address (before the RPC call returns)

Argument #1 - nblocks
~~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, required

How many blocks are generated immediately.

Argument #2 - address
~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The address to send the newly generated hivecoin to.

Argument #3 - maxtries
~~~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, optional, default=1000000

How many iterations to try.

Result
~~~~~~

::

  [           (json array) hashes of blocks generated
    "hex",    (string) blockhash
    ...
  ]

Examples
~~~~~~~~


.. highlight:: shell

Generate 11 blocks to myaddress::

  hive-cli generatetoaddress 11 "myaddress"

If you are using the hivecoin Core wallet, you can get a new address to send the newly generated hivecoin to with:::

  hive-cli getnewaddress

