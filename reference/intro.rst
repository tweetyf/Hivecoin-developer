Introduction
============

The Developer Reference aims to provide technical details and API information to help you start building Hivecoin-based applications, but it is `not a specification <../reference/intro.html#not-a-specification>`__. To make the best use of this documentation, you may want to install the current version of Hivecoin Core, either from `source <https://github.com/HiveProject2021/Hivecoin>`__ or from a `pre-compiled executable <https://www.hivecoin.org/wallets/>`__.


In the following documentation, some strings have been shortened or wrapped: “[…]” indicates extra data was removed, and lines ending in a single backslash “\\” are continued below. If you hover your mouse over a paragraph, cross-reference links will be shown in blue. If you hover over a cross-reference link, a brief definition of the term will be displayed in a tooltip.

JSON-RPC Interface
^^^^^^^^^^^^^^^^^^^

The headless daemon `hived` has the JSON-RPC API enabled by default, the GUI
`hive-qt` has it disabled by default. This can be changed with the `-server`
option. In the GUI it is possible to execute RPC methods in the Debug Console
Dialog.

Setup JSON-RPC
^^^^^^^^^^^^^^^^^^^
By default port 9766 for mainnet, port 19766 for testnet,
and port 19443 for regtest.

We can add rpc user in  ~/.hive/hive.conf
::

  rpcuser = ru
  rpcpassword = rp
  daemon = 1
  rpcworkqueue = 200


start daemon
::

  hived


Example
^^^^^^^
getblockcount

Returns the height of the most-work fully-validated chain.

The genesis block has height 0.

cli
::

  bitcoin-cli getblockcount


json-rpc
::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getblockcount", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/


Not A Specification
^^^^^^^^^^^^^^^^^^^

The Developer Documentation describes how Hivecoin works to help educate new Hivecoin developers, but it is not a specification—and it never will be.

However, the Hivecoin Core developers are working on making their consensus code portable so other implementations can use it

In addition, we also warn you that this documentation has not been extensively reviewed by Hivecoin experts and so likely contains numerous errors. At the bottom of the menu on the left, you will find links that allow you to report an issue or to edit the documentation on GitHub. Please use those links if you find any errors or important missing information.
