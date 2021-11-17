.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

issuerestrictedasset
====================

``issuerestrictedasset "asset_name" qty "verifier" "to_address" "( change_address )" (units) ( reissuable ) ( has_ipfs ) "( ipfs_hash )"``

Issue a restricted asset.
Restricted asset names must not conflict with any existing restricted asset.
Restricted assets have units set to 0.
Reissuable is true/false for whether additional asset quantity can be created and if the verifier string can be changed

Arguments:
~~~~~~~~~~

1. "asset_name"            (string, required) a unique name, starts with '$', if '$' is not there it will be added automatically
2. "qty"                   (numeric, required) the quantity of the asset to be issued
3. "verifier"              (string, required) the verifier string that will be evaluated when restricted asset transfers are made
4. "to_address"            (string, required) address asset will be sent to, this address must meet the verifier string requirements
5. "change_address"        (string, optional, default="") address that the hvn change will be sent to, if it is empty, change address will be generated for you
6. "units"                 (integer, optional, default=0, min=0, max=8) the number of decimals precision for the asset (0 for whole units ("1"), 8 for max precision ("1.00000000")
7. "reissuable"            (boolean, optional, default=true (false for unique assets)) whether future reissuance is allowed
8. "has_ipfs"              (boolean, optional, default=false) whether an ipfs hash or txid hash is going to be added to the asset
9. "ipfs_hash"             (string, optional but required if has_ipfs = 1) an ipfs hash or a txid hash once HIP5 is activated

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli issuerestrictedasset "$ASSET_NAME" 1000 "#KYC & !#AML" "myaddress"

::
    
    hive-cli issuerestrictedasset "$ASSET_NAME" 1000 "#KYC & !#AML" "myaddress"

::
    
    hive-cli issuerestrictedasset "$ASSET_NAME" 1000 "#KYC & !#AML" "myaddress" "changeaddress" 5

::
    
    hive-cli issuerestrictedasset "$ASSET_NAME" 1000 "#KYC & !#AML" "myaddress" "changeaddress" 8 true

::
    
    hive-cli issuerestrictedasset "$ASSET_NAME" 1000 "#KYC & !#AML" "myaddress" "changeaddress" 0 false true QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E

