PWR Chain Validator Node Setup Guide

Server Specifications
- Minimum Requirements:
  - 1 vCPU
  - 1GB RAM
  - 25GB Disk
  - Open TCP Ports: 8231, 8085
  - Open UDP Port: 7621

Installation Guide

1. Upgrade Software and Install Java
sudo apt update && sudo apt upgrade -y
sudo apt install openjdk-19-jre-headless

2. Install and Setup Your Validator Node
wget https://github.com/pwrlabs/PWR-Validator-Node/raw/main/validator.jar \
     https://github.com/pwrlabs/PWR-Validator-Node/raw/main/config.json
sudo nano password

3. Run Your Validator Node
nohup sudo java -jar validator.jar password <YOUR_SERVER_IP> --compression-level 0 &

Note: --compression-level ranges from 0 (no compression) to 9 (maximum compression).

Validator Address Setup
After setting up, get Validator Roles on Discord to claim your Faucet:
Join PWR Chain Discord: https://discord.gg/2Xq6XnmXu5

Additional Commands
Check your Node Private Key
java -jar validator.jar get-private-key password

Check your Validator Address
curl -sS http://<YOUR_SERVER_IP>:8085/address/

Check your Node Logs
sudo journalctl -u pwr -f

Restart your Node
sudo systemctl restart pwr && sudo journalctl -u pwr -f

PWR Chain Explorer
Monitor your node: https://explorer.pwrlabs.io/

Running an RPC Node Only

1. Upgrade Software and Install Java
sudo apt update && sudo apt upgrade -y
sudo apt install openjdk-19-jre-headless

2. Install and Setup Your RPC Node
wget https://github.com/pwrlabs/PWR-Validator-Node/raw/main/validator.jar \
     https://github.com/pwrlabs/PWR-Validator-Node/raw/main/rpc/config.json
nano config.json

3. Run Your RPC Node
nohup sudo java -jar validator.jar --rpc &

Validator Role Application Example
To apply for the Validator Role on Discord:
Dear PWR Teams,
I hope this ticket finds you well. I am writing to express my interest as a validator node operator at PWR Blockchain.
Details:
Name: saddope
Team: saddope | crypto 🗣
Blockchains: Rivalz AI, Sonaric AI, Initia, Chasm Node, Nubit BTC, Aligned Node, VOI, Nexus ZKEVM
How you heard of us: Telegram Channel
Thank you for considering my application.

Setup Your PWR Wallet

1. Download PWR Wallet Extension
Link: https://chromewebstore.google.com/u/3/detail/pwr-wallet/kennjipeijpeengjlogfdjkiiadhbmjl

2. Register a New Wallet
Save Your Phrase

3. Import Your Validator Account
- Go to "My Accounts"
- Click "Import Account"
- Set Wallet Name to "Validator"
- Paste Validator Private Key

4. Claim Your 1K PWR Faucet
Link: https://discord.com/channels/1141787507189624992/1142055910001352835
Note: Validator Roles required to claim Faucet.
