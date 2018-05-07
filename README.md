# MASTERNODE TUTO
masternode setup Guide

# VPS 

wget -q https://raw.githubusercontent.com/zoldur/Ultranatum/master/ultranatum_install.sh
bash ultranatum_install.sh

# Desktop Wallet

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:

Open the Ultranatum Desktop Wallet.
Go to RECEIVE and create a New Address: MN1
Send 1000 ULTRA to MN1. You need to send all 1000 coins in one single transaction.
Wait for 15 confirmations.
Go to Help -> "Debug Window - Console"
Type the following command: masternode outputs
Go to Tools -> "Open Masternode Configuration File"
Add the following entry:
Alias Address Privkey TxHash TxIndex
Alias: MN1
Address: VPS_IP:PORT
Privkey: Masternode Private Key
TxHash: First value from Step 6
TxIndex: Second value from Step 6
Save and close the file.
Go to Masternode Tab. If you tab is not shown, please enable it from: Settings - Options - Wallet - Show Masternodes Tab
Click Update status to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
Select your MN and click Start Alias to start it.
Alternatively, open Debug Console and type:
masternode start-alias MN1
Login to your VPS and check your masternode status by running the following command:
ultranatum-cli masternode status
