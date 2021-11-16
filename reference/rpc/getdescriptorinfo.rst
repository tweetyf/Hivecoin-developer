.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

getdescriptorinfo
=================

``getdescriptorinfo "descriptor"``

Analyses a descriptor.

Argument #1 - descriptor
~~~~~~~~~~~~~~~~~~~~~~~~

**Type:** string, required

The descriptor.

Result
~~~~~~

::

  {                                   (json object)
    "descriptor" : "str",             (string) The descriptor in canonical form, without private keys
    "checksum" : "str",               (string) The checksum for the input descriptor
    "isrange" : true|false,           (boolean) Whether the descriptor is ranged
    "issolvable" : true|false,        (boolean) Whether the descriptor is solvable
    "hasprivatekeys" : true|false     (boolean) Whether the input descriptor contained at least one private key
  }

Examples
~~~~~~~~


.. highlight:: shell

Analyse a descriptor::

  hive-cli getdescriptorinfo "wpkh([d34db33f/84h/0h/0h]0279be667ef9dcbbac55a06295Ce870b07029Bfcdb2dce28d959f2815b16f81798)"

