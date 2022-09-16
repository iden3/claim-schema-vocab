<h2> <i> Iden3ReverseSparseMerkleTreeProof example </i> </h2>

```json
{
  "id": "http://rhs:8080/node",
  "type": "Iden3ReverseSparseMerkleTreeProof",
  "issuer": "1198CWfQSB4PghrmL3u6gaU4iwCunz9Z5AeaFfCCq8",
  "statusIssuer": {
    "id": "http://host:8001/api/v1/identities/1198CWfQSB4PghrmL3u6gaU4iwCunz9Z5AeaFfCCq8/claims/revocation/status/{rev_nonce}",
    "type": "SparseMerkleTreeProof"
  }
}
```

# id

Path to RHS service for getting node children

# issuer

Issuer's ID that issued revocation info to user
