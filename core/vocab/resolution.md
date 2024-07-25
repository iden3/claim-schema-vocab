# retrieved

time of the document retrieval
```
  "retrieved":    "2024-07-24T13:05:02.522767624Z",
```
# proof

proof field for [sec](https://w3id.org/security#) vocabulary

# example for universal resolver field didResolutionMetadata
{
    "@context":[ "https://w3id.org/security/suites/eip712sig-2021/v1", "https://schema.iden3.io/core/jsonld/resolution.jsonld"],
    "retrieved": "2024-07-24T13:05:02.522686944Z",
    "type":"Iden3ResolutionMetadata",
    "proof": [
      {
        "type": "EthereumEip712Signature2021",
        "proofPurpose": "assertionMethod",
        "proofValue": "0xb60bd5c18798bd64531935e59356ed7105a7bfa7c80f2f7770dd71960428fe7314fbe4b82eab1239dabafebfe92ec549470d6bc12817c98625d073ea1667516b1c",
        "verificationMethod": "did:pkh:eip155:80002:0x615031554479128d65f30Ffa721791D6441d9727#blockchainAccountId",
        "created": "2024-07-24T13:05:02.522767624Z",
        "eip712": {
          "types": {
            "EIP712Domain": [
              { "name": "name", "type": "string" },
              { "name": "version", "type": "string" },
              { "name": "chainId", "type": "uint256" },
              { "name": "verifyingContract", "type": "address" }
            ],
            "IdentityState": [
              { "name": "from", "type": "address" },
              { "name": "timestamp", "type": "uint256" },
              { "name": "state", "type": "uint256" },
              { "name": "stateCreatedAtTimestamp", "type": "uint256" },
              { "name": "stateReplacedByState", "type": "uint256" },
              { "name": "stateReplacedAtTimestamp", "type": "uint256" },
              { "name": "gistRoot", "type": "uint256" },
              { "name": "gistRootCreatedAtTimestamp", "type": "uint256" },
              { "name": "gistRootReplacedByRoot", "type": "uint256" },
              { "name": "gistRootReplacedAtTimestamp", "type": "uint256" },
              { "name": "identity", "type": "uint256" }
            ]
          },
          "primaryType": "IdentityState",
          "domain": {
            "name": "StateInfo",
            "version": "1",
            "chainId": "0x0",
            "verifyingContract": "0x0000000000000000000000000000000000000000"
          },
          "message": {
            "from": "0x615031554479128d65f30Ffa721791D6441d9727",
            "gistRoot": "14933631566505326626037219459874298674245950925358973964994024169620294080369",
            "gistRootCreatedAtTimestamp": "1721824111",
            "gistRootReplacedAtTimestamp": "0",
            "gistRootReplacedByRoot": "0",
            "identity": "19090607534999372304474213543962416547920895595808567155882840509226423042",
            "state": "13704162472154210473949595093402377697496480870900777124562670166655890846618",
            "stateCreatedAtTimestamp": "1720111993",
            "stateReplacedAtTimestamp": "0",
            "stateReplacedByState": "0",
            "timestamp": "1721826302"
          }
        }
      }
    ]
  }