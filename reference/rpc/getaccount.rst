.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaccount
==========

``getaccount "address"``

DEPRECATED. Returns the account associated with the given address.

Arguments:
~~~~~~~~~~

1. "address"         (string, required) The hive address for account lookup.

Result:
~~~~~~~

::
    
    "accountname"        (string) the account address

Examples:
~~~~~~~~~

::
 
  hive-cli getaccount "1D1ZrZNe3JUo7ZycKEYQQiQAWd9y54F4XX"

:: 
   
   curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaccount", "params": ["1D1ZrZNe3JUo7ZycKEYQQiQAWd9y54F4XX"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

