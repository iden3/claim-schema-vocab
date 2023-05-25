<h2> <i> Iden3commRevocationStatusV1.0 example </i> </h2>

```json
{
  "id": "http://issuer:8080/agent",
  "type": "Iden3commRevocationStatusV1.0",
  "revocationNonce": "1234",
}
```

# id

Path to Issuer protocol endpoint

# revocationNonce

revocationNonce that is used for credential to check revocation info in the SMT

# statusIssuer

backup way to fetch revocation status directly from the centralized source
