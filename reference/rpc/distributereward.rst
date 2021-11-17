.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

distributereward
================

``distributereward "asset_name" snapshot_height "distribution_asset_name" gross_distribution_amount ( "exception_addresses" ) ("change_address") ("dry_run")``

Splits the specified amount of the distribution asset to all owners of asset_name that are not in the optional exclusion_addresses

Arguments:
~~~~~~~~~~

1. "asset_name"                 (string, required) The reward will be distributed all owners of this asset
2. "snapshot_height"            (number, required) The block height of the ownership snapshot
3. "distribution_asset_name"    (string, required) The name of the asset that will be distributed, or HVQ
4. "gross_distribution_amount"  (number, required) The amount of the distribution asset that will be split amongst all owners
5. "exception_addresses"        (string, optional) Ownership addresses that should be excluded
6. "change_address"             (string, optional) If the rewards can't be fully distributed. The change will be sent to this address

Result:
~~~~~~~

::
  
  {
  error_txn_gen_failed: (string),
  error_nsf: (string),
  error_rejects: (string),
  error_db_update: (string),
  batch_results: [
    {
      transaction_id: (string),
      error_txn_rejected: (string),
      total_amount: (number),
      fee: (number),
      expected_count: (number),
      actual_count: (number),
    }
  ]
  }

Examples:
~~~~~~~~~

::
  
  hive-cli distributereward "TRONCO" 12345 "HVQ" 1000

::
  
  hive-cli distributereward "PHATSTACKS" 12345 "DIVIDENDS" 1000 "mwN7xC3yomYdvJuVXkVC7ymY9wNBjWNduD,n4Rf18edydDaRBh7t6gHUbuByLbWEoWUTg"

:: 
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "distributereward", "params": ["TRONCO" 34987 "DIVIDENDS" 100000] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

:: 
  
  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "distributereward", "params": ["PHATSTACKS" 34987 "HVQ" 100000 "mwN7xC3yomYdvJuVXkVC7ymY9wNBjWNduD,n4Rf18edydDaRBh7t6gHUbuByLbWEoWUTg"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

