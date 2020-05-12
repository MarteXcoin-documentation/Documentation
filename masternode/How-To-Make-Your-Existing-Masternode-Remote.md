## Steps to do
### Fist method
Just dump you masternode wallet: using `dumpwallet "filename"`
Download to you computer.
Use the follow command to download your wallet from your VPS:
`scp user_name@your_vps_ip:/your_file_path local_file_path`
Then import to your local wallet using the Debug Console in the Tab Console.
Then use the follow commands: `importwallet file_path` or `importwallet "file_path"`
### Second method
Import your masternode wallet and masternode private key.
To do that, do on your wallet VPS: `dumpprivkey "address"`
Copy the privkey and import in you local wallet: `importprivkey "martexprivkey" ( "label" ) ( rescan )`
## On local wallet
After that, close your local wallet.
Go to your wallet folder.
Edit your masternode.conf located at the following link [data folder](https://github.com/MarteXcoin-documentation/Documentation/blob/master/commands/cmd-rpc.rst#arguments-and-commands) and put as showed in the example (**SINGLE SPACED SINGLE LINE** ):
>*MN_ALIAS REMOTE_MN_IP:51315 MASTERNODE_PRIVKEY TRANSACTION_HASH INDEX*

After that, reopen your wallet and active Masternode Tab in Setting> Options> Wallet
