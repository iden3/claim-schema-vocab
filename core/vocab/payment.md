# recipient

recipient of the payment

```
      "recipient": "0x1234567"
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
             "type":"Iden3PaymentRailsRequestV1",
             "context": "https://schema.iden3.io/core/jsonld/payment.jsonld#Iden3PaymentRailsRequestV1",
              "recipient": "0x1234567",
              "value": "100",
              "expirationDate": "ISO STRING",
              "nonce": "22",
              "metadata": "0x",
              "proof": [
			      {
			        "type": "EthereumEip712Signature2021",
			        "proofPurpose": "assertionMethod",
			        "proofValue": "0xa05292e9874240c5c2bbdf5a8fefff870c9fc801bde823189fc013d8ce39c7e5431bf0585f01c7e191ea7bbb7110a22e018d7f3ea0ed81a5f6a3b7b828f70f2d1c", // signature
			        "verificationMethod": "did:pkh:eip155:0:0x3e1cFE1b83E7C1CdB0c9558236c1f6C7B203C34e#blockchainAccountId",
			        "created": "2024-09-26T12:28:19.702580067Z",
			        "eip712": {
			         "types": "https://example.com/schemas/v1",
			          "primaryType": "Iden3PaymentRailsRequestV1",
			          "domain": {
			            "name": "MCPayment",
			            "version": "1",
			            "chainId": "0x0",
			            "verifyingContract": "0x0000000000000000000000000000000000000000",
			            "salt": ""
			          }
			        }
			      }
			    ]
         }],
         "expiration": "timestamp", // expiration time of payment-request
         "description":"you can pass the verification on our KYC provider by following the next link",
       }
```
