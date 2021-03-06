.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

listaddressgroupings
====================

``listaddressgroupings``

Lists groups of addresses which have had their common ownership
made public by common use as inputs or as the resulting change
in past transactions

Result
~~~~~~

::

  [               (json array)
    [             (json array)
      [           (json array)
        "str",    (string) The hivecoin address
        n,        (numeric) The amount in BTC
        "str",    (string, optional) The label
        ...
      ],
      ...
    ],
    ...
  ]

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli listaddressgroupings

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "listaddressgroupings", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

