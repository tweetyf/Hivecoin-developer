.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

transferfromaddress
===================


``transferfromaddress "asset_name" "from_address" qty "to_address" "message" expire_time "hvn_change_address" "asset_change_address"``

Transfer a quantity of an owned asset in a specific address to a given address

Arguments:
~~~~~~~~~~

1. "asset_name"               (string, required) name of asset
2. "from_address"             (string, required) address that the asset will be transferred from
3. "qty"                      (numeric, required) number of assets you want to send to the address
4. "to_address"               (string, required) address to send the asset to
5. "message"                  (string, optional) Once HIP5 is voted in ipfs hash or txid hash to send along with the transfer
6. "expire_time"              (numeric, optional) UTC timestamp of when the message expires
7. "hvn_change_address"       (string, optional, default = "") the transaction HVQ change will be sent to this address
8. "asset_change_address"     (string, optional, default = "") the transaction Asset change will be sent to this address

Result:
~~~~~~~

::
   
    txid[ 
    txid
    ]

Examples:
~~~~~~~~~

::
    
    hive-cli transferfromaddress "ASSET_NAME" "fromaddress" 20 "address" "QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E", 156545652

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "transferfromaddress", "params": ["ASSET_NAME" "fromaddress" 20 "address" "QmTqu3Lk3gmTsQVtjU7rYYM37EAW4xNmbuEAp2Mjr4AV7E", 156545652] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

