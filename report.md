
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
