# Addition

An addition is content appended to a topic. It’s used when a topic author misses some content or has new ideas for a
topic. It has the same format with the [answer](./answer.md) entity.

# Standard

```json
{
  "topic": {
    "type": "string",
    "description": "IPFS CID of a topic entity"
  },
  "content": {
    "type": "string",
    "description": "An addition of a topic"
  }
}
```

# Examples

```json
{
  "topic": "bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye",
  "content": "This is an addition of a topic"
}
```
