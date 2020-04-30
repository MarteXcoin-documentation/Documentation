Category | Command | Description
-|-|-
== MarteX ==
MarteX | anonsend "command" | Starts the process of sending coins anonymously. Available commands: start (Start mixing); stop (Stop mixing); reset (Reset mixing).
MarteX | getgovernanceinfo | Returns an object containing governance parameters.
MarteX | getpoolinfo | Returns an object containing mixing pool related information.
MarteX | getsuperblockbudget index | Returns the absolute maximum sum of superblock payments allowed.
MarteX | gobject "command"...|
MarteX | masternode "command"... | Displays various commands from the masternode function.
MarteX | masternodebroadcast "command"... |
MarteX | masternodelist ( "mode" "filter" ) |
MarteX | mnsync [status|next|reset] |
MarteX | sentinelping version |
MarteX | spork "command" | Shows information about current state of sporks. Available commands: 

    show
        Show all current spork values
    active
        Show which sporks are active


MarteX | voteraw <masternode-tx-hash> <masternode-tx-index> <governance-hash> <vote-signal> [yes|no|abstain] <time> <vote-sig> | Compile and relay a governance vote with provided external signature instead of signing vote internally

== Addressindex ==
Addressindex | getaddressbalance | Returns the balance for an address(es) (requires addressindex to be enabled).
Addressindex | getaddressdeltas | Returns all changes for an address (requires addressindex to be enabled).
Addressindex | getaddressmempool | Returns all mempool deltas for an address (requires addressindex to be enabled).
Addressindex | getaddresstxids | Returns the txids for an address(es) (requires addressindex to be enabled).
Addressindex | getaddressutxos | Returns all unspent outputs for an address (requires addressindex to be enabled).

== Blockchain ==
Blockchain | getbestblockhash | Returns the hash of the best (tip) block in the longest block chain.
Blockchain | getblock "blockhash" ( verbose ) | Shows all the information of the inserted block hash.
Blockchain | getblockchaininfo | Returns an object containing various state info regarding blockchain processing.
Blockchain | getblockcount | Displays the number of existing blocks on the blockchain.
Blockchain | getblockhash height | Displays the reported hash block.
Blockchain | getblockhashes timestamp | Returns array of hashes of blocks within the timestamp range provided.
Blockchain | getblockheader "hash" ( verbose ) | If verbose is false, returns a string that is serialized, hex-encoded data for blockheader 'hash'. If verbose is true, returns an Object with information about blockheader <hash>.
Blockchain | getblockheaders "hash" ( count verbose ) | Returns an array of items with information about <count> blockheaders starting from <hash>. If verbose is false, each item is a string that is serialized, hex-encoded data for a single blockheader. If verbose is true, each item is an Object with information about a single blockheader.
Blockchain | getchaintips ( count branchlen ) | Return information about all known tips in the block tree, including the main chain as well as orphaned branches.

getdifficulty
getmempoolancestors txid (verbose)
getmempooldescendants txid (verbose)
getmempoolentry txid
getmempoolinfo
getrawmempool ( verbose )
getspentinfo
gettxout "txid" n ( include_mempool )
gettxoutproof ["txid",...] ( blockhash )
gettxoutsetinfo
preciousblock "blockhash"
pruneblockchain
verifychain ( checklevel nblocks )
verifytxoutproof "proof"

== Control ==
debug ( 0|1|addrman|alert|bench|coindb|db|lock|rand|rpc|selectcoins|mempool|mempoolrej|net|proxy|prune|http|libevent|tor|zmq|martex|anonsend|fastsend|masternode|spork|keepass|mnpayments|gobject )
Control | getinfo | It exposes all relevant Node information.
getmemoryinfo
Control | help ( "command" ) | Show all commands list. (List commands, or get help for a command.)
Control | stop | Closes the MarteX wallet.

== Generating ==
generate nblocks ( maxtries )
generatetoaddress nblocks address (maxtries)

== Mining ==
Mining  | getblocktemplate ( TemplateRequest ) | Returns data needed to construct a block to work on.
getmininginfo
getnetworkhashps ( nblocks height )
getstakinginfo
prioritisetransaction <txid> <priority delta> <fee delta>
submitblock "hexdata" ( "jsonparametersobject" )

== Network ==
Network | addnode "node" "add|remove|onetry" | Attempts add or remove <node> from the addnode list or try a connection to <node> once.
Network | clearbanned | 
disconnectnode "address" 
getaddednodeinfo ( "node" )
getconnectioncount
getnettotals
getnetworkinfo
getpeerinfo
listbanned
Network | ping | Ping the peers you are connected to.
setban "subnet" "add|remove" (bantime) (absolute)
setnetworkactive true|false

