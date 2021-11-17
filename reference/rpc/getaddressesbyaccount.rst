.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaddressesbyaccount
=====================

``getaddressesbyaccount "account"``

DEPRECATED. Returns the list of addresses for the given account.

Arguments:
~~~~~~~~~~

1. "account"        (string, required) The account name.

Result:
~~~~~~~

::

  [                     (json array of string)
    "address"         (string) a hive address associated with the given account
    ,...
  ]

Examples:
~~~~~~~~~

::

  hive-cli getaddressesbyaccount "tabby"

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressesbyaccount", "params": ["tabby"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

