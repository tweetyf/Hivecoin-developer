.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaddressbalance
=================

getaddressbalance

Returns the balance for an address(es) (requires addressindex to be enabled).

Arguments:
~~~~~~~~~~

::

  {
    "addresses:"
      [
        "address"  (string) The base58check encoded address
        ,...
      ]
  },

"includeAssets" (boolean, optional, default false)  If true this will return an expanded result which includes asset balances


Result:
~~~~~~~

::

  {
    "balance"  (string) The current balance in satoshis
    "received"  (string) The total number of satoshis received (including change)
  }

OR

::

  [
    {
      "assetName"  (string) The asset associated with the balance (HVQ for Hivecoin)
      "balance"  (string) The current balance in satoshis
      "received"  (string) The total number of satoshis received (including change)
    },...

  ]

Examples:
~~~~~~~~~

::
  
  hive-cli getaddressbalance '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}'

::
  
  hive-cli getaddressbalance '{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}', true

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressbalance", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressbalance", "params": [{"addresses": ["12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX"]}, true] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

