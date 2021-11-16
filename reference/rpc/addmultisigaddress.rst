.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

addmultisigaddress
==================

``addmultisigaddress nrequired ["key",...] ( "label" "address_type" )``

Add an nrequired-to-sign multisignature address to the wallet. Requires a new wallet backup.

Each key is a hivecoin address or hex-encoded public key.

This functionality is only intended for use with non-watchonly addresses.

See `importaddress` for watchonly p2sh address support.

If 'label' is specified, assign address to that label.

Argument #1 - nrequired
~~~~~~~~~~~~~~~~~~~~~~~

**Type:** numeric, required

The number of required signatures out of the n keys or addresses.

Argument #2 - keys
~~~~~~~~~~~~~~~~~~

**Type:** json array, required

The hivecoin addresses or hex-encoded public keys

::

     [
       "key",      (string) hivecoin address or hex-encoded public key
       ...
     ]

Argument #3 - label
~~~~~~~~~~~~~~~~~~~

**Type:** string, optional

A label to assign the addresses to.

Argument #4 - address_type
~~~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, optional, default=set by -addresstype

The address type to use. Options are "legacy", "p2sh-segwit", and "bech32".

Result
~~~~~~

::

  {                            (json object)
    "address" : "str",         (string) The value of the new multisig address
    "redeemScript" : "hex",    (string) The string value of the hex-encoded redemption script
    "descriptor" : "str"       (string) The descriptor for this multisig
  }

Examples
~~~~~~~~


.. highlight:: shell

Add a multisig address from 2 addresses::

  hive-cli addmultisigaddress 2 "[\"H7jq09vm5lfy0j5reeulh4x5752q25uqqvz34hufdl\",\"H7jq02ad21edsxd23d32dfgqqsz4vv4nmtfzuklhy3\"]"

As a JSON-RPC call::

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id": "curltest", "method": "addmultisigaddress", "params": [2, "[\"H7jq09vm5lfy0j5reeulh4x5752q25uqqvz34hufdl\",\"H7jq02ad21edsxd23d32dfgqqsz4vv4nmtfzuklhy3\"]"]}' -H 'content-type: text/plain;' http://127.0.0.1:9766/

