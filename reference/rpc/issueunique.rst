.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

issueunique
===========


``issueunique "root_name" [asset_tags] ( [ipfs_hashes] ) "( to_address )" "( change_address )"``
    
Issue unique asset(s).
root_name must be an asset you own.
An asset will be created for each element of asset_tags.
If provided ipfs_hashes must be the same length as asset_tags.
Five (5) HVQ will be burned for each asset created.

Arguments:
~~~~~~~~~~

1. "root_name"             (string, required) name of the asset the unique asset(s) are being issued under
2. "asset_tags"            (array, required) the unique tag for each asset which is to be issued
3. "ipfs_hashes"           (array, optional) ipfs hashes or txid hashes corresponding to each supplied tag (should be same size as "asset_tags")
4. "to_address"            (string, optional, default=""), address assets will be sent to, if it is empty, address will be generated for you
5. "change_address"        (string, optional, default=""), address the the hvn change will be sent to, if it is empty, change address will be generated for you

Result:
~~~~~~~

"txid"                     (string) The transaction id

Examples:
~~~~~~~~~

::
    
    hive-cli issueunique "MY_ASSET" '["primo","secundo"]'

::
    
    hive-cli issueunique "MY_ASSET" '["primo","secundo"]' '["first_hash","second_hash"]'

