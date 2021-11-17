.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

listassets
==========

``listassets "( asset )" ( verbose ) ( count ) ( start )``

Returns a list of all assets

This could be a slow/expensive operation as it reads from the database

Arguments:
~~~~~~~~~~

1. "asset"                    (string, optional, default="*") filters results -- must be an asset name or a partial asset name followed by '*' ('*' matches all trailing characters)
2. "verbose"                  (boolean, optional, default=false) when false result is just a list of asset names -- when true results are asset name mapped to metadata
3. "count"                    (integer, optional, default=ALL) truncates results to include only the first _count_ assets found
4. "start"                    (integer, optional, default=0) results skip over the first _start_ assets found (if negative it skips back from the end)

Result (verbose=false):
~~~~~~~~~~~~~~~~~~~~~~~

::

  [
  asset_name,
  ...
  ]

Result (verbose=true):
~~~~~~~~~~~~~~~~~~~~~~

::

  {
  (asset_name):
    {
      amount: (number),
      units: (number),
      reissuable: (number),
      has_ipfs: (number),
      ipfs_hash: (hash) (only if has_ipfs = 1 and data is a ipfs hash)
      ipfs_hash: (hash) (only if has_ipfs = 1 and data is a txid hash)
    },
  {...}, {...}
  }

Examples:
~~~~~~~~~

::
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listassets", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli listassets ASSET


::
  
  hive-cli listassets "ASSET*" true 10 20

