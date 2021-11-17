.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listmyassets
============

``listmyassets "( asset )" ( verbose ) ( count ) ( start ) (confs)``

Returns a list of all asset that are owned by this wallet

Arguments:
~~~~~~~~~~

1. "asset"                    (string, optional, default="*") filters results -- must be an asset name or a partial asset name followed by '*' ('*' matches all trailing characters)
2. "verbose"                  (boolean, optional, default=false) when false results only contain balances -- when true results include outpoints
3. "count"                    (integer, optional, default=ALL) truncates results to include only the first _count_ assets found
4. "start"                    (integer, optional, default=0) results skip over the first _start_ assets found (if negative it skips back from the end)
5. "confs"                    (integet, optional, default=0) results are skipped if they don't have this number of confirmations

Result (verbose=false):
~~~~~~~~~~~~~~~~~~~~~~~

::

  {
  (asset_name): balance,
  ...
  }

Result (verbose=true):
~~~~~~~~~~~~~~~~~~~~~~

::

  {
  (asset_name):
    {
      "balance": balance,
      "outpoints":
        [
          {
            "txid": txid,
            "vout": vout,
            "amount": amount
          }
          {...}, {...}
        ]
    }
  }
  {...}, {...}

Examples:
~~~~~~~~~

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listmyassets", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli listmyassets ASSET

::
  
  hive-cli listmyassets "ASSET*" true 10 20

::
  
  hive-cli listmyassets "ASSET*" true 10 20 1

