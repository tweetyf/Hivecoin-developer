.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

walletlock
==========

``walletlock``

Removes the wallet encryption key from memory, locking the wallet.

After calling this method, you will need to call walletpassphrase again
before being able to call any methods which require the wallet to be unlocked.

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

Set the passphrase for 2 minutes to perform a transaction::

  hive-cli walletpassphrase "my pass phrase" 120

Perform a send (requires passphrase set)::

  hive-cli sendtoaddress "H7jq09vm5lfy0j5reeulh4x5752q25uqqvz34hufdl" 1.0

Clear the passphrase since we are done before 2 minutes is up::

  hive-cli walletlock

As a JSON-RPC call::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "walletlock", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

