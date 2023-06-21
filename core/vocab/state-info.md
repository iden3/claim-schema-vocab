# id
Identifier in DID format.
```
"id": "did:polygonid:polygon:mumbai:2qHaobUk3dBVCkox8HtJezfWLDnGrBPufieEJ5A5o8?state=0a4f612419d84ca6ddaa377ec3f2411aba4bc6a3caac6996bc726790a0693424"
```

# type
Representation type.
```
"type": "Iden3StateInfo2023"
```

# stateContractAddress
The chain info is encoded in the format "${chain_id}:${stateContractAddress}".
```
  "stateContractAddress": "80001:0x134B1BE34911E39A8397ec6289782989729807a4"
```

# published
The field 'publisher' indicates whether the state of the user has been recorded on the blockchain. It can be either 'true' or 'false'.

```
  "published": true
```

# info
Information about state of user.
```json
{
  "id": "did:polygonid:polygon:mumbai:2qHaobUk3dBVCkox8HtJezfWLDnGrBPufieEJ5A5o8",
  "state": "0a4f612419d84ca6ddaa377ec3f2411aba4bc6a3caac6996bc726790a0693424",
  "replacedByState": "0000000000000000000000000000000000000000000000000000000000000000",
  "createdAtTimestamp": "1677692829",
  "replacedAtTimestamp": "0",
  "createdAtBlock": "32582803",
  "replacedAtBlock": "0"
}
```

# info.id
The URI representing the identifier of the user for whom the state was requested.
```
"id": "did:polygonid:polygon:mumbai:2qHaobUk3dBVCkox8HtJezfWLDnGrBPufieEJ5A5o8"
```

# info.state
State of user in hex format.
```
"state": "0a4f612419d84ca6ddaa377ec3f2411aba4bc6a3caac6996bc726790a0693424"
```

# info.replacedByState
A non-empty string is present when a user's state is updated with a newer state. Hex format.
`0000000000000000000000000000000000000000000000000000000000000000` equal to empty string.
```
"replacedByState": "a1b2c3d4e5f678901112131415161718191a1b1c1d1e1f202122232425262728"
```

# info.createdAtTimestamp
Timestamp string in UNIX format when user's state was recorded in smart contract. `0` for genesis state.
```
"createdAtTimestamp": "1677692829"
```

# info.replacedAtTimestamp
Timestamp string in UNIX format when user's state was replaced by new state. `0` for the non-replaced state.
```
"replacedAtTimestamp": "0"
```

# info.createdAtBlock
The block number that contains the user state. `0` for genesis state.
```
"createdAtBlock": "32582803"
```

# info.replacedAtBlock
The block number at which the user's state was replaced by the newer state in the blockchain can be used to track the most recent update to the user's state in the smart contract. `0` for non-replaced state.
```
"replacedAtBlock": "0"
```

# global
Information about GIST.
```json
{
  "root": "577b96295c0d3b18ea681978c580718eae4f0069f31fea87b1d8e92cb8d15f2e",
  "replacedByRoot": "0000000000000000000000000000000000000000000000000000000000000000",
  "createdAtTimestamp": "1677692829",
  "replacedAtTimestamp": "0",
  "createdAtBlock": "32582803",
  "replacedAtBlock": "0"
}
```

# global.root
Merkle tree root for current GIST. In hex format.
```
"root": "577b96295c0d3b18ea681978c580718eae4f0069f31fea87b1d8e92cb8d15f2e"
```

# global.replacedByRoot
A non-empty string is present when a GIST root is updated with a newer root. Hex format.
`0000000000000000000000000000000000000000000000000000000000000000` equal to empty string.
```
"replacedByRoot": "5b83b40164632bb721b48baa0423bd8846e7e3d99efd3dd35b2859870939850e"
```

# global.createdAtTimestamp
Timestamp string in UNIX format when GIST root was recorded in smart contract.
```
"createdAtTimestamp": "1677692829"
```

# global.replacedAtTimestamp
Timestamp string in UNIX format when GIST root was replaced by new root. `0` for the non-replaced root.
```
"replacedAtTimestamp": "0"
```

# global.createdAtBlock
The block number that contains the GIST root.
```
"createdAtBlock": "32582803"
```

# global.replacedAtBlock
The block number at which the GIST root was replaced by the newer GIST root in the blockchain can be used to track the most recent update to the GIST state in the smart contract. `0` for non-replaced state.
```
"replacedAtBlock": "0"
```

## Vocab

**GIST** - global identity state.
