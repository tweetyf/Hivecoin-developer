.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

walletpassphrasechange
======================

``walletpassphrasechange "oldpassphrase" "newpassphrase"``

Changes the wallet passphrase from 'oldpassphrase' to 'newpassphrase'.

Argument #1 - oldpassphrase
~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The current passphrase

Argument #2 - newpassphrase
~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The new passphrase

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli walletpassphrasechange "old one" "new one"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "walletpassphrasechange", "params": ["old one", "new one"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

