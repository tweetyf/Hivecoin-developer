.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

decodeblock
===========

``decodeblock "blockhex"``

Arguments:
~~~~~~~~~~

1. "blockhex"          (string, required) The block hex

Result:
~~~~~~~

::
  
  {
    "hash" : "hash",     (string) the block hash (same as provided)
    "size" : n,            (numeric) The block size
    "strippedsize" : n,    (numeric) The block size excluding witness data
    "weight" : n           (numeric) The block weight as defined in BIP 141
    "height" : n,          (numeric) The block height or index
    "version" : n,         (numeric) The block version
    "versionHex" : "00000000", (string) The block version formatted in hexadecimal
    "merkleroot" : "xxxx", (string) The merkle root
    "tx" : [               (array of string) The transaction ids
      "transactionid"     (string) The transaction id
      ,...
    ],
    "time" : ttt,          (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
    "nonce" : n,           (numeric) The nonce
    "bits" : "1d00ffff", (string) The bits
  }

Examples:
~~~~~~~~~

::
  
  hive-cli decodeblock "xxxx"
  
::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "decodeblock", "params": ["xxxx"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

