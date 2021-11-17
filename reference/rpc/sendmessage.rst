.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

sendmessage
===========

``sendmessage "channel_name" "ipfs_hash" (expire_time)``

Creates and broadcasts a message transaction to the network for a channel this wallet owns

Arguments:
~~~~~~~~~~

1. "channel_name"             (string, required) Name of the channel that you want to send a message with (message channel, administrator asset), if a non administrator asset name is given, the administrator '!' will be added to it
2. "ipfs_hash"                (string, required) The IPFS hash of the message
3. "expire_time"              (numeric, optional) UTC timestamp of when the message expires

Result:
~~~~~~~

::
    [
    txid
    ]

Examples:
~~~~~~~~~

::
    
    hive-cli sendmessage "ASSET_NAME!" "QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E" 15863654

::
    
    hive-cli sendmessage "ASSET_NAME!" "QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E" 15863654

