.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getinfo
=======

getinfo

DEPRECATED. Returns an object containing various state info.

Result:
~~~~~~~

::

  {
  "deprecation-warning": "..." (string) warning that the getinfo command is deprecated and will be removed in 0.16
  "version": xxxxx,           (numeric) the server version
  "protocolversion": xxxxx,   (numeric) the protocol version
  "walletversion": xxxxx,     (numeric) the wallet version
  "balance": xxxxxxx,         (numeric) the total Hivecoin balance of the wallet
  "blocks": xxxxxx,           (numeric) the current number of blocks processed in the server
  "timeoffset": xxxxx,        (numeric) the time offset
  "connections": xxxxx,       (numeric) the number of connections
  "proxy": "host:port",       (string, optional) the proxy used by the server
  "difficulty": xxxxxx,       (numeric) the current difficulty
  "testnet": true|false,      (boolean) if the server is using testnet or not
  "keypoololdest": xxxxxx,    (numeric) the timestamp (seconds since Unix epoch) of the oldest pre-generated key in the key pool
  "keypoolsize": xxxx,        (numeric) how many new keys are pre-generated
  "unlocked_until": ttt,      (numeric) the timestamp in seconds since epoch (midnight Jan 1 1970 GMT) that the wallet is unlocked for transfers, or 0 if the wallet is locked
  "paytxfee": x.xxxx,         (numeric) the transaction fee set in HVQ/kB
  "relayfee": x.xxxx,         (numeric) minimum relay fee for transactions in HVQ/kB
  "errors": "..."             (string) any error messages
  }

Examples:
~~~~~~~~~

::
  
  hive-cli getinfo 

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

