.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

addwitnessaddress
=================

``addwitnessaddress "address"``

Add a witness address for a script (with pubkey or redeemscript known).
It returns the witness script.

Arguments:
~~~~~~~~~~

1. "address"       (string, required) An address known to the wallet

Result:
~~~~~~~

::

  {
  "witnessaddress",  (string) The value of the new address (P2SH of witness script).
  }

