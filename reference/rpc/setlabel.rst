.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

setlabel
========

``setlabel "address" "label"``

Sets the label associated with the given address.

Argument #1 - address
~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The hivecoin address to be associated with a label.

Argument #2 - label
~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The label to assign to the address.

Result
~~~~~~

::

  null    (json null)

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli setlabel "H7jq09vm5lfy0j5reeulh4x5752q25uqqvz34hufdl" "tabby"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "setlabel", "params": ["H7jq09vm5lfy0j5reeulh4x5752q25uqqvz34hufdl", "tabby"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

