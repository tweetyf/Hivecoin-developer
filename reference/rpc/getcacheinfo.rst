.. This file is licensed under the Apache License 2.0 available on  http://www.apache.org/licenses/. 

getcacheinfo
============

``getcacheinfo``

Result:
~~~~~~~

::

  [
  uxto cache size:
  asset total (exclude dirty):
  asset address map:
  asset address balance:
  my unspent asset:
  reissue data:
  asset metadata map:
  asset metadata list (est):
  dirty cache (est):
  ]

Examples:
~~~~~~~~~

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getcacheinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9766/

::
  
  hive-cli getcacheinfo 

