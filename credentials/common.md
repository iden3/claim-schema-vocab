[comment]: <> (_[proof]&# 40;# _proof&# 41;_)

# proof

proof contains information that is required for verification of credential.
supported type for Iden3Credentials: _Iden3SparseMerkleTreeProof_

Proof example   
```
{
            "@type": "Iden3SparseMerkleProof",
            "issuer_data": {
                "id": "114WWtmHRG26ea4HgZMhj6hP2P8F9fmFA5DKG1rSea",
                "state": {
                    "tx_id": "0x7d2dfbe61ecffe544b284e0f3f9ac2809cb9ddbcc95e4a31e1f985b46ab608c7",
                    "block_timestamp": 1661250103,
                    "block_number": 27743928,
                    "root_of_roots": "01248c6acd754b8049b8fcca90c5d372a13175eee6dfcc11f9b862a2c211120c",
                    "claims_tree_root": "c31102da08496d64ddfe29adfe0781717a14ff8f87775970003e46ab4002ac24",
                    "revocation_tree_root": "0000000000000000000000000000000000000000000000000000000000000000",
                    "value": "eeddcb23f19a8a31a86307d6aea864ec56f7dfccc7f27edb70e567d95cca7522"
                }
            },
            "mtp": {
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

# subject_position
The value shows where to save the subject in the index or value.<br>
`index` - indicates that subject's position in the index of a claim;<br>
`value` - indicates that the subject position in the value of a claim;<br>
`none` - indicates that the subject not located in a claim.

```
    "subject_position": "value"
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
# secret

A secret number to use for enforcing sybil resistance property
```
  "secret": 55066263022277343669578718895168534326250603453777594175500187360389116729240
```

# credentialStatus

property for the discovery of information about the current status of a iden3 credential, such as whether it is suspended or revoked.

id - property is an URI to get revocation information
type - property, which expresses the credential status type, now it's `SparseMetkleTreeProof`

# Iden3JSONLDValidator

a type of validator that can be used to syntactically validate JSON-LD documents and transform the credential data into a format, which can then be used by a user to generate a valid zero-knowledge proof.
To get schema validator need to make request <credentialSchema.id>#<credentialSubject.type>. Example: `https://raw.githubusercontent.com/iden3/claim-schema-vocab/main/schemas/json-ld/kyc-v2.json-ld#KYCAgeCredential`
