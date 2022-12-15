# claim-schema-vocab

> Repository for credential schema definition and vocabularies.
>

Repository: https://github.com/iden3/claim-schema-vocab

### General description:

This repository contains JSON-LD and JSON schemas for Iden3 Credentials.
At the current stage, the **Iden3Credential** data model utilizes W3C Verifiable Credential Model but has some additional defined fields. In the future, it can be fully adapted to the W3C Verifiable Credential standard.

The repository structure is following:

1. credentials

   The folder contains vocabulary definitions for common claim structure, authentication claim, KYC-specific vocabulary, and serialization vocabulary.
   For example, field *countryCode* is defined in [kyc.md](credentials/kyc.md) vocabulary file and resolved to link [https://github.com/iden3/claim-schema-vocab/blob/main/credentials/kyc.md#countrycode](https://github.com/iden3/claim-schema-vocab/blob/main/credentials/kyc.md#countrycode) that gives information about the field: description, type, example.

   - Example of Iden3Credential:

       ```json
       {
           "id": "8af6c48a-547a-4af6-a1c6-b4c049691cd2",
           "@context": [
               "https://raw.githubusercontent.com/iden3/claim-schema-vocab/main/schemas/json-ld/iden3credential.json-ld",
               "https://raw.githubusercontent.com/iden3/claim-schema-vocab/main/schemas/json-ld/kyc.json-ld"
           ],
           "@type": [
               "Iden3Credential"
           ],
           "expiration": "2361-03-21T21:14:48+02:00",
           "updatable": false,
           "version": 0,
           "rev_nonce": 10525844421148161795,
           "credentialSubject": {
               "birthdayDay": 24,
               "birthdayMonth": 4,
               "birthdayYear": 1995,
               "documentType": 1,
               "id": "117C9YUVPqEcAAAVMWvew1qc5cogC7nVTU4swnkAcB",
               "type": "KYCAgeCredential"
           },
           "credentialStatus": {
               "id": "http://localhost:8001/api/v1/identities/11AqUpgUacPUy6BwZeDW2kJYBJSEzBQKCLvEtwa2Rs/claims/revocation/status/10525844421148161795",
               "type": "SparseMetkleTreeProof"
           },
           "credentialSchema": {
               "@id": "https://raw.githubusercontent.com/iden3/claim-schema-vocab/main/schemas/json/KYCAgeCredential.json",
               "type": "JsonSchemaValidator2018"
           },
           "proof": [
               {
                   "@type": "BJJSignature2021",
                   "created": 1638468318,
                   "issuer_mtp": {
                       "@type": "Iden3SparseMerkleProof",
                       "state": {
                           "claims_tree_root": "c71299a362950a08a900bcb260cbdac97378ed611d5f9348c58e06ac6875bd2a",
                           "value": "d66f2b1f07d8a9bfaf570d8d746dfb11bce9f33fdabcacf8d46e5cf787e7e22b"
                       },
                       "mtp": {
                           "@type": "SparseMerkleProof",
                           "existence": true,
                           "siblings": []
                       },
                       "issuer": "11AqUpgUacPUy6BwZeDW2kJYBJSEzBQKCLvEtwa2Rs"
                   },
                   "creator": "11AqUpgUacPUy6BwZeDW2kJYBJSEzBQKCLvEtwa2Rs",
                   "verification_method": "ba483cc1ffa1b01750db0de4c560f13146c82e281d6d7bdf05484987a87aea23",
                   "proof_value": "26674458c9fb7dea57506bca887f12372f062c797f76643c66b81a1d73784218dbd914a9c630fdd677da147eeba7aa903905e81145ecb8d7e0e54296e33c3304",
                   "proof_purpose": "Authentication"
               },
               {
                   "@type": "Iden3SparseMerkleProof",
                   "state": {
                       "tx_id": "0xd85a6a72dd3d04a00d0e9cd8bbaac555820d60a5f1024d1c9c6c2c1390376cea",
                       "block_timestamp": 1638468530,
                       "block_number": 11539897,
                       "claims_tree_root": "8ef71c04cf00fecb0f0ab455088862198e8a66fd162bbb52c4dbd9d4de994929",
                       "revocation_tree_root": "0000000000000000000000000000000000000000000000000000000000000000",
                       "value": "b9488bc7a0d9bbe1ac74d5def9a9a7fc6bdadfb2269245ae0d2fd817bc0dc124"
                   },
                   "mtp": {
                       "@type": "SparseMerkleProof",
                       "existence": true,
                       "siblings": [
                           "19331884062013742676999221288855742156448004856978252244854118388210484187847",
                           "2250684463907041370291277709224474920208296274915622528394669370926641373444"
                       ]
                   },
                   "issuer": "11AqUpgUacPUy6BwZeDW2kJYBJSEzBQKCLvEtwa2Rs"
               }
           ]
       }
       ```

2. proofs

   This folder defines vocabularies for different proof types that can be used for **Iden3Credentials**. It defines vocabulary for **Iden3SparseMerkleTreeProof**

   - Example of valid **Iden3SparseMerkleTreeProof**

       ```json
       {
                   "@type": "Iden3SparseMerkleProof",
                   "state": {
                       "tx_id": "0xd85a6a72dd3d04a00d0e9cd8bbaac555820d60a5f1024d1c9c6c2c1390376cea",
                       "block_timestamp": 1638468530,
                       "block_number": 11539897,
                       "claims_tree_root": "8ef71c04cf00fecb0f0ab455088862198e8a66fd162bbb52c4dbd9d4de994929",
                       "revocation_tree_root": "0000000000000000000000000000000000000000000000000000000000000000",
                       "value": "b9488bc7a0d9bbe1ac74d5def9a9a7fc6bdadfb2269245ae0d2fd817bc0dc124"
                   },
                   "mtp": {
                       "@type": "SparseMerkleProof",
                       "existence": true,
                       "siblings": [
                           "19331884062013742676999221288855742156448004856978252244854118388210484187847",
                           "2250684463907041370291277709224474920208296274915622528394669370926641373444"
                       ]
                   },
                   "issuer": "11AqUpgUacPUy6BwZeDW2kJYBJSEzBQKCLvEtwa2Rs"
               }
       ```

3. schemas
   - JSON

     JSON schemas define the validation rules for claim content (using JSON standard)
     and also specifies the order of fields to fill claim slots (according to claim specification). For that *Index* and *Value* custom fields are used. Implementors *must* use these fields.

   - JSON-LD

     JSON-LD schema allows to provide both - association with data vocabulary and claim slot specification. It doesn't confront with JSON, but extending the possibilities. This create an opportunity to exchange documents in machine readable format with document normalization and linked data structures and human readable by providing needed vocabulary.

     For claim slots preparation several serialization types are used:

     *IndexDataSlotA*, *IndexDataSlotB, ValueDataSlotA, ValueDataSlotB*

     If specific can't be specified next types must be used: *Index, Value*
