.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

listlockunspent
===============

``listlockunspent``

Returns list of temporarily unspendable outputs.

See the lockunspent call to lock and unlock transactions for spending.

Result
~~~~~~

::

  [                      (json array)
    {                    (json object)
      "txid" : "hex",    (string) The transaction id locked
      "vout" : n         (numeric) The vout value
    },
    ...
  ]

Examples
~~~~~~~~


.. highlight:: shell

List the unspent transactions::

  hive-cli listunspent

Lock an unspent transaction::

  hive-cli lockunspent false "[{\"txid\":\"a08e6907dbbd3d809776dbfc5d82e371b764ed838b5655e72f463568df1aadf0\",\"vout\":1}]"

List the locked transactions::

  hive-cli listlockunspent

Unlock the transaction again::

  hive-cli lockunspent true "[{\"txid\":\"a08e6907dbbd3d809776dbfc5d82e371b764ed838b5655e72f463568df1aadf0\",\"vout\":1}]"

As a JSON-RPC call::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "listlockunspent", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

