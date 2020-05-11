## Steps to do
### Fist method
Just dump you masternode wallet, download to you computer and import to you local wallet.
Use the follow command to download your wallet from your VPS:
`scp user_name@your_vps_ip:/your_file_path local_file_path`
Then import to your local wallet using the Debug Console in the Tab Console.
Then use the follow commands: `importwallet file_path` or `importwallet "file_path"`
### Second method
Import your masternode wallet and masternode private key.
To do that do on your VPS:
## On local wallet
After that, close your local wallet.
Go to your wallet folder.
Edit your masternode.conf located at the following link [data folder](https://github.com/MarteXcoin-documentation/Documentation/blob/master/commands/cmd-rpc.rst#arguments-and-commands)
