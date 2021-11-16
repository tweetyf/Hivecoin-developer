.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

listwalletdir
=============

``listwalletdir``

Returns a list of wallets in the wallet directory.

Result
~~~~~~

::

  {                        (json object)
    "wallets" : [          (json array)
      {                    (json object)
        "name" : "str"     (string) The wallet name
      },
      ...
    ]
  }

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli listwalletdir

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "listwalletdir", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

