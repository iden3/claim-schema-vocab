<h2> <i> SparseMerkleProof example </i> </h2>


```json
{
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
```

# existence

Allows proving that a claim existed at some point

# siblings

The list of siblings in a path from a leaf to the root

# nodeAux

A claim is a statement made by one identity about another identity or itself. Each claim is composed of two parts: index and values. Claims are stored in the leafs of a MT. The index is hashed and used to determine in which leaf position the value of the claim will be stored.

# hIndex

index part of node_aux

# hValue

value part of node_aux
