.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

generatetodescriptor
====================

``generatetodescriptor num_blocks "descriptor" ( maxtries )``

Mine blocks immediately to a specified descriptor (before the RPC call returns)

Argument #1 - num_blocks
~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, required

How many blocks are generated immediately.

Argument #2 - descriptor
~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The descriptor to send the newly generated hivecoin to.

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

Generate 11 blocks to mydesc::

  hive-cli generatetodescriptor 11 "mydesc"

