.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

reissue
=======

``reissue "asset_name" qty "to_address" "change_address" ( reissuable ) ( new_units) "( new_ipfs )"``

Reissues a quantity of an asset to an owned address if you own the Owner Token
Can change the reissuable flag during reissuance
Can change the ipfs hash during reissuance

Arguments:
~~~~~~~~~~

1. "asset_name"               (string, required) name of asset that is being reissued
2. "qty"                      (numeric, required) number of assets to reissue
3. "to_address"               (string, required) address to send the asset to
4. "change_address"           (string, optional) address that the change of the transaction will be sent to
5. "reissuable"               (boolean, optional, default=true), whether future reissuance is allowed
6. "new_units"                (numeric, optional, default=-1), the new units that will be associated with the asset
7. "new_ipfs"                 (string, optional, default=""), whether to update the current ipfs hash or txid once HIP5 is active

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli reissue "ASSET_NAME" 20 "address"

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "reissue", "params": ["ASSET_NAME" 20 "address" "change_address" "true" 8 "Qmd286K6pohQcTKYqnS1YhWrCiS4gz7Xi34sdwMe9USZ7u"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

