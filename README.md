# Hyperledger Blockchain (Supply Chain)
This is a distribted ledger implementation in Hyperledger Fabric. The ledger is of a **Pharma Supply Chain**. It includes three nodes (manufacturer, wholesaler, and pharmacy). A big thank you to O'Reilly media for the tutorial.

## Motivation
After Covid'19 many Supply Chains are suffering globally. Some of the major problems that I encountered while working on a project under my Professor were: 
1. ***Transaperency and Traceability:*** The lack of reliable, permanent records of assets as they move along the value chain undermines customer confidence in asset provenance.

2. ***Immutability:***   To build a transparent and reliable log of the journey of the product, the data once entered cannot be changed.

3. ***Authenticity:*** o avoid counterfeit markets, a unique identification must be provided to the components at different stages, so that consumers can make sure that their retailers are getting legitimate products from a certified dealer.

## Prerequisite
Before you begin, you should install all the prerequisites from [here](https://hyperledger-fabric.readthedocs.io/en/release-2.2/prereqs.html). 


## Getting started
Almost all the functionalities are coded in the respective `scripts` files. The commands will automatically change the enviriomental variable as per the requirements and will execute the code from the shell.

### Run

1. **Clone the repository**
```
//git commads
```
2. **Change the directory**
```
//asd
```
Note: *All the files with .sh extension must require executable permission in Linux. Please make sure to change the permission by running the command below.*

```
sudo chmod +x [file_name.sh]
```


3.  **Run *loadFabric.sh*. This will download:**
    1. Samples: Some more examples in hyperledger fabric.
    2. Binaries: Precompiled codes of some libraries.
    3. Docker Images 
```
sudo ./loadFabric.sh
```
After this, you will see *bin* and *config* directories.


4. **Change the envrioment variables.**
```
export PATH=$PWD/bin:$PATH
```
5. **Change the directory.**
```
cd pharma-ledger-network/
```

### Project Structure ###
```
├── loadFabric.sh               #script to download images, bin and samples
├── pharma-ledger-network
│   ├── configtx                #configurations for transactions
│   │   └── configtx.yaml       #used by configtxgen tool
│   ├── docker                  #docker configurations
│   │   ├── docker-compose-ca.yaml
│   │   └── docker-compose-pln-net.yaml
│   ├── net-pln.sh              #main script
│   ├── organizations           
│   │   ├── cryptogen           #yaml files related to organisations crypto material
|   |   ├── manufacturer        #chain code(smart contract) for manufacturer
|   |   ├── pharmacy            #chain code(smart contract) for pharmacy
|   |   └── wholesaler          #chain code(smart contract) for wholesaler
│   ├── scripts                 #helping scripts for main script
│   │   ├── createChannel.sh    
│   │   ├── deploySmartContract.sh
│   │   ├── invokeContract.sh
│   │   ├── monitor.sh
│   │   └── utils.sh
│   └── system-genesis-block    #first block created to lay the foundation of thge network
└── README.md
```

*NOTE\* All the .yaml are the configuration files that defines how diffrent binaries will function. They are passed as arguments in net-pln.sh.*

6. **Starting the net work**
```
sudo ./net-pln up
```
*Note: Make sure you have set all your scripts to executable form in /scripts directory.*

## Install Go
Due to some unknown reasons, you need to install Go. [Link](https://go.dev/doc/install)

7. **Set the Go Path**

```
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin

echo $GOPATH
```
8. **Start a channel**
```
sudo ./net-pln createChannel
```

*Congratualtions! You created a blockchain network using Hyperledger Fabric.*

NOTE: While running all the above commands you can see + sign, this means the starting of the new command. 

Tests and more explanations will be posted later.