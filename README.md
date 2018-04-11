# Hera
Shell script to install a [Hera Masternode](https://www.hera-coin.com/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
```
wget -q https://raw.githubusercontent.com/zoldur/Hera/master/hera_install.sh
bash hera_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Hera Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **6000** HER to **MN1**. You need to send all 6000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
11. Close and open the wallet again.
12. Go to **Masternodes** -> **My Master Nodes** tab
13. If you don't see your masternode, click **Update**
14. Unlock your wallet if it is encrypted
15. Select your masternode and click on **Start**
16. Login to your VPS and check your masternode status by running the following command. If you get **Status 9**, it means your masternode is active.
```
Herad masternode status
```
***

## Usage:
```
Herad masternode status  
Herad getinfo
```
Also, if you want to check/start/stop **Hera**, run one of the following commands as **root**:

```
systemctl status Hera #To check if Hera service is running  
systemctl start Hera #To start Hera service  
systemctl stop Hera #To stop Hera service  
systemctl is-enabled Hera #To check if Hera service is enabled on boot  
```  
***

## Donations

Any donation is highly appreciated

**HER**: HDCWtQjXN89TexQ2VeVo3AqGiTXdDonDza  
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E  
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB  
