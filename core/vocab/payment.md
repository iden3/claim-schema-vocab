# recipient

recipient of the payment

```
      "recipient": "0x1234567"
```

# tokenAddress

address of erc20 token

```
      "tokenAddress": "0x1234567"
```

# features

list of eips supported by erc20 token

```
      "features": ["EIP-2612"]
```

# value 

amount to pay 

```
      "value": "1"
```

# nonce

unique nonce

```
      "nonce": "1"
```

# metadata

payment request metadata (optional)

```
      "metadata": "0x"
```

# expirationDate

when payment request is expired (ISO string)

```
      "expirationDate": "ISO"
```

# proof 

signature proof

# example for universal resolver field didResolutionMetadata
```json
{
  "@context": [
    "https://schema.iden3.io/core/jsonld/payment.jsonld#Iden3PaymentRailsRequestV1",
    "https://w3id.org/security/suites/eip712sig-2021/v1"
  ],
  "type": "Iden3PaymentRailsRequestV1",
  "recipient": "0xaddress",
  "value": "100",
  "expirationDate": "ISO string",
  "nonce": "25",
  "metadata": "0x",
  "proof": [
    {
      "type": "EthereumEip712Signature2021",
      "proofPurpose": "assertionMethod",
      "proofValue": "0xa05292e9874240c5c2bbdf5a8fefff870c9fc801bde823189fc013d8ce39c7e5431bf0585f01c7e191ea7bbb7110a22e018d7f3ea0ed81a5f6a3b7b828f70f2d1c",
      "verificationMethod": "did:pkh:eip155:0:0x3e1cFE1b83E7C1CdB0c9558236c1f6C7B203C34e#blockchainAccountId",
      "created": "2024-09-26T12:28:19.702580067Z",
      "eip712": {
        "types": "https://example.com/schemas/v1",
        "primaryType": "IdentityState",
        "domain": {
          "name": "StateInfo",
          "version": "1",
          "chainId": "0x0",
          "verifyingContract": "0x0000000000000000000000000000000000000000",
          "salt": ""
        }
      }
    }
  ]
}
```
