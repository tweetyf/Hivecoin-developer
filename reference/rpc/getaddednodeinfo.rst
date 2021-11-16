.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

getaddednodeinfo
================

``getaddednodeinfo ( "node" )``

Returns information about the given added node, or all added nodes
(note that onetry addnodes are not listed here)

Argument #1 - node
~~~~~~~~~~~~~~~~~~

**Type:** string, optional, default=all nodes

If provided, return information about this specific node, otherwise all nodes are returned.

Result
~~~~~~

::

  [                                (json array)
    {                              (json object)
      "addednode" : "str",         (string) The node IP address or name (as provided to addnode)
      "connected" : true|false,    (boolean) If connected
      "addresses" : [              (json array) Only when connected = true
        {                          (json object)
          "address" : "str",       (string) The hivecoin server IP and port we're connected to
          "connected" : "str"      (string) connection, inbound or outbound
        },
        ...
      ]
    },
    ...
  ]

Examples
~~~~~~~~


.. highlight:: shell

::

  hive-cli getaddednodeinfo "192.168.0.201"

::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "getaddednodeinfo", "params": ["192.168.0.201"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

