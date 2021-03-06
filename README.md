# eth-prepaid-transaction

Full Example for sending eth to a client for signing a contract

## Prerequisites

* Go [https://golang.org](https://golang.org)
* Docker [https://www.docker.com/](https://www.docker.com/) 
* A Web-Browser ;)

## Install & Run

```bash
docker pull harshjv/testrpc

docker run -d --name=preprpc -p 8545:8545 harshjv/testrpc --account="0xb4087f10eacc3a032a2d550c02ae7a3ff88bc62eb0d9f6c02c9d5ef4d1562862, 1000000000000000000000000" --account="0xd2a99b289915eb11ea50a51247e1cef2c4583ae1d9699a3bb0154c2792bda339,0"

go build . && ./eth-prepaid-transaction 

open client.html
```

To kill testrpc, use:

```bash
docker stop preprpc && docker rm preprpc
```

## Usage

* Create Agreement (any string will do)
* Refresh Balance & Refresh Agreement
* Sign
* Refresh Agreement & Refresh Balance

