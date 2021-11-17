.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getreceivedbyaccount
====================

``getreceivedbyaccount "account" ( minconf )``

DEPRECATED. Returns the total amount received by addresses with <account> in transactions with at least [minconf] confirmations.

Arguments:
~~~~~~~~~~

1. "account"      (string, required) The selected account, may be the default account using "".
2. minconf          (numeric, optional, default=1) Only include transactions confirmed at least this many times.

Result:
~~~~~~~

amount              (numeric) The total amount in HVQ received for this account.

Examples:
~~~~~~~~~

Amount received by the default account with at least 1 confirmation

::
    
    hive-cli getreceivedbyaccount ""

Amount received at the tabby account including unconfirmed amounts with zero confirmations

::
    
    hive-cli getreceivedbyaccount "tabby" 0

The amount with at least 6 confirmations

::
    
    hive-cli getreceivedbyaccount "tabby" 6

As a json rpc call

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getreceivedbyaccount", "params": ["tabby", 6] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

