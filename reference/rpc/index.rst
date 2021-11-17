.. This file is licensed under the Apache License 2.0 available on
   http://www.apache.org/licenses/.

RPC API Reference
=================

Addressindex RPCs
-----------------

.. toctree::
  :maxdepth: 1
  :caption: Contents:

  getaddressbalance
  getaddressdeltas
  getaddressmempool
  getaddresstxids
  getaddressutxos

Assets RPCs
-----------

.. toctree::
  :maxdepth: 1
  :caption: Contents:

  getassetdata
  getcacheinfo 
  getsnapshot
  issue
  issueunique
  listassets
  listmyassets
  purgesnapshot
  reissue 
  transfer
  transferfromaddress
  transferfromaddresses

Blockchain RPCs
---------------

.. toctree::
  :maxdepth: 1
  :caption: Contents:

  clearmempool
  decodeblock
  getbestblockhash
  getblock
  getblockchaininfo
  getblockcount
  getblockhash
  getblockhashes
  getblockheader
  getchaintips
  getchaintxstats
  getdifficulty
  getmempoolancestors
  getmempooldescendants
  getmempoolentry
  getmempoolinfo
  getrawmempool
  getspentinfo
  gettxout
  gettxoutproof
  gettxoutsetinfo
  preciousblock
  pruneblockchain
  savemempool
  verifychain
  verifytxoutproof

Control RPCs
------------

.. toctree::
  :maxdepth: 1

  getinfo
  getmemoryinfo
  getrpcinfo
  help
  stop
  uptime

Generating RPCs
---------------

.. toctree::
  :maxdepth: 1
  
  generate
  generatetoaddress
  getgenerate
  setgenerate

Mining RPCs
-----------

.. toctree::
  :maxdepth: 1

  getblocktemplate
  getkawpowhash
  getmininginfo
  getnetworkhashps
  pprpcsb
  prioritisetransaction
  submitblock

Messages RPCs
-------------

.. toctree::
  :maxdepth: 1

  clearmessages 
  sendmessage
  subscribetochannel 
  unsubscribefromchannel 
  viewallmessagechannels 
  viewallmessages 

Network RPCs
------------

.. toctree::
  :maxdepth: 1

  addnode
  clearbanned
  disconnectnode
  getaddednodeinfo
  getconnectioncount
  getnettotals
  getnetworkinfo
  getpeerinfo
  listbanned
  ping
  setban
  setnetworkactive

Rawtransactions RPCs
--------------------

.. toctree::
  :maxdepth: 1

  combinerawtransaction
  createrawtransaction
  decoderawtransaction
  decodescript
  fundrawtransaction
  getrawtransaction
  sendrawtransaction
  signrawtransaction
  testmempoolaccept

Restricted assets RPCs
----------------------

.. toctree::
  :maxdepth: 1

  addtagtoaddress
  checkaddressrestriction
  checkaddresstag
  checkglobalrestriction
  freezeaddress
  freezerestrictedasset
  getverifierstring
  issuequalifierasset
  issuerestrictedasset
  isvalidverifierstring
  listaddressesfortag
  listaddressrestrictions
  listglobalrestrictions
  listtagsforaddress
  reissuerestrictedasset
  removetagfromaddress
  transferqualifier 
  unfreezeaddress
  unfreezerestrictedasset

Restricted RPCs
---------------

.. toctree::
  :maxdepth: 1

  viewmyrestrictedaddresses 
  viewmytaggedaddresses 

Rewards RPCs
------------

.. toctree::
  :maxdepth: 1

  cancelsnapshotrequest
  distributereward
  getdistributestatus
  getsnapshotrequest
  listsnapshotrequests
  requestsnapshot

Util RPCs
---------

.. toctree::
  :maxdepth: 1

  createmultisig
  estimatefee
  estimatesmartfee
  signmessagewithprivkey
  validateaddress
  verifymessage

Wallet RPCs
-----------

**Note:** the wallet RPCs are only available if hivecoin Core was built
with wallet support, which is the default.

.. toctree::
  :maxdepth: 1

  abandontransaction
  abortrescan
  addmultisigaddress
  addwitnessaddress
  backupwallet
  bumpfee
  dumpprivkey
  dumpwallet
  encryptwallet
  getaccount
  getaccountaddress
  getaddressesbyaccount
  getbalance
  getmasterkeyinfo
  getmywords
  getnewaddress
  getrawchangeaddress
  getreceivedbyaccount
  getreceivedbyaddress
  gettransaction
  getunconfirmedbalance
  getwalletinfo
  importaddress
  importmulti
  importprivkey
  importprunedfunds
  importpubkey
  importwallet
  keypoolrefill
  listaccounts
  listaddressgroupings
  listlockunspent
  listreceivedbyaccount
  listreceivedbyaddress
  listsinceblock
  listtransactions
  listunspent
  listwallets
  lockunspent
  removeprunedfunds
  rescanblockchain
  sendfrom
  sendfromaddress
  sendmany
  sendtoaddress
  settxfee
  signmessage
