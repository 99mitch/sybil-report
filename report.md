
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
3. [Cluster 3](#cluster-3)
4. [Cluster 4](#cluster-4)
5. [Cluster 5](#cluster-5)
6. [Cluster 6](#cluster-6)
7. [Cluster 7](#cluster-7)
8. [Cluster 8](#cluster-8)
9. [Cluster 9](#cluster-9)


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

```
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

The addresses have the same on-chain activity. Here we can observe the same interaction with Galxe approximately with the same timespan :

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


## CLUSTER 3

The first 12 addresses of the cluster share the same Binance deposit address 0x90D1574aDA5007266F9D9834Ee413BE1c5488B03. The rest are linked to numerous addresses of the cluster.

```
0x5e0fdd8495eca7d5b966a66aa5f5cac5f441e9a1
0x86b34e94e0307d049ac361c841ca187812f2bef2
0x95b9852a24235b158b0ed29ee8652f565683e1b1
0x0291c611fcf96ae006bfeb0958c5395725473438
0xabdf9b75166a5b647b6dbd1bca1b23407d02fc60
0xd343b83bf66e24a5fef7d3a8d50980ec0d82a945
0xd6de58ce85dda96fe4aa26aad631c5113f4835bc
0x0c04183b92ec26c8bb8e9336e1981377b6da76fe
0x7d1564854e8ba39472848df1855f3caa135e48cf
0x466337057bba53b8113d34729fe65f7872b983bb
0x917d2235fc0390e94a960f7dff262d7c27e9c68f
0xe622188bacf0d299a0daa8575d82185c8862f55a
0x680c15770dd13e463de8cd824079916cc658d9f6
0x3bfc0b688933481af2cc7903fd54d46ffb65d771
0x4e45ca4e00e1b735d6479d343a0cd4b2637768ca
0x70bd865e671044e525b632e08542f59cf7f77e25
0x8ed3e9cfb668f9901b11f48b8520544509d7f287
0x2f21d79099644a9ac8243f2cee5ff95825ff4a11
0x49c7fe58d69b5dbac3b0078b402667319487fb49
0x38db52d222329b65099f58d883e3c54acb5fd597
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/5d04ffef-e475-4f6e-b54e-753d98d362ed)

The addresses have the same on-chain activity. Their L0 is the same, probably due to a script. For example, their latest L0 interaction is the same: Merkly transaction 7 months ago from Fuse, and/or Angle transaction 11 months ago from Gnosis and Celo, for every address. The same patterns happen over and over.
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/71c11bbe-811d-469e-8172-77f646e833e6)
![image](https://github.com/99mitch/sybil-report/assets/163365834/ef1a949c-d0d7-4b16-8c5e-253de2b3f29f)
![image](https://github.com/99mitch/sybil-report/assets/163365834/f35f3e81-ad47-4d51-b4a7-0576236ed831)
![image](https://github.com/99mitch/sybil-report/assets/163365834/12661caf-ea72-4179-bd8f-8f907dbd8d9e)
![image](https://github.com/99mitch/sybil-report/assets/163365834/e98ef1e1-d521-472a-8171-5c780d5f88b1)
![image](https://github.com/99mitch/sybil-report/assets/163365834/205861d1-c137-4e25-8472-4895c59e1ec3)

</details>

Cluster + same CEX deposit address + same on-chain activity. Without a doubt a sybil cluster.

## CLUSTER 4

The first 9 addresses of the cluster share the same Kucoin deposit address 0xA2847183FDef870736C8ff1681b16a5521CdF9c5. The rest are linked to numerous addresses of the cluster.

```
0x7d0faf59aa2c13be86ea7d08de31881372349ba4
0x7576f8bdc643cdee38fc5f632d5fdd1d13450803
0x29fec76ab80e47c7dc45193f9317567f67758411
0x03adaf38829f8307099db5ea4ddf54919410e2f3
0xc441b17978cbe90671b9d6e4014c323404f3fcc8
0x6816bf1e88c5e0e8d3c45559f8733712f7a1012d
0x5f3582b06b6697fd64e791ab7ace882fe66bc835
0x4bcc72aece459f92b7095dc408a6d646fcce35cb
0x14de75a716c6d75dc8bda719f381b6dbb113e995
0x1bb1296bd63f3c50059f45065ca1ca006be5efe8
0x5770b98e09d69ba91dd68d5cbf20d18826775b82
0xbf18062443c8697ef6b3d3935c2d3a1440642635
0xcb71a8f2387fb6250c445939b61243f0be2f345a
0x5f0b726d9b98a0744fe19141fea973546cd009f9
0xcc1c9902de1a716f8dc926461058444f49a39b50
0xc7d978b8ac926eadd7c79587d3d6cdbe51a967cf
0x6bbce026dc4cee027e8e33b83a44da150a49fea3
0xd9be17108a0783f68464f2aa78510f40ba154f5b
0x01e4683487849ca6002eefe16c5236e867493e30
0xf7756e25081fd36a3a734bef77331581f6d61535
0xbcf633e185089f46badc4920a7f368252b31da2c
0x6bdc7a993085fdd1e77c7c61b8772162fba08cf5
0xd1e00611cc8a8f7bc02ab1748f810e862701c908
0x9824298f695ee57657cb0633444625e806c77770
0x0000bbefde6e3b6613a4f021854cfbd6d3cd66b4
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/bad9b266-4a39-4cb7-b722-bc698ea06bfd)

The addresses have the same on-chain activity. Their L0 is the same, probably due to a script. For example, their latest L0 interaction is the same: Stargate transaction 26 days ago for every address. The same pattern happen over and over.
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/bc759d2c-7950-4b98-a31c-393b35413c45)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b4d7ee10-a4ad-4a3c-9ee1-1929464b3cdd)
![image](https://github.com/99mitch/sybil-report/assets/163365834/d328064b-63cc-401a-997a-3e2afac49f0d)
![image](https://github.com/99mitch/sybil-report/assets/163365834/8133026b-33ce-4944-beff-f5bc8c4f7149)
![image](https://github.com/99mitch/sybil-report/assets/163365834/4ddb03e6-0dfa-4b20-90b8-58d47408fc42)
![image](https://github.com/99mitch/sybil-report/assets/163365834/2d794417-d693-4ddf-bc21-10823c25f64b)
![image](https://github.com/99mitch/sybil-report/assets/163365834/46c862a8-2c81-4955-a474-648121d7f0aa)
![image](https://github.com/99mitch/sybil-report/assets/163365834/c4433b62-65b9-448e-937e-2b5ac855f984)


</details>

Moreover, They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/ce4d1f51-7a12-4ba1-afb0-328f6e8e58f4)


Cluster + same CEX deposit address + same on-chain activity. Without a doubt a sybil cluster.

## CLUSTER 5

The first 11 addresses of the cluster share the same Binance deposit address 0xA4a3A63efDe3753f3a86986d6E08E046C7353406. The rest are linked to numerous addresses of the cluster.

```
0x5d7adb0d79846fcc2b6ffbda98f33adb4b00f2e7
0x9f45f7f50e90337fa50c625db98ae584bc1dc48c
0x65fc291a2252199a6dfac06fed2e5246db341ac0
0x26914add47df18adbe372fc4d6f8d3ea97e7e063
0x79fb1cbafdf2395980a649a86fd2afe275b0eed6
0x3dc75d5e1693a3c27ba9a54a7de67d34c6694f8c
0x67b98d282aec23fc4d52b41c755f22b31081ffa4
0x65b740a41dba844e4de430095da76972e16f1602
0xe8c907430e1ed83797e0a8bf1eda14a8087cac92
0x7c5b381535b3170043ad444274086123757871d6
0xf38b2abed6c38667a63240678cf84e119041d195
0x082677a0ea5566b3e6b65af9dfb61f17aa7b73d5
0xde009afccce855405e57f4342eb62c9a4520cf6f
0x8a4ad70f227ef77ca371b6eb12445d6d52681850
0x84db1c103066df7b9dd510397c8ade8b0e5999d0
0xaee5666c82df7aad6c7f7e7538e631c9d0c89eb9
0x69848a3b8ed8d1424a846c807a240538f0ff0197
0x136c2b7118beb7bd7981360d36bb5010b5608f25
0xfff84b5e92ac9fe353e2c0fd6ac2e42af390b865
0xaa885b4bc2d2dd326bbe604d55d52421d0a72ea1
0x456c55b4aed43928ff619007e25b847a9939e9cc
0xaa7134be644fa155fc299132633d14fc81018c87
0xa1c55dec3f08fbe6a8b6cf399bbe2d016150eca8
0x7ff34da86a1b03a83e1f021c37b0b4ab6598f212
0x3b11a9a33fb286eb564b387fc7daa8b8b154d949
0x01fabc7e3ee0d830a134f4b744e6fdceb592f97b
0x4568806f725fd5b96950194a87dea09d293bcb3c
0x38c192d6056e8a7b1b91176435eb9b8657689ab8
0x9da9fc9f85c70c029bcb1316cd162ed62a94f506
0x2c6263cc7d914777a12461d622e2edf523885ab5
0xa7a3d484b2229681214d21a08262ebb05b46946f
0x26327d036cc08b93bcb9e475c8450ba8a3225daf
0x3f82dab372a375285e0243583aebd088ee59d625
0x5010e94232f3f2df4b303a759c4a8ed6b24c5309
0xb328cfc34b3dee0e01182826a5405ac306151c36
0xc9315fc369afd5a55689f033b4e6fe90d4da9a9d
0x7078943ba34c0064f8e7ea40c368520e002a4575
0xe8f4fcf52f76f82109327553945250c986c6d0f3
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/94380a0d-8888-4fdb-bb0a-ba693ef92e2f)

The addresses have the same on-chain activity. Here we can observe the same interaction with Stargate approximately with the same timespan :

<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/0e23bc07-7df4-4c90-a33d-6b4db530f41a)
![image](https://github.com/99mitch/sybil-report/assets/163365834/b4d7ee10-a4ad-4a3c-9ee1-1929464b3cdd)
![image](https://github.com/99mitch/sybil-report/assets/163365834/87b53191-272e-45ff-a749-86bc92fd2d6f)
![image](https://github.com/99mitch/sybil-report/assets/163365834/244f686b-ce06-4da9-89c0-82f59bec65d6)
![image](https://github.com/99mitch/sybil-report/assets/163365834/ca229c89-08bb-4ec1-9c02-12ced1e49d65)
![image](https://github.com/99mitch/sybil-report/assets/163365834/fde9558b-3aa2-4fc4-850b-85f4dc72c4b9)


</details>

Moreover, They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/be0c6700-3deb-46df-9615-36002be0f27a)


Cluster + same CEX address + same activity accross +20 wallets to farm airdrop. This is surely a sybil cluster.

## CLUSTER 6

The first 12 addresses of the cluster share the same Binance deposit address 0xDc14Cfa9294d1816781f8CFA04398D95d9aBf675. The rest are linked to numerous addresses of the cluster.

```
0x231466ee5a820e1802081ee4828f6673a400a2a1
0xbdb0884f0a422843f8846869f1909fc6cf921b70
0x0b24b6b5a2b1bac48904fea84b8bd23d16515c5b
0x5a1b39f31e894729217fc10ee7ba1d602a56accd
0xcb43410589a3fb3a2c31e9c6a118af5887d3a64d
0x9668b5b5e5dd787bc84044929727fe8d44a659d8
0xce70dfcb8126f9794c85f857ac5f68b042dad801
0x28784a9d1d45ca2f31da678fd5b3091938b8598e
0x9e16786929eecd46216115adad27dc9b9cca821d
0xddeaa37a75573278fbf9fc51b03bd863db1b63f4
0x735008aeaec303cdc3814bf3a0952a1aac2d7d37
0xaf18c71487eec382c6cc6bf3284a08dcc9a87ce9
0x50b2112ae316630decb1cf170e650b1253decf12
0x542e21321e798724cdcb6bd88024f7eb5439ea48
0x03d91f6df2e871bfdcaff863de3c2a9feaa391e1
0xa656902a2c99fcfa61d6b40d8900f37a4daccf6f
0xe44a5a0d512cc0542c759580c087307c14543cf8
0x00cfc2ee6ba2c77ccb905d2dc795b5e6c10d12b5
0x9c6050375d3e721e9ed127d1f8c0ad58f32ad624
0x203d76528dd0f36ccfc3c400c20baec0c2bb98a7
0x611a0d18c38fad11c2b1f67f3aca76da32682fcf
0x1639baed28d1f76a347e81f92a890064c10105ae
0x51858b79a725a5bf4de8aedbdab006f274578401
0x94cc44233e1c5f5e51f817f88bff610a3ec4fc22
0xf8e164a8121569ee85505491231a3c2c7ab09186
0x2e690239a67c8f0805df0bffc7056ed067d8022d
0xac94be38c5f72783e769feef92eb0e8eed65ba8c
```

![image](https://github.com/99mitch/sybil-report/assets/163365834/080b403d-f6d0-4913-8379-bbe116d91cc5)

The addresses execute similar transaction at the same time to farm airdrop accross planty wallets. For example, they interacted with Stargate back and forth to lock STG with similar amounts during the same timespan.
<details>

![image](https://github.com/99mitch/sybil-report/assets/163365834/597076e1-225e-4ed0-a1dc-4978e86cc9c7)
![image](https://github.com/99mitch/sybil-report/assets/163365834/698c67d8-e061-43aa-8680-1e7b830112e9)
![image](https://github.com/99mitch/sybil-report/assets/163365834/2fe4d2e2-14ba-48e8-af27-cbec382e4f7c)
![image](https://github.com/99mitch/sybil-report/assets/163365834/1a3c4833-2630-4c5b-a8d5-34649b6d82c0)
![image](https://github.com/99mitch/sybil-report/assets/163365834/748c1a34-c63a-46d3-876b-5daeed43f8ee)
![image](https://github.com/99mitch/sybil-report/assets/163365834/db5cf645-450b-4cb5-9517-ced30045517b)
![image](https://github.com/99mitch/sybil-report/assets/163365834/6c7ad112-d842-4f82-87c5-17616f5d9ea6)


</details>

Moreover, They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/c2042f32-76b0-4a9f-a97c-344af5f59899)


Cluster + same CEX address + same activity to farm airdrop. This is surely a sybil cluster.

## CLUSTER 7

The first 12 addresses of the cluster share the same OKX deposit address 0xaF2E326D4C89c8e9e59FF170F451ce306cb60D42. The rest are linked to numerous addresses of the cluster.

```
0xa2468ae73dda2aba7ea11ec97d35410e5dddcd84
0x68141d2a9658d1b58592bcdf81b2976e43537b8f
0x4f4c3ab2c02733e65742aec39af49f0ab80dfe15
0xfcb59a8c5d5be3b514ebcbaf71567fd2bd4bffcc
0xea596320baba2112398b281b79aff1a9a6b07656
0x7e79ccc87f08969cdf3e97ad6529ab5a2c0576ef
0x4b15a92c77d290961c99df629b7ab94fca144c29
0x37a213ab3edc49f82674fb98159e3609c6812ec3
0x1b27c88ce8ddac32e5cd4dcbaecf67d4c8fdee49
0x6fa50e6f0027222582080a20149d0bff9a6842ed
0x2c6802060c60162c0bf45e3df533415c49c7c0ba
0x90f044e97d67e7fa450b5fa56d7fd65bdd199c6f
0xe4f15252d4d3d9d8eb740dd6619a3f7d431df3a1
0x24781c9adba5e4ab8aedaf82f1e6a0018f1de350
0xbb41a00fe950fd88fe556343fc4e345f3ef4e1eb
0xfdfd36b8c94c1f36adcf2318d1250434f5c359d7
0x24fd52b9a97ee5fa4bd4d02e2ceb22af3f786d45
0xcf7e9d3136c6b6597eec2c32e5243d815c211422
0xe9ec9f7233862462a1d007b8df12b60a961578ab
0x5ac2affb99437a6bc3a9df539fc3146f029356bb
0x84d31cbfa184746acf08aaf7b5ea95cf50d06f4a
0x7df61326a523ae6370a7c7e70da904d86b006d93
0x61a30247e119daf8b24f507ab81ab421b27b17c3
0x58962f05b8503f3ca1737d52b37e4c96cd1e581d
0x5f6f1a3bea5d366721105338ef0ece97c12b4ae8
0x430bd9aeed2c4e409b8742bc27dcc9df398eafe7
0x672a31d93d2d02fe4c7396a01b0b01e1b6485630
0xe9ffb19109f547e8e9ce546daf29aaefe2ef66de
0x9844820f0e8d6ca6fab74133d820e5864b1e1c19
0xad3454093a99e34990ccafe195091d4f70f50e5f
0xa6790b9829898eb407cbefddd2ea46adb8841ef0
0x4103d2fa741316fa36fea82c446dd256ab543c13
0x113d3a76f43df30c84f14fa168a2d428b29979bc
0x62be51149a6bb9fe7de7ff4ebfa5ab6a461351e2
```

We can observe from the arkham modelization that the adresses are more than linked :

![image](https://github.com/99mitch/sybil-report/assets/163365834/cdda65cc-50e6-4725-b949-28dc156dc84b)

They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/1a1b85ac-2988-40b9-b914-462cf72e8da8)

Cluster + same CEX address + same adresses interactions pattern. This is surely a sybil cluster.

## CLUSTER 8

The first 10 addresses of the cluster share the same OKX deposit address 0xe0e4c1b6Eda8E3406Be1c188e144E960205EBE84. The rest are linked to numerous addresses of the cluster.

```

0xeb8c666fd0583986a70264e8417da060efc6a0bd
0x08c56fc2f230df3a6d4866ce256459aa8daeee37
0x323401a2053c7494fa569d71c2757bc95f371be2
0x74880c530bc43213b724fce037a54789b19eba36
0x59a1234d72d16b1279eac2d52ba13ce5ab01f341
0x986ea7bbbb42fa0f314eeec493eee1a42b68a8ca
0xb8f407ae47e867ba0de607a5aedfc854a60da03e
0x49917e9fdf5c46477ead5184687582df156251cb
0x3de4780276d6d3667fc57f03f7457d128012e900
0xd70d40b06dc869202216e4158e807333cf3a8d3c
0x6491b25c2bccb96d117eb1bdc5a67ce619a2c0df
0x2f10dd94850bb76ec929c4db8a0f43a9bdc91134
0x3f92d252103b0836b5a06673acbc14096249ed5b
0x59c7be2a9cb9f367033dd1c7d5531098b315b380
0xf0fa35fa9b1f0e443c901b2e127cd8c1d0285262
0x003851e5aca9167c1c0cfd09f73e64bb2768f631
0x5d35822e0ce560e874317e96af39e2e72db51ad1
0x5517d99568f5ce22ad6e445cc79bfc040b96778f
0x0c15c72c07b791acc5fd53d86de484c786738cbf
0xb6af5f2a8f05a1af50f180bf31e1ffa11bfe3ed6
0x5a4a61d54151c3e07e984aaa2716d33ba1808023
```

We can observe from the arkham modelization that the adresses are more than linked :

![image](https://github.com/99mitch/sybil-report/assets/163365834/9a4f336d-8957-4842-abe1-d1d613416800)

They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/9b4d2020-d4a7-42e1-88ca-2924e3c0613a)

Cluster + same CEX address + same adresses interactions pattern. This is surely a sybil cluster.

## CLUSTER 9

The first 10 addresses of the cluster share the same OKX deposit address 0xe0e4c1b6Eda8E3406Be1c188e144E960205EBE84. The rest are linked to numerous addresses of the cluster.

```

0xf67b969da936b4733bc75541ed3901ecedcaf353
0x4d4428b2d29080092842bca10edcf31b06d00c95
0x1411bccec4001c0eb18de07b1973caba9b7058e6
0x2f4c4a0080fb92bda321ff5cfd97d7f285a2f4ec
0x2c3517f6a15944d3adb960f0d1c5dd475b252bc2
0x8a6bf259bd79b03e069a32df22727b55570f8b35
0xc476fdbaa63682d23bf8fcda9e9de59affb9153e
0x153eea2d6a7cf03c2c229a19bccb8571182596f5
0x5abdc9108087fa8c8a3b2eab94a3daf23b30c012
0xc3e65dede3aee84e8877c1646e2cee5aa22068fa
0x8385452ba02a588dfe4753544995d688c7fdd1f5
0xca85ef9af5f64eea898eb78dcc11aec3597a7b41
0x66e8bd359d576c4703096679753b8754e45577b8
0x892676e69f4912ff6ccfcdf3026254715cf64080
0xfcb9d6d9bc04361e7a69efd29d7d93856a81753c
0x8857535a6f35ffb94a7d2b4432424e52defcce71
0x7c9842d9e619ce85392855467cac761e0ac9b103
0xc25d4e71c3e2313ac70d5daaf2a3ffb57711a19b
0x5eca494f77ea7cb7ff7e3656de7104f391eaf100
0xd0e9c403bc33b79644564a1c04c273dad2517370
```

We can observe from the arkham modelization that the adresses are more than linked :

![image](https://github.com/99mitch/sybil-report/assets/163365834/cc9d58a0-67d1-4ddb-bedf-5cba116f9871)

They have similar LZ Age (date of first L0 interaction), amount bridged, contract count, interacted source chains, Unique Active Days etc...

![image](https://github.com/99mitch/sybil-report/assets/163365834/34b48860-437e-4d48-b21f-2887656a25b4)

Considering the cluster, the usage of the same CEX deposit address and the exact same on-chain behavior, there is no doubt this is an industrial scale sybil cluster managed with a script.
