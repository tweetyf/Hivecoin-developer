.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getmasterkeyinfo
================

getmasterkeyinfo

Fetches and displays the master private key and the master public key.

Result:
~~~~~~~

::
  
  {                           (json object)
  "bip32_root_private" : (string) extended master private key,
  "bip32_root_public" :  (string) extended master public key,
  "account_derivation_path" : (string) The derivation path to the account public/private keys
  "account_extended_private_key" : (string) extended account private key,
  "account_extended_public_key" :  (string) extended account public key,
  }

Examples:
~~~~~~~~~

::
  
  hive-cli getmasterkeyinfo 

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getmasterkeyinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

