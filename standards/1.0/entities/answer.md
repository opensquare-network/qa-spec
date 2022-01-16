# Answer

It means an answer to a topic. It has 2 parts:

1. an [message](./message.md) entity to a topic which has the answer content.
2. the address of the answer and the corresponding signature.

# Standard

```json
{
  "answer": {
    "topic": {
      "type": "string",
      "description": "IPFS CID of a topic entity"
    },
    "content": {
      "type": "string",
      "description": "An message to a topic"
    }
  },
  "address": {
    "type": "string",
    "description": "The address of the answer author"
  },
  "signature": {
    "type": "string",
    "description": "The signature to the stringify value of the answer field by the corresponding private key of the author address"
  }
}
```

# Examples

```json
{
  "answer": {
    "topic": "bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye",
    "content": "This is an answer"
  },
  "address": "HHyxCP1oWuZqdk9gneHx6RuEqXFs1SGpL51e3LS4aUoiriN",
  "signature": "0x0c54e9750cbafbf76d666151b2ec1a61035b8b1234e105dbb381aa5c564a753d16a1fbdd6ade7e89d4c09391d7ea3aedf4932fcf439025c828c397e5900d2080"
}
```

In above fields,

```javascript
signature = sign(JSON.stringify({
  "topic": "bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye",
  "content": "This is an answer"
}))
```

The corresponding IPFS CID of above answer is:

```
bafybeibknoqig3k472ke56llloupmlf7g6u6xwxntje4pm2a37npb343n4
```
