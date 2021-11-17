.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

transferqualifier
=================


``transferqualifier "qualifier_name" qty "to_address" ("change_address") ("message") (expire_time)``

Transfer a qualifier asset owned by this wallet to the given address

Arguments:
~~~~~~~~~~

1. "qualifier_name"           (string, required) name of qualifier asset
2. "qty"                      (numeric, required) number of assets you want to send to the address
3. "to_address"               (string, required) address to send the asset to
4. "change_address"           (string, optional, default = "") the transaction change will be sent to this address
5. "message"                  (string, optional) Once HIP5 is voted in ipfs hash or txid hash to send along with the transfer
6. "expire_time"              (numeric, optional) UTC timestamp of when the message expires

Result:
~~~~~~~

::
    
    txid[ 
    txid
    ]

Examples:
~~~~~~~~~

::
    
    hive-cli transferqualifier "#QUALIFIER" 20 "to_address" "" "QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E" 15863654

::
    hive-cli transferqualifier "#QUALIFIER" 20 "to_address" "change_address" "QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E" 15863654

