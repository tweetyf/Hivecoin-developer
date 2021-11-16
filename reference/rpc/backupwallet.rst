.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

backupwallet
============

``backupwallet "destination"``

Safely copies current wallet file to destination, which can be a directory or a path with filename.

Argument #1 - destination
~~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The destination directory or file

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli backupwallet "backup.dat"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "backupwallet", "params": ["backup.dat"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

