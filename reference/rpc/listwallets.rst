.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

listwallets
===========

``listwallets``

Returns a list of currently loaded wallets.

For full information on the wallet, use "getwalletinfo"

Result
~~~~~~

::

  [           (json array)
    "str",    (string) the wallet name
    ...
  ]

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli listwallets

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "listwallets", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

