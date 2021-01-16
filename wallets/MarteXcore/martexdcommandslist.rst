MarteX Core Daemon version v4.0.4.3-cbee601-dirty

Usage:
  martexd [options]                     Start MarteX Core Daemon

Options:

  -?
       Print this help message and exit

  -version
       Print version and exit

  -alerts
       Receive and display P2P network alerts (default: 1)

  -alertnotify=<cmd>
       Execute command when a relevant alert is received or we see a really
       long fork (%s in cmd is replaced by message)

  -blocknotify=<cmd>
       Execute command when the best block changes (%s in cmd is replaced by
       block hash)

  -assumevalid=<hex>
       If this block is in the chain assume that it and its ancestors are valid
       and potentially skip their script verification (0 to verify all,
       default:
       1e4c89904d231fbb61c9d35a8730ca1055fa39c872d8913a6e29d5c92b82268d,
       testnet:
       8ad40d557632ce92ac361c5c8407a2364431c94167e52e9f4f23d09b0161e379)

  -conf=<file>
       Specify configuration file (default: MarteX.conf)

  -daemon
       Run in the background as a daemon and accept commands

  -datadir=<dir>
       Specify data directory

  -dbcache=<n>
       Set database cache size in megabytes (4 to 16384, default: 300)

  -loadblock=<file>
       Imports blocks from external blk000??.dat file on startup

  -maxorphantx=<n>
       Keep at most <n> unconnectable transactions in memory (default: 100)

  -maxmempool=<n>
       Keep the transaction memory pool below <n> megabytes (default: 300)

  -mempoolexpiry=<n>
       Do not keep transactions in the mempool longer than <n> hours (default:
       75)

  -blockreconstructionextratxn=<n>
       Extra transactions to keep in memory for compact block reconstructions
       (default: 100)

  -par=<n>
       Set the number of script verification threads (-2 to 16, 0 = auto, <0 =
       leave that many cores free, default: 0)

  -pid=<file>
       Specify pid file (default: martexd.pid)

  -prune=<n>
       Reduce storage requirements by enabling pruning (deleting) of old
       blocks. This allows the pruneblockchain RPC to be called to
       delete specific blocks, and enables automatic pruning of old
       blocks if a target size in MiB is provided. This mode is
       incompatible with -txindex and -rescan. Warning: Reverting this
       setting requires re-downloading the entire blockchain. (default:
       0 = disable pruning blocks, 1 = allow manual pruning via RPC,
       >945 = automatically prune block files to stay under the
       specified target size in MiB)

  -reindex-chainstate
       Rebuild chain state from the currently indexed blocks

  -reindex
       Rebuild chain state and block index from the blk*.dat files on disk

  -sysperms
       Create new files with system default permissions, instead of umask 077
       (only effective with disabled wallet functionality)

  -txindex
       Maintain a full transaction index, used by the getrawtransaction rpc
       call (default: 1)

  -addressindex
       Maintain a full address index, used to query for the balance, txids and
       unspent outputs for addresses (default: 0)

  -timestampindex
       Maintain a timestamp index for block hashes, used to query blocks hashes
       by a range of timestamps (default: 0)

  -spentindex
       Maintain a full spent index, used to query the spending txid and input
       index for an outpoint (default: 0)

