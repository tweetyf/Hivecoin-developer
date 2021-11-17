.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getaccountaddress
=================

``getaccountaddress "account"``

DEPRECATED. Returns the current Hive address for receiving payments to this account.

Arguments:
~~~~~~~~~~

1. "account"       (string, required) The account name for the address. It can also be set to the empty string "" to represent the default account. The account does not need to exist, it will be created and a new address created  if there is no account by the given name.

Result:
~~~~~~~

::
    
    "address"          (string) The account hive address

Examples:
~~~~~~~~~

::
  
  hive-cli getaccountaddress 

::
    
    hive-cli getaccountaddress ""
    
::
    
    hive-cli getaccountaddress "myaccount"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaccountaddress", "params": ["myaccount"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

