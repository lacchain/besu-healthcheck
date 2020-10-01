# Besu Health Check #

## Introduction
* The besu-health-check service helps users test interactions with a Besu node by accessing it through RPC

## Requirements
* Docker compose

### Clone Repository ####

```shell
$ git clone https://github.com/lacchain/besu-healthcheck.git
$ cd besu-healthcheck/
```

### Edit the docker compose file ###
```shell
$ vi docker-compose.yml
...
environment: &environment     
    - RPC_URL=https://YOUR_IP_BESU_RPC:YOUR_BESU_RPC_PORT # <========== Add the rpc url that your Besu node exposes
```
You can use http or https depending how you are accessing your Besu Node.

### Running the code ###
Run the code with:
```shell
$ docker-compose up
```

If the test is **successful** then a transaction receipt object will be shown, here you have an example:
```shell
{ blockHash: '0x548e47dd3165b0f45ddec69c7d309ea6e048c1be2f6bd2e7e52404557bd31063',
   blockNumber: 6993077,
   contractAddress: '0xefe9215d1e4ba9a8e01f90559b45adfde10f3719',
   cumulativeGasUsed: 800000,
   from: '0x75f4149c9e403ecbcf15ceea796c85489b567fe4',
   gasUsed: 800000,
   logs: [],
   logsBloom: '0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000',
   status: '0x0',
   to: null,
   transactionHash: '0x7fdf96c93fe681ea526a2910e9c1b95c07efb78d466a49480492ae8b264ef5a6',
   transactionIndex: 0
}
```

## Copyright 2020 LACChain

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.