<img src="https://github.com/carebitcoin/carebit-brand/blob/master/assets_raster/logotypes/L3H_text_light_alpha_500x188.png" alt="Carebit logo" width=350px >

# Carebit Masternode Setup Guide (Ubuntu 16.04)
This guide will assist you in setting up a Carebit Masternode on a Linux Server running Ubuntu 16.04. (Use at your own risk)

If you require further assistance contact the support team @ [Discord](https://discord.gg/BBBms9Z)
***
## Requirements
1. **120000 Carebit coins.**
2. **A Vultr VPS running Linux Ubuntu 16.04.**
3. **A Windows local wallet.**
4. **An SSH client such as [Bitvise](https://dl.bitvise.com/BvSshClient-Inst.exe)**
***
## Contents
* **Section A**: Creating the VPS within [Vultr](https://www.vultr.com/?ref=7371462).
* **Section B**: Downloading and installing Bitvise.
* **Section C**: Connecting to the VPS and installing the MN script via Bitvise.
* **Section D**: Preparing the local wallet.
* **Section E**: Connecting & Starting the masternode.
***

## Section A: Creating the VPS within [Vultr](https://www.vultr.com/?ref=7371462)
***Step 1***
* Register at [Vultr](https://www.vultr.com/?ref=7371462)
***

***Step 2***
* After you have added funds to your account go [here](https://my.vultr.com/deploy/) to create your Server
***

***Step 3***
* Choose a server location (preferably somewhere close to you)
![Example-Location](https://i.imgur.com/ozi7Bkr.png)
***

***Step 4***
* Choose a server type: Ubuntu 16.04
![Example-OS](https://i.imgur.com/aSMqHUK.png)
***

***Step 5***
* Choose a server size: $5/mo will be fine
![Example-OS](https://i.imgur.com/UoGoHcM.png)
***

***Step 6***
* Set a Server Hostname & Label (name it whatever you want)
![Example-hostname](https://i.imgur.com/NtualgA.png)
***

***Step 7***
* Click "Deploy now"

![Example-Deploy](https://i.imgur.com/4qpYuH0.png)
***


## Section B: Downloading and installing BitVise.

***Step 1***
* Download Bitvise [here](https://dl.bitvise.com/BvSshClient-Inst.exe)
***

***Step 2***
* Select the correct installer depending upon your operating system. Then follow the install instructions.

![Example-PuttyInstaller](https://i.imgur.com/yF3694G.png)
***


## Section C: Connecting to the VPS & Installing the MN script via Bitvise.

***Step 1***
* Copy your VPS IP (you can find this by going to the server tab within Vultr and clicking on your server.
![Example-Vultr](https://i.imgur.com/spEVVCy.png)
***

***Step 2***
* Open the bitvise application and fill in the "Hostname" box with the IP of your VPS then click "Open"
![Example-PuttyInstaller](https://i.imgur.com/vkN1alC.png)
***

***Step 3***
* Once you have clicked open it will open a security alert (click yes).  
***


***Step 4***
* Type "root" as the login/username then press enter

![Example-Root](https://i.imgur.com/11GMkvA.png)
***

***Step 5***
* Copy the root password from the VULTR server page.
![Example-RootPass](https://i.imgur.com/JnXQXav.png)

***


***Step 6***
* Paste the password into the Bitvise terminal by right clicking (it will not show the password so just press enter)
![Example-RootPassEnter](https://i.imgur.com/34Qky1K.png)
***

***Step 7***
* Paste the code below into the Bitvise terminal then press enter (it will just go to a new line)

`wget -q https://github.com/carebitcoin/carebitcoin/raw/master/doc/masternode-install.sh`
***

***Step 8***
* Paste the code below into the Bitvise terminal then press enter

`bash masternode-install.sh`

![Example-Bash](https://i.imgur.com/YIz5dA6.png)

***

***Step 9***
* Sit back and wait for the install (this will take a couple of minutes)
***

***Step 10***
* When prompted to enter your Gen key - press enter

![Example-installing](https://i.imgur.com/sLvWd1S.png)
***

***Step 11***
* You will now see all of the relevant information for your server.
* Keep this terminal open as we will need the info for the wallet setup.
![Example-installing](https://i.imgur.com/Q87LcnW.png)
***

## Section D: Preparing the Local wallet

***Step 1***
* Download and install on the local PC / mac the Carebit wallet from [here](https://github.com/carebitcoin/carebitcoin/releases/latest)
***

***Step 2***
* Send EXACTLY 120000 CARE to a receive address within your wallet.
***

***Step 3***
* Create a text document to temporarily store information that you will need.
***

***step 4***
* Go to the console within the wallet

![Example-console](https://i.imgur.com/Z0a8dVy.png)
***

***Step 5***
* Type the command below and press enter

`masternode outputs`

![Example-outputs](https://i.imgur.com/iCvrPrb.png)
***

***Step 6***
* Copy the long key (this is your transaction ID) and the 0 or 1 at the end (this is your output index)
* Paste these into the text document you created earlier as you will need them in the next step.
***

# Section E: Connecting & Starting the masternode

***Step 1***
* Go to the tools tab within the wallet and click "Open Masternode Configuration File"
![Example-create](https://i.imgur.com/NSn9ffU.png)
***

***Step 2***

* Fill in the form.
* For `Alias` type something like "MN01" **don't use spaces**
* The `Address` is the IP and port of your server (this will be in the Bitvise terminal that you still have open); make sure the port is set to **9192**.
* The `Genkey` is your masternode Gen key output (this is also in the Bitvise terminal that you have open).
* The `TxHash` is the transaction ID/long key that you copied to the text file.
* The `Output Index` is the 0 or 1 that you copied to your text file.
![Example-create](https://i.imgur.com/9b1I3bk.png)

Click "File Save"
***

***Step 3***
* Close out of the wallet and reopen Wallet
*Click on the Masternodes tab "My masternodes"
* Click start all in the masternodes tab
***

***step 4***
* Check the status of your masternode within the VPS by using the command below:

`carebitcoin-cli masternode status`

*You should see ***status 4***

If you do, congratulations! You have now setup a masternode. If you do not, please contact [support](https://discord.gg/BBBms9Z) and they will assist you.  
***

## Donations:  

Any donation is highly appreciated.  

**CARE**: CZBLWnbbadvezDLe5BfuBSyRht53xqCkzF  
**BTC**: 14tDjF852mSwBTwJU9sbAquw66aUFuNptu  
**LTC**: LLekStTMGcPYTGifNzQkhpA4s1jzm86X34  
