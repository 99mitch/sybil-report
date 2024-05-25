
Please note that all cluster of that report are independent and have their very own description & argumentation. An issue per cluster would be a better option, but it is impossible as that many opened issues would result in my account being flagged for spam by Github.

# Detailed Methodology & Walkthrough

After gathering as many hot wallet addresses and gas suppliers for several centralized exchanges (CEXs) such as Binance, Coinbase, Kucoin, Bybit, and OKX using blockchain explorers, a simple Dune SQL request was employed to collect around 2.5 million CEX deposit addresses. These are the addresses where users send assets to deposit into a CEX.

Using Dune Dashboard again, I filtered these CEX deposit addresses to identify those that received funds from at least seven addresses that regularly interacted with LayerZero (using an unofficial Dune Dashboard).

Clusters of 7-300 active LayerZero addresses sharing the same CEX deposit address were formed. A script then expanded these clusters by including addresses interacting with the cluster addresses but not directly with the CEX deposit address. To minimize false positives, an address needed to be linked to at least four other cluster addresses to join. Clusters with fewer than 20 addresses (21 including the CEX deposit address) were discarded.

This initial detection/proof layer is fully automated, leveraging scripts to create clusters. Although these clusters are less common due to the requirement of multiple interactions and the common CEX deposit address, a small percentage of false positives remains.

The second detection/proof layer involves manual verification. Each cluster in this report underwent thorough manual inspection to remove false positives and add on-chain arguments supporting the cluster's sybil nature. These on-chain arguments vary, such as addresses within a cluster executing identical transactions simultaneously with the same amounts, or showing similar transaction patterns for LayerZero activities. Resources like LayerZero Scan, Dune, Debank, Arkham, Etherscan, and others were extensively used.

This manual verification, despite being time-consuming, ensures a high accuracy rate by minimizing false positives and demonstrating that the report is not merely a dump of addresses. The combination of automated clustering and manual verification, along with the consistent use of the same CEX deposit address and similar on-chain activities, provides robust detection with minimal false positives.

The activity predating the snapshot was screened across 14 blockchains: Ethereum (endblock 19757726), Optimism (endblock 119326917), BSC (endblock 38236464), Polygon (endblock 56379454), Arbitrum (endblock 205653169), Gnosis (endblock 33677943), Linea (endblock 4059728), Scroll (endblock 5184468), Zksync (endblock 32656745), Moonbeam (endblock 6045324), Moonriver (endblock 6637617), Fantom (endblock 80127182), Base (endblock 13709885), and Celo (endblock 25273962).

Lastly, please note that Arkham diagrams in this report may often lack links, as Arkham only supports 7 out of these 14 blockchains.

# Reward Address (If Eligible)


0x7BA28B2bcD582f56f9B517c0228FF1AB3948557F
This is a fresh address.


# Table of Contents

<details>

