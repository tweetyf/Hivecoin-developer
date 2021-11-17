.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getdistributestatus
===================


``getdistributestatus "asset_name" snapshot_height "distribution_asset_name" gross_distribution_amount ( "exception_addresses" )``

Give information about the status of the distribution

Arguments:
~~~~~~~~~~

1. "asset_name"                 (string, required) The reward will be distributed all owners of this asset
2. "snapshot_height"            (number, required) The block height of the ownership snapshot
3. "distribution_asset_name"    (string, required) The name of the asset that will be distributed, or HVQ
4. "gross_distribution_amount"  (number, required) The amount of the distribution asset that will be split amongst all owners
5. "exception_addresses"        (string, optional) Ownership addresses that should be excluded

Examples:
~~~~~~~~~

::
  
  hive-cli getdistributestatus "TRONCO" 12345 "HVQ" 1000

::
    
    hive-cli getdistributestatus "PHATSTACKS" 12345 "DIVIDENDS" 1000 "mwN7xC3yomYdvJuVXkVC7ymY9wNBjWNduD,n4Rf18edydDaRBh7t6gHUbuByLbWEoWUTg"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getdistributestatus", "params": ["TRONCO" 34987 "DIVIDENDS" 100000] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getdistributestatus", "params": ["PHATSTACKS" 34987 "HVQ" 100000 "mwN7xC3yomYdvJuVXkVC7ymY9wNBjWNduD,n4Rf18edydDaRBh7t6gHUbuByLbWEoWUTg"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

