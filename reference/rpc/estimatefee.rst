.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

estimatefee
===========

``estimatefee nblocks``

DEPRECATED. Please use estimatesmartfee for more intelligent estimates.
Estimates the approximate fee per kilobyte needed for a transaction to begin
confirmation within nblocks blocks. Uses virtual transaction size of transaction
as defined in BIP 141 (witness data is discounted).

Arguments:
~~~~~~~~~~

1. nblocks     (numeric, required)

Result:
~~~~~~~

n              (numeric) estimated fee-per-kilobyte

A negative value is returned if not enough transactions and blocks
have been observed to make an estimate.
-1 is always returned for nblocks == 1 as it is impossible to calculate
a fee that is high enough to get reliably included in the next block.

Example:
~~~~~~~~~

::

  hive-cli estimatefee 6