Connection options:

  -addnode=<ip>
       Add a node to connect to and attempt to keep the connection open

  -allowprivatenet
       Allow RFC1918 addresses to be relayed and connected to (default: 0)

  -banscore=<n>
       Threshold for disconnecting misbehaving peers (default: 100)

  -bantime=<n>
       Number of seconds to keep misbehaving peers from reconnecting (default:
       86400)

  -bind=<addr>
       Bind to given address and always listen on it. Use [host]:port notation
       for IPv6

  -connect=<ip>
       Connect only to the specified node(s); -noconnect or -connect=0 alone to
       disable automatic connections

  -discover
       Discover own IP addresses (default: 1 when listening and no -externalip
       or -proxy)

  -dns
       Allow DNS lookups for -addnode, -seednode and -connect (default: 1)

  -dnsseed
       Query for peer addresses via DNS lookup, if low on addresses (default: 1
       unless -connect/-noconnect)

  -externalip=<ip>
       Specify your own public address

  -forcednsseed
       Always query for peer addresses via DNS lookup (default: 0)

  -listen
       Accept connections from outside (default: 1 if no -proxy or
       -connect/-noconnect)

  -listenonion
       Automatically create Tor hidden service (default: 1)

  -maxconnections=<n>
       Maintain at most <n> connections to peers (temporary service connections
       excluded) (default: 125)

  -maxreceivebuffer=<n>
       Maximum per-connection receive buffer, <n>*1000 bytes (default: 5000)

  -maxsendbuffer=<n>
       Maximum per-connection send buffer, <n>*1000 bytes (default: 1000)

  -maxtimeadjustment
       Maximum allowed median peer time offset adjustment. Local perspective of
       time may be influenced by peers forward or backward by this
       amount. (default: 4200 seconds)

  -onion=<ip:port>
       Use separate SOCKS5 proxy to reach peers via Tor hidden services
       (default: -proxy)

  -onlynet=<net>
       Only connect to nodes in network <net> (ipv4, ipv6 or onion)

  -permitbaremultisig
       Relay non-P2SH multisig (default: 1)

  -peerbloomfilters
       Support filtering of blocks and transaction with bloom filters (default:
       1)

  -port=<port>
       Listen for connections on <port> (default: 51315 or testnet: 41315)

  -proxy=<ip:port>
       Connect through SOCKS5 proxy

  -proxyrandomize
       Randomize credentials for every proxy connection. This enables Tor
       stream isolation (default: 1)

  -seednode=<ip>
       Connect to a node to retrieve peer addresses, and disconnect

  -timeout=<n>
       Specify connection timeout in milliseconds (minimum: 1, default: 5000)

  -torcontrol=<ip>:<port>
       Tor control port to use if onion listening enabled (default:
       127.0.0.1:9051)

  -torpassword=<pass>
       Tor control port password (default: empty)

  -upnp
       Use UPnP to map the listening port (default: 0)

  -whitebind=<addr>
       Bind to given address and whitelist peers connecting to it. Use
       [host]:port notation for IPv6

  -whitelist=<IP address or network>
       Whitelist peers connecting from the given IP address (e.g. 1.2.3.4) or
       CIDR notated network (e.g. 1.2.3.0/24). Can be specified multiple
       times. Whitelisted peers cannot be DoS banned and their
       transactions are always relayed, even if they are already in the
       mempool, useful e.g. for a gateway

  -whitelistrelay
       Accept relayed transactions received from whitelisted peers even when
       not relaying transactions (default: 1)

  -whitelistforcerelay
       Force relay of transactions from whitelisted peers even if they violate
       local relay policy (default: 1)

  -maxuploadtarget=<n>
       Tries to keep outbound traffic under the given target (in MiB per 24h),
       0 = no limit (default: 0)

