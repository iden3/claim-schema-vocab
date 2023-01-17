# blockchainAccountId
The chain info is encoded in the format "${chain_id}:${contractAddress}".
```
  "blockchainAccountId": "1:0xab16a96d359ec26a11e2c2b3d8f8b8942d5bfcdb"
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
    "id": "did:polygonid:polygon:mumbai:2qHCddrvjDoa2KGqiqTKy6EWXAGEFWdiqNXDFUwKCe?state=0eba6d85808457fc3bb1ea904dbc6040646b6485fddc53a5f8547a4ba6e8232e",
    "state": "0eba6d85808457fc3bb1ea904dbc6040646b6485fddc53a5f8547a4ba6e8232e",
    "replacedByState": "0000000000000000000000000000000000000000000000000000000000000000",
    "createdAtTimestamp": "1673875629",
    "replacedAtTimestamp": "0",
    "createdAtBlock": "31025169",
    "replacedAtBlock": "0"
}
```

# info.id
The URI representing the identifier of the user for whom the state was requested.
```
"id": "did:polygonid:polygon:mumbai:2qHCddrvjDoa2KGqiqTKy6EWXAGEFWdiqNXDFUwKCe?state=0eba6d85808457fc3bb1ea904dbc6040646b6485fddc53a5f8547a4ba6e8232e"
```

# info.state
State of user in hex format.
```
"state": "0eba6d85808457fc3bb1ea904dbc6040646b6485fddc53a5f8547a4ba6e8232e"
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
"createdAtTimestamp": "1673875629"
```

# info.replacedAtTimestamp
Timestamp string in UNIX format when user's state was replaced by new state. `0` for the non-replaced state.
```
"replacedAtTimestamp": "1922456712"
```

# info.createdAtBlock
The block number that contains the user state. `0` for genesis state.
```
"createdAtBlock": "694931"
```

# info.replacedAtBlock
The block number at which the user's state was replaced by the newer state in the blockchain can be used to track the most recent update to the user's state in the smart contract. `0` for non-replaced state.
```
"replacedAtBlock": "695000"
```

# global
Information about GIST.
```json
{
    "root": "0986d6c44665cffc43a2796ffcd8c324be07ddf12a0016ff4da130b9895f4000",
    "replacedByRoot": "0000000000000000000000000000000000000000000000000000000000000000",
    "createdAtTimestamp": "1673875629",
    "replacedAtTimestamp": "0",
    "createdAtBlock": "31025169",
    "replacedAtBlock": "0"
}
```

# global.root
Merkle tree root for current GIST. In hex format.
```
"root": "0986d6c44665cffc43a2796ffcd8c324be07ddf12a0016ff4da130b9895f4000"
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
"createdAtTimestamp": "1673875629"
```

# global.replacedAtTimestamp
Timestamp string in UNIX format when GIST root was replaced by new root. `0` for the non-replaced root.
```
"replacedAtTimestamp": "1922456712"
```

# global.createdAtBlock
The block number that contains the GIST root.
```
"createdAtBlock": "694931"
```

# global.replacedAtBlock
The block number at which the GIST root was replaced by the newer GIST root in the blockchain can be used to track the most recent update to the GIST state in the smart contract. `0` for non-replaced state.
```
"replacedAtBlock": "695000"
```

## Vocab

**GIST** - global identity state.
