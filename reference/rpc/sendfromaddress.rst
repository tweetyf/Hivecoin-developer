.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

sendfromaddress
===============

``sendfromaddress "from_address" "to_address" amount ( "comment" "comment_to" subtractfeefromamount replaceable conf_target "estimate_mode")``

Send an amount from a specific address to a given address. All hvn change will get sent back to the from_address

Arguments:
~~~~~~~~~~

1. "from_address"       (string, required) The hive address to send from.
2. "to_address"            (string, required) The hive address to send to.
3. "amount"             (numeric or string, required) The amount in HVQ to send. eg 0.1
4. "comment"            (string, optional) A comment used to store what the transaction is for. 
                             This is not part of the transaction, just kept in your wallet.
5. "comment_to"         (string, optional) A comment to store the name of the person or organization 
                             to which you're sending the transaction. This is not part of the 
                             transaction, just kept in your wallet.
6. subtractfeefromamount  (boolean, optional, default=false) The fee will be deducted from the amount being sent.
                             The recipient will receive less hives than you enter in the amount field.
7. conf_target            (numeric, optional) Confirmation target (in blocks)
8. "estimate_mode"      (string, optional, default=UNSET) The fee estimate mode, must be one of:
       "UNSET"
       "ECONOMICAL"
       "CONSERVATIVE"

Result:
~~~~~~~

"txid"                  (string) The transaction id.

Examples:
~~~~~~~~~

::
       
       hive-cli sendfromaddress "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" 0.1

::
       
       hive-cli sendfromaddress "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" 0.1 "donation" "seans outpost"

::
       
       hive-cli sendfromaddress "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" 0.1 "" "" true

::
       
       curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "sendfromaddress", "params": ["1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd" "1M72Sfpbz1BPpXFHz9m3CdqATR44Jvaydd", 0.1, "donation", "seans outpost"] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

