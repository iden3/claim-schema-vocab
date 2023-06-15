<h2> <i> Iden3OnchainSparseMerkleTreeProof2023 example </i> </h2>

```json
{
  "id": "did:polygonid:polygon:mumbai:2qCU58EJgrEMWhziKqC3qNXJkZPY8XCxDSBM4mqPkM/credentialStatus?revocationNonce=49853&contractAddress=1:0xf3bB959314B5D1e4587e1f597ccc289216608ac5",
  "type": "Iden3OnchainSparseMerkleTreeProof2023",
  "revocationNonce": "49853"
}
```

# id

The id field is valid did with query parameters.
`revocationNonce` - revocation nonce of a credential.
`contractAddress` - this field contains two parts. The first part is the chainID the second on-chain contract address. 

# revocationNonce

revocationNonce that is used for credential to check revocation info in the SMT

# statusIssuer

Is optional parameter. Backup way to fetch revocation status directly from the centralized source
