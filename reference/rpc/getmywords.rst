.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getmywords
==========


``getmywords ( "account" )``

Returns the 12 words and passphrase used by BIP39 to generate the wallets private keys
Only returns value if wallet was created by the 12 words import/generation

Result:
~~~~~~~

"word_list:"    (string) A string of words separated by spaces
"passphrase:"    (optional) Only show if passphrase was used when creating the wallet

Examples:
~~~~~~~~~

::
    
    hive-cli getmywords 
    
::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getmywords", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

