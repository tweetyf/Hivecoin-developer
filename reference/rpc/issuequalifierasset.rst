.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

issuequalifierasset
===================

``issuequalifierasset "asset_name" qty "( to_address )" "( change_address )" ( has_ipfs ) "( ipfs_hash )"``

Issue an qualifier or sub qualifier asset
If the '#' character isn't added, it will be added automatically
Amount is a number between 1 and 10
Asset name must not conflict with any existing asset.
Unit is always set to Zero (0) for qualifier assets
Reissuable is always set to false for qualifier assets

Arguments:
~~~~~~~~~~

1. "asset_name"            (string, required) a unique name
2. "qty"                   (numeric, optional, default=1) the number of units to be issued
3. "to_address"            (string), optional, default=""), address asset will be sent to, if it is empty, address will be generated for you
4. "change_address"        (string), optional, default=""), address the the hvn change will be sent to, if it is empty, change address will be generated for you
5. "has_ipfs"              (boolean, optional, default=false), whether ipfs hash is going to be added to the asset
6. "ipfs_hash"             (string, optional but required if has_ipfs = 1), an ipfs hash or a txid hash once HIP5 is activated

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli issuequalifierasset "#ASSET_NAME" 1000

::
    
    hive-cli issuequalifierasset "ASSET_NAME" 1000 "myaddress"

::
    
    hive-cli issuequalifierasset "#ASSET_NAME" 1000 "myaddress" "changeaddress"

::
    
    hive-cli issuequalifierasset "ASSET_NAME" 1000 "myaddress" "changeaddress"

::
    
    hive-cli issuequalifierasset "#ASSET_NAME" 1000 "myaddress" "changeaddress" true QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E

::
    
    hive-cli issuequalifierasset "ASSET_NAME/SUB_QUALIFIER" 1000 "myaddress" "changeaddress"

::
    
    hive-cli issuequalifierasset "#ASSET_NAME"

