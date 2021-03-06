.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

gettxoutproof
=============

``gettxoutproof ["txid",...] ( "blockhash" )``

Returns a hex-encoded proof that "txid" was included in a block.

NOTE: By default this function only works sometimes. This is when there is an
unspent output in the utxo for this transaction. To make it always work,
you need to maintain a transaction index, using the -txindex command line option or
specify the block in which the transaction is included manually (by blockhash).

Argument #1 - txids
~~~~~~~~~~~~~~~~~~~

**Type:** json array, required

The txids to filter

::

     [
       "txid",    (string) A transaction hash
       ...
     ]

Argument #2 - blockhash
~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, optional

If specified, looks for txid in the block with this hash

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - str
     - string
     - A string that is a serialized, hex-encoded data for the proof.