Wallet options:

  -disablewallet
       Do not load the wallet and disable wallet RPC calls

  -keypool=<n>
       Set key pool size to <n> (default: 100)

  -fallbackfee=<amt>
       A fee rate (in MXT/kB) that will be used when fee estimation has
       insufficient data (default: 0.00001)

  -mintxfee=<amt>
       Fees (in MXT/kB) smaller than this are considered zero fee for
       transaction creation (default: 0.00001)

  -paytxfee=<amt>
       Fee (in MXT/kB) to add to transactions you send (default: 0.00001)

  -rescan
       Rescan the block chain for missing wallet transactions on startup

  -salvagewallet
       Attempt to recover private keys from a corrupt wallet on startup

  -spendzeroconfchange
       Spend unconfirmed change when sending transactions (default: 1)

  -txconfirmtarget=<n>
       If paytxfee is not set, include enough fee so transactions begin
       confirmation on average within n blocks (default: 6)

  -usehd
       Use hierarchical deterministic key generation (HD) after BIP39/BIP44.
       Only has effect during wallet creation/first start (default: 1)

  -mnemonic
       User defined mnemonic for HD wallet (bip39). Only has effect during
       wallet creation/first start (default: randomly generated)

  -mnemonicpassphrase
       User defined mnemonic passphrase for HD wallet (BIP39). Only has effect
       during wallet creation/first start (default: empty string)

  -hdseed
       User defined seed for HD wallet (should be in hex). Only has effect
       during wallet creation/first start (default: randomly generated)

  -upgradewallet
       Upgrade wallet to latest format on startup

  -wallet=<file>
       Specify wallet file (within data directory) (default: wallet.dat)

  -walletbroadcast
       Make the wallet broadcast transactions (default: 1)

  -walletnotify=<cmd>
       Execute command when a wallet transaction changes (%s in cmd is replaced
       by TxID)

  -zapwallettxes=<mode>
       Delete all wallet transactions and only recover those parts of the
       blockchain through -rescan on startup (1 = keep tx meta data e.g.
       account owner and payment request information, 2 = drop tx meta
       data)

  -createwalletbackups=<n>
       Number of automatic wallet backups (default: 10)

  -walletbackupsdir=<dir>
       Specify full path to directory for automatic wallet backups (must exist)

  -keepass
       Use KeePass 2 integration using KeePassHttp plugin (default: 0)

  -keepassport=<port>
       Connect to KeePassHttp on port <port> (default: 19455)

  -keepasskey=<key>
       KeePassHttp key for AES encrypted communication with KeePass

  -keepassid=<name>
       KeePassHttp id for the established association

  -keepassname=<name>
       Name to construct url for KeePass entry that stores the wallet
       passphrase

ZeroMQ notification options:

  -zmqpubhashblock=<address>
       Enable publish hash block in <address>

  -zmqpubhashtx=<address>
       Enable publish hash transaction in <address>

  -zmqpubhashtxlock=<address>
       Enable publish hash transaction (locked via FastSend) in <address>

  -zmqpubrawblock=<address>
       Enable publish raw block in <address>

  -zmqpubrawtx=<address>
       Enable publish raw transaction in <address>

  -zmqpubrawtxlock=<address>
       Enable publish raw transaction (locked via FastSend) in <address>

Debugging/Testing options:

  -uacomment=<cmt>
       Append comment to the user agent string

  -debug=<category>
       Output debugging information (default: 0, supplying <category> is
       optional). If <category> is not supplied or if <category> = 1,
       output all debugging information.<category> can be: addrman,
       alert, bench, cmpctblock, coindb, db, http, leveldb, libevent,
       lock, mempool, mempoolrej, net, proxy, prune, rand, reindex, rpc,
       selectcoins, tor, zmq, martex (or specifically: gobject,
       fastsend, keepass, masternode, mnpayments, mnsync, anonsend,
       spork).

  -help-debug
       Show all debugging options (usage: --help -help-debug)

  -logips
       Include IP addresses in debug output (default: 0)

  -logtimestamps
       Prepend debug output with timestamp (default: 1)

  -minrelaytxfee=<amt>
       Fees (in MXT/kB) smaller than this are considered zero fee for relaying,
       mining and transaction creation (default: 0.00001)

  -maxtxfee=<amt>
       Maximum total fees (in MXT) to use in a single wallet transaction or raw
       transaction; setting this too low may abort large transactions
       (default: 0.20)

  -printtoconsole
       Send trace/debug info to console instead of debug.log file

  -printtodebuglog
       Send trace/debug info to debug.log file (default: 1)

  -shrinkdebugfile
       Shrink debug.log file on client startup (default: 1 when no -debug)

