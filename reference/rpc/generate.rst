.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

generate
========

``generate nblocks ( maxtries )``

Mine up to nblocks blocks immediately (before the RPC call returns) to an address in the wallet.

Arguments:
~~~~~~~~~~

1. nblocks      (numeric, required) How many blocks are generated immediately.
2. maxtries     (numeric, optional) How many iterations to try (default = 1000000).

Result:
~~~~~~~

::
    
    [ blockhashes ]     (array) hashes of blocks generated

Examples:
~~~~~~~~~

Generate 11 blocks

::
    
     hive-cli generate 11

