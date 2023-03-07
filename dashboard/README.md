## Pre-description
I am not in active set with low number of tokens, therefore some values are zeros.

## Link to Dashboard
http://88.198.159.143:3000/d/cpmSlubVk/nolus?orgId=1&refresh=5s&from=now-24h&to=now

## Description
The dashboard Was created from scratch as part of Nolus Crew3 activity.
There are four main areas and one additional I want to add in future that is related to Tendermint metrics. 
The dashboard is fully custom counting its nature: the monitoring system works with triangle of Grafana + InfluxDB + Telegraf.
Below there is a description about each value that is monitored

### Chain Health
[x] Binary: the name of the projects binary
[x] Current version
[x] Block height
[x] Last block time: the time when the last block was created
[x] Total tokens supply
[x] Min Active Delegation: the size of delegation required to be in active set
[x] Active validators: the number of active ones, but usually the maximum number of validators
[x] Inactive validators: everyone except actives including jailed
[x] Jailed validators: the number of inactive that were jailed
[x] Block Height graph: visualization of the blockchain growing

### Wallet
There were two possible approaches: just one address (selected) or the list of all under interest (table view). Since I have only one, I used the first approach
[x] Address: wallet address that was used to create validator
[x] Current balance
[x] Rewards: sum of all rewards from staking. 
[x] Delegations: the number of all delegations from the mentioned wallet address
[x] Total Delegated: tokens sum delegated from the wallet
[x] Redelegations: the number of all active redelegations from the mentioned wallet address
[x] Total Redelegated: tokens sum redelegated by this wallet
[x] Unbondings: the number of all active unbondings from the mentioned wallet address
[x] Total Unbonded: tokens sum unbonding by the wallet
[x] Balance graph to see the trend
[x] Delegations: list of all delegations from the wallet
[x] Redelegations: list of all active redelegations from the wallet
[x] Unbondings: list of all active unbondings from the wallet

### Validator
[x] Moniker
[x] Valoper address
[x] Health - there are 5 different states: 
* 0 - Running - all is good
* 1 - No binary found
* 2 - No RPC available - not exposed
* 3 - No Status - it is not possible to get status of the validator
* 4 - Late block - the time of the lat block is more than 30 seconds ago
* 5 - Network Halted - the time of the last block is older than 5 minutes. The network is halted
[x] Peers: the number of active peers
[x] Bond Status: Bonded, Unbonded, Unbonding - shows the actual status of validator
[x] Rank: rank of validator in the active list
[x] Commission rate: actually commission rate for the validator
[x] Commission Rewards: current rewards from validating
[x] Catching Up: synchronization status of the node
[x] Jailed: jailed status
[x] Blocks missed graph: historical view of the misssed blocks
[x] Delegations: the number of actual delegations to the validator
[x] Total delegated: the volume of actual delegations to the validator in tokens
[x] Redelegations: the number of actual redelegations to/from the validator
[x] Total redelegated: the volume of actual redelegations to/from the validator in tokens
[x] Unbondings: the number of actual unbondings from the validator
[x] Total unbonded: the volume of actual unbondings from the validator in tokens
[x] Delegations list: all delegations to the validator 
[x] Redelegations list: all redelegations to/from the validator
[x] Unbondings list: all unbondings from the validator

### Host performance
[x] The list of metrics to control the envirnoment
* Uptime
* CPU Usage
* RAM Usage
* Disk Space Usage: root, home, boot
* Swap usage
* Users
* Processes
* Dockers
* Network