Chain selection options:

  -testnet
       Use the test chain

  -devnet=<name>
       Use devnet chain with provided name

  -litemode=<n>
       Disable all MarteX specific functionality (Masternodes, AnonSend,
       FastSend, Governance) (0-1, default: 0)

  -sporkaddr=<hex>
       Override spork address. Only useful for regtest and devnet. Using this
       on mainnet or testnet will ban you.

Masternode options:

  -masternode=<n>
       Enable the client to act as a masternode (0-1, default: 0)

  -mnconf=<file>
       Specify masternode configuration file (default: masternode.conf)

  -mnconflock=<n>
       Lock masternodes from masternode configuration file (default: 1)

  -masternodeprivkey=<n>
       Set the masternode private key

AnonSend options:

  -enableanonsend=<n>
       Enable use of automated AnonSend for funds stored in this wallet (0-1,
       default: 0)

  -anonsendmultisession=<n>
       Enable multiple AnonSend mixing sessions per block, experimental (0-1,
       default: 0)

  -anonsendrounds=<n>
       Use N separate masternodes for each denominated input to mix funds
       (2-16, default: 2)

  -anonsendamount=<n>
       Keep N MXT anonymized (2-21000000, default: 1000)

  -liquidityprovider=<n>
       Provide liquidity to AnonSend by infrequently mixing coins on a
       continual basis (0-100, default: 0, 1=very frequent, high fees,
       100=very infrequent, low fees)

FastSend options:

  -enablefastsend=<n>
       Enable FastSend, show confirmations for locked transactions (0-1,
       default: 1)

  -fastsenddepth=<n>
       Show N confirmations for a successfully locked transaction (0-60,
       default: 10)

  -fastsendnotify=<cmd>
       Execute command when a wallet FastSend transaction is successfully
       locked (%s in cmd is replaced by TxID)

Node relay options:

  -bytespersigop
       Minimum bytes per sigop in transactions we relay and mine (default: 20)

  -datacarrier
       Relay and mine data carrier transactions (default: 1)

  -datacarriersize
       Maximum size of data in data carrier transactions we relay and mine
       (default: 120)

  -mempoolreplacement
       Enable transaction replacement in the memory pool (default: 0)

Block creation options:

  -blockmaxsize=<n>
       Set maximum block size in bytes (default: 2000000)

  -blockprioritysize=<n>
       Set maximum size of high-priority/low-fee transactions in bytes
       (default: 10000)

  -blockmintxfee=<amt>
       Set lowest fee rate (in MXT/kB) for transactions to be included in block
       creation. (default: 0.00001)

RPC server options:

  -server
       Accept command line and JSON-RPC commands

  -rest
       Accept public REST requests (default: 0)

  -rpcbind=<addr>
       Bind to given address to listen for JSON-RPC connections. Use
       [host]:port notation for IPv6. This option can be specified
       multiple times (default: bind to all interfaces)

  -rpccookiefile=<loc>
       Location of the auth cookie (default: data dir)

  -rpcuser=<user>
       Username for JSON-RPC connections

  -rpcpassword=<pw>
       Password for JSON-RPC connections

  -rpcauth=<userpw>
       Username and hashed password for JSON-RPC connections. The field
       <userpw> comes in the format: <USERNAME>:<SALT>$<HASH>. A
       canonical python script is included in share/rpcuser. The client
       then connects normally using the
       rpcuser=<USERNAME>/rpcpassword=<PASSWORD> pair of arguments. This
       option can be specified multiple times

  -rpcport=<port>
       Listen for JSON-RPC connections on <port> (default: 51314 or testnet:
       41314)

  -rpcallowip=<ip>
       Allow JSON-RPC connections from specified source. Valid for <ip> are a
       single IP (e.g. 1.2.3.4), a network/netmask (e.g.
       1.2.3.4/255.255.255.0) or a network/CIDR (e.g. 1.2.3.4/24). This
       option can be specified multiple times

  -rpcthreads=<n>
       Set the number of threads to service RPC calls (default: 4)