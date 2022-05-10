[comment]: <> (_[proof]&# 40;# _proof&# 41;_)

# proof

proof contains information that is required for verification of credential.
supported type for Iden3Credentials: _Iden3SparseMerkleTreeProof_

Proof example   
```
    {
    "@type": "Iden3SparseMerkleProof",
    "state": {
            "tx_id": "0x12345",
            "block_timestamp": 1234,
            "block_number": 12345,
            "root_of_roots": "hash here",
            "claims_tree_root": "hash here",
            "revocation_tree_root": "hash here"
    },
    "mtp": {
    "@type": "SparseMerkleProof",
    "existence": false,
    "siblings": [array of siblings],
    "node_aux": {
    "h_index": "index value here",
    "h_value": "value here"
    }
    },
    "issuer": "11ArG697UD3F6TkGKKKvZidE4XeAW5rauUr8SXhhbP"
    }
}
```
# credentialSubject

The value of the credentialSubject property is defined as a set of objects that contain one or more properties that are each related to a subject of the Iden3Credential. ID fields must be identifier of credential subject. 
Credential subject example

```
"credential_subject": {
"age": 18,
"id": "116evtst8g4S2ZgfgKrbG2vJ3y9M6iNdxYd8oqGBeD",
"type": "KYCAgeCredential"
},
```

# subjectPosition
The value shows where save subject in index or value. The place of the subject indicates the uniqueness of the record in the sparse merkle tree. This field is optional, by default set to the "index" value.<br>
`index` - unique for tree.<br>
`value` - NOT unique for tree.

```
    "subjectPosition": "value"
```

# credentialSchema
The value of the credentialSchema property MUST be one or more data schemas that provide verifiers with enough information to determine if the provided data conforms to the provided schema. 
Each credentialSchema MUST specify its type (for example, JsonSchemaValidator2018), and an id property that MUST be a URI identifying the schema file. The precise contents of each data schema is determined by the specific type definition.

```
credentialSchema subject example
"credentialSchema": {
"@id": "https://raw.githubusercontent.com/iden3/claim-schema-vocab/main/schemas/json/KYCAgeCredential.json",
"type": "JsonSchemaValidator2018"
}
```

# expiration

The expiration is expected to be within an expected range for the verifier. For example, a verifier can check that the expiration of a verifiable credential is not in the past.
```
  "expiration": "2361-03-21T21:14:48+02:00"
```

# rev_nonce
In order to not reveal anything about the content of the claim in the ReT, the Claim contains a revocation nonce in the value part, which is added as a leaf in the ReT to revocate the Claim.
```
"rev_nonce": "2134247366"
```

# updatable

Updatable Claims are only updated with increasing versions, and only one version is valid at a time
```
 "updatable": false
```


# version
version of the claim
```
 "version": 0
```
# Index
represents index type

# Value
represents value type

# serialization

defines value type

```
 "serialization": Index
```

# credentialStatus

property for the discovery of information about the current status of a iden3 credential, such as whether it is suspended or revoked.

id - property is an URI to get revocation information
type - property, which expresses the credential status type, now it's `SparseMetkleTreeProof`