== Rawtransactions ==
createrawtransaction [{"txid":"id","vout":n},...] {"address":amount,"data":"hex",...} ( locktime )
decoderawtransaction "hexstring"
decodescript "hexstring"
fundrawtransaction "hexstring" ( options )
getrawtransaction "txid" ( verbose )
sendrawtransaction "hexstring" ( allowhighfees fastsend bypasslimits)
signrawtransaction "hexstring" ( [{"txid":"id","vout":n,"scriptPubKey":"hex","redeemScript":"hex"},...] ["privatekey1",...] sighashtype )

== Util ==
createmultisig nrequired ["key",...]
estimatefee nblocks
estimatepriority nblocks
estimatesmartfee nblocks
estimatesmartpriority nblocks
signmessagewithprivkey "privkey" "message"
validateaddress "address"
verifymessage "address" "signature" "message"

== Wallet ==
Wallet | abandontransaction "txid" | Mark in-wallet transaction <txid> as abandoned. This will mark this transaction and all its in-wallet descendants as abandoned which will allow for their inputs to be respent.
addmultisigaddress nrequired ["key",...] ( "account" )
backupwallet "destination"
Wallet | checkwallet | Checks the integrity of the wallet.
dumphdinfo
Wallet | dumpprivkey "address" | Shows the private key of the entered Martex public address.
Wallet | dumpwallet "filename" | Exports all wallet private keys to file.
encryptwallet "passphrase"
fastsendtoaddress "address" amount ( "comment" "comment-to" subtractfeefromamount )
Wallet | getaccount "address" | Returns the account associated with the given address.
Wallet | getaccountaddress "account" | Returns the current bitcoin address for receiving payments to this account. If <account> does not exist, it will be created along with an associated new address that will be returned.
Wallet | getaddressesbyaccount "account" | Returns the list of addresses for the given account.
Wallet | getbalance ( "account" minconf addlockconf include_watchonly ) | If [account] is not specified, returns the server's total available balance.<br/>If [account] is specified, returns the balance in the account.
Wallet | getnewaddress ( "account" ) | Returns a new MarteXcoin address for receiving payments. If [account] is specified payments received with the address will be credited to [account].
getrawchangeaddress
Wallet | getreceivedbyaccount "account" ( minconf addlockconf ) | Returns the total amount received by addresses with [account] in transactions with at least [minconf] confirmations. If [account] not provided return will include all transactions to all accounts.
Wallet | getreceivedbyaddress "address" ( minconf addlockconf ) | Returns the amount received by <MartexCoin naddress> in transactions with at least [minconf] confirmations. It correctly handles the case where someone has sent to the address in multiple transactions. Keep in mind that addresses are only ever used for receiving transactions. Works only for addresses in the local wallet, external addresses will always show 0.
gettransaction "txid" ( include_watchonly )
getunconfirmedbalance
getwalletinfo
importaddress "address" ( "label" rescan p2sh )
importelectrumwallet "filename" index
importmulti "requests" "options"
Wallet | importprivkey "martexprivkey" ( "label" ) ( rescan ) | Adds a private key (as returned by dumpprivkey) to your wallet. This may take a while, as a rescan is done, looking for existing transactions. Optional [rescan] parameter added in . Note: There's no need to import public key, as in ECDSA (unlike RSA) this can be computed from private key.
importprunedfunds
importpubkey "pubkey" ( "label" rescan )
Wallet | importwallet "filename" | Imports a wallet from a file.
keepass <genkey|init|setpassphrase>
keypoolrefill ( newsize )
Wallet | listaccounts ( minconf addlockconf include_watchonly) | Returns Object that has account names as keys, account balances as values.
listaddressbalances ( minamount )
listaddressgroupings
listlockunspent
listreceivedbyaccount ( minconf addlockconf include_empty include_watchonly)
listreceivedbyaddress ( minconf addlockconf include_empty include_watchonly)
listsinceblock ( "blockhash" target_confirmations include_watchonly)
listtransactions ( "account" count skip include_watchonly)
listunspent ( minconf maxconf  ["addresses",...] [include_unsafe] )
lockunspent unlock ([{"txid":"txid","vout":n},...])
move "fromaccount" "toaccount" amount ( minconf "comment" )
removeprunedfunds "txid"
Wallet | repairwallet | Repairs the wallet and returns the value in boolean (true or false).
sendfrom "fromaccount" "toaddress" amount ( minconf addlockconf "comment" "comment_to" )
sendmany "fromaccount" {"address":amount,...} ( minconf addlockconf "comment" ["address",...] subtractfeefromamount use_is use_ps )
sendtoaddress "address" amount ( "comment" "comment_to" subtractfeefromamount use_is use_ps )
setaccount "address" "account"
settxfee amount
signmessage "address" "message"
