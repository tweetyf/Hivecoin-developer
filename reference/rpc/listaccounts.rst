.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listaccounts
============

``listaccounts ( minconf include_watchonly)``

DEPRECATED. Returns Object that has account names as keys, account balances as values.

Arguments:
~~~~~~~~~~

1. minconf             (numeric, optional, default=1) Only include transactions with at least this many confirmations
2. include_watchonly   (bool, optional, default=false) Include balances in watch-only addresses (see 'importaddress')

Result:
~~~~~~~

::
  
  {                      (json object where keys are account names, and values are numeric balances
  "account": x.xxx,  (numeric) The property name is the account name, and the value is the total balance for the account.
  ...
  }

Examples:
~~~~~~~~~

List account balances where there at least 1 confirmation

::
  
  hive-cli listaccounts 

List account balances including zero confirmation transactions

::
  
  hive-cli listaccounts 0

List account balances for 6 or more confirmations

::
  
  hive-cli listaccounts 6

As json rpc call

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listaccounts", "params": [6] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

