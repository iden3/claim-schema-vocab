<h2> <i> Iden3ReverseSparseMerkleTreeProof example </i> </h2>

```json
{
  "id": "http://rhs:8080/node",
  "type": "Iden3ReverseSparseMerkleTreeProof",
  "revocationNonce": "1234",
  "statusIssuer": {
    "id": "http://host:8001/api/v1/identities/1198CWfQSB4PghrmL3u6gaU4iwCunz9Z5AeaFfCCq8/claims/revocation/status/{rev_nonce}",
    "type": "SparseMerkleTreeProof",
    "revocationNonce": "1234"
  }
}
```

# id

Path to RHS service for getting node children

# revocationNonce

revocationNonce that is used for credential to check revocation info in the SMT

# statusIssuer

backup way to fetch revocation status directly from the centralized source
