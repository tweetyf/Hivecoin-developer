.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getkawpowhash
=============

``getkawpowhash "header_hash" "mix_hash" nonce, height, "target"``

Get the kawpow hash for a block given its block data

Arguments
~~~~~~~~~

1. "header_hash"        (string, required) the prow_pow header hash that was given to the gpu miner from this rpc client
2. "mix_hash"           (string, required) the mix hash that was mined by the gpu miner via rpc
3. "nonce"              (string, required) the hex nonce of the block that hashed the valid block
4. "height"             (number, required) the height of the block data that is being hashed
5. "target"             (string, optional) the target of the block that is hash is trying to meet

Result:
~~~~~~~


Examples:
~~~~~~~~~

::
    
    hive-cli getkawpowhash "header_hash" "mix_hash" "0x100000" 2456

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getkawpowhash", "params": ["header_hash" "mix_hash" "0x100000" 2456] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

