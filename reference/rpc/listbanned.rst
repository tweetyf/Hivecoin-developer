.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

listbanned
==========

``listbanned``

List all manually banned IPs/Subnets.

Result
~~~~~~
::

  [
    {
    "address": <address>,             (string) The banned address.
    "banned_until": <time>,           (numeric) The time (in seconds since Jan 1 1970 GMT) until the address is banned.
    "ban_created": <time>,            (numeric) The time (in seconds since Jan 1 1970 GMT) when the ban was created.
    }
  ]

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli listbanned

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "listbanned", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

