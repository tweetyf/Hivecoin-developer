hive-cli Reference
==================

Most hive cli interfaces are same as JSON-RPC API, please search in RPC API for help.

Example
~~~~~~~

getblockcount

Returns the height of the most-work fully-validated chain.

The genesis block has height 0.

cli
::

  bitcoin-cli getblockcount


json-rpc
::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getblockcount", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

