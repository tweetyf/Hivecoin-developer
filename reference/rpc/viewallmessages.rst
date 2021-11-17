.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

viewallmessages
===============

``viewallmessages``

View all messages that the wallet contains

Result:
~~~~~~~

"Asset Name:"                     (string) The name of the asset the message was sent on
"Message:"                        (string) The IPFS hash of the message
"Time:"                           (Date) The time as a date in the format (YY-mm-dd Hour-minute-second)
"Block Height:"                   (number) The height of the block the message was included in
"Status:"                         (string) Status of the message (READ, UNREAD, ORPHAN, EXPIRED, SPAM, HIDDEN, ERROR)
"Expire Time:"                    (Date, optional) If the message had an expiration date assigned, it will be shown here in the format (YY-mm-dd Hour-minute-second)
"Expire UTC Time:"                (Date, optional) If the message contains an expire date that is too large, the UTC number will be displayed

Examples:
~~~~~~~~~

::
    
    hive-cli viewallmessages 

::
    
    curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "viewallmessages", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

