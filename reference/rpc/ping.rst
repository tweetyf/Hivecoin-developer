.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

ping
====

``ping``

Requests that a ping be sent to all other nodes, to measure ping time.

Results provided in getpeerinfo, pingtime and pingwait fields are decimal seconds.

Ping command is handled in queue with all other commands, so it measures processing backlog, not just network ping.

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli ping

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "ping", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

