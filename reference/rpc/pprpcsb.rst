.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

pprpcsb
=======

``pprpcsb "header_hash" "mix_hash" "nonce"``

Attempts to submit new block to network mined by kawpow gpu miner via rpc.

Arguments
~~~~~~~~~

1. "header_hash"        (string, required) the prow_pow header hash that was given to the gpu miner from this rpc client
2. "mix_hash"           (string, required) the mix hash that was mined by the gpu miner via rpc
3. "nonce"              (string, required) the nonce of the block that hashed the valid block

Result:
~~~~~~~

Examples:
~~~~~~~~~

::
    
    hive-cli pprpcsb "header_hash" "mix_hash" 100000

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "pprpcsb", "params": ["header_hash" "mix_hash" 100000] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

