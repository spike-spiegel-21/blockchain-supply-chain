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



