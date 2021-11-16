.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

keypoolrefill
=============

``keypoolrefill ( newsize )``

Fills the keypool.

Requires wallet passphrase to be set with walletpassphrase call if wallet is encrypted.

Argument #1 - newsize
~~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, optional, default=100

The new keypool size

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli keypoolrefill

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "keypoolrefill", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

