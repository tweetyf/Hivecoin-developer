.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

reissuerestrictedasset
======================

``reissuerestrictedasset "asset_name" qty to_address ( change_verifier ) ( "new_verifier" ) "( change_address )" ( new_units ) ( reissuable ) "( new_ipfs )"``

Reissue an already created restricted asset
Reissuable is true/false for whether additional asset quantity can be created and if the verifier string can be changed

Arguments:
~~~~~~~~~~

1. "asset_name"            (string, required) a unique name, starts with '$'
2. "qty"                   (numeric, required) the additional quantity of the asset to be issued
3. "to_address"            (string, required) address asset will be sent to, this address must meet the verifier string requirements
4. "change_verifier"       (boolean, optional, default=false) if the verifier string will get changed
5. "new_verifier"          (string, optional, default="") the new verifier string that will be evaluated when restricted asset transfers are made
6. "change_address"        (string, optional, default="") address that the hvn change will be sent to, if it is empty, change address will be generated for you
7. "new_units"             (numeric, optional, default=-1) the new units that will be associated with the asset
8. "reissuable"            (boolean, optional, default=true (false for unique assets)) whether future reissuance is allowed
9. "new_ipfs"              (string, optional, default="") whether to update the current ipfs hash or txid once HIP5 is active

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli reissuerestrictedasset "$ASSET_NAME" 1000  "myaddress" true "KYC & !AML"

::
    
    hive-cli reissuerestrictedasset "$ASSET_NAME" 1000  "myaddress" true "KYC & !AML" 

::
    
    hive-cli reissuerestrictedasset "$ASSET_NAME" 1000  "myaddress" true "KYC & !AML" "changeaddress"

::
    
    hive-cli reissuerestrictedasset "$ASSET_NAME" 1000  "myaddress" true "KYC & !AML" "changeaddress" -1 true

::
    
    hive-cli reissuerestrictedasset "$ASSET_NAME" 1000  "myaddress" false "" "changeaddress" -1 false QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E

