.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

issue
=====

``issue "asset_name" qty "( to_address )" "( change_address )" ( units ) ( reissuable ) ( has_ipfs ) "( ipfs_hash )"``

Issue an asset, subasset or unique asset.
Asset name must not conflict with any existing asset.
Unit as the number of decimals precision for the asset (0 for whole units ("1"), 8 for max precision ("1.00000000")
Reissuable is true/false for whether additional units can be issued by the original issuer.
If issuing a unique asset these values are required (and will be defaulted to): qty=1, units=0, reissuable=false.

Arguments:
~~~~~~~~~~

1. "asset_name"            (string, required) a unique name
2. "qty"                   (numeric, optional, default=1) the number of units to be issued
3. "to_address"            (string), optional, default=""), address asset will be sent to, if it is empty, address will be generated for you
4. "change_address"        (string), optional, default=""), address the the hvn change will be sent to, if it is empty, change address will be generated for you
5. "units"                 (integer, optional, default=0, min=0, max=8), the number of decimals precision for the asset (0 for whole units ("1"), 8 for max precision ("1.00000000")
6. "reissuable"            (boolean, optional, default=true (false for unique assets)), whether future reissuance is allowed
7. "has_ipfs"              (boolean, optional, default=false), whether ipfs hash is going to be added to the asset
8. "ipfs_hash"             (string, optional but required if has_ipfs = 1), an ipfs hash or a txid hash once HIP5 is activated

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli issue "ASSET_NAME" 1000

::
    
    hive-cli issue "ASSET_NAME" 1000 "myaddress"

::
    
    hive-cli issue "ASSET_NAME" 1000 "myaddress" "changeaddress" 4

::
    
    hive-cli issue "ASSET_NAME" 1000 "myaddress" "changeaddress" 2 true

::
    
    hive-cli issue "ASSET_NAME" 1000 "myaddress" "changeaddress" 8 false true QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E

::
    
    hive-cli issue "ASSET_NAME/SUB_ASSET" 1000 "myaddress" "changeaddress" 2 true

::
    
    hive-cli issue "ASSET_NAME#uniquetag"

