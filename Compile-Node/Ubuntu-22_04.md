# COMPILE RADIANT NODE WITH UBUNTU 22.04
Small guide to compile the Radiant node and use its commands

#### GITHUB
- **Radiant node source code:** https://github.com/RadiantBlockchain/radiant-node
- **Original guide to compile in Ubuntu:** https://github.com/RadiantBlockchain/radiant-node/blob/master/doc/build-unix-deb.md
--------------------------------------------------------------------------------------------

**Necessary libraries and applications to compile the node**
```
sudo apt-get install build-essential cmake git libboost-chrono-dev libboost-filesystem-dev libboost-test-dev libboost-thread-dev libevent-dev libminiupnpc-dev libssl-dev libzmq3-dev help2man ninja-build python3 libdb-dev libdb++-dev
```

**Download radiant node source code to compile**
```
git clone https://github.com/radiantblockchain/radiant-node.git
```

**Once you have downloaded the source code, enter the generated folder, create the build folder and enter inside it**
```
cd radiant-node/
mkdir build
cd build
```
--------------------------------------------------------------------------------------------

**Two options to compile (QT does not work properly)**
- **No wallet, no QT >>>** `cmake -GNinja .. -DBUILD_RADIANT_WALLET=OFF -DBUILD_RADIANT_QT=OFF`
- **No QT >>>** `cmake -GNinja .. -DBUILD_RADIANT_QT=OFF`

--------------------------------------------------------------------------------------------

**Once everything is configured, proceed to compile with ninja and wait a few minutes.**
```
ninja
```

**The result will be generated in the src folder**
src/radiantd	
src/radiantd
src/radiant-cli
src/radiant-wallet


**To run the node from any location, we can copy the file to a system directory**
```
sudo cp src/radiant* /usr/local/bin/
```

--------------------------------------------------------------------------------------------

### **CREATE INITIAL CONFIGURATION FILE**
```
mkdir ~/.radiant
touch ~/.radiant/radiant.conf
```

**Copy main data to the configuration file**
```
cat > ~/.radiant/radiant.conf << EOL
rpcuser=$(cat /dev/urandom | tr -dc 'a-zA-Z0-9' | fold -w 12 | head -n 1)
rpcpassword=$(cat /dev/urandom | tr -dc 'a-zA-Z0-9' | fold -w 32 | head -n 1)

listen=1
server=1
daemon=1

maxconnections=16

EOL
```

--------------------------------------------------------------------------------------------

### **USEFUL COMMANDS**
- **START NODE:** `radiantd`
- **STOP NODE:** `radiant-cli stop`
- **NODE INFO:** `radiant-cli -getinfo`
- **NODE SYNCHRONISM:** `radiant-cli getblockchaininfo`
- **CONNECTIVITY:** `radiant-cli getnetworkinfo`
- **WALLET STATUS:** `radiant-cli getwalletinfo`
- **CREATE NEW ADDRESS:** `radiant-cli getnewaddress "Principal"`
- **GET PRIVATE ADDRESS KEY:**`radiant-cli dumpprivkey Direccion_Generada`
- **IMPORT PRIVATE KEY:** `radiant-cli importprivkey L1NLnbPQWaE3sDMedHgHy9q3wMjzZ2HCRAtgfQqfwXppAvnPBeit Test `
- **WALLET ADDRESSES:** `radiant-cli listreceivedbyaddress 1 true`