1. [Cluster 1](#cluster-1)
2. [Cluster 2](#cluster-2)

</details>


As the cluster are independant and a description comes with every cluster, the two following sections have been regrouped.

This following section is an rotation of the list of the addresses of the cluster and its description: the CEX deposit address some of the addresses share, an Arkham diagram & the second layer of detection.



# Reported Addresses & Description


## CLUSTER 1


The first 10 addresses of the cluster share the same Binance deposit address 0xd2E1cC562786cE8d803128FD8710B79CCCd28260. The rest are linked to numerous addresses of the cluster, multiple times.


```
0x385c0a94802704784331ef5f76208fb918ab3667
0x909e19174a5aa7a3d2aedccfc6e05e0c64fc5f5d
0x3e73311aa4e71af0f5472765fd334bb32f6ff916
0x88632307d47b660f03e376536c7003581c07999a
0xabf5b2f259c3acef7ac0672d2e1851614f6b9a5d
0xc7c7b46c9232b208a8bc43540f42e794086d9881
0x397a5c10c18039676cec523fb509b9ba01280d21
0x79a8874c761b9982ee4d150ebc707846a9d88de6
0x443f33f63de9094f7fcd6f39f1540fe4412641d5
0xad76adfff1668d2bb3c34f8455e13330b54f0444
0x4c4a3c846d5fc34ccfa9dc7955ef6310ef0db19e
0xd0f02cb782fba0f7dbca1eccfcb192b7cf007d91
0xdf99e6d56553a2763bbf2e1c32a44efc05355bf9
0x3b97eb72be539d3cbe4759be7daf001cb8d040df
0x3afb126adb1d5db00aee3e21482fe17198086f66
0x627f4ae1f83871bc503ee2a6349e420a750e2e4b
0xada85f3a8c31d7f22b1db90a514a6a3182837558
0x13976bb80460cf989544c512fa2a04b11c3e1889
0x257ed1ee5b7ae4eceb6f1818829bab8917894944
0x35a35695f3111733df39d99806c68d6be8bc3338
0xee58e3f21ebf1bac5a1bef2f29dd9930a7c78e97
0xf90895702499cd18409e7fd19ba712dd331415da
```

![Capture d'écran 2024-05-25 011418](https://github.com/99mitch/sybil-report/assets/163365834/28c0c1f9-0bb8-4ed3-a865-0a2b170461b2)



The addresses all have the same on-chain activity. For example, the 29/04, the same transaction was made nearly at the same time for 10 of the adresses: interaction with mintCube.

<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/15732be6-0a48-47ee-ac54-e70c6e052723)


![image](https://github.com/99mitch/sybil-report/assets/163365834/4afda5da-ea70-45c7-8249-a0cc66b5335d)


![image](https://github.com/99mitch/sybil-report/assets/163365834/747f68d4-f579-4fc2-814d-40ea06845150)


![image](https://github.com/99mitch/sybil-report/assets/163365834/e129ce0c-7e8b-4b58-9714-e48cafa41624)

![image](https://github.com/99mitch/sybil-report/assets/163365834/1a8995e8-04eb-4d74-8918-dd7d6e1fba49)


![image](https://github.com/99mitch/sybil-report/assets/163365834/d1fa922c-b48d-4064-bb72-0497a51419ce)


![image](https://github.com/99mitch/sybil-report/assets/163365834/ee64673b-c67f-4311-a9a0-a1a28c0b57a6)


![image](https://github.com/99mitch/sybil-report/assets/163365834/df5e77f7-57ab-4662-9f98-0ec3a7974d03)

![image](https://github.com/99mitch/sybil-report/assets/163365834/5e51236f-1db4-4d7c-bb95-22df12c28e47)

</details>

The addresses also all have similar scam tx recognized by debank.

The address share the same CEX deposit address, are part of a cluster with multiple links between one another, and have the same on-chain activity. This is a big scale sybil operation, probably the result of scripts.

## CLUSTER 2

The first 10 addresses of the cluster share the same Binance deposit address 0x70D4282501F8951FeDe458ac53B7D4BBC5360483. The rest are linked to numerous addresses of the cluster.

````
0x237ea6a3840e895eec42bb2c7343d10c097db483
0xb1c6b51cc745665740e77a37237ac506e1a7a179
0xdf49886fe8f44f1358d30654d86c3b418d949fbe
0x16fcd2c7a8d96e1f91e167d34db78f7f0db8ac7a
0x6418122a235d6e7831aec936e79e1fd12d51ad6c
0x2e2a422972472d9bf30ffe1513c4367f7ea20038
0x40e592a8f5c967ac8cc00931e58e3398588b0d97
0x4fe78dee13b94872de53ba4c65dd19dbd7da13db
0xf5918270511997b484d592a3d7b89798fb348007
0xdc2ca72397afb38b72294e658083c0a794bf68d5
0xdffba37790141b5fe20146542834157cd8ad78c4
0xbeb2e566eec5f05cf16cf9112768c21fab0c8db9
0x0af322fffb89b878828211bdc9d4be874cc7017f
0xb4eaa1996ab41f0502cb974bc7154128269d58d3
0x316072ccbeee4f504a4030f9ce3561459b205868
0x2bc9b27433846d505c75cd9bafaea5e6839d6bb9
0x36e60f1f63a158ef441726c5a2ef84a75857c962
0x356cc8ead33d302bed83f5fb62fd01e6bde29b2b
0x60bd18e1bc4dd3f3cb5ba92b436bbe0cf5d0db0c
0xccf302607b73fa3142cbbca11ad8eb8cb5d538ec
0x981c796da09805f3dc54124ec397bac3cf6311c8
0x8043088c341b6b8e906a415f2056a81e417f61df
0xc749a97d4bd68b042e60cf6d39dd40b33824a997
0x1163d2edd37bab505ce520b54554393155583f88
0x1f55f5508dc75185d7d54ef839208ed7a3c4ca8d
0xded2d3916455a840fbd012cb025f82ff23b1de14
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/4ff78058-88c7-4776-8571-b1cd7ccc4ffc)

The addresses have the same on-chain activity. Here we can observe the same interaction with Galxe approximately at the time :

<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/1cde080e-db01-4c02-b223-519d87e1c145)
![image](https://github.com/99mitch/sybil-report/assets/163365834/57678fda-4acf-4ab4-982f-9b9c1f0a2b5f)
![image](https://github.com/99mitch/sybil-report/assets/163365834/7bee2bbb-66c1-4346-bf34-1cd96bea616c)
![image](https://github.com/99mitch/sybil-report/assets/163365834/3438de28-37de-4e52-b013-4ffcdf30bff5)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b4faaac4-c6a3-41da-9031-d87d217a9819)
![image](https://github.com/99mitch/sybil-report/assets/163365834/3362a6b7-c9de-4fe5-b56c-884c69f5893b)
![image](https://github.com/99mitch/sybil-report/assets/163365834/39a8af43-f9e9-453b-9638-a95f2f3ece35)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b08b4afc-df5d-45b0-85a7-c8085d388d71)
</details>


Also here with the interaction done with Stargate and LayerZeroLabs :
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/fbc493e0-9e97-406d-931d-c193e4dd9252)
![image](https://github.com/99mitch/sybil-report/assets/163365834/9ea80373-83af-49c4-b04f-ae1dd0c830bc)
![image](https://github.com/99mitch/sybil-report/assets/163365834/1c28e484-3a5c-4614-8c29-b560ab1295e8)
![image](https://github.com/99mitch/sybil-report/assets/163365834/ebcdb864-d48e-4c48-b101-269fe3e40161)
![image](https://github.com/99mitch/sybil-report/assets/163365834/942fc77e-91d5-4f2f-b381-78f205808683)
</details>


Cluster + same CEX deposit address + same on-chain activity. Without a doubt a sybil cluster.


