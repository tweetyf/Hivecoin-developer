.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

getnewaddress
=============

``getnewaddress ( "label" "address_type" )``

Returns a new hivecoin address for receiving payments.

If 'label' is specified, it is added to the address book
so payments received with the address will be associated with 'label'.

Argument #1 - label
~~~~~~~~~~~~~~~~~~~

**Type:** string, optional, default=""

The label name for the address to be linked to. It can also be set to the empty string "" to represent the default label. The label does not need to exist, it will be created if there is no label by the given name.

Argument #2 - address_type
~~~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, optional, default=set by -addresstype

The address type to use. Options are "legacy", "p2sh-segwit", and "bech32".

Result
~~~~~~

.. list-table::
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - str
     - string
     - The new hivecoin address

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli getnewaddress

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getnewaddress", "params": []}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

