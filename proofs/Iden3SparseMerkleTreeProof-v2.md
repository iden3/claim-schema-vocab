<h2> <i> Iden3SparseMerkleProof example </i> </h2>

```json
{
  "@type": "Iden3SparseMerkleProof",
  "issuerData": {
    "id": "114WWtmHRG26ea4HgZMhj6hP2P8F9fmFA5DKG1rSea",
    "state": {
      "txId": "0x7d2dfbe61ecffe544b284e0f3f9ac2809cb9ddbcc95e4a31e1f985b46ab608c7",
      "blockTimestamp": 1661250103,
      "blockNumber": 27743928,
      "rootOfRoots": "01248c6acd754b8049b8fcca90c5d372a13175eee6dfcc11f9b862a2c211120c",
      "claimsTreeRoot": "c31102da08496d64ddfe29adfe0781717a14ff8f87775970003e46ab4002ac24",
      "revocationTreeRoot": "0000000000000000000000000000000000000000000000000000000000000000",
      "value": "eeddcb23f19a8a31a86307d6aea864ec56f7dfccc7f27edb70e567d95cca7522"
    }
  },
  "mtp": {
    "@type": "SparseMerkleProof",
    "existence": true,
    "siblings": [
      "3209477889731368895290226963942611194724988461418914989031986679474662665977",
      "5821923715436628962921237210722412671895165928731279231225763562513832742516",
      "8868773527863326006398323114380410928721165746282984684038414284639192202613",
      "223953603800789996602416888960727263975802475407586832880729824276914409729",
      "5237339015438092387677260885932503292591750863836982122283671892562100201578",
      "12403925706567780419344638926735967016240444513505844846324162258360029163796",
      "0",
      "0",
      "0",
      "331169271746201375375920410218204804628997320611520025210008420361907998657"
    ]
  }
}
```

# issuerData 

Represents all information about issuer that was used for mtp proof generation

# confirmed

Confirmed is a state of transaction which is completed

# blockNumber

Block where identity state has been included

# blockTimestamp

Timestamp of block where identity state has been included

# txId

ID of transaction of published state


# state

state includes basic information of issuer identity


# value

state value

# rootOfRoots


A merkle tree of Roots is generated by the Issuer and uploaded to the Smart Contract. This allows the recipients to hide the particular Root they are using to prove a claim, and to prove that the Root is valid by proving inclusion in the Roots Tree of the Issuer.


# claimsTreeRoot

A merkle tree of claim information according to specification


# revocationTreeRoot

Every Identity has a ClT (Claim Tree) and a separate ReT (Revocation Tree). While the claim tree would be private and only the root public, the revocation tree would be entirely public. The roots of both trees (ClT and ReT) are linked via the IdS (Identity State) which is published in the Smart Contract. The revocation tree could be published in IPFS or any other public storage system



# authCoreClaim

Hex representation of the conversion result from issuer's Auth BJJ Verifiable Credential to iden3 core claim according to specification https://docs.iden3.io/protocol/claims-structure/


# mtp

Sparse merkle tree proof of credential in the issuer state

# id 

Issuer identifier

# created 

Time in Unix when signature has been created


# coreClaim

Hex representation of the conversion result from Verifiable Credential to iden3 core claim according to specification https://docs.iden3.io/protocol/claims-structure/
These bytes are used for mtp proof.
